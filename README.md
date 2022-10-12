# install-titanium

This action installs [Titanium SDK](https://titaniumsdk.com) so your workflow can run
Titanium commands like `ti --version`.

# Inputs

## `version`

By default, the `11.1.1.GA` will be used. But you can change it to a custom version too.

# Example

```yaml
name: Titanium Workflow
on: push
jobs:
  test:
    name: Run Tests
    runs-on: macos-latest
    steps:
      - uses: actions/checkout@v2
      - name: Install Titanium SDK
        uses:  m1ga/install-titanium@v1
        with:
          version: 11.1.1.GA
      - name: Output version
        run: ti --version
```
