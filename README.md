# dependabot-automerge

[![GitHub issues](https://img.shields.io/github/issues/gloomberry-ci/dependabot-automerge)](https://github.com/gloomberry-ci/dependabot-automerge/issues)

 Automatically merge Dependabot PRs with GitHub Actions. 
 
## Found a bug? 💁‍♀️

Thanks for letting us know! Please [file an issue](../../issues/new?assignees=&labels=&template=bug_report.md&title=) and we should reply shortly.

## Configuration

This action requires the presence of inputs, which are listed below.

### Inputs

- `github-token`: The [GitHub Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) used to merge the pull-request. (**required**)
- `target`: The version comparison target (major, minor, patch). *Default*: `patch` (**optional**)
- `command`: The command to pass to Dependabot. *Default*: `merge` (**optional**)
- `botName`: The bot to tag in approve/comment message. *Default*: `dependabot` (**optional**)
- `approve`: Auto-approve pull-requests. *Default*: `true` (**optional**)

### GitHub Personal Access Token

The GitHub Personal Access Token requires the following scopes:

- `repo` for private repositories.
- `public_repo` for public repositories.

The token **MUST** be created from a user with `push` permission to the repository.

## Example

Below you will find an example of how you can use this action.

```yaml
uses: gloomberry-ci/dependabot-automerge@main
with:
  # configuration
  github-token: ${{ secrets.DEPENDABOT_AUTOMERGE_PERSONAL_ACCESS_TOKEN }}
  target: minor
```

## License

The code is provided under a GNU General Public License (v2).
