# UMass Amherst Drupal orchestration
This represents a suite of tools based primarily on ansible with bash wrappers we use to move drupals around our various stacks.

## Functional/in use
### devtostag
Moves a Drupal 7 site from our development node to our staging node
**Arguments** [SITENAME] [OWNER] **todo** call fixpermissions role to remove it's tasks from playbook

### stagtoprod
Moves a Drupal 7 site from our staging node to our production node
**Arguments** [SITENAME] [OWNER] **todo** call fixpermissions role to remove it's tasks from playbook

### prodtodev
Moves a Drupal 7 site from our production node to our development node
**Arguments** [SITENAME] [OWNER] **todo** call fixpermissions role to remove it's tasks from playbook

### fixpermissions
Adjusts a Drupal 7 site's directory permissions to a state usable by Activetheme, as well as our defaults
**Arguments** [SITENAME] [HOST] [OWNER]



## ToDo
### sitebackup
dumps a site's database and makes it a .tar.gz in our archive directory

### provision-d7
Creates a new site including the umass_core theme, umass_auth, umass_tokens as well as our current list of contrib modules, with configuration to include default shibboleth headers

### prodtostag
Moves a Drupal 7 site from our production node to our staging node

### dissite
UMass Fork of default apache disable site functionality

### ensite
UMass Fork of default apache enable site functionality

## deprovision-d7
backup the site along with a copy of it's configuration and delete it; restart apache

## shibprovision
register all users or given a username create relationship between drupal uid and shib

## addmodule
Add a module for a user
**Arguments** [SITENAME] [HOST] [MODULENAME]

## secpatch
Pull a site down to staging, update drupal core and update drupal contrib using the --security-only flag ** * ** on a single site or all sites