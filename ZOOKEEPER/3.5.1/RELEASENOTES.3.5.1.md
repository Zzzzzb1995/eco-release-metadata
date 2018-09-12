
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
# Apache Zookeeper  3.5.1 Release Notes

These release notes cover new developer and user-facing incompatibilities, important issues, features, and major improvements.


---

* [ZOOKEEPER-1948](https://issues.apache.org/jira/browse/ZOOKEEPER-1948) | *Major* | **Enable JMX remote monitoring**

Changes in zkServer.sh to support JMX remote monitoring of Zookeeper processes. The change doesn't impact current installations and new installations requiring JMX remote monitoring need to set the jmx port to enable it.


---

* [ZOOKEEPER-2079](https://issues.apache.org/jira/browse/ZOOKEEPER-2079) | *Minor* | **Stop daemon with "kill" rather than "kill -9"**

Kill java process with \`SIGTERM\` rather than \`SIGKILL\`


---

* [ZOOKEEPER-1784](https://issues.apache.org/jira/browse/ZOOKEEPER-1784) | *Major* | **Logic to process INFORMANDACTIVATE packets in syncWithLeader seems bogus**

Committed to trunk. Thanks Raul, and sorry that it took so long to commit.


---

* [ZOOKEEPER-2114](https://issues.apache.org/jira/browse/ZOOKEEPER-2114) | *Major* | **jute generated allocate\_\* functions are not externally visible**

Expose jute-generated allocate\_XXX functions in libzookeeper.


---

* [ZOOKEEPER-2190](https://issues.apache.org/jira/browse/ZOOKEEPER-2190) | *Major* | **In StandaloneDisabledTest, testReconfig() shouldn't take leaving servers as joining servers**

trunk: http://svn.apache.org/viewvc?view=revision&revision=1679444
branch-3.5: http://svn.apache.org/viewvc?view=revision&revision=1679446


---

* [ZOOKEEPER-1504](https://issues.apache.org/jira/browse/ZOOKEEPER-1504) | *Major* | **Multi-thread NIOServerCnxn**

There is a possibility of file descriptor leakage issue under high workload. Please upgrade to the latest version of JVM or the version that has a fix for this bug (http://bugs.sun.com/bugdatabase/view\_bug.do?bug\_id=7118373)



