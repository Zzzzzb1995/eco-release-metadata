
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
# Apache Hadoop Changelog

## Release 2.7.4 - Unreleased (as of 2017-03-24)

### INCOMPATIBLE CHANGES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [HDFS-7933](https://issues.apache.org/jira/browse/HDFS-7933) | fsck should also report decommissioning replicas. |  Major | namenode | Jitendra Nath Pandey | Xiaoyu Yao |
| [HADOOP-13812](https://issues.apache.org/jira/browse/HADOOP-13812) | Upgrade Tomcat to 6.0.48 |  Blocker | kms | John Zhuge | John Zhuge |


### NEW FEATURES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [HDFS-9804](https://issues.apache.org/jira/browse/HDFS-9804) | Allow long-running Balancer to login with keytab |  Major | balancer & mover, security | Xiao Chen | Xiao Chen |


### IMPROVEMENTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [HDFS-8200](https://issues.apache.org/jira/browse/HDFS-8200) | Refactor FSDirStatAndListingOp |  Major | . | Haohui Mai | Haohui Mai |
| [HDFS-8709](https://issues.apache.org/jira/browse/HDFS-8709) | Clarify automatic sync in FSEditLog#logEdit |  Minor | . | Andrew Wang | Andrew Wang |
| [HADOOP-12259](https://issues.apache.org/jira/browse/HADOOP-12259) | Utility to Dynamic port allocation |  Major | test, util | Brahma Reddy Battula | Brahma Reddy Battula |
| [HDFS-8883](https://issues.apache.org/jira/browse/HDFS-8883) | NameNode Metrics : Add FSNameSystem lock Queue Length |  Major | namenode | Anu Engineer | Anu Engineer |
| [HDFS-9019](https://issues.apache.org/jira/browse/HDFS-9019) | Adding informative message to sticky bit permission denied exception |  Minor | security | Thejas M Nair | Xiaoyu Yao |
| [HDFS-9145](https://issues.apache.org/jira/browse/HDFS-9145) | Tracking methods that hold FSNamesytemLock for too long |  Major | namenode | Jing Zhao | Mingliang Liu |
| [HADOOP-12668](https://issues.apache.org/jira/browse/HADOOP-12668) | Support excluding weak Ciphers in HttpServer2 through ssl-server.conf |  Critical | security | Vijay Singh | Vijay Singh |
| [HADOOP-13290](https://issues.apache.org/jira/browse/HADOOP-13290) | Appropriate use of generics in FairCallQueue |  Major | ipc | Konstantin Shvachko | Jonathan Hung |
| [YARN-5483](https://issues.apache.org/jira/browse/YARN-5483) | Optimize RMAppAttempt#pullJustFinishedContainers |  Major | . | sandflee | sandflee |
| [HDFS-10798](https://issues.apache.org/jira/browse/HDFS-10798) | Make the threshold of reporting FSNamesystem lock contention configurable |  Major | logging, namenode | Zhe Zhang | Erik Krogen |
| [HDFS-10807](https://issues.apache.org/jira/browse/HDFS-10807) | Doc about upgrading to a version of HDFS with snapshots may be confusing |  Minor | documentation | Mingliang Liu | Mingliang Liu |
| [HDFS-10625](https://issues.apache.org/jira/browse/HDFS-10625) |  VolumeScanner to report why a block is found bad |  Major | datanode, hdfs | Yongjun Zhang | Rushabh S Shah |
| [YARN-5550](https://issues.apache.org/jira/browse/YARN-5550) | TestYarnCLI#testGetContainers should format according to CONTAINER\_PATTERN |  Minor | client, test | Jonathan Hung | Jonathan Hung |
| [HDFS-10817](https://issues.apache.org/jira/browse/HDFS-10817) | Add Logging for Long-held NN Read Locks |  Major | logging, namenode | Erik Krogen | Erik Krogen |
| [YARN-5540](https://issues.apache.org/jira/browse/YARN-5540) | scheduler spends too much time looking at empty priorities |  Major | capacity scheduler, fairscheduler, resourcemanager | Nathan Roberts | Jason Lowe |
| [MAPREDUCE-6741](https://issues.apache.org/jira/browse/MAPREDUCE-6741) | add MR support to redact job conf properties |  Major | mrv2 | Haibo Chen | Haibo Chen |
| [HDFS-11069](https://issues.apache.org/jira/browse/HDFS-11069) | Tighten the authorization of datanode RPC |  Major | datanode, security | Kihwal Lee | Kihwal Lee |
| [HADOOP-12325](https://issues.apache.org/jira/browse/HADOOP-12325) | RPC Metrics : Add the ability track and log slow RPCs |  Major | ipc, metrics | Anu Engineer | Anu Engineer |
| [HADOOP-13782](https://issues.apache.org/jira/browse/HADOOP-13782) | Make MutableRates metrics thread-local write, aggregate-on-read |  Major | metrics | Erik Krogen | Erik Krogen |
| [HDFS-10941](https://issues.apache.org/jira/browse/HDFS-10941) | Improve BlockManager#processMisReplicatesAsync log |  Major | namenode | Xiaoyu Yao | Chen Liang |
| [HADOOP-13742](https://issues.apache.org/jira/browse/HADOOP-13742) | Expose "NumOpenConnectionsPerUser" as a metric |  Major | . | Brahma Reddy Battula | Brahma Reddy Battula |
| [HDFS-10534](https://issues.apache.org/jira/browse/HDFS-10534) | NameNode WebUI should display DataNode usage histogram |  Major | namenode, ui | Zhe Zhang | Kai Sasaki |
| [HDFS-11333](https://issues.apache.org/jira/browse/HDFS-11333) | Print a user friendly error message when plugins are not found |  Minor | namenode | Wei-Chiu Chuang | Wei-Chiu Chuang |
| [HDFS-11466](https://issues.apache.org/jira/browse/HDFS-11466) | Change dfs.namenode.write-lock-reporting-threshold-ms default from 1000ms to 5000ms |  Major | namenode | Andrew Wang | Andrew Wang |
| [HADOOP-14169](https://issues.apache.org/jira/browse/HADOOP-14169) | Implement listStatusIterator, listLocatedStatus for ViewFs |  Minor | viewfs | Erik Krogen | Erik Krogen |


### BUG FIXES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [YARN-3269](https://issues.apache.org/jira/browse/YARN-3269) | Yarn.nodemanager.remote-app-log-dir could not be configured to fully qualified path |  Major | . | Xuan Gong | Xuan Gong |
| [HADOOP-11859](https://issues.apache.org/jira/browse/HADOOP-11859) | PseudoAuthenticationHandler fails with httpcomponents v4.4 |  Major | . | Eugene Koifman | Eugene Koifman |
| [YARN-3707](https://issues.apache.org/jira/browse/YARN-3707) | RM Web UI queue filter doesn't work |  Blocker | . | Wangda Tan | Wangda Tan |
| [HDFS-8682](https://issues.apache.org/jira/browse/HDFS-8682) | Should not remove decommissioned node,while calculating the number of live/dead decommissioned node. |  Major | . | J.Andreina | J.Andreina |
| [HDFS-5802](https://issues.apache.org/jira/browse/HDFS-5802) | NameNode does not check for inode type before traversing down a path |  Trivial | namenode | Harsh J | Xiao Chen |
| [HADOOP-12483](https://issues.apache.org/jira/browse/HADOOP-12483) | Maintain wrapped SASL ordering for postponed IPC responses |  Critical | ipc | Daryn Sharp | Daryn Sharp |
| [HADOOP-12418](https://issues.apache.org/jira/browse/HADOOP-12418) | TestRPC.testRPCInterruptedSimple fails intermittently |  Major | test | Steve Loughran | Kihwal Lee |
| [HADOOP-11149](https://issues.apache.org/jira/browse/HADOOP-11149) | Increase the timeout of TestZKFailoverController |  Major | test | Rajat Jain | Steve Loughran |
| [HDFS-9467](https://issues.apache.org/jira/browse/HDFS-9467) | Fix data race accessing writeLockHeldTimeStamp in FSNamesystem |  Major | namenode | Mingliang Liu | Mingliang Liu |
| [HDFS-10270](https://issues.apache.org/jira/browse/HDFS-10270) | TestJMXGet:testNameNode() fails |  Minor | test | Andras Bokor | Gergely Novák |
| [HDFS-10276](https://issues.apache.org/jira/browse/HDFS-10276) | HDFS should not expose path info that user has no permission to see. |  Major | . | Kevin Cox | Yuanbo Liu |
| [YARN-5197](https://issues.apache.org/jira/browse/YARN-5197) | RM leaks containers if running container disappears from node update |  Major | resourcemanager | Jason Lowe | Jason Lowe |
| [YARN-5262](https://issues.apache.org/jira/browse/YARN-5262) | Optimize sending RMNodeFinishedContainersPulledByAMEvent for every AM heartbeat |  Major | resourcemanager | Rohith Sharma K S | Rohith Sharma K S |
| [HDFS-10396](https://issues.apache.org/jira/browse/HDFS-10396) | Using -diff option with DistCp may get "Comparison method violates its general contract" exception |  Major | . | Yongjun Zhang | Yongjun Zhang |
| [HDFS-10336](https://issues.apache.org/jira/browse/HDFS-10336) | TestBalancer failing intermittently because of not reseting UserGroupInformation completely |  Major | test | Yiqun Lin | Yiqun Lin |
| [HDFS-10512](https://issues.apache.org/jira/browse/HDFS-10512) | VolumeScanner may terminate due to NPE in DataNode.reportBadBlocks |  Major | datanode | Wei-Chiu Chuang | Yiqun Lin |
| [HADOOP-13362](https://issues.apache.org/jira/browse/HADOOP-13362) | DefaultMetricsSystem leaks the source name when a source unregisters |  Blocker | metrics | Jason Lowe | Junping Du |
| [YARN-5353](https://issues.apache.org/jira/browse/YARN-5353) | ResourceManager can leak delegation tokens when they are shared across apps |  Critical | resourcemanager | Jason Lowe | Jason Lowe |
| [HADOOP-11361](https://issues.apache.org/jira/browse/HADOOP-11361) | Fix a race condition in MetricsSourceAdapter.updateJmxCache |  Major | . | Brahma Reddy Battula | Brahma Reddy Battula |
| [HDFS-10544](https://issues.apache.org/jira/browse/HDFS-10544) | Balancer doesn't work with IPFailoverProxyProvider |  Major | balancer & mover, ha | Zhe Zhang | Zhe Zhang |
| [HADOOP-13202](https://issues.apache.org/jira/browse/HADOOP-13202) | Avoid possible overflow in org.apache.hadoop.util.bloom.BloomFilter#getNBytes |  Major | util | zhengbing li | Kai Sasaki |
| [HADOOP-12991](https://issues.apache.org/jira/browse/HADOOP-12991) | Conflicting default ports in DelegateToFileSystem |  Major | fs | Kevin Hogeland | Kai Sasaki |
| [MAPREDUCE-6744](https://issues.apache.org/jira/browse/MAPREDUCE-6744) | Increase timeout on TestDFSIO tests |  Major | . | Eric Badger | Eric Badger |
| [HDFS-10691](https://issues.apache.org/jira/browse/HDFS-10691) | FileDistribution fails in hdfs oiv command due to ArrayIndexOutOfBoundsException |  Major | . | Yiqun Lin | Yiqun Lin |
| [MAPREDUCE-6724](https://issues.apache.org/jira/browse/MAPREDUCE-6724) | Single shuffle to memory must not exceed Integer#MAX\_VALUE |  Major | mrv2 | Haibo Chen | Haibo Chen |
| [HDFS-8780](https://issues.apache.org/jira/browse/HDFS-8780) | Fetching live/dead datanode list with arg true for removeDecommissionNode,returns list with decom node. |  Major | . | J.Andreina | J.Andreina |
| [YARN-5462](https://issues.apache.org/jira/browse/YARN-5462) | TestNodeStatusUpdater.testNodeStatusUpdaterRetryAndNMShutdown fails intermittently |  Major | . | Eric Badger | Eric Badger |
| [YARN-5469](https://issues.apache.org/jira/browse/YARN-5469) | Increase timeout of TestAmFilter.testFilter |  Minor | . | Eric Badger | Eric Badger |
| [HDFS-10716](https://issues.apache.org/jira/browse/HDFS-10716) | In Balancer, the target task should be removed when its size \< 0. |  Minor | balancer & mover | Yiqun Lin | Yiqun Lin |
| [HDFS-10693](https://issues.apache.org/jira/browse/HDFS-10693) | metaSave should print blocks, not LightWeightHashSet |  Major | namenode | Konstantin Shvachko | Yuanbo Liu |
| [HDFS-10694](https://issues.apache.org/jira/browse/HDFS-10694) | BlockManager.processReport() should print blockReportId in each log message. |  Major | logging, namenode | Konstantin Shvachko | Yuanbo Liu |
| [HDFS-8224](https://issues.apache.org/jira/browse/HDFS-8224) | Schedule a block for scanning if its metadata file is corrupt |  Major | datanode | Rushabh S Shah | Rushabh S Shah |
| [YARN-5382](https://issues.apache.org/jira/browse/YARN-5382) | RM does not audit log kill request for active applications |  Major | resourcemanager | Jason Lowe | Vrushali C |
| [HDFS-9696](https://issues.apache.org/jira/browse/HDFS-9696) | Garbage snapshot records lingering forever |  Critical | . | Kihwal Lee | Kihwal Lee |
| [HDFS-10747](https://issues.apache.org/jira/browse/HDFS-10747) | o.a.h.hdfs.tools.DebugAdmin usage message is misleading |  Minor | hdfs-client | Mingliang Liu | Mingliang Liu |
| [HADOOP-13494](https://issues.apache.org/jira/browse/HADOOP-13494) | ReconfigurableBase can log sensitive information |  Major | security | Sean Mackrory | Sean Mackrory |
| [HADOOP-13512](https://issues.apache.org/jira/browse/HADOOP-13512) | ReloadingX509TrustManager should keep reloading in case of exception |  Critical | security | Mingliang Liu | Mingliang Liu |
| [HDFS-10763](https://issues.apache.org/jira/browse/HDFS-10763) | Open files can leak permanently due to inconsistent lease update |  Critical | . | Kihwal Lee | Kihwal Lee |
| [MAPREDUCE-6763](https://issues.apache.org/jira/browse/MAPREDUCE-6763) | Shuffle server listen queue is too small |  Major | mrv2 | Jason Lowe | Jason Lowe |
| [HDFS-8915](https://issues.apache.org/jira/browse/HDFS-8915) | TestFSNamesystem.testFSLockGetWaiterCount fails intermittently in jenkins |  Minor | test | Anu Engineer | Masatake Iwasaki |
| [HADOOP-12765](https://issues.apache.org/jira/browse/HADOOP-12765) | HttpServer2 should switch to using the non-blocking SslSelectChannelConnector to prevent performance degradation when handling SSL connections |  Major | . | Min Shen | Min Shen |
| [MAPREDUCE-6768](https://issues.apache.org/jira/browse/MAPREDUCE-6768) | TestRecovery.testSpeculative failed with NPE |  Major | mrv2 | Haibo Chen | Haibo Chen |
| [MAPREDUCE-4784](https://issues.apache.org/jira/browse/MAPREDUCE-4784) | TestRecovery occasionally fails |  Major | mrv2, test | Jason Lowe | Haibo Chen |
| [HDFS-10809](https://issues.apache.org/jira/browse/HDFS-10809) | getNumEncryptionZones causes NPE in branch-2.7 |  Major | encryption, namenode | Zhe Zhang | Vinitha Reddy Gankidi |
| [HADOOP-13558](https://issues.apache.org/jira/browse/HADOOP-13558) | UserGroupInformation created from a Subject incorrectly tries to renew the Kerberos ticket |  Major | security | Alejandro Abdelnur | Xiao Chen |
| [HDFS-9038](https://issues.apache.org/jira/browse/HDFS-9038) | DFS reserved space is erroneously counted towards non-DFS used. |  Major | datanode | Chris Nauroth | Brahma Reddy Battula |
| [HADOOP-13579](https://issues.apache.org/jira/browse/HADOOP-13579) | Fix source-level compatibility after HADOOP-11252 |  Blocker | . | Akira Ajisaka | Tsuyoshi Ozawa |
| [HADOOP-13601](https://issues.apache.org/jira/browse/HADOOP-13601) | Fix typo in a log messages of AbstractDelegationTokenSecretManager |  Trivial | . | Mehran Hassani | Mehran Hassani |
| [HDFS-10879](https://issues.apache.org/jira/browse/HDFS-10879) | TestEncryptionZonesWithKMS#testReadWrite fails intermittently |  Major | . | Xiao Chen | Xiao Chen |
| [HDFS-10843](https://issues.apache.org/jira/browse/HDFS-10843) | Update space quota when a UC block is completed rather than committed. |  Major | hdfs, namenode | Erik Krogen | Erik Krogen |
| [HADOOP-13535](https://issues.apache.org/jira/browse/HADOOP-13535) | Add jetty6 acceptor startup issue workaround to branch-2 |  Major | . | Wei-Chiu Chuang | Min Shen |
| [HADOOP-12597](https://issues.apache.org/jira/browse/HADOOP-12597) | In kms-site.xml configuration "hadoop.security.keystore.JavaKeyStoreProvider.password" should be updated with new name |  Minor | security | huangyitian | Surendra Singh Lilhore |
| [HDFS-9885](https://issues.apache.org/jira/browse/HDFS-9885) | Correct the distcp counters name while displaying counters |  Minor | distcp | Archana T | Surendra Singh Lilhore |
| [HDFS-10889](https://issues.apache.org/jira/browse/HDFS-10889) | Remove outdated Fault Injection Framework documentaion |  Major | documentation | Brahma Reddy Battula | Brahma Reddy Battula |
| [HDFS-10713](https://issues.apache.org/jira/browse/HDFS-10713) | Throttle FsNameSystem lock warnings |  Major | logging, namenode | Arpit Agarwal | Hanisha Koneru |
| [HDFS-10915](https://issues.apache.org/jira/browse/HDFS-10915) | Fix time measurement bug in TestDatanodeRestart#testWaitForRegistrationOnRestart |  Minor | test | Xiaobing Zhou | Xiaobing Zhou |
| [HDFS-9444](https://issues.apache.org/jira/browse/HDFS-9444) | Add utility to find set of available ephemeral ports to ServerSocketUtil |  Major | . | Brahma Reddy Battula | Masatake Iwasaki |
| [HADOOP-11780](https://issues.apache.org/jira/browse/HADOOP-11780) | Prevent IPC reader thread death |  Critical | ipc | Daryn Sharp | Daryn Sharp |
| [MAPREDUCE-6771](https://issues.apache.org/jira/browse/MAPREDUCE-6771) | RMContainerAllocator sends container diagnostics event after corresponding completion event |  Major | mrv2 | Haibo Chen | Haibo Chen |
| [HDFS-10878](https://issues.apache.org/jira/browse/HDFS-10878) | TestDFSClientRetries#testIdempotentAllocateBlockAndClose throws ConcurrentModificationException |  Major | hdfs-client | Rushabh S Shah | Rushabh S Shah |
| [HDFS-10609](https://issues.apache.org/jira/browse/HDFS-10609) | Uncaught InvalidEncryptionKeyException during pipeline recovery may abort downstream applications |  Major | encryption | Wei-Chiu Chuang | Wei-Chiu Chuang |
| [HDFS-10991](https://issues.apache.org/jira/browse/HDFS-10991) | Export hdfsTruncateFile symbol in libhdfs |  Blocker | libhdfs | Surendra Singh Lilhore | Surendra Singh Lilhore |
| [HDFS-11002](https://issues.apache.org/jira/browse/HDFS-11002) | Fix broken attr/getfattr/setfattr links in ExtendedAttributes.md |  Major | documentation | Mingliang Liu | Mingliang Liu |
| [HDFS-10301](https://issues.apache.org/jira/browse/HDFS-10301) | BlockReport retransmissions may lead to storages falsely being declared zombie if storage report processing happens out of order |  Critical | namenode | Konstantin Shvachko | Vinitha Reddy Gankidi |
| [HDFS-10712](https://issues.apache.org/jira/browse/HDFS-10712) | Fix TestDataNodeVolumeFailure on 2.\* branches. |  Major | . | Konstantin Shvachko | Vinitha Reddy Gankidi |
| [HDFS-10627](https://issues.apache.org/jira/browse/HDFS-10627) | Volume Scanner marks a block as "suspect" even if the exception is network-related |  Major | hdfs | Rushabh S Shah | Rushabh S Shah |
| [HADOOP-13236](https://issues.apache.org/jira/browse/HADOOP-13236) | truncate will fail when we use viewfilesystem |  Major | . | Brahma Reddy Battula | Brahma Reddy Battula |
| [HDFS-11015](https://issues.apache.org/jira/browse/HDFS-11015) | Enforce timeout in balancer |  Major | balancer & mover | Kihwal Lee | Kihwal Lee |
| [HDFS-11053](https://issues.apache.org/jira/browse/HDFS-11053) | Unnecessary superuser check in versionRequest() |  Major | namenode, security | Kihwal Lee | Kihwal Lee |
| [HDFS-10921](https://issues.apache.org/jira/browse/HDFS-10921) | TestDiskspaceQuotaUpdate doesn't wait for NN to get out of safe mode |  Major | . | Eric Badger | Eric Badger |
| [HADOOP-13201](https://issues.apache.org/jira/browse/HADOOP-13201) | Print the directory paths when ViewFs denies the rename operation on internal dirs |  Major | viewfs | Tianyin Xu | Rakesh R |
| [YARN-4328](https://issues.apache.org/jira/browse/YARN-4328) | Findbugs warning in resourcemanager in branch-2.7 and branch-2.6 |  Minor | resourcemanager | Varun Saxena | Akira Ajisaka |
| [YARN-3432](https://issues.apache.org/jira/browse/YARN-3432) | Cluster metrics have wrong Total Memory when there is reserved memory on CS |  Major | capacityscheduler, resourcemanager | Thomas Graves | Brahma Reddy Battula |
| [HDFS-9500](https://issues.apache.org/jira/browse/HDFS-9500) | datanodesSoftwareVersions map may counting wrong when rolling upgrade |  Major | . | Phil Yang | Erik Krogen |
| [YARN-5001](https://issues.apache.org/jira/browse/YARN-5001) | Aggregated Logs root directory is created with wrong group if nonexistent |  Major | log-aggregation, nodemanager, security | Haibo Chen | Haibo Chen |
| [YARN-5837](https://issues.apache.org/jira/browse/YARN-5837) | NPE when getting node status of a decommissioned node after an RM restart |  Major | . | Robert Kanter | Robert Kanter |
| [HADOOP-13804](https://issues.apache.org/jira/browse/HADOOP-13804) | MutableStat mean loses accuracy if add(long, long) is used |  Minor | metrics | Erik Krogen | Erik Krogen |
| [HDFS-8307](https://issues.apache.org/jira/browse/HDFS-8307) | Spurious DNS Queries from hdfs shell |  Trivial | hdfs-client | Anu Engineer | Andres Perez |
| [HDFS-11087](https://issues.apache.org/jira/browse/HDFS-11087) | NamenodeFsck should check if the output writer is still writable. |  Major | namenode | Konstantin Shvachko | Erik Krogen |
| [HDFS-11056](https://issues.apache.org/jira/browse/HDFS-11056) | Concurrent append and read operations lead to checksum error |  Major | datanode, httpfs | Wei-Chiu Chuang | Wei-Chiu Chuang |
| [YARN-4355](https://issues.apache.org/jira/browse/YARN-4355) | NPE while processing localizer heartbeat |  Major | nodemanager | Jason Lowe | Varun Saxena |
| [HDFS-10966](https://issues.apache.org/jira/browse/HDFS-10966) | Enhance Dispatcher logic on deciding when to give up a source DataNode |  Major | balancer & mover | Zhe Zhang | Mark Wagner |
| [HDFS-11174](https://issues.apache.org/jira/browse/HDFS-11174) | Wrong HttpFS test command in doc |  Minor | documentation, httpfs | John Zhuge | John Zhuge |
| [YARN-5694](https://issues.apache.org/jira/browse/YARN-5694) | ZKRMStateStore can prevent the transition to standby in branch-2.7 if the ZK node is unreachable |  Critical | resourcemanager | Daniel Templeton | Daniel Templeton |
| [HDFS-11180](https://issues.apache.org/jira/browse/HDFS-11180) | Intermittent deadlock in NameNode when failover happens. |  Blocker | namenode | Abhishek Modi | Akira Ajisaka |
| [HDFS-11229](https://issues.apache.org/jira/browse/HDFS-11229) | HDFS-11056 failed to close meta file |  Blocker | datanode | Wei-Chiu Chuang | Wei-Chiu Chuang |
| [HDFS-11160](https://issues.apache.org/jira/browse/HDFS-11160) | VolumeScanner reports write-in-progress replicas as corrupt incorrectly |  Major | datanode | Wei-Chiu Chuang | Wei-Chiu Chuang |
| [HDFS-11263](https://issues.apache.org/jira/browse/HDFS-11263) | ClassCastException when we use Bzipcodec for Fsimage compression |  Critical | . | Brahma Reddy Battula | Brahma Reddy Battula |
| [YARN-6024](https://issues.apache.org/jira/browse/YARN-6024) | Capacity Scheduler 'continuous reservation looking' doesn't work when sum of queue's used and reserved resources is equal to max |  Major | . | Wangda Tan | Wangda Tan |
| [HADOOP-13839](https://issues.apache.org/jira/browse/HADOOP-13839) | Fix outdated tracing documentation |  Minor | documentation, tracing | Masatake Iwasaki | Elek, Marton |
| [HDFS-11280](https://issues.apache.org/jira/browse/HDFS-11280) | Allow WebHDFS to reuse HTTP connections to NN |  Major | hdfs | Zheng Shao | Zheng Shao |
| [MAPREDUCE-6711](https://issues.apache.org/jira/browse/MAPREDUCE-6711) | JobImpl fails to handle preemption events on state COMMITTING |  Major | . | Li Lu | Prabhu Joseph |
| [HADOOP-13958](https://issues.apache.org/jira/browse/HADOOP-13958) | Bump up release year to 2017 |  Blocker | . | Junping Du | Junping Du |
| [HDFS-10733](https://issues.apache.org/jira/browse/HDFS-10733) | NameNode terminated after full GC thinking QJM is unresponsive. |  Major | namenode, qjm | Konstantin Shvachko | Vinitha Reddy Gankidi |
| [HADOOP-14001](https://issues.apache.org/jira/browse/HADOOP-14001) | Improve delegation token validity checking |  Major | . | Akira Ajisaka | Akira Ajisaka |
| [HDFS-11352](https://issues.apache.org/jira/browse/HDFS-11352) | Potential deadlock in NN when failing over |  Critical | namenode | Erik Krogen | Erik Krogen |
| [YARN-6152](https://issues.apache.org/jira/browse/YARN-6152) | Used queue percentage not accurate in UI for 2.7 and below when using DominantResourceCalculator |  Major | . | Jonathan Hung | Jonathan Hung |
| [HADOOP-13433](https://issues.apache.org/jira/browse/HADOOP-13433) | Race in UGI.reloginFromKeytab |  Major | security | Duo Zhang | Duo Zhang |
| [HADOOP-13119](https://issues.apache.org/jira/browse/HADOOP-13119) | Web UI error accessing links which need authorization when Kerberos |  Major | . | Jeffrey E  Rodriguez | Yuanbo Liu |
| [HDFS-11379](https://issues.apache.org/jira/browse/HDFS-11379) | DFSInputStream may infinite loop requesting block locations |  Critical | hdfs-client | Daryn Sharp | Daryn Sharp |
| [YARN-1728](https://issues.apache.org/jira/browse/YARN-1728) | Workaround guice3x-undecoded pathInfo in YARN WebApp |  Major | . | Abraham Elmahrek | Yuanbo Liu |
| [YARN-6310](https://issues.apache.org/jira/browse/YARN-6310) | OutputStreams in AggregatedLogFormat.LogWriter can be left open upon exceptions |  Major | yarn | Haibo Chen | Haibo Chen |
| [HDFS-11499](https://issues.apache.org/jira/browse/HDFS-11499) | Decommissioning stuck because of failing recovery |  Major | hdfs, namenode | Lukas Majercak | Lukas Majercak |
| [HADOOP-9631](https://issues.apache.org/jira/browse/HADOOP-9631) | ViewFs should use underlying FileSystem's server side defaults |  Major | fs, viewfs | Lohit Vijayarenu | Erik Krogen |


### TESTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [HDFS-9888](https://issues.apache.org/jira/browse/HDFS-9888) | Allow reseting KerberosName in unit tests |  Minor | . | Xiao Chen | Xiao Chen |
| [YARN-4717](https://issues.apache.org/jira/browse/YARN-4717) | TestResourceLocalizationService.testPublicResourceInitializesLocalDir fails Intermittently due to IllegalArgumentException from cleanup |  Minor | nodemanager | Daniel Templeton | Daniel Templeton |
| [YARN-5092](https://issues.apache.org/jira/browse/YARN-5092) | TestRMDelegationTokens fails intermittently |  Major | test | Rohith Sharma K S | Jason Lowe |
| [HADOOP-10980](https://issues.apache.org/jira/browse/HADOOP-10980) | TestActiveStandbyElector fails occasionally in trunk |  Minor | . | Ted Yu | Eric Badger |
| [HDFS-9745](https://issues.apache.org/jira/browse/HDFS-9745) | TestSecureNNWithQJM#testSecureMode sometimes fails with timeouts |  Minor | . | Xiao Chen | Xiao Chen |
| [HDFS-9333](https://issues.apache.org/jira/browse/HDFS-9333) | Some tests using MiniDFSCluster errored complaining port in use |  Minor | test | Kai Zheng | Masatake Iwasaki |
| [HDFS-11290](https://issues.apache.org/jira/browse/HDFS-11290) | TestFSNameSystemMBean should wait until JMX cache is cleared |  Major | test | Akira Ajisaka | Erik Krogen |


### SUB-TASKS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [HDFS-8721](https://issues.apache.org/jira/browse/HDFS-8721) | Add a metric for number of encryption zones |  Major | encryption | Rakesh R | Rakesh R |
| [HDFS-8824](https://issues.apache.org/jira/browse/HDFS-8824) | Do not use small blocks for balancing the cluster |  Major | balancer & mover | Tsz Wo Nicholas Sze | Tsz Wo Nicholas Sze |
| [YARN-4393](https://issues.apache.org/jira/browse/YARN-4393) | TestResourceLocalizationService#testFailedDirsResourceRelease fails intermittently |  Major | test | Varun Saxena | Varun Saxena |
| [HDFS-9621](https://issues.apache.org/jira/browse/HDFS-9621) | getListing wrongly associates Erasure Coding policy to pre-existing replicated files under an EC directory |  Critical | erasure-coding | Sushmitha Sreenivasan | Jing Zhao |
| [HDFS-9601](https://issues.apache.org/jira/browse/HDFS-9601) | NNThroughputBenchmark.BlockReportStats should handle NotReplicatedYetException on adding block |  Major | test | Masatake Iwasaki | Masatake Iwasaki |
| [YARN-4573](https://issues.apache.org/jira/browse/YARN-4573) | TestRMAppTransitions.testAppRunningKill and testAppKilledKilled fail on trunk |  Major | resourcemanager, test | Takashi Ohnishi | Takashi Ohnishi |
| [HDFS-10653](https://issues.apache.org/jira/browse/HDFS-10653) | Optimize conversion from path string to components |  Major | hdfs | Daryn Sharp | Daryn Sharp |
| [HDFS-10656](https://issues.apache.org/jira/browse/HDFS-10656) | Optimize conversion of byte arrays back to path string |  Major | hdfs | Daryn Sharp | Daryn Sharp |
| [HDFS-10674](https://issues.apache.org/jira/browse/HDFS-10674) | Optimize creating a full path from an inode |  Major | hdfs | Daryn Sharp | Daryn Sharp |
| [HDFS-10655](https://issues.apache.org/jira/browse/HDFS-10655) | Fix path related byte array conversion bugs |  Major | hdfs | Daryn Sharp | Daryn Sharp |
| [HDFS-10662](https://issues.apache.org/jira/browse/HDFS-10662) | Optimize UTF8 string/byte conversions |  Major | hdfs | Daryn Sharp | Daryn Sharp |
| [HDFS-8818](https://issues.apache.org/jira/browse/HDFS-8818) | Allow Balancer to run faster |  Major | balancer & mover | Tsz Wo Nicholas Sze | Tsz Wo Nicholas Sze |
| [HDFS-10673](https://issues.apache.org/jira/browse/HDFS-10673) | Optimize FSPermissionChecker's internal path usage |  Major | hdfs | Daryn Sharp | Daryn Sharp |
| [HDFS-10744](https://issues.apache.org/jira/browse/HDFS-10744) | Internally optimize path component resolution |  Major | hdfs | Daryn Sharp | Daryn Sharp |
| [HDFS-10896](https://issues.apache.org/jira/browse/HDFS-10896) | Move lock logging logic from FSNamesystem into FSNamesystemLock |  Major | namenode | Erik Krogen | Erik Krogen |
| [HDFS-10745](https://issues.apache.org/jira/browse/HDFS-10745) | Directly resolve paths into INodesInPath |  Major | hdfs | Daryn Sharp | Daryn Sharp |
| [HADOOP-10597](https://issues.apache.org/jira/browse/HADOOP-10597) | RPC Server signals backoff to clients when all request queues are full |  Major | . | Ming Ma | Ming Ma |
| [HADOOP-10300](https://issues.apache.org/jira/browse/HADOOP-10300) | Allowed deferred sending of call responses |  Major | ipc | Daryn Sharp | Daryn Sharp |
| [HDFS-10872](https://issues.apache.org/jira/browse/HDFS-10872) | Add MutableRate metrics for FSNamesystemLock operations |  Major | namenode | Erik Krogen | Erik Krogen |
| [HADOOP-13655](https://issues.apache.org/jira/browse/HADOOP-13655) | document object store use with fs shell and distcp |  Major | documentation, fs, fs/s3 | Steve Loughran | Steve Loughran |
| [HADOOP-14138](https://issues.apache.org/jira/browse/HADOOP-14138) | Remove S3A ref from META-INF service discovery, rely on existing core-default entry |  Critical | fs/s3 | Steve Loughran | Steve Loughran |


### OTHER:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [HADOOP-13670](https://issues.apache.org/jira/browse/HADOOP-13670) | Update CHANGES.txt to reflect all the changes in branch-2.7 |  Blocker | . | Brahma Reddy Battula | Brahma Reddy Battula |
| [YARN-6274](https://issues.apache.org/jira/browse/YARN-6274) | Documentation refers to incorrect nodemanager health checker interval property |  Trivial | documentation | Charles Zhang | Weiwei Yang |


