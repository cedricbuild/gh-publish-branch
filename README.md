Github actions to publish branch to github repository branch. It uses action's access_token to publish/write branch. required params need to be set

```yaml
on: [push]

jobs:
  publish-directory:
    runs-on: ubuntu-latest
    steps:
      - uses: cedricbuild/gh-publish-branch@main
        with:
            github_repository: ${{ github.repository }}
            branch: gh-pages
            directory: build
            commit_message: "publish directory to branch"
```