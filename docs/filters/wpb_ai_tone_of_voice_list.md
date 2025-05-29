---
sidebar_position: 6
---

# wpb_ai_tone_of_voice_list

This filter is handy if you want to change the ‘Tone of voice’ dropdown for a particular element param type in a WPBakery AI popup.

:::info
Available Since 8.3
:::

```php
<?php
add_filter('wpb_ai_tone_of_voice_list', 'add_custom_ai_wpb_processor', 10, 2);
function add_custom_ai_wpb_processor(array $list, string $wpb_ai_element_type): array {
    if ($wpb_ai_element_type !== 'textarea_html') {
        return $list;
    }
    unset($list['zealous']);
    $list['corporate'] = 'Corporate';
    
    return $list;
}
?>
```
