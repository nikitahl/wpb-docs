---
sidebar_position: 8
---

# wpb_module_ai_element_param_types

This filter is handy if you want to change element param types on which the AI icon is shown. Please note that simply attaching the AI icon does not guarantee that the popup can process AI properly. You should configure it with [`wpb_module_ai_type_response_route_lib`](/docs/filters/wpb_module_ai_type_response_route_lib/).

:::info
Available Since 8.3
:::

```php
<?php
add_filter('wpb_module_ai_element_param_types', 'add_custom_ai_wpb_processor');
function add_custom_ai_wpb_processor(array $list): array {
    $list[] = 'dropdown';
    
    return $list;
}
?>
```
