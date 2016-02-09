## Enable RTE for a field

```php
<?php

// ...

'description' => array(
    'exclude' => 1,
    'label' =>    'LLL:EXT:gravity/Resources/Private/L ...',
    'config' => array(
        'type' => 'text', 
        'cols' => 40,
        'rows' => 15,
        'eval' => 'trim'
    ),
    'defaultExtras' => 'richtext[]', // <= This is the imporant bit
)

```