
<!---
# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
-->
# Apache HBase  2.2.0 Release Notes

These release notes cover new developer and user-facing incompatibilities, important issues, features, and major improvements.


---

* [HBASE-18569](https://issues.apache.org/jira/browse/HBASE-18569) | *Major* | **Add prefetch support for async region locator**

Add prefetch support for async region locator. The default value is 10. Set 'hbase.client.locate.prefetch.limit' in hbase-site.xml if you want to use another value for it.


---

* [HBASE-20357](https://issues.apache.org/jira/browse/HBASE-20357) | *Major* | **AccessControlClient API Enhancement**

This enhances the AccessControlClient APIs to retrieve the permissions based on namespace, table name, family and qualifier for specific user. AccessControlClient can also validate a user whether allowed to perform specified operations on a particular table.
Following APIs have been added,
1) getUserPermissions(Connection connection, String tableRegex, byte[] columnFamily, byte[] columnQualifier, String userName) 
	 Scope of retrieving permission will be same as existing.
2) hasPermission(onnection connection, String tableName, byte[] columnFamily, byte[] columnQualifier, String userName, Permission.Action... actions)
     Scope of validating user privilege,
           User can perform self check without any special privilege but ADMIN privilege will be required to perform check for other users.
           For example, suppose there are two users "userA" & "userB" then there can be below scenarios,
            a. When userA want to check whether userA have privilege to perform mentioned actions
                 userA don't need ADMIN privilege, as it's a self query.
            b. When userA want to check whether userB have privilege to perform mentioned actions,
                 userA must have ADMIN or superuser privilege, as it's trying to query for other user.


---

* [HBASE-20193](https://issues.apache.org/jira/browse/HBASE-20193) | *Critical* | **Basic Replication Web UI - Regionserver**

After HBASE-20193, we add a section to web ui to show the replication status of each wal group. There are 2 parts of this section, they both show the peerId, wal group and current replicating log of each replication source. And one is showing the information of replication log queue, i.e. size of current log, log queue size and replicating offset. The other one is showing the delay of replication, i.e. last shipped age and replication delay.
If the offset shows -1 and replication delay is UNKNOWN, that means replication is not started. This may be caused by this peer is disabled or the replicationEndpoint is sleeping due to some reason.


---

* [HBASE-20244](https://issues.apache.org/jira/browse/HBASE-20244) | *Blocker* | **NoSuchMethodException when retrieving private method decryptEncryptedDataEncryptionKey from DFSClient**

HDFS-12574 made an incompatible change to HdfsKMSUtil with different method signature.
This issue uses reflection to try known method signatures in order to work with hadoop releases with and without HDFS-12574


---

* [HBASE-20839](https://issues.apache.org/jira/browse/HBASE-20839) | *Blocker* | **Fallback to FSHLog if we can not instantiated AsyncFSWAL when user does not specify AsyncFSWAL explicitly**

As we hack into the internal of DFSClient when implementing AsyncFSWAL to get better performance, a patch release of hadoop can make it broken.

So now, if user does not specify a wal provider, then we will first try to use 'asyncfs', i.e, the AsyncFSWALProvider. If we fail due to some compatible issues, we will fallback to 'filesystem', i.e, FSHLog.


---

* [HBASE-6028](https://issues.apache.org/jira/browse/HBASE-6028) | *Minor* | **Implement a cancel for in-progress compactions**

Added a new command to the shell to switch on/off compactions called "compaction\_switch". Disabling compactions will interrupt any currently ongoing compactions. This setting will be lost on restart of the server. Added the configuration hbase.regionserver.compaction.enabled so user can enable/disable compactions via hbase-site.xml.


---

* [HBASE-20672](https://issues.apache.org/jira/browse/HBASE-20672) | *Minor* | **New metrics ReadRequestRate and WriteRequestRate**

Exposing 2 new metrics in HBase to provide ReadRequestRate and WriteRequestRate at region server level. These metrics give the rate of request handled by the region server and are reset after every monitoring interval.


---

* [HBASE-20846](https://issues.apache.org/jira/browse/HBASE-20846) | *Major* | **Restore procedure locks when master restarts**

1. Make hasLock method final, and add a locked field in Procedure to record whether we have the lock. We will set it to true in doAcquireLock and to false in doReleaseLock. The sub procedures do not need to manage it any more.

2. Also added a locked field in the proto message. When storing, the field will be set according to the return value of hasLock. And when loading, there is a new field in Procedure called lockedWhenLoading. We will set it to true if the locked field in proto message is true.

3. The reason why we can not set the locked field directly to true by calling doAcquireLock is that, during initialization, most procedures need to wait until master is initialized. So the solution here is that, we introduced a new method called waitInitialized in Procedure, and move the wait master initialized related code from acquireLock to this method. And we added a restoreLock method to Procedure, if lockedWhenLoading is true, we will call the acquireLock to get the lock, but do not set locked to true. And later when we call doAcquireLock and pass the waitInitialized check, we will test lockedWhenLoading, if it is true, when we just set the locked field to true and return, without actually calling the acquireLock method since we have already called it once.


---

* [HBASE-20538](https://issues.apache.org/jira/browse/HBASE-20538) | *Critical* | **Upgrade our hadoop versions to 2.7.7 and 3.0.3**

Update hadoop-two.version to 2.7.7 and hadoop-three.version to 3.0.3 due to a JDK issue which is solved by HADOOP-15473.


---

* [HBASE-20856](https://issues.apache.org/jira/browse/HBASE-20856) | *Minor* | **PITA having to set WAL provider in two places**

With this change if a WAL's meta provider (hbase.wal.meta\_provider) is not explicitly set, it now defaults to whatever hbase.wal.provider is set to. Previous, the two settings operated independently, each with its own default.

This change is operationally incompatible with previous HBase versions because the default WAL meta provider no longer defaults to AsyncFSWALProvider but to hbase.wal.provider.

The thought is that this is more in line with an operator's expectation, that a change in hbase.wal.provider is sufficient to change how WALs are written, especially given hbase.wal.meta\_provider is an obscure configuration and that the very idea that meta regions would have their own wal provider would likely come as a surprise.


---

* [HBASE-20986](https://issues.apache.org/jira/browse/HBASE-20986) | *Major* | **Separate the config of block size when we do log splitting and write Hlog**

After HBASE-20986, we can set different value to block size of WAL and recovered edits. Both of their default value is 2 \* default HDFS blocksize. And hbase.regionserver.recoverededits.blocksize is for block size of recovered edits while hbase.regionserver.hlog.blocksize is for block size of WAL.


---

* [HBASE-20813](https://issues.apache.org/jira/browse/HBASE-20813) | *Minor* | **Remove RPC quotas when the associated table/Namespace is dropped off**

In previous releases, when a Space Quota was configured on a table or namespace and that table or namespace was deleted, the Space Quota was also deleted. This change improves the implementation so that the same is also done for RPC Quotas.


---

* [HBASE-20965](https://issues.apache.org/jira/browse/HBASE-20965) | *Major* | **Separate region server report requests to new handlers**

After HBASE-20965, we can use MasterFifoRpcScheduler in master to separate RegionServerReport requests to indenpedent handler. To use this feature, please set "hbase.master.rpc.scheduler.factory.class" to
 "org.apache.hadoop.hbase.ipc.MasterFifoRpcScheduler". Use "hbase.master.server.report.handler.count" to set RegionServerReport handlers count, the default value is half of "hbase.regionserver.handler.count" value, but at least 1, and the other handlers count in master is "hbase.regionserver.handler.count" value minus RegionServerReport handlers count, but at least 1 too.


---

* [HBASE-21012](https://issues.apache.org/jira/browse/HBASE-21012) | *Critical* | **Revert the change of serializing TimeRangeTracker**

HFiles generated by 2.0.0, 2.0.1, 2.1.0 are not forward compatible to 1.4.6-, 1.3.2.1-, 1.2.6.1-, and other inactive releases. Why HFile lose compatability is hbase in new versions (2.0.0, 2.0.1, 2.1.0) use protobuf to serialize/deserialize TimeRangeTracker (TRT) while old versions use DataInput/DataOutput. To solve this, We have to put HBASE-21012 to 2.x and put HBASE-21013 in 1.x. For more information, please check HBASE-21008.


---

* [HBASE-20881](https://issues.apache.org/jira/browse/HBASE-20881) | *Major* | **Introduce a region transition procedure to handle all the state transition for a region**

Introduced a new TransitRegionStateProcedure to replace the old AssignProcedure/UnassignProcedure/MoveRegionProcedure. In the old code, MRP will not be attached to RegionStateNode, so it can not be interrupted by ServerCrashProcedure, which introduces lots of tricky code to deal with races, and also causes lots of other difficulties on how to prevent scheduling redundant or even conflict procedures for a region.

And now TRSP is the only one procedure which can bring region online or offline. When you want to schedule one, you need to check whether there is already one attached to the RegionStateNode, under the lock of the RegionStateNode. If not just go ahead, and if there is one, then you should do something, for example, give up and fail directly, or tell the TRSP to give up(This is what SCP does). Since the check and attach are both under the lock of RSN, it will greatly reduce the possible races, and make the code much simpler.


---

* [HBASE-21072](https://issues.apache.org/jira/browse/HBASE-21072) | *Major* | **Block out HBCK1 in hbase2**

Fence out hbase-1.x hbck1 instances. Stop them making state changes on an hbase-2.x cluster; they could do damage. We do this by writing the hbck1 lock file into place on hbase-2.x Master start-up.

To disable this new behavior, set hbase.write.hbck1.lock.file to false


---

* [HBASE-21071](https://issues.apache.org/jira/browse/HBASE-21071) | *Major* | **HBaseTestingUtility::startMiniCluster() to use builder pattern**

Cleanup all the cluster start override combos in HBaseTestingUtility by adding a StartMiniClusterOption and Builder.


---

* [HBASE-20941](https://issues.apache.org/jira/browse/HBASE-20941) | *Major* | **Create and implement HbckService in master**

Adds an HBCK Service and a first method to force-change-in-table-state for use by an HBCK client effecting 'repair' to a malfunctioning HBase.


---

* [HBASE-20649](https://issues.apache.org/jira/browse/HBASE-20649) | *Minor* | **Validate HFiles do not have PREFIX\_TREE DataBlockEncoding**

<!-- markdown -->
Users who have previously made use of prefix tree encoding can now check that their existing HFiles no longer contain data that uses it with an additional preupgrade check command.

```
hbase pre-upgrade validate-hfile
```

Please see the "HFile Content validation" section of the ref guide's coverage of the pre-upgrade validator tool for usage details.


---

* [HBASE-20942](https://issues.apache.org/jira/browse/HBASE-20942) | *Major* | **Improve RpcServer TRACE logging**

Allows configuration of the length of RPC messages printed to the log at TRACE level via "hbase.ipc.trace.param.size" in RpcServer.


---

* [HBASE-21153](https://issues.apache.org/jira/browse/HBASE-21153) | *Major* | **Shaded client jars should always build in relevant phase to avoid confusion**

Client facing artifacts are now built whenever Maven is run through the "package" goal. Previously, the client facing artifacts would create placeholder jars that skipped repackaging HBase and third-party dependencies unless the "release" profile was active.

Build times may be noticeably longer depending on your build hardware. For example, the Jenkins worker nodes maintained by ASF Infra take ~14% longer to do a full packaging build. An example portability-focused personal laptop took ~25% longer.


---

* [HBASE-21107](https://issues.apache.org/jira/browse/HBASE-21107) | *Minor* | **add a metrics for netty direct memory**

Add a new nettyDirectMemoryUsage under server's ipc metrics to show direct memory usage for netty rpc server.


---

* [HBASE-21171](https://issues.apache.org/jira/browse/HBASE-21171) | *Major* | **[amv2] Tool to parse a directory of MasterProcWALs standalone**

Make it so can run the WAL parse and load system in isolation. Here is an example:

{code}$ HBASE\_OPTS=" -XX:+UnlockDiagnosticVMOptions -XX:+UnlockCommercialFeatures -XX:+FlightRecorder -XX:+DebugNonSafepoints" ./bin/hbase org.apache.hadoop.hbase.procedure2.store.wal.WALProcedureStore ~/big\_set\_of\_masterprocwals/
{code}


---

* [HBASE-21021](https://issues.apache.org/jira/browse/HBASE-21021) | *Major* | **Result returned by Append operation should be ordered**

This change ensures Append operations are assembled into the expected order.



