# DRUSH

Commands:

```bash
# _global ----------------------------------------------------------------------
# list all drush commands
list

# site -------------------------------------------------------------------------
# install Drupal site
site:install

# cache ------------------------------------------------------------------------
# cache clear (cc all is deprecated)
cache:clear (cc)
# cache rebuild
cache:rebuild (cr)

# devel-generate ---------------------------------------------------------------
# generate content
devel-generate:content 10 (genc 10)
devel-generate:content 20 --kill --bundles=client,county

# list all Drupal modules
pm-list
pml
pm-list | grep module_name

# enabled Drupal module
en module_name

# enabled Drupal theme
theme-enable theme_name
```

1. clear-cache (cc) ------------------------------------------------------------
2. pm-list (pml) ---------------------------------------------------------------
3. feature-update (fu) ---------------------------------------------------------
If you have a Feature and you change something that is stored in that Feature (e.g. you update a View), you will need to update it. This will export the components to code. Rather than manually exporting the feature in the admin interface, you can just run feature-update.
drush feature-update feature_name
4. feature-revert (fr) ---------------------------------------------------------
If you decide you don’t want to keep the changes that you have made, you can run feature-revert to bring it back to the code version. This makes it easy to play around with various settings.
drush feature-revert feature_name
5. updatedb (updb) -------------------------------------------------------------
This will run any pending database updates. This is normally required if you update module code and that module needs to update the database. This saves you from running updates via update.php.
drush updatedb
6. variable_get (vget)----------------------------------------------------------
I sometimes need to quickly see the value of a particular variable, so variable_get can be a real time saver.
drush variable_get variable_name
7. watchdog-show (ws)-----------------------------------------------------------
Rather than going to the watchdog page to see errors and warnings, you only have to run watchdog_show.
drush watchdog-show
8. pm-download (dl)-------------------------------------------------------------
I am often downloading new modules to try out. Rather than going to drupal.org to download them, I just run pml-download with the module or theme name.
drush pm-download project_name
9. pm-enable (en) & pm-disable (dis)--------------------------------------------
Once a new module or theme has been downloaded, it needs to be enabled. I do this with the pm-enable command, rather than going to the module page.
drush pm-enable project_name
If I no longer want a particular module enabled, I run pm-disable. Like pm-enable, it saves me from going to the module page.
drush pm-disable project_name
10. pm-update (up)--------------------------------------------------------------
Update Drupal core, modules and themes with pm-update.
drush pm-update
