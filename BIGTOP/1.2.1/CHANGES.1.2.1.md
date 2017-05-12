
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
# Apache BigTop Changelog

## Release 1.2.1 - Unreleased (as of 2017-05-12)



### NEW FEATURES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [BIGTOP-2253](https://issues.apache.org/jira/browse/BIGTOP-2253) | Rewrite Bigtop Docker Provisioner to use native solutions and support multi-host cluster deployment |  Major | docker, provisioner | Evans Ye | Evans Ye |


### IMPROVEMENTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [BIGTOP-2677](https://issues.apache.org/jira/browse/BIGTOP-2677) | layer-spark: Improve sparkpi action output |  Minor | spark | Antonio Rosales | Kevin W Monroe |


### BUG FIXES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [BIGTOP-2738](https://issues.apache.org/jira/browse/BIGTOP-2738) | spark-worker fails to start |  Critical | spark | Amir Sanjar | Amir Sanjar |
| [BIGTOP-2740](https://issues.apache.org/jira/browse/BIGTOP-2740) | hbase 1.1.3 does not work on ppc64le |  Critical | hbase | Kevin W Monroe | Kevin W Monroe |
| [BIGTOP-2762](https://issues.apache.org/jira/browse/BIGTOP-2762) | Zeppelin installation failed due to JDK not installed |  Major | deployment | Evans Ye | Evans Ye |
| [BIGTOP-2765](https://issues.apache.org/jira/browse/BIGTOP-2765) | fix roles logic for spark/zeppelin charms |  Minor | deployment | Kevin W Monroe | Kevin W Monroe |
| [BIGTOP-2764](https://issues.apache.org/jira/browse/BIGTOP-2764) | deployment failure when roles include spark::common and spark::yarn\* |  Major | deployment | Kevin W Monroe | Kevin W Monroe |


### SUB-TASKS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [BIGTOP-2396](https://issues.apache.org/jira/browse/BIGTOP-2396) | Create CI jobs for new Docker Provisioner |  Major | docker, provisioner | Evans Ye | Evans Ye |
| [BIGTOP-2761](https://issues.apache.org/jira/browse/BIGTOP-2761) | Remove bigtop-deploy image build scripts |  Minor | docker | Evans Ye | Evans Ye |
| [BIGTOP-2758](https://issues.apache.org/jira/browse/BIGTOP-2758) | [Sandbox] Support dryrun in build script |  Major | docker, sandbox | Evans Ye | Evans Ye |


### OTHER:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [BIGTOP-2747](https://issues.apache.org/jira/browse/BIGTOP-2747) | new charm revs for bigtop-1.2 |  Major | deployment | Kevin W Monroe | Kevin W Monroe |

