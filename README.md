# ktlintFormat pre-commit hook

This uses https://pre-commit.com/ and requires the gradle ktlint plugin to be specified in your `build.gradle`.

e.g.

```kotlin
id("org.jlleitschuh.gradle.ktlint") version "10.3.0"
```

It simply runs `./gradlew ktlintFormat` every time you commit.

# Installation

Put this in your `.pre-commit-config.yaml`:

```yaml
repos:
- repo: https://github.com/ScoreUnder/pre-commit-gradle-ktlint.git
  rev: 25e4dcab26cb6c5d5c8310e8f47f0a4e023540bf
  hooks:
    - id: gradle-ktlint
```

Then if you have pre-commit installed correctly, next commit should trigger the formatting process automatically.
