
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
# Apache Hadoop  2.7.3 Release Notes

These release notes cover new developer and user-facing incompatibilities, important issues, features, and major improvements.


---

* [MAPREDUCE-5485](https://issues.apache.org/jira/browse/MAPREDUCE-5485) | *Critical* | **Allow repeating job commit by extending OutputCommitter API**

Previously, the MR job will get failed if AM get restarted for some reason (like node failure, etc.) during its doing commit job no matter if AM attempts reach to the maximum attempts. 
In this improvement, we add a new API isCommitJobRepeatable() to OutputCommitter interface which to indicate if job's committer can do commitJob again if previous commit work is interrupted by NM/AM failures, etc. The instance of OutputCommitter, which support repeatable job commit (like FileOutputCommitter in algorithm 2), can allow AM to continue the commitJob() after AM restart as a new attempt.


---

* [YARN-4380](https://issues.apache.org/jira/browse/YARN-4380) | *Major* | **TestResourceLocalizationService.testDownloadingResourcesOnContainerKill fails intermittently**

Committed this to trunk, branch-2, and branch-2.7. Thanks Varun Saxena for your contribution.


