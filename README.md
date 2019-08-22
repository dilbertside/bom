# Bill of Material

Bill of Material for Maven Java Spring framework projects

[![Release](https://jitpack.io/v/dilbertside/bom.svg)](https://jitpack.io/#dilbertside/bom)
[![Build Status](https://travis-ci.org/dilbertside/bom.svg)](https://travis-ci.org/dilbertside/bom)

## Purpose

Gather all Java libraries versions in my various projects.

### Key drivers for this Bill of Material

My public and corporate projects are biased toward following major libraries 

* Spring Framework
* Spring Boot
* Hibernate
* Docker

In that effect, it should not be surprising some other framework are not represented. (PR are welcome!)

# Versioning rules

This Platform bill of materials is based on [Cairo SR7](https://docs.spring.io/platform/docs/Cairo-SR7/reference/htmlsingle/)

As spring.io/platform is EOL, it also follows closely latest iteration of Spring Boot 2.1.x

Versioning will follow closely that of Spring Framework and Spring Boot major release X.Y in X.Y.Z

minor Z in X.Y.Z will be for incremental changes with dependent libraries which do not break a Spring Framework and Spring Boot build. 

## Migration to Spring Framework 5.1.x

Migrating to Spring [Framework 5.1.x](https://github.com/spring-projects/spring-framework/wiki/Migrating-to-Spring-Framework-5.1)


## Maven howto

### Prerequisites

#### Minimum version

* Maven 3.5.x https://maven.apache.org/
* Java 1.8

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

#### Maven settings.xml

Modify in your ~/.m2/settings.xml along those lines, or download following template [settings.xml](resources/settings.xml) if none exists currently.

[Maven Settings Reference](https://maven.apache.org/settings.html#Repositories)


```xml
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
                      https://maven.apache.org/xsd/settings-1.0.0.xsd">
	<profiles>
		<profile>
			<id>dev</id>
			<activation>
				<activeByDefault>true</activeByDefault>
			</activation>
			<repositories>
				<repository>
					<id>jitpack.io</id>
					<url>https://jitpack.io</url>
				</repository>
			</repositories>
		</profile>
	</profiles>
</settings>

```
#### Parent:


```xml
  <parent>
    <groupId>com.github.dilbertside</groupId>
    <artifactId>bom</artifactId>
    <version>5.1.19</version>
    <relativePath></relativePath>
  </parent>
```

# License

MIT https://opensource.org/licenses/MIT

