## Usage:

```yaml
name: JIRA Connection

on:
  pull_request:
    types:
      - opened
      - reopened
      - edited
      - synchronize
  issue_comment:
    types:
      - created
      - edited
      - deleted

jobs:
  enforce-issue:
    runs-on: ubuntu-latest
    name: JIRA Link Enforcer
    steps:
      - name: Check for JIRA Link
        id: check
        uses: aumni-fund/tool-github-action-jira-pr-link@v1
        with:
          jira-project: "DEV"
          jira-host: "company.atlassian.net"
```
