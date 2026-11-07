# OpenCodeReview (OCR)

## Links

- [Code Repository](https://github.com/alibaba/open-code-review)

## Installation

```sh
# Using NPM
npm install -g @alibaba-group/open-code-review
```

## Configuration

```sh
#
ocr config provider

#
ocr config model
```

<!--
ocr review

ocr review --from main --to feature-branch

ocr review --commit abc123

ocr session list
ocr review --from main --to feature-branch --resume <session-id>

ocr scan                          # scan the entire repository
ocr scan --path internal/agent    # scan a directory or specific files
ocr scan --resume <session-id>   # resume an interrupted full-file scan

ocr review --format json --output result.json

ocr delegate preview
ocr delegate rule src/main.go src/handler.go
-->
