MNG-7371

Reproducer:

1. build this project `mvn clean install` (assuming no MRM or anything, just against Central)
2. EDIT your locally cached org.apache.maven:maven:3.6.3 pom to be like this
```
<?xml version="1.0" encoding="UTF-8"?>

<!--
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.
-->

<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>

  <parent>
    <groupId>org.apache.maven</groupId>
    <artifactId>maven-parent</artifactId>
    <version>33</version>
    <relativePath>../pom/maven/pom.xml</relativePath>
  </parent>

  <artifactId>maven</artifactId>
  <version>3.6.3</version>
  <packaging>tar.gz</packaging>
</project>
```
3. build again

