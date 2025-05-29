---
sidebar_position: 11
---

# vc_map()

To register new content element you can use `vc_map()` function. List of available [parameters](/docs/element-development/parameter-types).

```php
<?php vc_map( $params ); ?>
```
## Parameters

List of available [parameters](/docs/element-development/parameter-types).

## Example

How to register new content element with `vc_map()` function.

```php
<?php
$params = array(
    'name' => __( 'My Custom Element', 'my-text-domain' ),
    'base' => 'my_custom_element',
    'category' => __( 'Custom Elements', 'my-text-domain' ),
    'description' => __( 'This is a custom content element.', 'my-text-domain' ),
    'params' => array(
        array(
            'type' => 'textfield',
            'heading' => __( 'Custom Heading', 'my-text-domain' ),
            'param_name' => 'custom_param',
            'value' => '',
            'description' => __( 'This is a custom parameter for the my_custom_element shortcode.', 'my-text-domain' ),
        ),
    ),
);

vc_map( $params );
?>
```
