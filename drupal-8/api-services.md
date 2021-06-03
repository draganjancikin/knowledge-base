# API Services
<https://api.drupal.org/api/drupal/services/8.9.x>

## path.matcher

```php
# Check if the current page is the front page (bolean).
\Drupal::service('path.matcher')->isFrontPage();




# Returns the processed value of a named route parameter.
# https://api.drupal.org/api/drupal/core%21lib%21Drupal%21Core%21Routing%21RouteMatch.php/class/RouteMatch/8.9.x
\Drupal::routeMatch()->getParameter($param);
# example: $param = 'node'.
$node = \Drupal::routeMatch()->getParameter('node');
# Get content type from node.
$content_type = $node->bundle();
```