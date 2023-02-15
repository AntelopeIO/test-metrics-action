# xUnit Test Metrics Action CI
This GitHub Actions workflow initializes, lints, and tests the `xunit-test-metrics-action` GitHub Action nodeJS project and source code.

### Index
1. [Triggers](#triggers)
1. [Inputs](#inputs)
1. [Steps](#steps)
1. [Outputs](#outputs)
1. [See Also](#see-also)

## Triggers
This GitHub action will run under the following circumstances:
1. When code is pushed.
1. Workflow dispatch event, a manual CI run, which can be triggered by the "Workflow Dispatch" button in the Actions tab of the GitHub repository, among other means.

## Inputs
There are currently no user-defined inputs for this pipeline, aside from the source code itself.

## Steps
This workflow performs the following steps on GitHub runners:
1. Attach Documentation
    1. Checkout the repo with no submodules.
    1. Attach an annotation to the GitHub Actions build summary page containing CI documentation.
1. nodeJS Build and Test - matrix build testing on a variety of nodeJS versions
    1. Checkout the repo.
    1. Initialize the nodeJS project using `yarn`.
    1. Lint the project using `eslint` with `yarn lint`.
    1. Test the project using `jest` with `yarn test`.

## Outputs
There are currently no outputs of this GitHub Actions workflow besides the exit status.

## See Also
- [xUnit Test Metrics Action Documentation](../../README.md)

For assistance with the CI system, please open an issue in this repo or reach out in the `#help-automation` channel via IM.

***
**_Legal notice_**  
This document was generated in collaboration with ChatGPT from OpenAI, a machine learning algorithm or weak artificial intelligence (AI). At the time of this writing, the [OpenAI terms of service agreement](https://openai.com/terms) §3.a states:
> Your Content. You may provide input to the Services (“Input”), and receive output generated and returned by the Services based on the Input (“Output”). Input and Output are collectively “Content.” As between the parties and to the extent permitted by applicable law, you own all Input, and subject to your compliance with these Terms, OpenAI hereby assigns to you all its right, title and interest in and to Output.

This notice is required in some countries.
