
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
# Apache Pig Changelog

## Release 0.16.1 - Unreleased (as of 2016-07-29)



### BUG FIXES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [PIG-4949](https://issues.apache.org/jira/browse/PIG-4949) | Fix registering jar in S3 which was broken by PIG-4417 in Pig 0.16 |  Major | parser | Yishan Yang | Yishan Yang |
| [PIG-4945](https://issues.apache.org/jira/browse/PIG-4945) | Update document for conflicting macro params |  Trivial | documentation | Koji Noguchi | Koji Noguchi |
| [PIG-4950](https://issues.apache.org/jira/browse/PIG-4950) | Fix minor issues with running scripts in non-local FileSystems |  Minor | . | Peter Slawski | Peter Slawski |
| [PIG-4942](https://issues.apache.org/jira/browse/PIG-4942) | Fix mvn-install ant target |  Major | build | Peter Slawski | Peter Slawski |
| [PIG-4948](https://issues.apache.org/jira/browse/PIG-4948) | Pig on Tez AM use too much memory on a small cluster |  Major | tez | Daniel Dai | Daniel Dai |
| [PIG-4947](https://issues.apache.org/jira/browse/PIG-4947) | LOAD with HBaseStorage using a mix of pure wildcards and prefixed wildcards results in empty maps for the pure wildcarded column families. |  Major | grunt | Youngjin | Daniel Dai |
| [PIG-4960](https://issues.apache.org/jira/browse/PIG-4960) | Split followed by order by/skewed join is skewed in Tez |  Major | . | Rohini Palaniswamy | Rohini Palaniswamy |
| [PIG-4961](https://issues.apache.org/jira/browse/PIG-4961) | CROSS followed by LIMIT inside nested foreach drop data from result |  Major | . | Sergey Svinarchuk | Rohini Palaniswamy |
| [PIG-4935](https://issues.apache.org/jira/browse/PIG-4935) | TEZ\_USE\_CLUSTER\_HADOOP\_LIBS is always set to true |  Major | . | Rohini Palaniswamy | Rohini Palaniswamy |

