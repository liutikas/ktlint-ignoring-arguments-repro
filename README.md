# Repro of ktlint ignoring arguments

## Steps

1. Run `./gradlew ktlint`

## Expected

Sucess!

## Actual

Failure
```text
> Task :lib:ktlint FAILED
/ssd/ssd1/temp/ktlint-repro/lib/src/main/kotlin/com/example/Library.kt:1:1: File must end with a newline (\n) (final-newline)

********************************************************************************
FAILED
********************************************************************************

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':lib:ktlint'.
> Process 'command '/usr/local/buildtools/java/jdk11/bin/java'' finished with non-zero exit value 1
```

## Side notes

Changing ktlint version in lib/build.gradle.kts back to `0.45.0` makes it pass
again