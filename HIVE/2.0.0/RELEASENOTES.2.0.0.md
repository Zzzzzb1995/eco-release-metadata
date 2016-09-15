
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
# Apache Hive  2.0.0 Release Notes

These release notes cover new developer and user-facing incompatibilities, important issues, features, and major improvements.


---

* [HIVE-10509](https://issues.apache.org/jira/browse/HIVE-10509) | *Major* | **Bump trunk version to 1.3 as branch-1.2 has been created.**

Hive master/trunk version bumped up to 1.3


---

* [HIVE-9365](https://issues.apache.org/jira/browse/HIVE-9365) | *Minor* | **The Metastore should take port configuration from hive-site.xml**

**WARNING: No release note provided for this change.**


---

* [HIVE-10974](https://issues.apache.org/jira/browse/HIVE-10974) | *Major* | **Use Configuration::getRaw() for the Base64 data**

Use Configuration::getRaw() to read Base64 data out of Configuration objects


---

* [HIVE-10746](https://issues.apache.org/jira/browse/HIVE-10746) | *Critical* | ** Hive 1.2.0+Tez produces 1-byte FileSplits from mapred.TextInputFormat**

Use sane split min-sizes when using legacy mapred.InputFormat::getSplits(job, num)


---

* [HIVE-10707](https://issues.apache.org/jira/browse/HIVE-10707) | *Trivial* | **CBO: debug logging OOMs**

CBO: dump AST only when in DEBUG mode.


---

* [HIVE-6026](https://issues.apache.org/jira/browse/HIVE-6026) | *Minor* | **Ldap Authenticator should be more generic with BindDN**

Hive LDAP Authenticator now has filter support for LDAP users and groups.


---

* [HIVE-10790](https://issues.apache.org/jira/browse/HIVE-10790) | *Major* | **orc write on viewFS throws exception**

**WARNING: No release note provided for this change.**


---

* [HIVE-11043](https://issues.apache.org/jira/browse/HIVE-11043) | *Major* | **ORC split strategies should adapt based on number of files**

Use ETLStrategy for a small number of ORC files.


---

* [HIVE-11073](https://issues.apache.org/jira/browse/HIVE-11073) | *Minor* | **ORC FileDump utility ignores errors when writing output**

orcfiledump exits if errors are detected when writing to stdout.


---

* [HIVE-10165](https://issues.apache.org/jira/browse/HIVE-10165) | *Major* | **Improve hive-hcatalog-streaming extensibility and support updates and deletes.**

Expanded streaming API to include update and delete operations and support merge type processes.


---

* [HIVE-11055](https://issues.apache.org/jira/browse/HIVE-11055) | *Major* | **HPL/SQL - Implementing Procedural SQL in Hive (PL/HQL Contribution)**

Adds procedural SQL to Hive


---

* [HIVE-11051](https://issues.apache.org/jira/browse/HIVE-11051) | *Critical* | **Hive 1.2.0  MapJoin w/Tez - LazyBinaryArray cannot be cast to [Ljava.lang.Object;**

HIVE-11051: Hive 1.2.0 MapJoin w/Tez - LazyBinaryArray cannot be cast to [Ljava.lang.Object; (Matt McCline via Gopal V)


---

* [HIVE-10191](https://issues.apache.org/jira/browse/HIVE-10191) | *Major* | **ORC: Cleanup writer per-row synchronization**

Remove per-row synchronization from ORC WriterImpl


---

* [HIVE-11054](https://issues.apache.org/jira/browse/HIVE-11054) | *Major* | **Read error : Partition Varchar column cannot be cast to string**

HIVE-11054: Handle varchar/char partition columns in vectorization


---

* [HIVE-11228](https://issues.apache.org/jira/browse/HIVE-11228) | *Major* | **Mutation API should use semi-shared locks.**

Streaming mutation API uses semi-shared locks.


---

* [HIVE-11215](https://issues.apache.org/jira/browse/HIVE-11215) | *Minor* | **Vectorized grace hash-join throws FileUtil warnings**

 HIVE-11215: Delete spills only if they exist (Gopal V, reviewed by Matt Mccline)


---

* [HIVE-11145](https://issues.apache.org/jira/browse/HIVE-11145) | *Major* | **Remove OFFLINE and NO\_DROP from tables and partitions**

OFFLINE and NO\_DROP mode for partitions removed, use SQLStandardAuth or other authorization scheme to prevent partitions from being dropped or read.


---

* [HIVE-11229](https://issues.apache.org/jira/browse/HIVE-11229) | *Major* | **Mutation API: Coordinator communication with meta store should be optional**

Mutation coordinator meta store dependency now optional.


---

* [HIVE-10673](https://issues.apache.org/jira/browse/HIVE-10673) | *Major* | **Dynamically partitioned hash join for Tez**

This adds configuration parameter hive.optimize.dynamic.partition.hashjoin, which enables selection of the dynamically partitioned hash join with the Tez execution engine


---

* [HIVE-11476](https://issues.apache.org/jira/browse/HIVE-11476) | *Minor* | **TypeInfoParser cannot handle column names with spaces in them**

HIVE-11476: TypeInfoParser cannot handle column names with spaces in them (Gopal V, reviewed by Hari Sankar Sivarama Subramaniyan)


---

* [HIVE-11457](https://issues.apache.org/jira/browse/HIVE-11457) | *Major* | **Vectorization: Improve SIMD JIT in GenVectorCode StringExpr instrinsics**

Vectorization: Improve GenVectorCode string equals intrinsic


---

* [HIVE-11462](https://issues.apache.org/jira/browse/HIVE-11462) | *Major* | **GenericUDFStruct should constant fold at compile time**

Constant fold struct() UDF


---

* [HIVE-11304](https://issues.apache.org/jira/browse/HIVE-11304) | *Major* | **Migrate to Log4j2 from Log4j 1.x**

Migration from Log4j1.x to Log4j2


---

* [HIVE-11594](https://issues.apache.org/jira/browse/HIVE-11594) | *Major* | **Analyze Table For Columns cannot handle columns with embedded spaces**

Analyze Table for column names with embedded spaces


---

* [HIVE-11472](https://issues.apache.org/jira/browse/HIVE-11472) | *Minor* | **ORC StringDirectTreeReader is thrashing the GC due to byte[] allocation per row**

HIVE-11472: ORC StringDirectTreeReader is thrashing the GC due to byte[] allocation per row (Gopal V, reviewed by Ashutosh Chauhan)


---

* [HIVE-11366](https://issues.apache.org/jira/browse/HIVE-11366) | *Major* | **Avoid right leaning tree hashCode depth during ExprNodeDescEqualityWrapper HashMaps**

HIVE-11366: Avoid right leaning tree hashCode depth in ExprNodeDescEqualityWrapper hashmaps (Gopal V, reviewed by Ashutosh Chauhan)


---

* [HIVE-11638](https://issues.apache.org/jira/browse/HIVE-11638) | *Major* | **ExprNodeDesc hashMap accidentally degrades into O(N) instead of O(1)**

Use fastest hashmap implementation of ExprNodeDesc lookups


---

* [HIVE-11573](https://issues.apache.org/jira/browse/HIVE-11573) | *Major* | **PointLookupOptimizer can be pessimistic at a low nDV**

Provide configurable limits to the PointLookupOptimizer


---

* [HIVE-11544](https://issues.apache.org/jira/browse/HIVE-11544) | *Minor* | **LazyInteger should avoid throwing NumberFormatException**

Improve LazySimpleSerDe null data handling for Byte, Short, Integer, Float, Long and Double.


---

* [HIVE-11821](https://issues.apache.org/jira/browse/HIVE-11821) | *Major* | **JDK8 strict build broken for master**

JDK8 strict build broken for master


---

* [HIVE-11468](https://issues.apache.org/jira/browse/HIVE-11468) | *Critical* | **Vectorize: Struct IN() clauses**

HIVE-11468: Vectorize Struct IN() clauses (Matt McCline, via Gopal V)


---

* [HIVE-11831](https://issues.apache.org/jira/browse/HIVE-11831) | *Major* | **TXN tables in Oracle should be created with ROWDEPENDENCIES**

ROWDEPENDENCIES cannot be added to the table after it has already been created. If you hit this issue on an existing database, you might want to (this requires stopping all Hive workloads for the duration), for each table (see the patch for what tables need to be updated; locks and txns table are the ones most affected):

1) create temp table
2) move contents of existing table to temp table
3) drop existing table
4) create new table with ROWDEPENDENCIES, as per the attached patch
5) move data back from temp table


---

* [HIVE-12005](https://issues.apache.org/jira/browse/HIVE-12005) | *Major* | **Remove hbase based stats collection mechanism**

Removed hbase based stats collection mechanism.


---

* [HIVE-11908](https://issues.apache.org/jira/browse/HIVE-11908) | *Critical* | **LLAP: Merge branch to hive-2.0**

**WARNING: No release note provided for this change.**


---

* [HIVE-12090](https://issues.apache.org/jira/browse/HIVE-12090) | *Major* | **Dead-code: Vectorized map-join murmur hash is run twice**

Dead-code: Vectorized map-join runs Murmurhash twice


---

* [HIVE-11882](https://issues.apache.org/jira/browse/HIVE-11882) | *Major* | **Fetch optimizer should stop source files traversal once it exceeds the hive.fetch.task.conversion.threshold**

 HIVE-11882: Fetch optimizer should stop source files traversal once it exceeds the hive.fetch.task.conversion.threshold (Illya Yalovyy, via Gopal V)


---

* [HIVE-11578](https://issues.apache.org/jira/browse/HIVE-11578) | *Major* | **ATS hook fails for ExplainWork**

HIVE-11578: Fix NPE in ExplainWork (Rajesh Balamohan, via Gopal V)


---

* [HIVE-11785](https://issues.apache.org/jira/browse/HIVE-11785) | *Major* | **Support escaping carriage return and new line for LazySimpleSerDe**

This change with HIVE-12820 in addition adds the support of carriage return and new line characters in the fields. Before this change, the user needs to preprocess the text by replacing them with some characters other than carriage return and new line in order for the files to be properly processed. With this change, it will automatically escape them if {{serialization.escape.crlf}} serde property is set to true. One incompatible change is: characters \'r\' and \'n\' cannot be used as separator or field delimiter.


---

* [HIVE-12164](https://issues.apache.org/jira/browse/HIVE-12164) | *Major* | **Remove jdbc stats collection mechanism**

**WARNING: No release note provided for this change.**


---

* [HIVE-12224](https://issues.apache.org/jira/browse/HIVE-12224) | *Major* | **Remove HOLD\_DDLTIME**

**WARNING: No release note provided for this change.**


---

* [HIVE-11378](https://issues.apache.org/jira/browse/HIVE-11378) | *Major* | **Remove hadoop-1 support from master branch**

Support for Hadoop 1.x has been removed from Hive 2.0


---

* [HIVE-11306](https://issues.apache.org/jira/browse/HIVE-11306) | *Major* | **Add a bloom-1 filter for Hybrid MapJoin spills**

Add a bloom-1 filter to reduce Hybrid MapJoin spills


---

* [HIVE-12209](https://issues.apache.org/jira/browse/HIVE-12209) | *Major* | **Vectorized simple CASE expressions with nulls**

Vectorize simple UDFs with null arguments


---

* [HIVE-12281](https://issues.apache.org/jira/browse/HIVE-12281) | *Minor* | **Vectorized MapJoin - use Operator::isLogDebugEnabled**

HIVE-12281: Vectorized MapJoin - use Operator::isLogDebugEnabled (Gopal V, reviewed by Matt McCline)


---

* [HIVE-12238](https://issues.apache.org/jira/browse/HIVE-12238) | *Major* | **Vectorization: Thread-safety errors in VectorUDFDate**

HIVE-12238: Vectorization: Thread-safety errors in VectorUDFDate (Gopal V, reviewed by Gunther Hagleitner)


---

* [HIVE-12202](https://issues.apache.org/jira/browse/HIVE-12202) | *Major* | **NPE thrown when reading legacy ACID delta files**

Reading legacy ACID formats (prior to 1.3.0) no longer results in an NPE.


---

* [HIVE-12063](https://issues.apache.org/jira/browse/HIVE-12063) | *Major* | **Pad Decimal numbers with trailing zeros to the scale of the column**

**WARNING: No release note provided for this change.**


---

* [HIVE-12320](https://issues.apache.org/jira/browse/HIVE-12320) | *Major* | **hive.metastore.disallow.incompatible.col.type.changes should be true by default**

**WARNING: No release note provided for this change.**


---

* [HIVE-12315](https://issues.apache.org/jira/browse/HIVE-12315) | *Critical* | **vectorization\_short\_regress.q has a wrong result issue for a double calculation**

HIVE-12315: Fix Vectorized double divide by zero (Gopal V, reviewed by Matt McCline)


---

* [HIVE-12288](https://issues.apache.org/jira/browse/HIVE-12288) | *Major* | **Extend HIVE-11306 changes to apply to Native vectorized map-joins**

Bloom-1 filters for Vectorized map-joins


---

* [HIVE-7575](https://issues.apache.org/jira/browse/HIVE-7575) | *Major* | **GetTables thrift call is very slow**

This adds 5 additional columns to the ResultSet of GetTables.  This is for compliance with the official JDBC API:

See:  http://docs.oracle.com/javase/7/docs/api/java/sql/DatabaseMetaData.html#getTables(java.lang.String,%20java.lang.String,%20java.lang.String,%20java.lang.String[])


---

* [HIVE-12363](https://issues.apache.org/jira/browse/HIVE-12363) | *Major* | **Incorrect results with orc ppd across ORC versions**

"HIVE-12363: Incorrect results with orc ppd across ORC versions (Gopal V, reviewed by Prasanth Jayachandran)"


---

* [HIVE-11825](https://issues.apache.org/jira/browse/HIVE-11825) | *Critical* | **get\_json\_object(col,\'$.a\') is null in where clause didn`t work**

Enabled to accept quoting of all character backslash qooting mechanism


---

* [HIVE-11525](https://issues.apache.org/jira/browse/HIVE-11525) | *Major* | **Bucket pruning**

Tez bucket pruning


---

* [HIVE-1841](https://issues.apache.org/jira/browse/HIVE-1841) | *Minor* | ** datanucleus.fixedDatastore should be true in hive-default.xml**

**WARNING: No release note provided for this change.**


---

* [HIVE-7926](https://issues.apache.org/jira/browse/HIVE-7926) | *Major* | **long-lived daemons for query fragment execution, I/O and caching**

LLAP is the new hybrid execution model that enables efficiencies across queries, such as caching of columnar data, JIT-friendly operator pipelines, and reduced overhead for multiple queries (including concurrent queries), as well as new performance features like asynchronous I/O, pre-fetching and multi-threaded processing. The hybrid model consists of a long-lived service interacting with on-demand elastic containers serving as a tightly integrated DAG-based framework for query execution. 

The first version of LLAP is being shipped in Hive 2.0 release. The component has been extensively exercised on test and live clusters, and tested, but is expected to have rough edges in this initial release.
The current limitations are: supported with Tez only; does not support ACID tables; the I/O elevator and cache only support ORC format and vectorized execution.


---

* [HIVE-12434](https://issues.apache.org/jira/browse/HIVE-12434) | *Major* | **Merge spark into master 11/17/1015**

Merge introduced some configurations.


---

* [HIVE-12443](https://issues.apache.org/jira/browse/HIVE-12443) | *Major* | **Hive Streaming should expose encoding and serdes for testing**

Any extensions of org.apache.hive.hcatalog.streaming.AbstractRecordWriter will need to implement two new public methods, SerDe and encode.


---

* [HIVE-12300](https://issues.apache.org/jira/browse/HIVE-12300) | *Major* | **deprecate MR in Hive 2.0**

Hive-on-MR has been deprecated in Hive 2 releases as the other, more modern and actively developed execution engines have been production-ready for some time. The support may be removed in future 2.X versions. Consider using a different execution engine (i.e. spark, tez) or using Hive 1.X releases if you want to keep using MR.


---

* [HIVE-12436](https://issues.apache.org/jira/browse/HIVE-12436) | *Major* | **Default hive.metastore.schema.verification to true**

**WARNING: No release note provided for this change.**


---

* [HIVE-12331](https://issues.apache.org/jira/browse/HIVE-12331) | *Major* | **Remove hive.enforce.bucketing & hive.enforce.sorting configs**

**WARNING: No release note provided for this change.**


---

* [HIVE-12329](https://issues.apache.org/jira/browse/HIVE-12329) | *Major* | **Turn on limit pushdown optimization by default**

**WARNING: No release note provided for this change.**


---

* [HIVE-12399](https://issues.apache.org/jira/browse/HIVE-12399) | *Critical* | **Native Vector MapJoin can encounter  "Null key not expected in MapJoin" and "Unexpected NULL in map join small table" exceptions**

HIVE-12399:  Filter out NULLs in the Native Vector MapJoin operators.


---

* [HIVE-12463](https://issues.apache.org/jira/browse/HIVE-12463) | *Major* | **VectorMapJoinFastKeyStore has Array OOB errors**

HIVE-12463: VectorMapJoinFastKeyStore has Array OOB errors


---

* [HIVE-8396](https://issues.apache.org/jira/browse/HIVE-8396) | *Major* | **Hive CliDriver command splitting can be broken when comments are present**

Hive interactive shell now strips full line comments from the input, matching the behaviour of hive -f, beeline (interactive), and beeline -f.


---

* [HIVE-12184](https://issues.apache.org/jira/browse/HIVE-12184) | *Major* | **DESCRIBE of fully qualified table fails when db and table name match and non-default database is in use**

Document the incompatible change.


---

* [HIVE-11261](https://issues.apache.org/jira/browse/HIVE-11261) | *Minor* | **DESCRIBE database qualifier does not work when calling DESCRIBE on column or nested columns.**

**WARNING: No release note provided for this change.**


---

* [HIVE-12413](https://issues.apache.org/jira/browse/HIVE-12413) | *Major* | **Default mode for hive.mapred.mode should be strict**

**WARNING: No release note provided for this change.**


---

* [HIVE-11372](https://issues.apache.org/jira/browse/HIVE-11372) | *Major* | **join with between predicate comparing integer types returns no rows when ORC format used**

Re-submit


---

* [HIVE-12609](https://issues.apache.org/jira/browse/HIVE-12609) | *Major* | **Remove javaXML serialization**

**WARNING: No release note provided for this change.**


---

* [HIVE-12694](https://issues.apache.org/jira/browse/HIVE-12694) | *Major* | **LLAP: Slider destroy semantics require force**

LLAP Slider registry cleanup requires destroy with --force


---

* [HIVE-12740](https://issues.apache.org/jira/browse/HIVE-12740) | *Critical* | **NPE with HS2 when using null input format**

HIVE-12740: NPE with HS2 when using null input format (Vikram Dixit K via Gunther Hagleitner)


---

* [HIVE-12717](https://issues.apache.org/jira/browse/HIVE-12717) | *Critical* | **Enabled to accept quoting of all character backslash qooting mechanism to json\_tuple UDTF**

Enabled to accept quoting of all character backslash qooting mechanism to JSON UDTF


---

* [HIVE-12875](https://issues.apache.org/jira/browse/HIVE-12875) | *Major* | **Verify sem.getInputs() and sem.getOutputs()**

No release notes needed here.


---

* [HIVE-12826](https://issues.apache.org/jira/browse/HIVE-12826) | *Major* | **Vectorization: fix VectorUDAF\* suspect isNull checks**

commit 36e855084da833915dfe6c34f74e19352b64fde9

    Vectorization: fix VectorUDAF\* suspect isNull checks (Gopal V, reviewed by Matt McCline)
    
    Signed-off-by: Gopal V \<gopalv@apache.org\>


---

* [HIVE-12827](https://issues.apache.org/jira/browse/HIVE-12827) | *Major* | **Vectorization: VectorCopyRow/VectorAssignRow/VectorDeserializeRow assign needs explicit isNull[offset] modification**

commit 9cab4414caf1bba2eb1852536a9d3676ba7eab21
Author: Gopal V \<gopalv@apache.org\>
Date:   Mon Jan 18 16:03:40 2016 -0800

    Vectorization: VectorCopyRow/VectorAssignRow/VectorDeserializeRow assign needs explicit isNull[offset] modification (Gopal V, reviewed by Sergey Shelukhin)
    
    Signed-off-by: Gopal V \<gopalv@apache.org\>


---

* [HIVE-12429](https://issues.apache.org/jira/browse/HIVE-12429) | *Major* | **Switch default Hive authorization to SQLStandardAuth in 2.0**

**WARNING: No release note provided for this change.**


---

* [HIVE-12809](https://issues.apache.org/jira/browse/HIVE-12809) | *Major* | **Vectorization: fast-path for coalesce if input.noNulls = true**

commit f15278af7970f8c857e52938f99c2b0fcc1a8155
Author: Gopal V \<gopalv@apache.org\>

    HIVE-12809: Vectorization: fast-path for coalesce if input.noNulls = true (Gopal V, reviewed by Sergey Shelukhin)
    
    Signed-off-by: Gopal V \<gopalv@apache.org\>



