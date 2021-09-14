# action-nuget-push
An action that runs a `nuget push` on a given directory, pushing all `.nupkg` files to a NuGet source.

## Usage
This action pushes all files with the `.nupkg` extension to the specified NuGet source.

### Usage example
```yaml
    steps:
      - uses: EasyDesk/action-nuget-push@v1
        with:
          # (Required) The API key used to authenticate the upload of the package.
          # Can be generated via the NuGet portal.
          nuget-api-key: '<your-api-key>'

          # (Optional) The URL to the NuGet source where packages will be uploaded.
          # If not specified, defaults to nuget.org (https://api.nuget.org/v3/index.json).
          nuget-url: '<your-nuget-url>'

          # (Optional) A directory where all your .nupkg files are located.
          # If not specified, defaults to the current directory.
          publish-dir: '<your-publish-directory>'
```