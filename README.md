# Bill of Material

Bill of Material for Maven Java Spring framework projects

[![Release](https://jitpack.io/v/dilbertside/bom.svg)](https://jitpack.io/#dilbertside/bom)
[![Build Status](https://travis-ci.org/dilbertside/bom.svg)](https://travis-ci.org/dilbertside/bom)

## Purpose

Gather all versions in my miscellaneous Maven Java libraries versions.

### Key drivers for this Bill of Material

My public and corporate projects are biased toward following major libraries 

. Spring Framework
. Spring Boot
. Hibernate
. Docker

In that effect, it should not be surprising some other framework are not represented. (PR are welcome!)

# Versioning rules

This Platform bill of materials is based on https://docs.spring.io/platform/docs/Cairo-SR6/reference/htmlsingle/

As spring.io/platform is EOL, it also follows closely latest iteration of Spring Boot 2.1.x

Versioning will follow closely that of Spring Framework and Spring Boot major release X.Y in X.Y.Z

minor Z in X.Y.Z will be for incremental changes with dependent libraries which do not break a Spring Framework and Spring Boot build. 

## migration to Spring Framework 5.1.x

Migrating to Spring Framework 5.1.x (https://github.com/spring-projects/spring-framework/wiki/Migrating-to-Spring-Framework-5.1)


## Maven howto

### Prerequisites

#### Minimum version

Maven 3.5.x https://maven.apache.org/

Java 1.8

### POM

To use it in your Maven build add:

#### Repository

```xml
<repositories>
  <repository>
      <id>jitpack.io</id>
      <url>https://jitpack.io</url>
  </repository>
</repositories>
```

#### Parent:


```xml
  <parent>
    <groupId>com.github.dilbertside</groupId>
    <artifactId>bom</artifactId>
    <version>5.1.12</version>
    <relativePath></relativePath>
  </parent>
```

# License

MIT https://opensource.org/licenses/MIT

