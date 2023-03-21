# Supabase_CLI
The Supabase CLI provides tools to develop your project locally and deploy to the Supabase Platform. You can also use the CLI to manage your Supabase projects, handle database migrations and CI/CD workflows, and generate types directly from your database schema.

The Supabase CLI is a command-line interface tool that enables developers to interact with the Supabase platform locally. It provides an easy way to create and manage databases, tables, and functions, as well as deploy Supabase projects directly from the command line. The Supabase CLI streamlines the management of Supabase projects, simplifying the deployment process and allowing developers to avoid navigating through the Supabase dashboard. It is easy to install and use, supports various operating systems, and is open source, allowing developers to contribute to its development and improve its functionality. Overall, the Supabase CLI is a powerful and essential tool for any developer working with Supabase.

## Installation

### npm
Install the CLI as dev dependency via npm:
```bash
npm install supabase --save-dev
```

### macOS & Linux
Install the CLI with Homebrew:
```bash
brew install supabase/tap/supabase
```

### Windows
Install the CLI with Scoop:
```bash
scoop bucket add supabase https://github.com/supabase/scoop-bucket.git
scoop install supabase
```

## Updates
When a new version is released, you can update the CLI using the following command:

### npm
```bash
npm update supabase --save-dev

```

### macOS & Linux

```bash
brew upgrade supabase
```

### Windows
```bash
scoop update supabase
```

## Basic commands

### Login
```bash
supabase login
```

### List Organizations

```bash
supabase orgs list
```

### Create a new project

```bash
supabase projects create my-new-project --db-password <string> --org-id <string> --region <string>
```

## Run Supabase Locally

### Prerequisites
Make sure you have these installed on your local machine:

* Docker
* Git
* Supabase CLI

```bash
supabase login
```
An access token must be generated in supabase, you can generate an access token from https://app.supabase.com/account/tokens

Make sure Docker is running. The start command uses Docker to start the Supabase services. This command may take a while to run if this is the first time using the CLI.

```bash
supabase start
```

Once all of the Supabase services are running, you'll see output containing your local Supabase credentials. You can use the stop command at any time to stop all services.

This way started supabase local development setup.

When the containers are finished creating, we will be able to enter the local development environment with URL Studio.

Studio URL: http://localhost:54323

* enter the table editor
* create a new table

Now we go to the console and execute:

```bash
supabase gen types typescript --local
```

We can get the table values directly.

*  At any time we can verify that supabase is running correctly with the command:
    ```bash
    supabase status
    ```

###  Compare database with migrations

```bash
supabase db diff
```

### Create migration
```bash
supabase db diff --use-migra -f new_table
```

* new_table is the name assigned of migration
9:28min
