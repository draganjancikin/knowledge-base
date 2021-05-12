# Drupal 8: Core and Module Update

Steps:
1. Enable "Update Manager" module
2. Check "/admin/reports/updates" for available updates
    - Optional you can check outdated modules in command line
  
    ```bash
    # Check outdated modules in Docksal. 
    $ fin composer outdated "drupal/*"
    ```

3. In project on LOCAL make a separate branch for updates

    ```bash
    $ git checkout -b branch_for_updates
    ```

4. First update Drupal Core
  
    ```bash
    # Update Drupal core in Docksal.
    $ fin composer require drupal/core-recommended:8.9.15 drupal/core:8.9.15 --update-with-all-dependencies
    # Update db.
    $ fin druch updatedb???
    # Clear cache.
    $ fin drush cr
    ```
    * Check site.
    * Commit changes ([Read more](../git/README.md))

5. Then update active modules with security update

    * Always check Release note for important updates.
  
    ```bash
    # Update Drupal module in Docksal.
    $ fin composer update drupal/modulename --with-dependencies
    # Clear cache.
    $ fin drush cr

    ```
    * Check site.
    * Commit changes ([Read more](../git/README.md))

6. Then update active modules with optional update

7. Then update inactive modules with optional update

Other steps:

* after all updates merge to dev if exist, if not merge to master
* deploy to dev
* backup db from dev
* db update on dev
* obeležiti testeru da istestira
