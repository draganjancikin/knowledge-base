# API - Form

## Taxonomy, tags, autocomlete

### New 'entity_autocomplete' form element added
<https://www.drupal.org/node/2418529>


<https://api.drupal.org/api/drupal/core%21lib%21Drupal%21Core%21Entity%21Element%21EntityAutocomplete.php/class/EntityAutocomplete/8.9.x>

```php
  $form['field_tags'] = [
    '#type' => 'entity_autocomplete', // Type of form field.
    '#title' => '', // Title of form fielf.
    '#target_type' => 'taxonomy_term', // Pošto je autocomplete treba navesti koji content_type se gadja
    '#tags' => TRUE, // Ovo dozvoljava višestruki unos tagova
    '#selection_settings' => [
      'target_bundles' => ['tags'], // Ovo selelektuje tačno gde gađa autocomplete
    ],
    '#autocreate' => [
      'bundle' => 'tags', // Required. The bundle name for the new entity.
      // 'uid' => <a valid user ID>, // Optional. The user ID for the new entity, if the target entity type implements \Drupal\user\EntityOwnerInterface. Defaults to the current logged-in user.
    ],
    '#attributes' => [
      'placeholder' => $this->t('Add tags e.g. #corona'),
    ],
  ];
```