# Environment variable build pack

This is a Cloud Native Buildpack that adds support for configuring runtime environment variables.

## Usage

Any environment var specified at build time starting with `RUNTIME_ENVVAR` will be managed.

Example:

* `RUNTIME_ENVVAR_RELEASE_TAG` at runtime becomes `RELEASE_TAG`

## Local build

```
$ pack build \
    --builder heroku/builder:24 \
    --buildpack envvar-buildpack \
    --path my-project-path \
    --buildpack envvar-buildpack \
    example-image
```
