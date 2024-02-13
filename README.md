# configuration-template

A template for writing a [Configuration].

To use this template:
1. Replace the name, metadata in crossplane.yaml to reflect your Configuration.
2. Add dependencies in crossplane.yaml
3. Add your XRD, and Compositions in the `apis/` directory
4. (Optionally) Add examples in the `examples/` directory
5. Update this file, `README.md`, to be about your Configuration!

To build a Configuration package, use the Crossplane CLI:
```shell
# Just builds the package. It will go through the repo and collect yaml files.
# Furthermore it will by default check for examples in `./examples` and add them to the package.
crossplane xpkg build

# You can specify various options for the build command, if needed
crossplane xpkg build --package-root=test-directory --output=test-package.xpkg --examples-root=/test-examples
```

Push the package to a registry:
```shell
crossplane xpkg push test-package.xpkg your-org/your-repo:v1.0.0
```

More info on the Crossplane CLI can be found [here][xp-cli].

Check out the Crossplane docs for more information on [creating] Configurations.

[Configuration]: https://docs.crossplane.io/v1.14/concepts/packages
[creating]: https://docs.crossplane.io/v1.14/concepts/packages/#create-a-configuration
[xp-cli]: https://docs.crossplane.io/v1.14/cli/command-reference/
