# Migrations Boilerplate
This project wires up Doctrine ORM & Migrations.

The project contains a working ORM + Migrations wiring/configuration. It's not a statement
of best practices or anything, just a working example to get you going. Feel free to change
things to your preference needs.

In order to use the command line tools you need to create the Entity Manager and provide
the configuration to your model/mapping paths. But you'll also need the same configuration
to create the Entity Manager in your application code. Rather than put this configuration
in your application configuration or bootstrap, it's a good idea to keep entity manager &
ORM configuration in a separate tiny config file. This lets you reuse the config in your
app bootstrap and your command line config (and or test suite configs) without having to
bootstrap your app config. This is just a suggestion though and you don't have to follow it.



## Installation
Use composer to create a new project based off this boilerplate.

```
composer create-project jeremygiberson/doctrine-migrations-boilerplate my-project
cd my-project
```

### Overrides
See `doctrine-config.php.dist` for overridable values. To override, copy 
the file to `doctrine-config.php` and change values to match your requirements.

## Usage
### Status
Check migrations status

`vendor/bin/doctrine-migration migrations:status`

### Migrate
Run pending migrations

`vendor/bin/doctrine-migration migrations:migrate`

### Diff
Generate a migration file by comparing current schema to your model definitions.

`vendor/bin/doctrine-migration migrations:diff`

### Other Commands
There are other commands available. You can see the list by running doctrine-migration without arguments. 

`vendor/bin/doctrine-migration`
