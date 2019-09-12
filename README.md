# [:] Using SourceClear via GitHub Actions

1. We'll [do this](.github/actions/sourceclear/entrypoint.sh) via the [CI script](https://help.veracode.com/reader/hHHR3gv0wYc2WbCclECf_A/_p_RJqZHXQ4S5pkjSXCrzQ), the recommended way to run scans.
1. [Define a container action](.github/actions/sourceclear), which makes it easy to set up a build environment for your project. You may have to customize the [Dockerfile](.github/actions/sourceclear/Dockerfile) to install build dependencies.
1. [Declare the `SRCCLR_API_TOKEN` secret](.github/actions/sourceclear/action.yml). We'll use the name of the environment variable SourceClear expects for consistency.
1. Go to `Settings` > `Secrets` and add a new secret with the same name.
1. [Pass the secret](.github/workflows/main.yml) to the container as an environment variable.
1. Enjoy!
