# DRUSH

Commands:

```bash
# install Drupal site
site:install

# cache clear (cc all is deprecated)
cc

# cache rebuild
cr

# list all Drupal modules
pm-list
pml
pm-list | grep modul_ename

# enabled Drupal module
en module_name
```

1. clear-cache (cc) ------------------------------------------------------------
When you are developing Drupal modules, you will often have to clear the cache (for example, when adding a new menu item in hook_menu). You can clear all caches with drush cc all, or choose a specific one with drush cc
drush cc all
2. pm-list (pml) ---------------------------------------------------------------
This shows you a list of modules and themes that are available for your Drupal site. When I am working on a site, I often want to know if a particular module is enabled. You can use pml in combination with grep to see if the module you are looking for exists in the site.
drush pm-list | grep modulename
One of the advantages of using grep is that you don’t even need to know the full module name.
For example:
drush pm-list | grep media
This will find any module or theme with media in the name. In my case, it returns Media, Media Desk, Media Internet Sources and Multimedia Editorial Element.
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
