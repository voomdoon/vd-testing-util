# vd-testing-util

[![License](https://img.shields.io/github/license/voomdoon/vd-testing-util)](https://github.com/voomdoon/vd-testing-util/blob/main/LICENSE)
[![Java](https://img.shields.io/badge/Java-21-blue)](https://adoptium.net/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=voomdoon_vd-testing-util&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=voomdoon_vd-testing-util)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=voomdoon_vd-testing-util&metric=coverage)](https://sonarcloud.io/summary/new_code?id=voomdoon_vd-testing-util)
[![Bugs](https://sonarcloud.io/api/project_badges/measure?project=voomdoon_vd-testing-util&metric=bugs)](https://sonarcloud.io/summary/new_code?id=voomdoon_vd-testing-util)
[![Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=voomdoon_vd-testing-util&metric=vulnerabilities)](https://sonarcloud.io/summary/new_code?id=voomdoon_vd-testing-util)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=voomdoon_vd-testing-util&metric=security_rating)](https://sonarcloud.io/summary/new_code?id=voomdoon_vd-testing-util)
[![Code Smells](https://sonarcloud.io/api/project_badges/measure?project=voomdoon_vd-testing-util&metric=code_smells)](https://sonarcloud.io/summary/new_code?id=voomdoon_vd-testing-util)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=voomdoon_vd-testing-util&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=voomdoon_vd-testing-util)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=voomdoon_vd-testing-util&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=voomdoon_vd-testing-util)
[![Duplicated Lines (%)](https://sonarcloud.io/api/project_badges/measure?project=voomdoon_vd-testing-util&metric=duplicated_lines_density)](https://sonarcloud.io/summary/new_code?id=voomdoon_vd-testing-util)

Reusable JUnit testing helpers for voomdoon modules.

## Installation

```xml
<dependency>
	<groupId>de.voomdoon.testing</groupId>
	<artifactId>vd-testing-util</artifactId>
	<version>0.2.0</version>
	<scope>test</scope>
</dependency>
```

## Usage

Use `SystemPrintStreamCapturer` to assert output written to `System.out` or `System.err`:

```java
SystemPrintStreamCapturer capturer = SystemPrintStreamCapturer.run(() -> System.out.println("hello"));

assertThat(capturer.getOut()).isEqualTo("hello%n".formatted());
assertThat(capturer.getErr()).isEmpty();
```

`TestBase` is available for JUnit tests that should log test start and end markers.

## Related Modules

- [vd-logging](https://github.com/voomdoon/vd-logging)
