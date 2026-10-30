# setup-cover100

Install an exact [Cover100 CLI](https://github.com/sneat-dev/cover100-cli) release in GitHub Actions without Go. This action installs the CLI only; workflows choose which commands to run. Release-provided license and notice files are kept alongside the executable.

`version` is required and must be an exact release tag. `expected-sha256` optionally supplies an independently obtained digest for the selected archive. A checksum from the same release detects corruption but cannot authenticate a replaced release. Outputs include the installed tag and binary path.

The action supports Linux, macOS, and Windows on amd64 and arm64 where the requested release publishes those assets.

```yaml
- uses: sneat-dev/setup-cover100@4e9259f9e946a24bd7cf852bf7ec0f5e5b95e3be
  with:
    version: v0.4.1
- run: cover100 --version
```
