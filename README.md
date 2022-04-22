# Integrating Lw-Scanner into CI Pipeline using GitHub Action

## Steps:

- publish your docker image to github container registry using github workflows. Your file should look something [like this](.github/workflows/publish.yml).

- at the end of publishing, ou will have a published package name similar to `ghcr.io/ladykerr/gh-action-demo:latest` and it will show up on your repos page.

- using the package name, add a yml file to your github workflow to perform the vulnerability scan with lw-inline scanner. Your file should look something [like this ](.github/workflows/test-inline-scanner.yml).

- save your changes and push the repo to Github. Your workflows will automagically begin and lacework will scan your image for any known vulnerabilities.
