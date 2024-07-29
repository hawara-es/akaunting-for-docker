# Akaunting for Traefik

## Description

This repository was created using the [official Akaunting images](https://github.com/akaunting/docker) as a starting point but modifying them to make them work in a Traefik environment.

> Akaunting is online, open source and free accounting software built with modern technologies. Track your income and expenses with ease. For more information on Akaunting, please visit the [website](https://akaunting.com).

## Usage

```shell
# Download these Composer files
git clone https://github.com/hawara-es/akaunting-docker
cd akaunting-docker

# Create your environment files
cp .env.example .env
cp env/run.env.example env/run.env

# Customize them

# Run the Docker components for the first time
# setting the AKAUNTING_SETUP to true
AKAUNTING_SETUP=true docker compose up -d
```

Then head to the **APP_URL** that you stablished in **env/run.env** and finish configuring your Akaunting company through the interactive wizard.

After setup is complete, bring the containers down before bringing them back up without the setup variable.

```shell
docker compose down
docker compose up -d
```

> Please never use `AKAUNTING_SETUP=true` environment variable again after the first time use.

## License

Akaunting is released under the [GPLv3 license](LICENSE.txt).
