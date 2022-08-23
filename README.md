# ktlintFormat pre-commit hook

This uses https://pre-commit.com/ and requires the gradle ktlint plugin to be specified in your `build.gradle`:

```kotlin
id("org.jlleitschuh.gradle.ktlint") version "10.3.0"
```

It simply runs `./gradlew ktlintFormat` every time you commit.

# Installation

Put this in your `.pre-commit-config.yaml`:

```yaml
- repo: git://github.com/ScoreUnder/pre-commit-gradle-ktlint
  sha: main
  hooks:
    - id: gradle-ktlint
```

Then if you have pre-commit installed correctly, next commit should trigger the formatting process automatically.
