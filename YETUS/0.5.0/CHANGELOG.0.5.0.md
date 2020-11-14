
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
# Apache Yetus Changelog

## Release 0.5.0 - 2017-07-11



### IMPORTANT ISSUES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [YETUS-509](https://issues.apache.org/jira/browse/YETUS-509) | Remove maven-eclipse plugin support |  Major | Precommit | Allen Wittenauer | Allen Wittenauer |
| [YETUS-512](https://issues.apache.org/jira/browse/YETUS-512) | Switch default docker image over to Xenial |  Blocker | Precommit | Allen Wittenauer | Allen Wittenauer |
| [YETUS-511](https://issues.apache.org/jira/browse/YETUS-511) | github PR handler shouldn't use raw numbers |  Major | Precommit | Allen Wittenauer | Allen Wittenauer |


### NEW FEATURES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [YETUS-315](https://issues.apache.org/jira/browse/YETUS-315) | smart-apply-patch committer mode should support signed commits |  Major | Precommit | Allen Wittenauer | Suraj Acharya |
| [YETUS-522](https://issues.apache.org/jira/browse/YETUS-522) | smart-apply-patch should do more to infer author in committer mode |  Major | Precommit | Sean Busbey | Akira Ajisaka |
| [YETUS-523](https://issues.apache.org/jira/browse/YETUS-523) | create a separate tool for docker cleanup |  Major | Precommit | Allen Wittenauer | Allen Wittenauer |


### IMPROVEMENTS:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [YETUS-471](https://issues.apache.org/jira/browse/YETUS-471) | Add possibility to skip the source check for Findbugs |  Major | Precommit | Peter Vary | Peter Vary |
| [YETUS-459](https://issues.apache.org/jira/browse/YETUS-459) | Option to suppress assignee and contributor from RDM output |  Major | Release Doc Maker | Allen Wittenauer | Suraj Acharya |
| [YETUS-506](https://issues.apache.org/jira/browse/YETUS-506) | Enhance maven\_reorder\_module\_process to handle modules where directory name is different than the artifactId |  Major | Precommit | Peter Vary | Peter Vary |
| [YETUS-488](https://issues.apache.org/jira/browse/YETUS-488) | Checkstyle reports new error if the file still longer than expected |  Minor | Precommit | Peter Vary | Peter Vary |
| [YETUS-483](https://issues.apache.org/jira/browse/YETUS-483) | shellcheck plugin should be smarter about its queue |  Major | Precommit | Allen Wittenauer | Allen Wittenauer |
| [YETUS-500](https://issues.apache.org/jira/browse/YETUS-500) | Add section headers to break out precheck/branch compilation checks from patch checks. |  Major | Precommit | Allen Wittenauer | Allen Wittenauer |


### BUG FIXES:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [YETUS-484](https://issues.apache.org/jira/browse/YETUS-484) | Fixing bug when checkstyle runs on multiple modules |  Major | Precommit | Peter Vary | Peter Vary |
| [YETUS-460](https://issues.apache.org/jira/browse/YETUS-460) | RDM should handle connection reset by peer |  Major | Release Doc Maker | Allen Wittenauer | Adam Faris |
| [YETUS-489](https://issues.apache.org/jira/browse/YETUS-489) | checkstyle.sh does not support checkstyle 6.14 or upper |  Major | Precommit | Akira Ajisaka | Akira Ajisaka |
| [YETUS-476](https://issues.apache.org/jira/browse/YETUS-476) | Replace docker's time handler with awk |  Major | Precommit | Allen Wittenauer | Akira Ajisaka |
| [YETUS-498](https://issues.apache.org/jira/browse/YETUS-498) | shelllcheck needs to have -x support |  Minor | Precommit | Allen Wittenauer | Allen Wittenauer |
| [YETUS-496](https://issues.apache.org/jira/browse/YETUS-496) | Fix UnboundLocalError in releasedocmaker.py |  Blocker | Release Doc Maker | Allen Wittenauer | Akira Ajisaka |
| [YETUS-487](https://issues.apache.org/jira/browse/YETUS-487) | docker cleanup needs to handle 'dead' |  Major | Precommit | Allen Wittenauer | Suraj Acharya |
| [YETUS-493](https://issues.apache.org/jira/browse/YETUS-493) | Gemlock.lock fails for OS X 10.11 |  Major | website and documentation | Allen Wittenauer | Allen Wittenauer |
| [YETUS-508](https://issues.apache.org/jira/browse/YETUS-508) | improve build tool command detection w/docker |  Critical | Precommit | Allen Wittenauer | Allen Wittenauer |
| [YETUS-518](https://issues.apache.org/jira/browse/YETUS-518) | Update years to 2017 |  Blocker | build, website and documentation | Allen Wittenauer | Allen Wittenauer |
| [YETUS-521](https://issues.apache.org/jira/browse/YETUS-521) | Update some website build dependencies |  Major | website and documentation | Allen Wittenauer | Allen Wittenauer |
| [YETUS-524](https://issues.apache.org/jira/browse/YETUS-524) | audience-annotations can not be used as a dependency in a gradle build |  Major | Audience Annotations | Grant Henke | Grant Henke |
| [YETUS-485](https://issues.apache.org/jira/browse/YETUS-485) | Yetus run is failing on branch after rebase/force push |  Critical | Precommit | Subramaniam Krishnan | Subramaniam Krishnan |
| [YETUS-514](https://issues.apache.org/jira/browse/YETUS-514) | docker gives multiple time formats |  Major | Precommit | Allen Wittenauer | Allen Wittenauer |


### OTHER:

| JIRA | Summary | Priority | Component | Reporter | Contributor |
|:---- |:---- | :--- |:---- |:---- |:---- |
| [YETUS-481](https://issues.apache.org/jira/browse/YETUS-481) | Add 0.4.0 release to the website |  Major | website and documentation | Ajay Yadav | Ajay Yadav |
| [YETUS-482](https://issues.apache.org/jira/browse/YETUS-482) | Binary file gets added to the release candidates |  Major | build, Release Doc Maker, ShellDocs | Ajay Yadav | Allen Wittenauer |
| [YETUS-520](https://issues.apache.org/jira/browse/YETUS-520) | EOL 0.1.0 through 0.3.0 |  Trivial | build, website and documentation | Allen Wittenauer | Allen Wittenauer |
| [YETUS-525](https://issues.apache.org/jira/browse/YETUS-525) | Release 0.5.0 |  Blocker | website and documentation | Sean Busbey | Allen Wittenauer |


