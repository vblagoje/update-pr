# vblagoje/update-pr

## Description
The `vblagoje/update-pr` GitHub Action is designed to update the description of a pull request. It can either use a specified pull request number or automatically detect the number when triggered by a pull request event.

## Usage
To use this action in your workflow, add the following step:

```yaml
- name: Update Pull Request Description
  uses: vblagoje/update-pr@v1
  with:
    pr-body: 'Your new PR description here'
    # pr-number is optional; if omitted, it is taken from the PR triggering the workflow
    pr-number: 'optional-pr-number'
```

## Inputs
- `pr-body`: **Required** The new body text for the pull request.
- `pr-number`: **Optional** The number of the pull request to update. If omitted, the action will attempt to use the pull request number from the triggering event.

## Example Workflow
Here's an example of how to use `vblagoje/update-pr` in a workflow:

```yaml
name: Update PR Description Example
on: [pull_request]

jobs:
  update-pr-description:
    runs-on: ubuntu-latest
    steps:
      - name: Update Pull Request Description
        uses: vblagoje/update-pr@v1
        with:
          pr-body: 'This is an updated description for the PR.'
```

In this example, the action will update the description of the pull request that triggered the workflow.

## Contributing
Contributions to `vblagoje/update-pr` are welcome! 

## License
This project is licensed under [LICENSE_NAME]. See the [LICENSE](LICENSE) file for details.

