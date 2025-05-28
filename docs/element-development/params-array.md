---
sidebar_position: 3
---

# `params` array

Here you should describe all you shortcode’s attributes that should be editable with WPBakery Page Builder interface. Each shortcode’s attribute should be described in the separate array element.

Defining “Text” attribute:

```php
array(
    "type" => "textfield",
    "holder" => "div",
    "class" => "",
    "heading" => __( "Text", "my-text-domain" ),
    "param_name" => "foo",
    "value" => __( "This is test param for creating new project", "my-text-domain" ),
    "description" => __( "Enter foo.", "my-text-domain" )
)
```
