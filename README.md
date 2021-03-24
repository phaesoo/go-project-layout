# go-project-layout

My go project layout. 

Most of concepts are came from [`golang-standards/project-layout`](https://github.com/golang-standards/project-layout)


## Top-level Directories

### `/apps`

Main applications for this project.

The directory name for each application should match the name of the executable you want to have (e.g., `/apps/myapp`).

### `/configs`

Configs for this project. Currently I'm using `spf13/viper` for the config loader.

The various configs are aggregated into `/configs/config.go`.

### `/db`

DB related resources. Include migration code, db init file(e.g. mysql-init.sql).

### `/internal`

Private application and library code. This is the code you don't want others importing in their applications or libraries. 

### `/pkg`

Library code that's ok to use by external applications.

### `/vendor`
Application dependencies. It would be ignored by `.gitignore`


## Directories You Shouldn't Have

### `/src`

Some Go projects do have a `src` folder, but it usually happens when the devs came from the Java world where it's a common pattern. If you can help yourself try not to adopt this Java pattern. You really don't want your Go code or Go projects to look like Java :-)
