# Cypress Automation Framewrok

# Quickstart
## Cypress Set Up
Run the following command to install the dependencies after clone the repo.

```sh
npm install
```
## Dev Dependencies
* Cypress
* Cucumber

# Running Tests

## Prerequisites

Beacon uses a library from our [gitlab.com package registry](https://gitlab.com/groups/slingshot-aerospace/-/packages). To access this you need to:

1. Create a personal access token
2. Once you've created a .env file in subsequent steps, add the following env var:
   `NPM_TOKEN=<your personal access token>`
3. Optionally, add the following lines to your ~/.npmrc file

```
@slingshot-aerospace:registry=https://gitlab.com/api/v4/projects/31900423/packages/npm/
//gitlab.com/api/v4/projects/31900423/packages/npm/:_authToken=<your personal access token>
```

## Option 1: Run Beacon in Docker

```sh
# Make sure you have zx installed
npm install -g zx

# Install dependencies needed for the beacon script
npm install

# Run the app
./beacon start --fresh --dev-data
```


Run `./beacon --help` to see more options.

**Important**: since the app is running in a docker container, management commands need to be run in the container too. You can use `./beacon exec` to run commands in the container. For example:


- Data
  - [Prisma DB TypeGraphql Apollo setup](docs/data/prisma-db-typegraphql-apollo-setup.md)
  - [How to deploy a beacon stack](docs/data/deploy-beacon-stack-walkthrough.md)
- AWS setup
  - [Local AWS Chime setup](docs/aws-chime-setup.md)
