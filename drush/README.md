# DRUSH

## Commands

* [Global](#global)
* [Cache](#cache)
* [Config](#config)
* [Core](#core)
* [pm](#pm)
* [Site](#site)
* [Theme](#theme)
* [User](#user)

### Global

```bash
# List available commands
list
```

### Cache

```bash
# cache clear (cc all is deprecated)
cache:clear (cc)
# cache rebuild
cache:rebuild (cr)
```

### Config

```bash
# Set config value directly. Does not perform a config import.
config:set (cset)
# set default theme
config:set system.theme default theme_name
```

### Core

```bash
# Run all cron hooks in all active modules for specified site
core:cron (cron)
```

### pm

```bash
# list all Drupal modules
pm:list (pml)
pm:list | grep module_name
pm:list --filter=search_term
# Enable one or more modules
pm:enable module_name (en)
# Uninstall one or more modules and their dependent modules
pm:uninstall (pmu)
```

### Site

```bash
# Install Drupal along with modules/themes/configuration/profile
site:install (si, sin)
```

### Theme

```bash
# Enable one or more themes.
theme:enable theme_name (then)
```

### User

```bash
#Display a one time login link for user ID 1, or another user.
user:login (uli)
```

########################################################################################################################

```bash
# devel-generate ---------------------------------------------------------------
# generate content
devel-generate:content 10 (genc 10)
devel-generate:content 20 --kill --bundles=content_type
# generate vocabulars
devel-generate:vocabs 10 (genv)
devel-generate:terms  10 --bundles=vocabulary_name (gent)
```

* feature-update (fu) ---------------------------------------------------------
If you have a Feature and you change something that is stored in that Feature (e.g. you update a View), you will need to update it. This will export the components to code. Rather than manually exporting the feature in the admin interface, you can just run feature-update.
drush feature-update feature_name

* feature-revert (fr) ---------------------------------------------------------
If you decide you don’t want to keep the changes that you have made, you can run feature-revert to bring it back to the code version. This makes it easy to play around with various settings.
drush feature-revert feature_name

* updatedb (updb) -------------------------------------------------------------
This will run any pending database updates. This is normally required if you update module code and that module needs to update the database. This saves you from running updates via update.php.
drush updatedb

* variable_get (vget)----------------------------------------------------------
I sometimes need to quickly see the value of a particular variable, so variable_get can be a real time saver.
drush variable_get variable_name

* watchdog-show (ws)-----------------------------------------------------------
Rather than going to the watchdog page to see errors and warnings, you only have to run watchdog_show.
drush watchdog-show
