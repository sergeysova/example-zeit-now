# Zeit Now GitHub Action Example

An example workflow, using [the GitHub Action for Zeit Now](https://github.com/actions/now) to deploy [a static website](site/), [octozen.now.sh](https://octozen.now.sh/).

## Workflow

The [example workflow](.github/main.workflow) will trigger on every push to this repo.

For pushes to a _feature_ branch, the workflow will:

1. Trigger a new deployment using the `now` cli
1. Set up a unique alias for that deployment, based on the SHA of the most recent commit on the Git ref that was pushed

For pushes to the _default_ branch (`master`), in addition to the above Actions, the workflow will:

1. Set up a global alias, based on [the `now.json` configuration](site/now.json)

## License

This repository is [licensed under CC0-1.0](LICENSE), which waives all copyright restrictions.
