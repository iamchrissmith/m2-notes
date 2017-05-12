# create new rails app
`rails new [dir_name] -d postgresql`

[reseting defaults for rails](https://www.natashatherobot.com/how-to-configure-your-rails-defaults/)

# Databse Commands
1. `rake db:create`
2. `rake db:migrate`

Rollback migration: `rake db:rollback`
[Good list of descriptions](http://stackoverflow.com/a/10302357/6761672)

# One-To-Many Relationships
create migrations and models:
`rails generate migration [name of migrations] [first column:type] ... `

    * default to `string` type if you don't specify column types
    * make sure you include timestamps if you want them on the table

Remove a migration: `rails destroy migration [name of migrations]`


