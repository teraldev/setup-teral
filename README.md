# setup-teral

Installs the [Teral CLI](https://github.com/teraldev/cli) in GitHub Actions.

```yaml
- uses: actions/checkout@v4
- uses: teraldev/setup-teral@v1
- run: teral up --project acme --app api --env production
  env:
    TERAL_API_KEY: ${{ secrets.TERAL_API_KEY }}
```

Create the key with `teral keys create github-actions --preset deploy` or in the
dashboard under Settings → API Keys, and store it as the `TERAL_API_KEY`
repository secret.

| Input | Default | |
| --- | --- | --- |
| `version` | `latest` | CLI version to install, e.g. `1.2.0` |

Works on Linux, macOS, and Windows runners (x64 and ARM64). Downloads are
verified against the release checksums.
