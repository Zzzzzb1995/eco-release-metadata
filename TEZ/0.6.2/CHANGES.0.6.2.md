
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
# Apache Tez Changelog

## Release 0.6.2 - 2015-08-07

### INCOMPATIBLE CHANGES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |


### IMPORTANT ISSUES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |


### NEW FEATURES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |


### IMPROVEMENTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [TEZ-2561](https://issues.apache.org/jira/browse/TEZ-2561) | Port for TaskAttemptListenerImpTezDag should be configurable |  Major | . | Johannes Zillmann | Jeff Zhang |


### BUG FIXES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [TEZ-2080](https://issues.apache.org/jira/browse/TEZ-2080) | Localclient should be using tezconf in init instead of yarnconf |  Major | . | Prakash Ramachandran | Siddharth Seth |
| [TEZ-2483](https://issues.apache.org/jira/browse/TEZ-2483) | Tez should close task if processor fail |  Major | . | Daniel Dai | Jeff Zhang |
| [TEZ-2509](https://issues.apache.org/jira/browse/TEZ-2509) | YarnTaskSchedulerService should not try to allocate containers if AM is shutting down |  Major | . | Hitesh Shah | Hitesh Shah |
| [TEZ-2304](https://issues.apache.org/jira/browse/TEZ-2304) | InvalidStateTransitonException TA\_SCHEDULE at START\_WAIT during recovery |  Major | . | Jason Lowe | Jeff Zhang |
| [TEZ-2489](https://issues.apache.org/jira/browse/TEZ-2489) | Disable warn log for Timeline ACL error when tez.allow.disabled.timeline-domains set to true |  Major | . | Hitesh Shah | Chang Li |
| [TEZ-2537](https://issues.apache.org/jira/browse/TEZ-2537) | mapreduce.map.env and mapreduce.reduce.env need to fall back to mapred.child.env for compatibility |  Major | . | Jonathan Eagles | Rohini Palaniswamy |
| [TEZ-2533](https://issues.apache.org/jira/browse/TEZ-2533) | AM deadlock when shutdown |  Major | . | Jeff Zhang | Jeff Zhang |
| [TEZ-2541](https://issues.apache.org/jira/browse/TEZ-2541) | DAGClientImpl enable TimelineClient check is wrong. |  Major | . | Prakash Ramachandran | Prakash Ramachandran |
| [TEZ-2534](https://issues.apache.org/jira/browse/TEZ-2534) | Error handling summary event when shutting down AM |  Major | . | Jeff Zhang | Jeff Zhang |
| [TEZ-2548](https://issues.apache.org/jira/browse/TEZ-2548) | TezClient submitDAG can hang if the AM is in the process of shutting down |  Major | . | Hitesh Shah | Hitesh Shah |
| [TEZ-2475](https://issues.apache.org/jira/browse/TEZ-2475) | Tez local mode hanging in big testsuite |  Major | . | André Kelpe | Siddharth Seth |
| [TEZ-2566](https://issues.apache.org/jira/browse/TEZ-2566) | Allow TaskAttemptFinishedEvent without TaskAttemptStartedEvent when it is KILLED/FAILED |  Major | . | Jeff Zhang | Jeff Zhang |
| [TEZ-1529](https://issues.apache.org/jira/browse/TEZ-1529) | ATS and TezClient integration  in secure kerberos enabled cluster |  Blocker | . | Prakash Ramachandran | Prakash Ramachandran |
| [TEZ-2579](https://issues.apache.org/jira/browse/TEZ-2579) | Incorrect comparison of TaskAttemptId |  Major | . | Jeff Zhang | Jeff Zhang |
| [TEZ-2600](https://issues.apache.org/jira/browse/TEZ-2600) | When used with HDFS federation(viewfs) ,tez will throw a error |  Major | . | Xiaowei Wang | Xiaowei Wang |
| [TEZ-2560](https://issues.apache.org/jira/browse/TEZ-2560) | fix tex-ui build for maven 3.3+ |  Major | . | Prakash Ramachandran | Prakash Ramachandran |
| [TEZ-2623](https://issues.apache.org/jira/browse/TEZ-2623) | Fix module dependencies related to hadoop-auth |  Major | . | Rajat Jain | Rajat Jain |
| [TEZ-2636](https://issues.apache.org/jira/browse/TEZ-2636) | MRInput and MultiMRInput should work for cases when there are 0 physical inputs |  Major | . | Siddharth Seth | Siddharth Seth |
| [TEZ-2635](https://issues.apache.org/jira/browse/TEZ-2635) | Limit number of attempts being downloaded in unordered fetch |  Major | . | Rajesh Balamohan | Rajesh Balamohan |
| [TEZ-2311](https://issues.apache.org/jira/browse/TEZ-2311) | AM can hang if kill received while recovering from previous attempt |  Major | . | Jason Lowe | Jeff Zhang |
| [TEZ-2552](https://issues.apache.org/jira/browse/TEZ-2552) | CRC errors can cause job to run for very long time in large jobs |  Major | . | Rajesh Balamohan | Rajesh Balamohan |
| [TEZ-2685](https://issues.apache.org/jira/browse/TEZ-2685) | Tez 0.6.2 Release |  Major | . | Jonathan Eagles | Jonathan Eagles |


### TESTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |


### SUB-TASKS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [TEZ-2511](https://issues.apache.org/jira/browse/TEZ-2511) | Add exitCode to diagnostics when container fails |  Major | . | Jeff Zhang | Jeff Zhang |
| [TEZ-2549](https://issues.apache.org/jira/browse/TEZ-2549) | Reduce Counter Load on the Timeline Server |  Major | . | Jonathan Eagles | Jason Lowe |


### OTHER:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |


