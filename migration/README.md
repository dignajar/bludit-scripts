## Migration Script for Bludit v1.6.2 to v2.0

* Script is tested on PHP7+
* Only `bl-content` is migrated.
* Script migrates only the Core plugin data and user data (posts, pages, uploads etc.) to the new db structure.
* Third party plugin data is not migrated intentionally. We do not know if v1 plugins are compatible with v2.
* Script sets the theme to "log" for safer/better compatibility. Change your custom/stock theme manually after migration.

### Instructions:
* Take a backup of current installation.
* Copy migrate.php to root of Bludit v1.6 installation.
* Run it and Copy freshly generated `bl-content` directory from migrations/* to the new Bludit v2 installation.
* If there were posts migrations conflicts, add them manually to your new Bludit installation from `failed-posts` directory.
* Done!

### I found a bug:
* Report an issue describing it as verbosely as possible.

### Current Bugs:
* Installations having Pages with Child Pages might be buggy since Bludit v2 Static Pages cannot have a child.