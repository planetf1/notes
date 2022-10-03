# Enforcing PR Reviews

## Rationale

* Improve code quality
* Demonstrate code governance

## Implications

* Slower to get code changes in
* Requires other maintainers to check for open PRs and act upon them

## Mechanisms

* defined by branch
* required approvals: n (1..)
* Require review from code owner
* Optional: Limit approvals/require changes only to contributors/maintainers

### Bots
* Auto approve (not merge) after no other reviews added?
* label requires reviews -- label defines how many

## Other thoughts
* Slack bot?
* Action to bypass checks based on label ('urgent') etc
* Maintainers also need to monitor for issues & PRs
* Issues to be assigned
