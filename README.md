# SlackLint

This is intended to show an issue with upgrading the dependency for [Slack Compose Lint](https://slackhq.github.io/compose-lints/) from 1.3.1 in the below scenarios.\
This project is simply the default empty activty project that Android Studio will create.

The command run to check each was simply checking lint for the app
```console
./gradlew lintDebug
```

On Main
| AGP      | Gradle  | Slack Compose Lint |
| -------- | ------- | -------            |
| 8.3.2    | 8.4     |  1.3.1             |

On upgrade_slack_1.4.1
| AGP      | Gradle  | Slack Compose Lint |
| -------- | ------- | -------            |
| 8.3.2    | 8.4     |  1.4.1             |

On upgrade_slack_agp_8.6
| AGP      | Gradle  | Slack Compose Lint |
| -------- | ------- | -------            |
| 8.6.1    | 8.7     |  1.4.1             |

On upgrade_all
| AGP      | Gradle  | Slack Compose Lint |
| -------- | ------- | -------            |
| 8.7      | 8.9     |  1.4.1             |

Lint Outcomes
| Main     | upgrade_slack_1.4.1 | upgrade_slack_agp_8.6 | upgrade_all |
| -------- | -------             | -------               | -------     |
| Fail     | Fail                | Fail                  | Pass        |
