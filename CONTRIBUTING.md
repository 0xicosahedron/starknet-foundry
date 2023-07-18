# Contribution Guideline

Starknet Foundry is under active development and is open for contributions!
Want to get started?
Grab any [issue](https://github.com/foundry-rs/starknet-foundry/issues) labeled with `good-first-issue`!
Need some guidance?

Reach out to other developers on [Telegram](https://t.me/+d8ULaPxeRqlhMDNk) or open
a [GitHub discussion](https://github.com/foundry-rs/starknet-foundry/discussions)!

### Environment setup

See [development guide](https://foundry-rs.github.io/starknet-foundry/development/environment-setup.html) in Starknet
Foundry book for environment setup.

### Running Tests and Checks

To run tests scripts, you have to install:

- [asdf](https://asdf-vm.com/guide/getting-started.html)
- [starknet-devnet](https://0xspaceshard.github.io/starknet-devnet/docs/intro)

> ⚠️ Make sure you run `./scripts/prepare_for_tests.sh` after setting up the development environment, otherwise the
> tests will fail.

Before creating a contribution, make sure your code passes the following checks

```shell
./scripts/test_forge.sh
./scripts/test_cast.sh
cargo fmt --check
cargo lint
```

Otherwise, it won't be possible to merge your contribution.

## Contributing

Before you open a pull request, it is always a good idea to search
the [issues](https://github.com/foundry-rs/starknet-foundry/issues) and verify if the feature you would like
to add hasn't been already discussed.
We also appreciate creating a feature request before making a contribution, so it can be discussed before you get to
work.

### Writing Tests

Please make sure the feature you are implementing is thoroughly tested with automatic tests.
You can check existing tests in the repository to see the recommended approach to testing.

### Breaking Changes

If the change you are introducing is changing or breaking the behavior of any already existing features, make sure to
include that information in the pull request description.

### Pull Request Size

Try to make your pull request self-contained, only introducing the necessary changes.
If your feature is complicated,
consider splitting the changes into meaningful parts and introducing them as separate pull requests.

While creating large pull requests usually will not prevent them from being merged, it may significantly increase review
time and increase the risk of complicated to resolve merge conflicts.