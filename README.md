# univer-friday

> A humble servant of Univer community.

## What does Friday do?

### Assign issue to Univer members

When an issue is created, Friday will assign it to a Univer member according to the `scope:x` tag. For example, if an issue has a `scope:core` tag, Friday will assign it to a Univer member who is responsible for `packages/core`.

Tags and their corresponding owners should be listed in each repository's config file.

### Arrange quality assurance tasks for pull requests

When a pull request is created, Friday will check if its title begins with `fix` or `feat`. It so, it will add a `pr:bugfix` or `pr:feature`, and a `qa:untested` label and assign it to QA team members. Friday will forbid a PR to being merged before the `qa:untested` label is removed and a `qa:verified` label is added.

## Translate non-English issues to English issues

## Setup

```sh
# Install dependencies
npm install

# Run the bot
npm start
```

## Docker

```sh
# 1. Build container
docker build -t univer-friday .

# 2. Start container
docker run -e APP_ID=<app-id> -e PRIVATE_KEY=<pem-value> univer-friday
```

## Contributing

If you have suggestions for how univer-friday could be improved, or want to report a bug, open an issue! We'd love all and any contributions.

For more, check out the [Contributing Guide](CONTRIBUTING.md).

## License

[Apache-2.0](LICENSE) © 2023 DreamNum Inc.
