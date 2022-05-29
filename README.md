# Drupal Ethereum

A project template to work on the [Ethereum module](https://www.drupal.org/project/ethereum).

Forked from this [Drupal project template](https://github.com/MatthieuScarset/drupal-template).

## Requirement

Install [Lando](https://docs.lando.dev/drupal/) on your machine.

## Usage

Click on the button _Use this template_ to generate your own project, then:

```bash
git clone git@github.com:<UsernameOrOrganization>/drupal-ethereum.git myproject 

cd myproject

# Edit project name in base config files.
code .lando.yml      # ->  edit the lando file with your project name (e.g. name: myproject)
cp .env.example .env # ->  create your environment file
code .env.example    # ->  edit your env file (e.g DRUSH_OPTIONS_URI=https://myproject.lndo.site)

# Commit your changes
git add . && git commit -m "Rename project" && git push 

# Start the project
lando start 

# Download dependencies
lando composer install -o

# Install Drupal
lando drush site:install --existing-config -y
lando drush user:password admin admin
lando drush user:login # -> Ctrl+Click the URL to open your site :)
```

Start to build things! 
