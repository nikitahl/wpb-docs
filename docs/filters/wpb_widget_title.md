---
sidebar_position: 4
---

# wpb_widget_title


To output title for content elements WPBakery Page Builder is using `h2` tag, if you need to modify it, here is how it can be done:

```php
<?php
add_filter('wpb_widget_title', 'override_widget_title', 10, 2);

function override_widget_title($output = '', $params = array('')) {
    $extraclass = (isset($params['extraclass'])) ? " ".$params['extraclass'] : "";
    return '<h3 class="entry-title'.$extraclass.'">'.$params['title'].'</h3>';
}
?>
```
