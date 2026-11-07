# Google Workspace

<!--
https://gsuite.google.com/products/gmail/
https://gsuite.google.com/products/admin/
-->

## Links

- [Admin Console](https://admin.google.com)
- [Status Page](https://google.com/appsstatus/dashboard)

## Guides

- [Gmail sending limits in Google Workspace](https://support.google.com/a/answer/166852)
- [MX record values](https://support.google.com/a/answer/174125?hl=en)

## CLI

### Links

- [Code Repository](https://github.com/googleworkspace/cli)

### Dependencies

- [Google Cloud Platform (GCP) CLI](/gcp/README.md#cli)

### Installation

```sh
# Using Homebrew
brew install googleworkspace-cli
```

### Configuration

```sh
#
gws auth setup
# https://console.cloud.google.com/apis/credentials

#
gws auth login

#
gws drive files list --params '{"pageSize": 5}'
```
