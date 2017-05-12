`rails c` = `rails console`
 * will have to restart anytime you edit files in your project(to see changes)

`rails server`
 * will have to restart if you add a directory to your project (to see changes)

# create new rails app
`rails new [dir_name] -d postgresql`

[reseting defaults for rails](https://www.natashatherobot.com/how-to-configure-your-rails-defaults/)

# Databse Commands
1. `rake db:create`
2. `rake db:migrate`
3. `rake db:seed`

Can combine commands such as: `rake db:{create,migrate,seed}` (must *not* have spaces inside the hash)

You (generally) don't need to run rake `db:test:prepare`; running `rake test` will load the schema to the test database

Rollback migration: `rake db:rollback`
[Good list of descriptions](http://stackoverflow.com/a/10302357/6761672)

# One-To-Many Relationships
create migrations and models:
`rails generate migration [name of migrations] [first column:type] ...`
* default to `string` type if you don't specify column types
* make sure you include timestamps if you want them on the table

(`rails g migration` is shorthand for `rails generate migration`)

Remove a migration: `rails destroy migration [name of migrations]`

`rails g model [name of the model] [first column:type]`
to relate to the model to an existing model:
`rails g model ... [column]:references`
 * This creates the model and creates the migration for us

