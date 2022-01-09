## Glossary

Gemfile == package.json
M == db
V == webpages HTML
C == logic

## Rails commands

- `rails new <project name>`
- start server: `rails s`
- generate something new: `rails g <what> <directory> <page name>`. E.g. `rails g controller home index`
- show all routes: `rails routes`

## Notes

- `layouts/application.html.erb` is the main app view file
- The name of a controller is its route
- `<%= yield %>` in `application.html.erb` will render the `.html.erb` for the route we're on.
- A partial is like a component, part of a page. The filename starts with an underscore. E.g. `_header.html.erb`
- To create link to partial in another html erb template: `<%= %>`. With the `=` it outputs it to the screen. Without the `=` it doesn't. Without the `=` is useful for other code like loops or if/else statements.
- `<%= render 'home/header' %>`. The header partial lives at `home/_header`, but the `render` keyword tells it it's a partial, so you leave the `_` out.
- links: `<%= link_to '<name>', <path>, class:"<class name>" %>` E.g. `<%= link_to 'Friend App', root_path, class:"navbar-brand" %>`. E.g. `<%= link_to 'About Us', home_about_path, class:"nav-link" %>`. The path will always be `<dir>_<filename>_path`. You can also find that by running `rails routes`, finding the prefix (e.g. `home_about`) and appending `_path` to it.
