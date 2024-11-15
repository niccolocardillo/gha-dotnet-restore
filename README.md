# .NET Restore

Uses the .NET CLI `dotnet restore` [command](https://learn.microsoft.com/en-us/dotnet/core/tools/dotnet-restore) to restore the dependencies for specified projects or the solution itself.

## Usage

To use this action in your GitHub repository, you can follow these steps:

```yaml
uses: maurosoft1973/dotnet-restore@v1
```

### Inputs

```yaml
with:
  # Optional path to the project(s) file to restore. Pass empty to restore all dependencies and tools of a solution. 
  # Supports globbing.
  projects: '**/*.csproj'
  # Sets the verbosity level of the command.
  # Allowed values are q[uiet], m[inimal], n[ormal], d[etailed], and diag[nostic].
  level: 'quiet'
  # Whether to use the default restore cache ('**/*.csproj', '**/*.cs') or not. Default is not to use the restore cache.
  useRestoreCache: 'false'
  # Allows for a custom provided key that will be used instead of the default implementation.
  restoreCacheKey: ''
```

### Outputs

```yaml
outputs:
  # The restore cache key that can be used by other actions.
  restoreCacheKey: dotnet-restore-sha256
```

## Examples

### Restore all C# projects

```yaml
steps:
  - name: Restore Dependencies
    uses: maurosoft1973/dotnet-restore@v1
```

## Contributing to .NET Restore

Contributions are welcome! 
Feel free to submit issues, feature requests, or pull requests to help improve this action.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
