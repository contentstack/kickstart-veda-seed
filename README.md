# Kickstart Veda Stack Seed Content

This repository provides the Kickstart stack content for the Veda Kickstart project. An easy way to import this stack content is by using the CLI seed command.

> Contentstack stack must have English as Master Language

To import this content to your stack, perform the following steps:

### Install the CLI

```bash
npm install -g @contentstack/cli
```

### Set your region

Using the CLI for the first time? It might ask you to set your default region.
You can get all regions and their codes [here](https://www.contentstack.com/docs/developers/cli/configure-regions-in-the-cli) or run `csdx config:get:region`.

> Beware, Free Contentstack developer accounts are bound to the EU region.

Set your region like so:

```bash
csdx config:set:region EU
```

### Authenticate

Next, log in to your Contentstack account via CLI:

```bash
csdx auth:login
```

### Seed your stack

To be able to seed a new Stack, find your `Organization UID` in Contentstack.

> Contentstack Stacks overview > Org Admin > Info

Run the `seed` command to import content to your stack (`-n` can be used for a custom Stack name):

```bash
csdx cm:stacks:seed --repo "contentstack/kickstart-veda-seed" --org "<YOUR_ORG_UID>" -n "Kickstart Veda"
```

Refer to the [Seed command documentation](https://www.contentstack.com/docs/developers/cli/import-content-using-the-seed-command/) to learn more.

## Additional info

This stack seed was exported like this from its origin. Follow the steps.

```bash
csdx cm:stacks:export --stack-api-key <stack_api_key> --data-dir <path/to/export/destination>
```
