# rye-update-bot

This is a simple workflow to update rye dependencies and create a PR with beautiful Output
Inspired by https://github.com/EdmundGoodman/update-bot

## Motivation

As [EdmundGoodman](https://github.com/EdmundGoodman) stated, until now there is now support of Dependabot with updating dependencies from rye or uv.
In our company we're using primarly rye for project management. So the need arised to create an workflow which
enables us to create PRs which contains package updates on a regular basis.

## Usage

This is a goto workflow - simply copy and paste the code and everything should work. The basic configuration runs the workflow
on every wednesday @ 02:00.

## Output

The workflow generates a PR with title `BOT: Update dependencies` and commit-message `Update dependencies` on the branch `update-dependencies`.
The PR is created against the `main` branch and contains as body every updated dependency of the files `pyproject.toml`, `requirements.lock` and `requirements-dev.lock`.
Updates are grouped by major, minor and patch changes.

A sample output looks like this:


## Updated dependencies

The following dependencies have been updated:

### pyproject.toml
```diff
No changes detected.
```
### requirements.lock
#### Major Updates 🚨
* cryptography: `43.0.3` → `44.0.0` 🚨

#### Minor Updates 🟡
* amqp: `5.2.0` → `5.3.1` 🟡

#### Patch Updates 🟢
* bcrypt: `4.2.0` → `4.2.1` 🟢

### requirements-dev.lock
#### Major Updates 🚨
* asttokens: `2.4.1` → `3.0.0` 🚨

#### Minor Updates 🟡
* amqp: `5.2.0` → `5.3.1` 🟡

#### Patch Updates 🟢
* bcrypt: `4.2.0` → `4.2.1` 🟢

