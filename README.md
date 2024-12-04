# rye-update-bot

This is a simple workflow to update rye dependencies and create a PR with beautiful output,
inspired by https://github.com/EdmundGoodman/update-bot

## Motivation

As [EdmundGoodman](https://github.com/EdmundGoodman) stated, until now there is now support of Dependabot with updating dependencies from rye or uv.
In our company we're using primarly rye for project management. So the need arised to create an workflow which
enables us to create PRs which contains package updates on a regular basis.

## Usage

This is a goto workflow - simply copy and paste the code and everything should work. The basic configuration runs the workflow
on every wednesday @ 02:00.

### Sample Project

This project contains a sample RYE project to show the functionality.

## Output

The workflow generates a PR with title `BOT: Update dependencies` and commit-message `Update dependencies` on the branch `update-dependencies`.
The PR is created against the `main` branch and contains as body every updated dependency of the files `pyproject.toml`, `requirements.lock` and `requirements-dev.lock`.
Updates are grouped by major, minor and patch changes.

A sample output looks like this
