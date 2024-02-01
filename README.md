# Setup Virtualenv

Setup Python 3 Virtual Environment. Especially handy for self-hosted runners.

## Usage

```yaml
- uses: cdqag/setup-virtualenv@v1
```

### Inputs

| Name              | Required | Default    | Description                          |
|-------------------|----------|------------|--------------------------------------|
| `python-bin`      | Yes      | `python3`  | Python binary to use                 |
| `virtualenv-path` | Yes      | `.venv`    | Path where virtualenv will be stored |

### Example

```yaml
name: Example

on:
  workflow_dispatch:

jobs:
  example_job:
    runs-on: my-self-hosted-runner

    steps:
      - uses: cdqag/setup-virtualenv@v1
      - run: pip --version  # This should output also location of used pip (you should see path/.venv/bin/pip)
 
```

## License

This project is licensed under the MIT License. See the LICENSE file for details.
