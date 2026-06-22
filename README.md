# vd-testing-util

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
