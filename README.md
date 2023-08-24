# 🥪 The Jaffle Shop 🦘

This is a template for creating a fully functional dbt project for teaching, learning, writing,
demoing, or any other scenarios where you need a basic project with a synthesized jaffle shop
business.

## How to use

### 1. Create new Codespace based on this repo

![Create codespace on main](.github/static/open-codespace.gif)

This will create a new Codespace, a sandboxed devcontainer with everything you need for a dbt
project.

Alternatively, you can clone this repo locally. You need Python 3.10 to successfully build the
project.

### 2. Setup Python

This will create a new virtual environment and install Python and DBT dependencies.

```console
python -m venv .venv
source .venv/bin/activate

pip install --upgrade pip
pip install -r requirements.txt

dbt deps
```

### 3. Create new DBT profile

Current DBT profile is using Postgres database on `localhost`, which does not run in Codespace.

So you'll need to update `host`, `user`, and `password` in `profiles.yml` to point to a running
Postgres instance.

### 4. Build the DBT project

Let's build our models, metrics and everything:

```console
dbt build
```
