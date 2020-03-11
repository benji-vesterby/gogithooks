# Go Hooks Installation

## Linter Installation

```bash
go get -u golang.org/x/lint/golint
```

## Hook Installation

Execute the following shell commands on Linux or Mac to install the hooks globally for your system.

```bash
git clone git@github.com:benjivesterby/gogithooks ~/hooks
chmod +x ~/hooks/pre-commit
git config --global core.hookspath ~/hooks
```

This installs the hooks for all repositories and will trigger the linting tools on all of your `.go` files.

## Hook Bypass

To bypass linter errors which may occasionally be necessary add the `--no-verify` flag to your commit like this.

```bash
git commit --no-verify -m "commit message"
```

## Future Linters

```bash
go get -u github.com/gordonklaus/ineffassign
go get -u github.com/client9/misspell/cmd/misspell
go get -u github.com/kisielk/errcheck
go get -u github.com/securego/gosec/cmd/gosec
go get -u honnef.co/go/tools/cmd/staticcheck
```
