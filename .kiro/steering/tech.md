# Tech constraints

> Replace this file per project. It exists so an agent knows what it is allowed
> to reach for before it starts making choices on your behalf.

## Stack

- **Language:** <!-- e.g. Python 3.12 / TypeScript, Node 20 -->
- **Runtime / platform:** <!-- e.g. AWS Lambda, container, local CLI -->
- **IaC:** <!-- e.g. Terraform, AWS CDK, none -->
- **Test framework:** <!-- e.g. pytest, vitest -->
- **Package manager:** <!-- e.g. uv, pnpm -->

## Allowed

List what an agent may use without asking.

## Requires approval

Anything not listed above. Specifically: new runtime dependencies, a new AWS service, a new datastore, anything that costs money.

## Forbidden

- Long-lived static credentials anywhere, including CI. Use OIDC and short-lived role assumption.
- Resource identifiers in source or in workflow files.
- Committing any `.env` file.
- Disabling a check to make CI pass.

## Cloud

- Region: <!-- -->
- Everything deployable must be reproducible from this repository. If a resource was created by hand in the console, either codify it or write it down in the README as a known gap.
