# dotenv-op

Utility to manage dotenv files on 1Password

## Requirements 

- A 1Password account
- 1Password CLI (https://support.1password.com/command-line-getting-started/)

## Getting started

### Manually

- Change the following script variables according to your situation:

```
export DOTENVOP_VAULT=<VAULT_NAME>
export DOTENVOP_ACCOUNT=<1P Account name | default "my">
export DOTENVOP_EMAIL=<EMAIL>
```

- Place the script in: `/usr/local/bin/dotenv-op`

```bash
cp dotenv-op.sh /usr/local/bin/dotenv-op
```

## Usage

### Get a document

```bash
dotenv-op get -p project-name -e production
```

### Create a document

```bash
dotenv-op create -p project-name -e production -f .env.production
```

### Edit a document

```bash
dotenv-op edit -p project-name -e production -f .env.production
```

### Edit a document directly inside your terminal

This will download the existing document on 1Password and open your favorite editor to edit it

```
dotenv-op edit-inline -p project-name -e production
```

### Compare a document directly inside your terminal

This will download the existing document on 1Password and compare it with your local version

```
dotenv-op compare -p project-name -e production -f .env.production
```

