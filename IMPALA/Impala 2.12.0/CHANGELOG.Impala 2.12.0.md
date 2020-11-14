
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
# Apache Impala Changelog

## Release Impala 2.12.0 - 2018-04-24



### NEW FEATURES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [IMPALA-2248](https://issues.apache.org/jira/browse/IMPALA-2248) | Make idle\_session\_timeout a query option |  Major | . | Matthew Jacobs | Zoltán Borók-Nagy |
| [IMPALA-3282](https://issues.apache.org/jira/browse/IMPALA-3282) | Add build-in regex\_escape() |  Minor | Backend | Huaisi Xu | Jin Chul Kim |
| [IMPALA-5300](https://issues.apache.org/jira/browse/IMPALA-5300) | Implement TABLESAMPLE |  Critical | Frontend | Alexander Behm | Alexander Behm |
| [IMPALA-4167](https://issues.apache.org/jira/browse/IMPALA-4167) | Support insert plan hints for CREATE TABLE AS SELECT |  Major | Frontend | Alexander Behm | Csaba Ringhofer |
| [IMPALA-5752](https://issues.apache.org/jira/browse/IMPALA-5752) | Add support for DECIMAL on Kudu tables |  Critical | Backend, Frontend | Matthew Jacobs | Grant Henke |
| [IMPALA-6537](https://issues.apache.org/jira/browse/IMPALA-6537) | Add missing ODBC scalar functions |  Major | . | Greg Rahn | Greg Rahn |


### IMPROVEMENTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [IMPALA-5848](https://issues.apache.org/jira/browse/IMPALA-5848) | Account for TCMalloc overhead and client cache buffers in MemTracker |  Major | Backend | Tim Armstrong | Bikramjeet Vig |
| [IMPALA-6222](https://issues.apache.org/jira/browse/IMPALA-6222) | Make it easier to root-cause "failed to get minimum memory reservation" error |  Major | Backend | Tim Armstrong | Bikramjeet Vig |
| [IMPALA-6177](https://issues.apache.org/jira/browse/IMPALA-6177) | Clean up handcrafted IRs if they encounter error during creation |  Major | Backend | Bikramjeet Vig | Bikramjeet Vig |
| [IMPALA-4168](https://issues.apache.org/jira/browse/IMPALA-4168) | Adopt Oracle-style hint placement for INSERT statements |  Major | Frontend | Alexander Behm | Jin Chul Kim |
| [IMPALA-3651](https://issues.apache.org/jira/browse/IMPALA-3651) | Implement murmur\_hash() UDF |  Minor | Backend | Tim Armstrong | Jin Chul Kim |
| [IMPALA-6387](https://issues.apache.org/jira/browse/IMPALA-6387) | test\_breakpad.py::test\_sigusr1\_writes\_minidump fails on exhaustive build |  Blocker | Infrastructure | Lars Volker | Lars Volker |
| [IMPALA-5058](https://issues.apache.org/jira/browse/IMPALA-5058) | Improve concurrency of DDL/DML operations during catalog updates |  Critical | Catalog | Dimitris Tsirogiannis | Dimitris Tsirogiannis |
| [IMPALA-5478](https://issues.apache.org/jira/browse/IMPALA-5478) | run test\_tpcds\_queries with DECIMAL\_V2=true |  Major | Infrastructure | Daniel Hecht | Taras Bobrovytsky |
| [IMPALA-4993](https://issues.apache.org/jira/browse/IMPALA-4993) | Add support for dictionary filtering on nested fields |  Major | Backend | Joe McDonnell | Vuk Ercegovac |
| [IMPALA-5052](https://issues.apache.org/jira/browse/IMPALA-5052) | Read and write signed integer logical type metadata in Parquet |  Minor | Frontend | Ian Buss | Anuj Phadke |
| [IMPALA-3998](https://issues.apache.org/jira/browse/IMPALA-3998) | Remove refresh\_after\_connect option from impala-shell |  Critical | Clients | Tim Armstrong | Tim Armstrong |
| [IMPALA-5654](https://issues.apache.org/jira/browse/IMPALA-5654) | Disallow managed Kudu table to explicitly set Kudu tbl name in CREATE TABLE |  Major | Frontend | Matthew Jacobs | Gabor Kaszab |
| [IMPALA-6128](https://issues.apache.org/jira/browse/IMPALA-6128) | Spill-to-disk Encryption(AES-CFB + SHA256) can be a performance bottleneck while IO is getting faster |  Major | Backend | Xianda Ke |  |
| [IMPALA-5990](https://issues.apache.org/jira/browse/IMPALA-5990) | End-to-end compression of metadata |  Critical | Catalog, Frontend | Alexander Behm | Tianyi Wang |
| [IMPALA-6113](https://issues.apache.org/jira/browse/IMPALA-6113) | Skip row groups with predicates on NULL columns |  Major | Backend | Lars Volker | Gabor Kaszab |
| [IMPALA-6075](https://issues.apache.org/jira/browse/IMPALA-6075) | Add Impala daemon metric for catalog version |  Major | Catalog | Tim Armstrong | Pranay Singh |
| [IMPALA-5519](https://issues.apache.org/jira/browse/IMPALA-5519) | Allocate fragment instance runtime filter memory from BufferPool |  Major | Backend | Tim Armstrong | Bikramjeet Vig |
| [IMPALA-4132](https://issues.apache.org/jira/browse/IMPALA-4132) | Consider using -fno-omit-frame-pointer in release builds |  Major | Infrastructure | Silvius Rus | Gabor Kaszab |
| [IMPALA-6437](https://issues.apache.org/jira/browse/IMPALA-6437) | increase frequency of admission control topic updates |  Major | Distributed Exec | Tim Armstrong | Tim Armstrong |
| [IMPALA-4953](https://issues.apache.org/jira/browse/IMPALA-4953) | Prevent large statestore updates from head-of-line blocking subsequent updates to different topics |  Major | Distributed Exec | Henry Robinson | Tim Armstrong |
| [IMPALA-6519](https://issues.apache.org/jira/browse/IMPALA-6519) | Allow atomic allocation of an unreserved buffer |  Major | Backend | Tim Armstrong | Tim Armstrong |
| [IMPALA-4456](https://issues.apache.org/jira/browse/IMPALA-4456) | Address scalability issues of qs\_map\_lock\_ and client\_request\_state\_map\_lock\_ |  Major | Backend | Sailesh Mukil | Sailesh Mukil |
| [IMPALA-6497](https://issues.apache.org/jira/browse/IMPALA-6497) | Impala should expose when the last row is fetched |  Major | Backend | Tim Armstrong | Tim Armstrong |
| [IMPALA-6424](https://issues.apache.org/jira/browse/IMPALA-6424) | REFRESH right after invalidate metadata \<table\> loads file metadata twice |  Critical | Catalog | Juan Yu | Dimitris Tsirogiannis |
| [IMPALA-6627](https://issues.apache.org/jira/browse/IMPALA-6627) | Document Hive-incompatible behavior with the serialization.null.format table property |  Major | Docs | Alexander Behm | Alexandra Rodoni |
| [IMPALA-6059](https://issues.apache.org/jira/browse/IMPALA-6059) | Enhance ltrim() and rtrim() functions to trim any set of characters |  Minor | Backend | Zoram Thanga | Zoram Thanga |
| [IMPALA-6629](https://issues.apache.org/jira/browse/IMPALA-6629) | Clearer and more concise logging during catalog topic updates |  Critical | Catalog | Alexander Behm | Tianyi Wang |
| [IMPALA-6675](https://issues.apache.org/jira/browse/IMPALA-6675) | Change default configuration to --compact\_catalog\_topic=true |  Major | Backend | Alexander Behm | Alexander Behm |
| [IMPALA-2782](https://issues.apache.org/jira/browse/IMPALA-2782) | Allow Impala Shell to connect directly to impalad when config with proxy load balancer and kerberos |  Minor | Clients | Alan Choi | Vincent Tran |
| [IMPALA-6324](https://issues.apache.org/jira/browse/IMPALA-6324) | Support reading RLE-encoded boolean values in Parquet scanner |  Major | Backend | Tim Armstrong | Csaba Ringhofer |
| [IMPALA-6682](https://issues.apache.org/jira/browse/IMPALA-6682) | Support hash function other than md5 in pypi download script |  Major | Infrastructure | Tianyi Wang | Tianyi Wang |
| [IMPALA-6641](https://issues.apache.org/jira/browse/IMPALA-6641) | Support more separators between date and time in default timestamp format |  Major | Backend | Tim Armstrong | Vincent Tran |
| [IMPALA-6747](https://issues.apache.org/jira/browse/IMPALA-6747) | Add a diagnostics collection script |  Major | . | Bharath Vissapragada | Bharath Vissapragada |
| [IMPALA-5721](https://issues.apache.org/jira/browse/IMPALA-5721) | stress test: save profiles during binary search |  Major | Infrastructure | Michael Brown | Michael Brown |
| [IMPALA-6779](https://issues.apache.org/jira/browse/IMPALA-6779) | Impala Doc: Improve REPLICA\_PREFERENCE doc |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6820](https://issues.apache.org/jira/browse/IMPALA-6820) | Remove builtins db from catalogd |  Minor | Catalog | Tianyi Wang | Tianyi Wang |
| [IMPALA-6822](https://issues.apache.org/jira/browse/IMPALA-6822) | Provide a query option to not shuffle on distinct exprs |  Critical | Frontend | Tianyi Wang | Tianyi Wang |
| [IMPALA-4989](https://issues.apache.org/jira/browse/IMPALA-4989) | Improve filtering based on parquet::Statistics |  Major | Backend, Frontend | Lars Volker | Lars Volker |
| [IMPALA-4634](https://issues.apache.org/jira/browse/IMPALA-4634) | Investigate enabling FS handle caching |  Minor | Backend | Bharath Vissapragada | Joe McDonnell |


### BUG FIXES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [IMPALA-5017](https://issues.apache.org/jira/browse/IMPALA-5017) | Error on decimal overflow (rather than warn) |  Major | Backend | Daniel Hecht | Taras Bobrovytsky |
| [IMPALA-6319](https://issues.apache.org/jira/browse/IMPALA-6319) | Allocation/Dealloc mismatch unique\_ptr param seems to be overwritten (mem-leak) |  Blocker | Backend | Pranay Singh | Alexander Behm |
| [IMPALA-4664](https://issues.apache.org/jira/browse/IMPALA-4664) | Impala shell can accidentally convert certain literal strings to lowercase |  Major | Clients, Infrastructure | Andre Araujo | Jin Chul Kim |
| [IMPALA-6297](https://issues.apache.org/jira/browse/IMPALA-6297) | Remove partition/sort from Kudu INSERT for unpartitioned tables |  Major | Frontend | Thomas Tauber-Marshall | Thomas Tauber-Marshall |
| [IMPALA-5754](https://issues.apache.org/jira/browse/IMPALA-5754) | rand() algorithm is very non-random |  Major | Backend | Jim Apple | Jin Chul Kim |
| [IMPALA-6295](https://issues.apache.org/jira/browse/IMPALA-6295) | Inconsistent handling of 'nan' and 'inf' with min/max analytic fns |  Critical | Backend | Thomas Tauber-Marshall | Thomas Tauber-Marshall |
| [IMPALA-6296](https://issues.apache.org/jira/browse/IMPALA-6296) | DCheck in CodegenSymbolEmitter when --asm\_module\_dir is set on debug build |  Major | Backend | Tim Armstrong | Manaswini |
| [IMPALA-6370](https://issues.apache.org/jira/browse/IMPALA-6370) | Crash when querying nested data in partitioned Parquet table |  Critical | Backend | Tim Armstrong | Tim Armstrong |
| [IMPALA-6300](https://issues.apache.org/jira/browse/IMPALA-6300) | Decimal modulo sometimes returns incorrect results |  Critical | Backend | Taras Bobrovytsky | Taras Bobrovytsky |
| [IMPALA-6364](https://issues.apache.org/jira/browse/IMPALA-6364) | Lock contention in FileHandleCache results in \>2x slowdown for remote HDFS reads |  Blocker | . | Mostafa Mokhtar | Joe McDonnell |
| [IMPALA-6362](https://issues.apache.org/jira/browse/IMPALA-6362) | Queries don't make progress due to what seems like a memory reservation deadlock while running the stress tests |  Critical | Backend | Mostafa Mokhtar | Tim Armstrong |
| [IMPALA-6355](https://issues.apache.org/jira/browse/IMPALA-6355) | dcheck failure for decimal asan tests |  Blocker | Backend | Vuk Ercegovac | Tim Armstrong |
| [IMPALA-6348](https://issues.apache.org/jira/browse/IMPALA-6348) | Redact only sensitive fields in runtime profile |  Major | . | Bharath Vissapragada | Bharath Vissapragada |
| [IMPALA-6231](https://issues.apache.org/jira/browse/IMPALA-6231) | Do some fuzz testing of decimal v2 operations |  Major | Backend | Taras Bobrovytsky | Taras Bobrovytsky |
| [IMPALA-5014](https://issues.apache.org/jira/browse/IMPALA-5014) | DECIMAL V2 round when casting to/from DECIMAL, part 2 |  Major | Backend | Daniel Hecht | Taras Bobrovytsky |
| [IMPALA-6384](https://issues.apache.org/jira/browse/IMPALA-6384) | RequestPoolService doesn't honor custom user -\> group mapping overrides in HDFS config |  Major | Frontend | Bharath Vissapragada | Bharath Vissapragada |
| [IMPALA-3887](https://issues.apache.org/jira/browse/IMPALA-3887) | Planner tests failing due to metadata loading race with HDFS, fewer #hosts than expected |  Blocker | Infrastructure | Jim Apple | Tianyi Wang |
| [IMPALA-6363](https://issues.apache.org/jira/browse/IMPALA-6363) | cscope build step seems racy, breaks compilation |  Critical | Infrastructure | Michael Brown | Tim Armstrong |
| [IMPALA-6307](https://issues.apache.org/jira/browse/IMPALA-6307) | A CTAS query fails with error: AnalysisException: Duplicate column name: \<columnName\> |  Critical | Frontend | Zoram Thanga | Zoram Thanga |
| [IMPALA-6388](https://issues.apache.org/jira/browse/IMPALA-6388) | UnionNode sets the number of nodes incorrectly |  Critical | Frontend | Alexander Behm | Taras Bobrovytsky |
| [IMPALA-6353](https://issues.apache.org/jira/browse/IMPALA-6353) | Crash in snappy decompressor |  Blocker | Backend | Vuk Ercegovac | Tianyi Wang |
| [IMPALA-4315](https://issues.apache.org/jira/browse/IMPALA-4315) | USE \<db\> statement throws auth error if user only has column privileges |  Major | Frontend | Dimitris Tsirogiannis | Csaba Ringhofer |
| [IMPALA-6081](https://issues.apache.org/jira/browse/IMPALA-6081) | TestRuntimeFilters fails due to runtime profile missing portions |  Blocker | Backend | Jim Apple | Thomas Tauber-Marshall |
| [IMPALA-6386](https://issues.apache.org/jira/browse/IMPALA-6386) | Dataload can fail due to "invalidate metadata" concurrent with DDLs |  Critical | Infrastructure | Joe McDonnell | Joe McDonnell |
| [IMPALA-6419](https://issues.apache.org/jira/browse/IMPALA-6419) | hdfs-parquet-scanner.cc:624] Check failed: 0 == context\_-\>NumStreams() (0 vs. 11) |  Blocker | Backend | Tim Armstrong | Tim Armstrong |
| [IMPALA-6414](https://issues.apache.org/jira/browse/IMPALA-6414) | Impalad binary failed to start with SIGSEGV with GPerfTools 2.6.3 on certain platforms |  Critical | Backend | Michael Ho | Michael Ho |
| [IMPALA-6368](https://issues.apache.org/jira/browse/IMPALA-6368) | test\_chars.py races with itself when run in parallel |  Major | Infrastructure | Tim Armstrong | Tim Armstrong |
| [IMPALA-6382](https://issues.apache.org/jira/browse/IMPALA-6382) | Impalad crashes on SELECT query when spill buffer is set on certain values |  Critical | Backend | Xinran Tinney | Bikramjeet Vig |
| [IMPALA-6427](https://issues.apache.org/jira/browse/IMPALA-6427) | Planner test expected output drops QUERYOPTIONS sections |  Major | Infrastructure | Tim Armstrong | Tim Armstrong |
| [IMPALA-6399](https://issues.apache.org/jira/browse/IMPALA-6399) | test\_query\_profile\_thrift\_timestamps failure on exhaustive runs |  Blocker | Infrastructure | Sailesh Mukil | Lars Volker |
| [IMPALA-6418](https://issues.apache.org/jira/browse/IMPALA-6418) | Find a reliable way to detect supported TLS versions |  Blocker | Security | Sailesh Mukil | Sailesh Mukil |
| [IMPALA-3942](https://issues.apache.org/jira/browse/IMPALA-3942) | After creating a view that uses regexp\_replace we are getting the following error:  ERROR: AnalysisException: Failed to load metadata for table: |  Minor | Frontend | Jeff Lord | Jin Chul Kim |
| [IMPALA-6435](https://issues.apache.org/jira/browse/IMPALA-6435) | Codegen crash when UNIONing CHAR(n) literals |  Blocker | Backend | Balazs Jeszenszky | Anuj Phadke |
| [IMPALA-6377](https://issues.apache.org/jira/browse/IMPALA-6377) | Bump breakpad version to include the fix for Breakpad #752 |  Critical | Backend | Lars Volker | Lars Volker |
| [IMPALA-6334](https://issues.apache.org/jira/browse/IMPALA-6334) | test\_compute\_stats\_tablesample failing on Isilon builds |  Critical | . | David Knupp | Alexander Behm |
| [IMPALA-6455](https://issues.apache.org/jira/browse/IMPALA-6455) | test\_partition\_metadata\_compatibility flaky failures |  Blocker | Infrastructure | Sailesh Mukil | Tim Armstrong |
| [IMPALA-6450](https://issues.apache.org/jira/browse/IMPALA-6450) | Hit DCHECK in RuntimeProfile::EventSequence::Start() |  Blocker | Backend | Tim Armstrong | Tim Armstrong |
| [IMPALA-6383](https://issues.apache.org/jira/browse/IMPALA-6383) | Memory from previous row groups can accumulate in Parquet scanner |  Major | Backend | Tim Armstrong | Tim Armstrong |
| [IMPALA-6242](https://issues.apache.org/jira/browse/IMPALA-6242) | Flaky test: TimerCounterTest.CountersTestOneThread |  Critical | Backend | Tianyi Wang | Tianyi Wang |
| [IMPALA-6476](https://issues.apache.org/jira/browse/IMPALA-6476) | TestKrpcMemUsage.test\_krpc\_deferred\_memory\_usage fails on release build |  Blocker | Infrastructure | Alexander Behm | Lars Volker |
| [IMPALA-6485](https://issues.apache.org/jira/browse/IMPALA-6485) | BE compilation failure: error: ‘EVP\_CTRL\_GCM\_SET\_IVLEN’ was not declared in this scope |  Blocker | Backend | Alexander Behm | Tim Armstrong |
| [IMPALA-6478](https://issues.apache.org/jira/browse/IMPALA-6478) | NativeAddPendingTopicItem prints garbage into log |  Trivial | . | Tianyi Wang | Tianyi Wang |
| [IMPALA-6495](https://issues.apache.org/jira/browse/IMPALA-6495) | targeted-perf tests broken by column alias change |  Major | Infrastructure | Tim Armstrong | Tim Armstrong |
| [IMPALA-6484](https://issues.apache.org/jira/browse/IMPALA-6484) | Crash in impala::RuntimeProfile::SortChildren |  Blocker | Backend | Alexander Behm | Thomas Tauber-Marshall |
| [IMPALA-6486](https://issues.apache.org/jira/browse/IMPALA-6486) | INVALIDATE METADATA may hang after statestore restart |  Blocker | Catalog | Dimitris Tsirogiannis | Philip Martin |
| [IMPALA-6454](https://issues.apache.org/jira/browse/IMPALA-6454) | CTAS into Kudu fails with mixed-case partition and/pr primary key column names |  Critical | Frontend | Alexander Behm | Pranay Singh |
| [IMPALA-5909](https://issues.apache.org/jira/browse/IMPALA-5909) | File handle cache causes HDFS to log excessive errors when trying to unbuffer files |  Major | Backend | Tim Armstrong | Joe McDonnell |
| [IMPALA-6489](https://issues.apache.org/jira/browse/IMPALA-6489) | ASAN use-after-poison in impala::HdfsScanner::InitTupleFromTemplate |  Blocker | Backend | Alexander Behm | Tim Armstrong |
| [IMPALA-6511](https://issues.apache.org/jira/browse/IMPALA-6511) | Fix event "Open Finished" in state machine in FragmentInstanceState::UpdateState() |  Major | Backend | Lars Volker | Lars Volker |
| [IMPALA-6392](https://issues.apache.org/jira/browse/IMPALA-6392) | Explain format for parquet predicate statistics should be consistent with predicates |  Minor | Frontend | Vuk Ercegovac | Fredy Wijaya |
| [IMPALA-5269](https://issues.apache.org/jira/browse/IMPALA-5269) | Comment on Final Line of Query Breaks Parsing |  Major | Clients | Alan Jackoway | Fredy Wijaya |
| [IMPALA-6516](https://issues.apache.org/jira/browse/IMPALA-6516) | Avoid logging during catalog update if the catalog version didn't change |  Minor | Catalog | Michael Ho | Tianyi Wang |
| [IMPALA-6526](https://issues.apache.org/jira/browse/IMPALA-6526) | Regression: query\_test.test\_spilling.TestSpillingDebugActionDimensions.test\_spilling |  Blocker | Backend | Zach Amsden | Bikramjeet Vig |
| [IMPALA-6423](https://issues.apache.org/jira/browse/IMPALA-6423) | HDFS scanners do not get cancelled in a timely manner |  Critical | Backend | Quanlong Huang | Gabor Kaszab |
| [IMPALA-5152](https://issues.apache.org/jira/browse/IMPALA-5152) | Frontend requests metadata for one table at a time in the query |  Critical | Catalog, Frontend | Mostafa Mokhtar | Alexander Behm |
| [IMPALA-6517](https://issues.apache.org/jira/browse/IMPALA-6517) | bootstrap\_toolchain.py fails to recognize lsb\_release output from RHEL |  Minor | . | Vincent Tran | Vincent Tran |
| [IMPALA-6275](https://issues.apache.org/jira/browse/IMPALA-6275) | Successful CTAS logs warning |  Major | Frontend | Tim Armstrong | Fredy Wijaya |
| [IMPALA-6567](https://issues.apache.org/jira/browse/IMPALA-6567) | Dataload performance regression due to slow invalidate metadata |  Blocker | Frontend | Joe McDonnell | Alexander Behm |
| [IMPALA-6008](https://issues.apache.org/jira/browse/IMPALA-6008) | Creating a UDF from a shared library with a .ll extension crashes Impala |  Critical | Backend | Tim Armstrong | Anuj Phadke |
| [IMPALA-6579](https://issues.apache.org/jira/browse/IMPALA-6579) | Data load failing with Error opening Kudu table 'impala::tpch\_kudu.lineitem', Kudu error: The table does not exist: table\_name: "impala::tpch\_kudu.lineitem" |  Blocker | Infrastructure | Tim Armstrong | Joe McDonnell |
| [IMPALA-6580](https://issues.apache.org/jira/browse/IMPALA-6580) | Cannot load Kudu functional data on localfs build |  Blocker | Infrastructure | Tim Armstrong | Joe McDonnell |
| [IMPALA-6549](https://issues.apache.org/jira/browse/IMPALA-6549) | Enable file handle cache by default |  Critical | Backend | Joe McDonnell | Joe McDonnell |
| [IMPALA-6577](https://issues.apache.org/jira/browse/IMPALA-6577) | TestQueryExpiration::test\_concurrent\_query\_expiration failing |  Blocker | Backend | Tim Armstrong | Tim Armstrong |
| [IMPALA-6586](https://issues.apache.org/jira/browse/IMPALA-6586) | FrontendTest.TestGetTablesTypeTable failing on some builds |  Blocker | Frontend | Tim Armstrong | Alexander Behm |
| [IMPALA-6584](https://issues.apache.org/jira/browse/IMPALA-6584) | TestKuduOperations::test\_column\_storage\_attributes broken on exhaustive build |  Blocker | Infrastructure | Tim Armstrong | Grant Henke |
| [IMPALA-6588](https://issues.apache.org/jira/browse/IMPALA-6588) | test\_compute\_stats\_tablesample failing with "Cancelled" |  Blocker | Backend | Tim Armstrong | Tim Armstrong |
| [IMPALA-6543](https://issues.apache.org/jira/browse/IMPALA-6543) | Limit RowBatch serialization size to INT\_MAX |  Major | Backend | Joe McDonnell | Joe McDonnell |
| [IMPALA-6530](https://issues.apache.org/jira/browse/IMPALA-6530) | Track time spent opening HDFS file handles |  Major | Backend | Joe McDonnell | Joe McDonnell |
| [IMPALA-5139](https://issues.apache.org/jira/browse/IMPALA-5139) | Make mvn-quiet.sh write its output to a logfile |  Major | Infrastructure | Lars Volker | nithya |
| [IMPALA-6585](https://issues.apache.org/jira/browse/IMPALA-6585) | test\_low\_mem\_limit\_q21 flaky under ASAN |  Critical | Infrastructure | Tim Armstrong | Tim Armstrong |
| [IMPALA-6258](https://issues.apache.org/jira/browse/IMPALA-6258) | Uninitialized tuple pointers in row batch for empty rows |  Critical | Backend | Michael Ho | Zoltán Borók-Nagy |
| [IMPALA-6583](https://issues.apache.org/jira/browse/IMPALA-6583) | Various tests fail with missing database or table from catalog |  Blocker | Catalog | Tim Armstrong | Tianyi Wang |
| [IMPALA-6603](https://issues.apache.org/jira/browse/IMPALA-6603) | Fix output for cherry-picking job |  Major | Infrastructure | Lars Volker | Lars Volker |
| [IMPALA-6599](https://issues.apache.org/jira/browse/IMPALA-6599) | Log spam: ImpaladCatalog.java:525] NativeLibCacheSetNeedsRefresh(hdfs://localhost:20500/test-warehouse/test-udfs.ll) failed. |  Critical | Backend | Tim Armstrong | Vuk Ercegovac |
| [IMPALA-6601](https://issues.apache.org/jira/browse/IMPALA-6601) | ASAN memcpy-param-overlap in impala::RawValue::Write during RowBatchSerializeTest.RowBatchLZ4Success |  Blocker | Backend | Lars Volker | Joe McDonnell |
| [IMPALA-6553](https://issues.apache.org/jira/browse/IMPALA-6553) | Impala Doc: load\_catalog\_in\_background default changed to false |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-2642](https://issues.apache.org/jira/browse/IMPALA-2642) | Potential deadlock in statestore error path |  Minor | Distributed Exec | Henry Robinson | Zoram Thanga |
| [IMPALA-6405](https://issues.apache.org/jira/browse/IMPALA-6405) | There is no error under Decimal v2 when there is an overflow when casting String to Decimal |  Blocker | Backend | Taras Bobrovytsky | Taras Bobrovytsky |
| [IMPALA-6595](https://issues.apache.org/jira/browse/IMPALA-6595) | Hit crash freeing buffer in NljBuilder::Close() |  Blocker | Backend | Tim Armstrong | Tim Armstrong |
| [IMPALA-6606](https://issues.apache.org/jira/browse/IMPALA-6606) | date\_trunc with MILLENNIUM returns 2000 instead of 2001 |  Critical | Backend | Tim Armstrong | Attila Jeges |
| [IMPALA-6602](https://issues.apache.org/jira/browse/IMPALA-6602) | TestQueryExpiration.test\_query\_expiration fails on Isilon with FINISHED rather than EXCEPTION state |  Blocker | Backend | Lars Volker | Vuk Ercegovac |
| [IMPALA-6527](https://issues.apache.org/jira/browse/IMPALA-6527) | NaN values lead to incorrect statistics filtering under certain circumstances |  Blocker | Backend | Zoltan Ivanfi | Zoltán Borók-Nagy |
| [IMPALA-6515](https://issues.apache.org/jira/browse/IMPALA-6515) | Impala Doc: HAproxy with sticky session requires the check option |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6500](https://issues.apache.org/jira/browse/IMPALA-6500) | Impala crashes under certain hypervisors that return out-of-range CPU IDs |  Critical | Backend | Osama Suleiman | Tim Armstrong |
| [IMPALA-6638](https://issues.apache.org/jira/browse/IMPALA-6638) | File handle cache shows contention when cold |  Major | Backend | Joe McDonnell | Joe McDonnell |
| [IMPALA-6449](https://issues.apache.org/jira/browse/IMPALA-6449) | Use CLOCK\_MONOTONIC in ConditonVariable |  Minor | Backend | Michael Ho | Michael Ho |
| [IMPALA-6619](https://issues.apache.org/jira/browse/IMPALA-6619) | Alter table recover partitions creates unneeded partitions when faces percent sign |  Major | Frontend | Miklos Szurap | Fredy Wijaya |
| [IMPALA-6635](https://issues.apache.org/jira/browse/IMPALA-6635) | IllegalStateException when applying an "in" predicate on a Kudu DECIMAL col |  Critical | . | Thomas Tauber-Marshall | Grant Henke |
| [IMPALA-6488](https://issues.apache.org/jira/browse/IMPALA-6488) | Crash in LibCache::GetCacheEntryInternal() |  Blocker | Backend | Vuk Ercegovac | Vuk Ercegovac |
| [IMPALA-5270](https://issues.apache.org/jira/browse/IMPALA-5270) | Crash with ORDER BY in OVER clause with RANDOM |  Critical | Frontend | Thomas Tauber-Marshall | Alexander Behm |
| [IMPALA-6498](https://issues.apache.org/jira/browse/IMPALA-6498) | test\_query\_profile\_thrift\_timestamps causes following tests to fail |  Major | Infrastructure | Thomas Tauber-Marshall | Zoram Thanga |
| [IMPALA-6683](https://issues.apache.org/jira/browse/IMPALA-6683) | Restarting the Catalog without restarting Impalad and SS can block topic updates |  Blocker | Catalog | Mostafa Mokhtar | Tianyi Wang |
| [IMPALA-6697](https://issues.apache.org/jira/browse/IMPALA-6697) | Setuptools 39.0.0 does not work with Python 2.6 |  Blocker | Infrastructure | Lars Volker | Lars Volker |
| [IMPALA-6695](https://issues.apache.org/jira/browse/IMPALA-6695) | Builds fail with pkg\_resources.VersionConflict |  Blocker | Infrastructure | Lars Volker | Lars Volker |
| [IMPALA-6690](https://issues.apache.org/jira/browse/IMPALA-6690) | Invalid syntax in pip\_download.py due to a recent patch |  Blocker | Infrastructure | Taras Bobrovytsky | Tianyi Wang |
| [IMPALA-6613](https://issues.apache.org/jira/browse/IMPALA-6613) | Change TEST\_KRPC to DISABLE\_KRPC |  Major | Infrastructure | Lars Volker | Lars Volker |
| [IMPALA-6582](https://issues.apache.org/jira/browse/IMPALA-6582) | Flaky test: TestImpalaShellInteractive::test\_multiline\_queries\_in\_history |  Critical | Infrastructure | Tim Armstrong | Tim Armstrong |
| [IMPALA-6687](https://issues.apache.org/jira/browse/IMPALA-6687) | Upsert fails on Kudu table with upper case primary key and default value |  Critical | Catalog | Thomas Tauber-Marshall | Thomas Tauber-Marshall |
| [IMPALA-6589](https://issues.apache.org/jira/browse/IMPALA-6589) | Fuzz test on parquet table crashes impala |  Critical | Backend | Tim Armstrong | Tim Armstrong |
| [IMPALA-6654](https://issues.apache.org/jira/browse/IMPALA-6654) | [DOCS] Kudu/Sentry docs are out of date |  Critical | Docs | Thomas Tauber-Marshall | Alexandra Rodoni |
| [IMPALA-6670](https://issues.apache.org/jira/browse/IMPALA-6670) | Executor-only impalads do not refresh their lib-cache entries |  Blocker | Backend, Frontend | Vuk Ercegovac | Vuk Ercegovac |
| [IMPALA-6722](https://issues.apache.org/jira/browse/IMPALA-6722) | Local build failing due to missing libTestUdfs.so |  Blocker | Infrastructure | Taras Bobrovytsky | Vuk Ercegovac |
| [IMPALA-6715](https://issues.apache.org/jira/browse/IMPALA-6715) | stress test is double-counting TPCDS queries |  Major | Infrastructure | Michael Brown | Michael Brown |
| [IMPALA-6743](https://issues.apache.org/jira/browse/IMPALA-6743) | bump 2.x's version |  Major | Infrastructure | Vuk Ercegovac | Vuk Ercegovac |
| [IMPALA-6752](https://issues.apache.org/jira/browse/IMPALA-6752) | import kudu fails in python on Ubuntu 16.04 |  Blocker | Infrastructure | Tim Armstrong | Tim Armstrong |
| [IMPALA-6759](https://issues.apache.org/jira/browse/IMPALA-6759) | stress test can't parse explain string with petabyte memory estimates (really) |  Major | Infrastructure | Michael Brown | Michael Brown |
| [IMPALA-6717](https://issues.apache.org/jira/browse/IMPALA-6717) | common\_query\_options are not used in binary search phase of stress test |  Major | Infrastructure | Tim Armstrong | Michael Brown |
| [IMPALA-6731](https://issues.apache.org/jira/browse/IMPALA-6731) | Build failed with distutils.errors.DistutilsError: Could not find suitable distribution |  Blocker | Infrastructure | Michael Ho | Lars Volker |
| [IMPALA-2567](https://issues.apache.org/jira/browse/IMPALA-2567) | KRPC milestone 1 |  Critical | Distributed Exec | Henry Robinson | Michael Ho |
| [IMPALA-6694](https://issues.apache.org/jira/browse/IMPALA-6694) | BufferPool appears misaligned in query profile |  Critical | Backend | Michael Ho | Tim Armstrong |
| [IMPALA-6739](https://issues.apache.org/jira/browse/IMPALA-6739) | Exception in ALTER TABLE SET statements |  Minor | Frontend | Adam Holley | Fredy Wijaya |
| [IMPALA-6719](https://issues.apache.org/jira/browse/IMPALA-6719) | refresh function case sensitivity |  Major | Frontend | Vuk Ercegovac | Fredy Wijaya |
| [IMPALA-6371](https://issues.apache.org/jira/browse/IMPALA-6371) | Not correctly validating unicode delimiters. |  Minor | Frontend | Adam Holley | Adam Holley |
| [IMPALA-4323](https://issues.apache.org/jira/browse/IMPALA-4323) | It is not possible to set row format through alter table |  Major | Frontend | Taras Bobrovytsky | Adam Holley |
| [IMPALA-6571](https://issues.apache.org/jira/browse/IMPALA-6571) | NullPointerException in SHOW CREATE TABLE for HBase tables |  Major | Frontend | Fredy Wijaya | Fredy Wijaya |
| [IMPALA-6792](https://issues.apache.org/jira/browse/IMPALA-6792) | Appears to be a memory leak in orphaned fragments |  Critical | Backend | Mostafa Mokhtar | Sailesh Mukil |
| [IMPALA-6785](https://issues.apache.org/jira/browse/IMPALA-6785) | Starting an Impalad on an already running cluster may result in inconsistent cluster subscription |  Critical | Distributed Exec | Mostafa Mokhtar | Tim Armstrong |
| [IMPALA-6806](https://issues.apache.org/jira/browse/IMPALA-6806) | TLS certificate with Intermediate CA in server cert file fails with KRPC |  Blocker | Security | Sailesh Mukil | Sailesh Mukil |
| [IMPALA-6824](https://issues.apache.org/jira/browse/IMPALA-6824) | Crash in RuntimeProfile::EventSequence::AddNewerEvents() when events\_ is empty |  Blocker | Backend | Lars Volker | Lars Volker |
| [IMPALA-6215](https://issues.apache.org/jira/browse/IMPALA-6215) | Race between lib\_cache and java udf class loading |  Major | Backend, Frontend | Vuk Ercegovac | Vuk Ercegovac |
| [IMPALA-6710](https://issues.apache.org/jira/browse/IMPALA-6710) | Docs around INSERT into partitioned tables are misleading |  Major | Docs | Thomas Tauber-Marshall | Alexandra Rodoni |
| [IMPALA-6466](https://issues.apache.org/jira/browse/IMPALA-6466) | Impala 2.12 Doc: Document clustered/noclustered hint for inserts into Kudu table |  Major | Docs | Lars Volker | Alexandra Rodoni |
| [IMPALA-6092](https://issues.apache.org/jira/browse/IMPALA-6092) | Flaky test: query\_test/test\_udfs.py still happening |  Blocker | Infrastructure | Tim Armstrong | Vuk Ercegovac |
| [IMPALA-6811](https://issues.apache.org/jira/browse/IMPALA-6811) | test\_exchange\_delays failed |  Blocker | Backend | Tianyi Wang | Joe McDonnell |
| [IMPALA-6451](https://issues.apache.org/jira/browse/IMPALA-6451) | Creating a Kudu table with CTAS fails with AuthorizationException: User 'username' does not have privileges to access: server1 |  Critical | Frontend, Security | Tomas Farkas | Fredy Wijaya |
| [IMPALA-6774](https://issues.apache.org/jira/browse/IMPALA-6774) | SyntaxError: invalid syntax diagnostics/collect\_diagnostics.py |  Blocker | Infrastructure | Michael Ho | Bharath Vissapragada |
| [IMPALA-6394](https://issues.apache.org/jira/browse/IMPALA-6394) | GVO failed in "Waiting for HDFS replication" |  Critical | Infrastructure | Tim Armstrong | Tianyi Wang |
| [IMPALA-6381](https://issues.apache.org/jira/browse/IMPALA-6381) | test\_exchange\_delays.py failed on isilon build due to sender timeout |  Critical | Infrastructure | Zoram Thanga | Joe McDonnell |
| [IMPALA-6793](https://issues.apache.org/jira/browse/IMPALA-6793) | Metadata doesn't recover after restarting statestore |  Blocker | Catalog | Tianyi Wang | Tianyi Wang |
| [IMPALA-6896](https://issues.apache.org/jira/browse/IMPALA-6896) | NullPointerException in DESCRIBE FORMATTED on views |  Blocker | Frontend | Fredy Wijaya | Fredy Wijaya |
| [IMPALA-6475](https://issues.apache.org/jira/browse/IMPALA-6475) | Enable running TPCH on Kudu in our nightly tests |  Major | Infrastructure | Taras Bobrovytsky |  |
| [IMPALA-5747](https://issues.apache.org/jira/browse/IMPALA-5747) | Crash with --asm\_module\_dir set |  Minor | Backend | Tim Armstrong | Manaswini |
| [IMPALA-7305](https://issues.apache.org/jira/browse/IMPALA-7305) | membership entry for failed impalad gets stuck in statestore due to race between failure detection and update processing |  Critical | Distributed Exec | Tim Armstrong | Tim Armstrong |
| [IMPALA-7173](https://issues.apache.org/jira/browse/IMPALA-7173) | [DOCS] load balancer config should add "check" in more places |  Minor | Docs | Laurel Hale | Alexandra Rodoni |
| [IMPALA-7513](https://issues.apache.org/jira/browse/IMPALA-7513) | Fix Sentry compilation error in Impala 2.x branch |  Major | Infrastructure | Fredy Wijaya | Fredy Wijaya |
| [IMPALA-6764](https://issues.apache.org/jira/browse/IMPALA-6764) | Codegend UnionNode::MaterializeBatch() causes memory corruption crash of Impalad |  Critical | Backend | Zoram Thanga | Zoram Thanga |
| [IMPALA-7490](https://issues.apache.org/jira/browse/IMPALA-7490) | Uninitialized variable in data-load.py causes misleading error messages |  Major | Infrastructure | Quanlong Huang | Quanlong Huang |
| [IMPALA-4816](https://issues.apache.org/jira/browse/IMPALA-4816) | There is no way to determine if a filter was dropped due to OOM based on profile |  Major | Backend | Tim Armstrong | Bikramjeet Vig |
| [IMPALA-2648](https://issues.apache.org/jira/browse/IMPALA-2648) | catalogd crashes when serialized messages are over 2 GB |  Critical | Catalog | Silvius Rus | Tianyi Wang |
| [IMPALA-6754](https://issues.apache.org/jira/browse/IMPALA-6754) | Exchange node includes FirstBatchArrivalWaitTime in summary |  Minor | Backend | Balazs Jeszenszky | Michael Ho |


### SUB-TASKS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [IMPALA-5310](https://issues.apache.org/jira/browse/IMPALA-5310) | Implement TABLESAMPLE for COMPUTE STATS |  Major | Frontend | Alexander Behm | Alexander Behm |
| [IMPALA-5948](https://issues.apache.org/jira/browse/IMPALA-5948) | Conflicting port 29000 with Sentry |  Major | . | Daniel Hecht | Joe McDonnell |
| [IMPALA-5557](https://issues.apache.org/jira/browse/IMPALA-5557) | Disable rpc\_default\_keepalive\_time\_ms |  Major | Distributed Exec | Mostafa Mokhtar | Michael Ho |
| [IMPALA-6290](https://issues.apache.org/jira/browse/IMPALA-6290) | Simplify ScannerContext buffer management to only use one I/O buffer at a time. |  Major | Backend | Tim Armstrong | Tim Armstrong |
| [IMPALA-2397](https://issues.apache.org/jira/browse/IMPALA-2397) | Use atomic operations for simple numeric metrics |  Minor | Backend | Tim Armstrong | Michael Ho |
| [IMPALA-6268](https://issues.apache.org/jira/browse/IMPALA-6268) | KerberosOnAndOff/RpcMgrKerberizedTest.MultipleServices failing |  Critical | Backend | Philip Martin | Sailesh Mukil |
| [IMPALA-6190](https://issues.apache.org/jira/browse/IMPALA-6190) | Add a debug webpage to show fragment instances of a query |  Major | Backend, Distributed Exec | Lars Volker | Lars Volker |
| [IMPALA-6246](https://issues.apache.org/jira/browse/IMPALA-6246) | Add timeline information to fragment instances in profile |  Major | Backend, Distributed Exec | Lars Volker | Lars Volker |
| [IMPALA-6356](https://issues.apache.org/jira/browse/IMPALA-6356) | Excessive synchronous logging in RpczStore::LogTrace causes severe slowdown for exchange operators spanning 2-3 minutes |  Critical | Distributed Exec | Mostafa Mokhtar | Michael Ho |
| [IMPALA-5054](https://issues.apache.org/jira/browse/IMPALA-5054) | Enable KRPC TLS in Impala |  Major | Distributed Exec, Security | Henry Robinson | Sailesh Mukil |
| [IMPALA-6024](https://issues.apache.org/jira/browse/IMPALA-6024) | Add minimum sample size for COMPUTE STATS TABLESAMPLE |  Major | Frontend | Alexander Behm | Alexander Behm |
| [IMPALA-6193](https://issues.apache.org/jira/browse/IMPALA-6193) | Track RPC allocated memory in a memtracker |  Major | Backend | Lars Volker | Lars Volker |
| [IMPALA-6430](https://issues.apache.org/jira/browse/IMPALA-6430) | Log a detailed error message on failure of MetricVerifier |  Major | Backend | Bikramjeet Vig | Bikramjeet Vig |
| [IMPALA-3562](https://issues.apache.org/jira/browse/IMPALA-3562) | Extend "compute stats" syntax to support a list of columns |  Minor | Frontend | Mostafa Mokhtar | Vuk Ercegovac |
| [IMPALA-6346](https://issues.apache.org/jira/browse/IMPALA-6346) | Potential deadlock in KrpcDataStreamMgr |  Major | Distributed Exec | Lars Volker | Sailesh Mukil |
| [IMPALA-6228](https://issues.apache.org/jira/browse/IMPALA-6228) | More flexible configuration of stats extrapolation |  Major | Frontend | Alexander Behm | Alexander Behm |
| [IMPALA-6448](https://issues.apache.org/jira/browse/IMPALA-6448) | Re-enable kerberized testing with KRPC |  Critical | . | Sailesh Mukil | Sailesh Mukil |
| [IMPALA-6508](https://issues.apache.org/jira/browse/IMPALA-6508) | Allow tests to run with Krpc |  Blocker | Infrastructure | Lars Volker | Lars Volker |
| [IMPALA-6116](https://issues.apache.org/jira/browse/IMPALA-6116) | Bound memory usage of KRPC service queue |  Major | Distributed Exec | Michael Ho | Michael Ho |
| [IMPALA-5518](https://issues.apache.org/jira/browse/IMPALA-5518) | Allocate KrpcDataStreamRecvr RowBatch tuples from BufferPool |  Major | . | Henry Robinson | Michael Ho |
| [IMPALA-5528](https://issues.apache.org/jira/browse/IMPALA-5528) | tcmalloc contention much higher with concurrency after KRPC patch |  Critical | Distributed Exec | Henry Robinson | Mostafa Mokhtar |
| [IMPALA-4874](https://issues.apache.org/jira/browse/IMPALA-4874) | Increase maximum KRPC message size |  Major | Distributed Exec | Henry Robinson | Joe McDonnell |
| [IMPALA-6538](https://issues.apache.org/jira/browse/IMPALA-6538) | Fix read path when Parquet min(\_value)/max(\_value) statistics contain NaN |  Major | . | Zoltán Borók-Nagy | Zoltán Borók-Nagy |
| [IMPALA-6219](https://issues.apache.org/jira/browse/IMPALA-6219) | Use AES-GCM for spill-to-disk encryption when CLMUL instruction is present and performant |  Major | Backend | Jim Apple | Xianda Ke |
| [IMPALA-6482](https://issues.apache.org/jira/browse/IMPALA-6482) | Add query option for query time limit |  Major | Backend | Tim Armstrong | Tim Armstrong |
| [IMPALA-6512](https://issues.apache.org/jira/browse/IMPALA-6512) | test\_exchange\_delays does not work with KRPC enabled |  Major | Infrastructure | Lars Volker | Michael Ho |
| [IMPALA-6554](https://issues.apache.org/jira/browse/IMPALA-6554) | Check failed: consumption\_-\>current\_value() == 0 (126 vs. 0) KrpcDataStreamRecvr |  Blocker | Distributed Exec | Michael Ho | Michael Ho |
| [IMPALA-6565](https://issues.apache.org/jira/browse/IMPALA-6565) | Stress test with KRPC enabled shows inconsistent results for some queries |  Blocker | Distributed Exec | Michael Ho | Michael Ho |
| [IMPALA-6269](https://issues.apache.org/jira/browse/IMPALA-6269) | [observability] Add KRPC metrics to /rpcz and /metrics debug webpages |  Major | Distributed Exec | Sailesh Mukil | Lars Volker |
| [IMPALA-6432](https://issues.apache.org/jira/browse/IMPALA-6432) | Default rpc\_negotiation\_timeout\_ms may cause queries to fail on large clusters |  Critical | Distributed Exec | Mostafa Mokhtar | Sailesh Mukil |
| [IMPALA-6477](https://issues.apache.org/jira/browse/IMPALA-6477) | rpc-mgr-kerberized-test fails on CentOS 6.4 |  Blocker | Infrastructure | Alexander Behm | Sailesh Mukil |
| [IMPALA-6347](https://issues.apache.org/jira/browse/IMPALA-6347) | Monitor queue depth size for outgoing RPCs for Reactor threads |  Major | . | Mostafa Mokhtar | Sailesh Mukil |
| [IMPALA-6542](https://issues.apache.org/jira/browse/IMPALA-6542) | Fix inconsistent write path of Parquet min/max statistics |  Major | . | Zoltán Borók-Nagy | Zoltán Borók-Nagy |
| [IMPALA-6592](https://issues.apache.org/jira/browse/IMPALA-6592) | Fix test gap - no test of handling for invalid/unsupported Parquet codec |  Major | Backend | Tim Armstrong | Tim Armstrong |
| [IMPALA-6609](https://issues.apache.org/jira/browse/IMPALA-6609) | Some COUNTER\_ADD() in KrpcDataStreamRecvr may lead to use-after-free |  Blocker | Distributed Exec | Michael Ho | Michael Ho |
| [IMPALA-6576](https://issues.apache.org/jira/browse/IMPALA-6576) | Add metric for Data Stream Service Queue memory consumption |  Major | Backend | Lars Volker | Lars Volker |
| [IMPALA-6624](https://issues.apache.org/jira/browse/IMPALA-6624) | Network error: failed to write to TLS socket: error:1409F07F:SSL routines:SSL3\_WRITE\_PENDING:bad write retry:s3\_pkt.c |  Blocker | Distributed Exec | Michael Ho | Michael Ho |
| [IMPALA-6652](https://issues.apache.org/jira/browse/IMPALA-6652) | KRPC : Data Stream Manager Deferred RPCs in memz page should be renamed |  Major | Distributed Exec | Mostafa Mokhtar | Lars Volker |
| [IMPALA-6594](https://issues.apache.org/jira/browse/IMPALA-6594) | Various tests failing (some flaky) with memory limit exceeded |  Major | Backend | Tim Armstrong | Tim Armstrong |
| [IMPALA-6416](https://issues.apache.org/jira/browse/IMPALA-6416) | Extend Thread::Create to track fragment instance id automatically based on parent's fid |  Major | . | Zoltán Borók-Nagy | Zoltán Borók-Nagy |
| [IMPALA-6669](https://issues.apache.org/jira/browse/IMPALA-6669) | Remove NeedsSeedingForBatchedReading() |  Major | Backend | Tim Armstrong | Tim Armstrong |
| [IMPALA-6691](https://issues.apache.org/jira/browse/IMPALA-6691) | KRPC w/ kerberos fails on SLES11 |  Critical | . | Sailesh Mukil | Sailesh Mukil |
| [IMPALA-6510](https://issues.apache.org/jira/browse/IMPALA-6510) | Impala 2.12 Doc: Remove the refresh\_after\_connect option from INVALIDATE METADATA statemement |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6728](https://issues.apache.org/jira/browse/IMPALA-6728) | The combination use\_kudu\_kinit=false and use\_krpc=true crashes Impalad |  Blocker | Security | Michael Ho | Michael Ho |
| [IMPALA-6685](https://issues.apache.org/jira/browse/IMPALA-6685) | Improve profile in KrpcDataStreamRecvr and KrpcDataStreamSender |  Major | Distributed Exec | Michael Ho | Michael Ho |
| [IMPALA-6726](https://issues.apache.org/jira/browse/IMPALA-6726) | Catalog server's kerberos ticket gets deleted after 'ticket\_lifetime' on SLES11 |  Blocker | Security | Sailesh Mukil | Michael Ho |
| [IMPALA-6546](https://issues.apache.org/jira/browse/IMPALA-6546) | Impala 2.12 & 3.0 Docs: Document the new ODBC scalar functions |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6667](https://issues.apache.org/jira/browse/IMPALA-6667) | Impala 2.12 Doc: Enable file handle cache by default |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6457](https://issues.apache.org/jira/browse/IMPALA-6457) | Impala 2.12 Doc: DECIMAL support for Kudu tables |  Major | Docs | John Russell | Alexandra Rodoni |
| [IMPALA-6807](https://issues.apache.org/jira/browse/IMPALA-6807) | Known Issues needs to be updated to reflect resolution of HDFS-12528 |  Major | Docs | Joe McDonnell | Alexandra Rodoni |
| [IMPALA-6688](https://issues.apache.org/jira/browse/IMPALA-6688) | Impala 2.12 & 3.0 Docs: Change default configuration to --compact\_catalog\_topic=true |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6623](https://issues.apache.org/jira/browse/IMPALA-6623) | Impala 2.12 Doc: Update ltrim and rtrim functions |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6483](https://issues.apache.org/jira/browse/IMPALA-6483) | Impala 3.0 & 2.12 Docs: Describe the query option for query time limit |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6514](https://issues.apache.org/jira/browse/IMPALA-6514) | Impala 2.12 & 3.0 Docs: Allow Impala Shell to connect directly to impalad when config with proxy load balancer and kerberos |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6723](https://issues.apache.org/jira/browse/IMPALA-6723) | Impala 2.12 & 3.0 Docs: Support insert plan hints for CREATE TABLE AS SELECT |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6464](https://issues.apache.org/jira/browse/IMPALA-6464) | Impala 2.12 & 3.0 Docs: Extend "compute stats" syntax to support a list of columnss |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6748](https://issues.apache.org/jira/browse/IMPALA-6748) | Impala 2.12 & 3.0 Docs: Support more separators between date and time in default timestamp format |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6459](https://issues.apache.org/jira/browse/IMPALA-6459) | Doc: TABLESAMPLE for COMPUTE STATS |  Critical | Docs | John Russell | Alexander Behm |
| [IMPALA-6867](https://issues.apache.org/jira/browse/IMPALA-6867) | Impala 2.12 & 3.0 Docs: Provide a query option to not shuffle on distinct exprs |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6651](https://issues.apache.org/jira/browse/IMPALA-6651) | Impala 2.13 & 3.0 Docs: Fine-grained privileges |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6912](https://issues.apache.org/jira/browse/IMPALA-6912) | Impala Doc: Doc the minimum sample size for COMPUTE STATS TABLESAMPLE |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-2937](https://issues.apache.org/jira/browse/IMPALA-2937) | Introduce sampled statistics |  Minor | Backend | Mostafa Mokhtar |  |


### OTHER:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [IMPALA-6523](https://issues.apache.org/jira/browse/IMPALA-6523) | There is misinformation in the PARQUET\_FALLBACK\_SCHEMA\_RESOLUTION |  Major | Docs | Bo soon Park | Alexandra Rodoni |
| [IMPALA-6509](https://issues.apache.org/jira/browse/IMPALA-6509) | Impala Doc: Enabling haproxy for secure impala restricts connection to individual nodes |  Major | Docs | Michael Brown | Alexandra Rodoni |
| [IMPALA-6622](https://issues.apache.org/jira/browse/IMPALA-6622) | Backport parts of  IMPALA-4924 to 2.x |  Major | Frontend, Infrastructure | Lars Volker | Taras Bobrovytsky |
| [IMPALA-6736](https://issues.apache.org/jira/browse/IMPALA-6736) | stress test --filter-query-mem-ratio doesn't work |  Major | Infrastructure | Michael Brown | Michael Brown |
| [IMPALA-6732](https://issues.apache.org/jira/browse/IMPALA-6732) | Impala 2.12 Doc: Release Notes |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6886](https://issues.apache.org/jira/browse/IMPALA-6886) | Impala Doc: Remove Impala Cluster Sizing doc |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6869](https://issues.apache.org/jira/browse/IMPALA-6869) | Impala 2.12 Doc: Update Known Issues |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-6888](https://issues.apache.org/jira/browse/IMPALA-6888) | Impala Doc: Update the Table and Column Statistics doc |  Major | Docs | Alexandra Rodoni | Alexandra Rodoni |
| [IMPALA-5335](https://issues.apache.org/jira/browse/IMPALA-5335) | Review consistency of ADLS python client used for Impala testing |  Major | Infrastructure | Sailesh Mukil | Sailesh Mukil |
| [IMPALA-5632](https://issues.apache.org/jira/browse/IMPALA-5632) | Investigate use of transparent huge pages for Bloom Filters |  Major | Perf Investigation | Jim Apple |  |


