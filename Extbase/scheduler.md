## Register A Scheduler Task
Register your task controller with the following line in your extension's **ext_localconf.php**:

```php
$GLOBALS['TYPO3_CONF_VARS']['SC_OPTIONS']['extbase']['commandControllers'][] = 'Bash\Gravity\Command\MyAwesomeCommandController';
```

## Create A Task Controller
Your Task Controller must extend **\\TYPO3\\CMS\\Extbase\\Mvc\\Controller\\CommandController** and implement a public action method.
The parameters along with their descriptions will appear in the Scheduler.
The controller must be implemented in the scheme below:

```php
<?php

namespace Vendor\ExtensionKey\Command
{
    class DoSomethingCommandController extends \TYPO3\CMS\Extbase\Mvc\Controller\CommandController
    {
        /**
         * @param string $name The name of the awesome user.
         */
        public function doSomethingCommand($name)
        {
            // ...
        }
    }
}



```