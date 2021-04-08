# Drupal 8: Core and Module Update

```bash
# Check outdated modules. 
$ fin composer outdated "drupal/*"

# Update Drupal core.
$ fin composer require drupal/core-recommended:8.9.13 drupal/core:8.9.13 --update-with-all-dependencies

# Update Drupal module.
$ fin composer update drupal/modulename --with-dependencies
```

First Drupal core update:

* make a new branch
* update Drupal core
* clear cache
* check site

On link <http://psc.docksal/admin/reports/updates> is avaible updates. Need to enable Update Manager module.

Module update:

* make a new branch
* check Release Notes for important updates
* update module
* clear cache
* check site
* commit
* after all updates merge to dev if exist, if not merge to master
* deploy to dev
* backup db from dev
* db update on dev
* obeležiti testeru da istestira