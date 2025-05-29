---
sidebar_position: 10
---

# wpb_module_ai_type_response_route_lib

This filter is handy if you want to change the way a particular element param type is processed by the WPBakery AI API.

:::info
Available Since 8.3
:::

```php
<?php
add_filter('wpb_module_ai_type_response_route_lib', 'add_custom_ai_wpb_processor');
function add_custom_ai_wpb_processor(array $list): array {
    // You can use your custom types here
    unset($list['textfield']);
    $list['textfield'] = [
        // Path to processor class
        'path' => vc_path_dir('MODULES_DIR', 'ai/class-vc-ai-content-generator.php'),
        // Class name
        'class' => 'Vc_Ai_Content_Generator',
        // AI generator method name
        'method' => 'generate',
        // List of endpoints to remove server that specify what type of content to generate
        'endpoint' => [
            'default' => 'generate-text',
            'contentType' => [
                'improve_existing' => 'rewrite-text',
                'translate' => 'translate-text',
            ],
        ],
    ];
    
    return $list;
}
?>
```
