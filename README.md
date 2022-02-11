# Lunr filter demo

https://github.com/attiks/lunr-demo

## Setup

```bash
git clone git@github.com:attiks/lunr-demo.git
cd lunr-demo
fin start
fin composer install
fin drush -y si --existing-config
fin uli
fin drush devel-generate:terms --max-depth=1 10
fin drush devel-generate:content 50
```

- Open http://lunr-demo.docksal/admin/config/lunr_search/default/index to create the index.
- Open http://lunr-demo.docksal/search to test the search

```bash
mkdir -p static
drush tome:static --verbose
php -S localhost:8080 -t static
```

- Open http://localhost:8080/search

## settings.php

```php
<?php

$settings['config_sync_directory'] = dirname($app_root) . '/config';
$settings['tome_static_directory'] = '../static';
```
