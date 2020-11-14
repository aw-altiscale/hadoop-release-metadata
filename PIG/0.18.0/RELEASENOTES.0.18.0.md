
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
# Apache Pig  0.18.0 Release Notes

These release notes cover new developer and user-facing incompatibilities, important issues, features, and major improvements.


---

* [PIG-5272](https://issues.apache.org/jira/browse/PIG-5272) | *Minor* | **BagToTuple output schema is incorrect**

Removed Incorrect Schema Definition from BagToTuple


---

* [PIG-5328](https://issues.apache.org/jira/browse/PIG-5328) | *Major* | **expressionOperator Divide.equalsZero(DataType.BIGDECIMAL) is invalid**

the division operator checks for a zero denominator to prevent a divide-by-zero exception. Unlike other numeric types, BigDecimal has multiple representations of zero with different scales ... 0, 0.0, 0.00, etc. Previous versions of pig were were not properly detecting zero values with non-zero scales when performing denominator check prior to division.


---

* [PIG-5352](https://issues.apache.org/jira/browse/PIG-5352) | *Major* | **Please add OWASP Dependency Check to the build (ivy.xml)**

Now 
% ant owasp
would create a report for known vulnerabilities for the jars Pig depend on at ./build/owasp.


---

* [PIG-5404](https://issues.apache.org/jira/browse/PIG-5404) | *Blocker* | **FLATTEN infers wrong datatype**

**WARNING: No release note provided for this change.**



