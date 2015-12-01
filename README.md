# travis-ci-deloy-test

This repository is for testing Travis CI for deployments.

The `travis.yml` uses the `addons.artifcat` declaration to copy the deploy
artifcats to AWS S3
[Documentation](https://docs.travis-ci.com/user/uploading-artifacts/).
This requires the `ARTIFACTS_KEY` and `ARTIFACTS_SECRET` environment
variables to be set in the Settings section of Travis (on `travis-ci.org`)
for this Github repository.

## Resources
[Helpful linter for writing the `travis.yml`](https://lint.travis-ci.org/)
