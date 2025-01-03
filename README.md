# Lando Starter Project

A starter project for Wordpress local development using [Lando](https://lando.dev/). It bootstrap [Bedrock](https://roots.io/bedrock/) and [Sage](https://roots.io/sage/) into the project with a few simple commands.

## What does it do?

This project uses Lando in order to set up the local environment on your machine with:

- [Mailhog](https://github.com/mailhog/MailHog) - an email testing tool for developers.
- [PhpMyAdmin](https://www.phpmyadmin.net/) - A free software tool intended to manage databased on the web.
- [Node.js](https://nodejs.org/en) - Allows to run npm, yarn and thus build the sage theme.

## Set up

Download this repo and edit:

- .lando.yml - Change the name and the proxy settings in order to fit your project descriptions.
- .env.lando - This is the .env file that controls all the settings for the project. Change all the variables as needed.

## Starting

Just run ```lando start```

## Installing bedrock, wordpress and sage

### Installing WordPress (bedrock)

To install bedrock, please use the install-bedrock command. This will create a folder called site and create the website using the bedrock framework.

The create-env command will create the WordPress .env file using the settings defined in .env.lando.

```bash
lando install-bedrock
lando create-env
```

### Installing WordPress

Now that all the files are set up, it’s needed to install WordPress and set up the database. For this the install-wordpress command should be used.

```bash
lando install-wordpress
```

The user will be prompted with all the necessary variables in order to set up initialize the website.

### Installing the theme

After WordPress is installed, the theme needs to be installed as well. For this, just run the install-sage command.

```bash
lando install-sage
```

## Common tasks

For faster development, some common tasks were added to the starter project in order to facilitate the day-to-day activities.

### Buildind theme’s assets

```bash
lando theme-build
```

### Using composer

```bash
lando composer require "wpackagist-plugin/contact-form-7":"6.0.2"
```

### Using WP-CLI

```bash
lando wp user list
```