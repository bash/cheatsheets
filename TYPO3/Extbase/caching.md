## Disable Reflection (Docblock) Caching
Put the following code in **typo3conf/extTables.php**:

```php
<?php
$GLOBALS['TYPO3_CONF_VARS']['SYS']['caching']['cacheConfigurations']['extbase_reflection']['backend'] = TYPO3\CMS\Core\Cache\Backend\NullBackend::class;
$GLOBALS['TYPO3_CONF_VARS']['SYS']['caching']['cacheConfigurations']['extbase_object']['backend'] = TYPO3\CMS\Core\Cache\Backend\NullBackend::class;
```
