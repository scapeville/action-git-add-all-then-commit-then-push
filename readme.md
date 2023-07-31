GitHub action: `git add .` → `git commit` → `git push`


## Usage

```yml
jobs:
  ...:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: actions/checkout@v3
      - run: ...
      - uses: scapeville/action-git-add-all-then-commit-then-push@v1
        with:
          name: foo   # (optional)
          email: bar  # (optional)
          msg: baz    # (optional)
        env:
          GH_TOKEN: ${{ github.token }}
```