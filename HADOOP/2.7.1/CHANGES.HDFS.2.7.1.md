
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
# Hadoop Changelog

## Release 2.7.1 - Unreleased

### INCOMPATIBLE CHANGES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |


### NEW FEATURES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |


### IMPROVEMENTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [HDFS-8204](https://issues.apache.org/jira/browse/HDFS-8204) | Mover/Balancer should not schedule two replicas to the same DN |  Minor | balancer & mover | Walter Su | Walter Su |
| [HDFS-7770](https://issues.apache.org/jira/browse/HDFS-7770) | Need document for storage type label of data node storage locations under dfs.data.dir |  Major | documentation | Xiaoyu Yao | Xiaoyu Yao |


### BUG FIXES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [HDFS-8273](https://issues.apache.org/jira/browse/HDFS-8273) | FSNamesystem#Delete() should not call logSync() when holding the lock |  Blocker | namenode | Jing Zhao | Haohui Mai |
| [HDFS-8269](https://issues.apache.org/jira/browse/HDFS-8269) | getBlockLocations() does not resolve the .reserved path and generates incorrect edit logs when updating the atime |  Blocker | . | Yesha Vora | Haohui Mai |
| [HDFS-8213](https://issues.apache.org/jira/browse/HDFS-8213) | DFSClient should use hdfs.client.htrace HTrace configuration prefix rather than hadoop.htrace |  Critical | . | Billie Rinaldi | Colin Patrick McCabe |
| [HDFS-8179](https://issues.apache.org/jira/browse/HDFS-8179) | DFSClient#getServerDefaults returns null within 1 hour of system start |  Blocker | . | Xiaoyu Yao | Xiaoyu Yao |
| [HDFS-8163](https://issues.apache.org/jira/browse/HDFS-8163) | Using monotonicNow for block report scheduling causes test failures on recently restarted systems |  Blocker | datanode | Arpit Agarwal | Arpit Agarwal |
| [HDFS-8153](https://issues.apache.org/jira/browse/HDFS-8153) | Error Message points to wrong parent directory in case of path component name length error |  Major | namenode | Anu Engineer | Anu Engineer |
| [HDFS-8151](https://issues.apache.org/jira/browse/HDFS-8151) | Always use snapshot path as source when invalid snapshot names are used for diff based distcp |  Minor | distcp | Sushmitha Sreenivasan | Jing Zhao |
| [HDFS-8149](https://issues.apache.org/jira/browse/HDFS-8149) | The footer of the Web UI "Hadoop, 2014" is old |  Major | . | Akira AJISAKA | Brahma Reddy Battula |
| [HDFS-8147](https://issues.apache.org/jira/browse/HDFS-8147) | Mover should not schedule two replicas to the same DN storage |  Major | balancer & mover | surendra singh lilhore | surendra singh lilhore |
| [HDFS-8127](https://issues.apache.org/jira/browse/HDFS-8127) | NameNode Failover during HA upgrade can cause DataNode to finalize upgrade |  Blocker | ha | Jing Zhao | Jing Zhao |
| [HDFS-8091](https://issues.apache.org/jira/browse/HDFS-8091) | ACLStatus and XAttributes not properly presented to INodeAttributesProvider before returning to client |  Major | HDFS | Arun Suresh | Arun Suresh |
| [HDFS-8081](https://issues.apache.org/jira/browse/HDFS-8081) | Split getAdditionalBlock() into two methods. |  Major | . | Konstantin Shvachko | Konstantin Shvachko |
| [HDFS-8070](https://issues.apache.org/jira/browse/HDFS-8070) | Pre-HDFS-7915 DFSClient cannot use short circuit on post-HDFS-7915 DataNode |  Blocker | caching | Gopal V | Colin Patrick McCabe |
| [HDFS-7934](https://issues.apache.org/jira/browse/HDFS-7934) | Update RollingUpgrade rollback documentation: should use bootstrapstandby for standby NN |  Critical | documentation | J.Andreina | J.Andreina |
| [HDFS-7931](https://issues.apache.org/jira/browse/HDFS-7931) | DistributedFIleSystem should not look for keyProvider in cache if Encryption is disabled |  Minor | hdfs-client | Arun Suresh | Arun Suresh |
| [HDFS-7916](https://issues.apache.org/jira/browse/HDFS-7916) | 'reportBadBlocks' from datanodes to standby Node BPServiceActor goes for infinite loop |  Critical | datanode | Vinayakumar B | Vinayakumar B |


### TESTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |


### SUB-TASKS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |


### OTHER:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |

