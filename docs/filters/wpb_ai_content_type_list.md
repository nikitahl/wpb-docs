---
sidebar_position: 7
---

# wpb_ai_content_type_list

This filter is handy if you want to change the 'Content type' dropdown for a particular element param type in a WPBakery AI popup.
Please note. Right now, we support only the following content types:

* `new_content`
* `improve_existing`
* `translate`

:::info
Available Since 8.3
:::

```php
<?php
add_filter('wpb_ai_content_type_list', 'add_custom_ai_wpb_processor', 10, 2);
function add_custom_ai_wpb_processor(array $list, string $wpb_ai_element_type): array {
    if ($wpb_ai_element_type !== 'textarea_html') {
        return $list;
    }
    unset($list['translate']);
    
    return $list;
}
?>
```
