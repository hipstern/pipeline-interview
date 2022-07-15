# Will Campbell - Interview

## Issue

This application needs to be deployed into various environments (e.g. dev, qa, prod) and on different clouds (e.g. AWS, Azure)

Each environment has some desired setup, or profile but the deployer can choose to apply additional configs to control certain features.

## Assumptions

The configuration files (/config) are a collection of standard objects or key/value pairs that control various aspects of the app.
There should always be a base configuration, AKA the default configuration.
The deployment CLI (the tool that does the actual deployment) is expecting a single configuration file.
The environment profiles (/profiles) are a set of files that specify which configuration files must be applied when deploying a partcular environment.

## Requirements

Please take this simple build and deploy pipeline and extend it such that the requested configuration files are handled and applied to the deployment process based on the job parameters.
e.g. You may wish to parse and merge the relevant files and produce/generate a single output that will be passed to the deployment CLI.
