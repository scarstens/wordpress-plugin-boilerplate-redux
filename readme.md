# NOTE: BOILER PLATE DEPRECATED 
Please see the new composer based abstract plugin base for proper standized plugin development.
https://github.com/WordPress-Phoenix/abstract-plugin-base

# WordPress Plugin Boiler Plate Redux
A boiler plate intended to serve the starting point of simpler plugins.

# Basic Usage
* Clone/Download the boilerplate
* Rename the Folder and `main-plugin-file.php` to reflect your plugin
* Follow TODO messages in what used to be `main-plugin-file.php`

# Extended Usage
* create folder `includes` and build your classes there. They will be automatically included in your main plugin file
* create folder `assets` for any static javascript, css or data files that may be needed
* create folder `admin` and follow TODO in main plugin file for code that only runs on admin side
* create folders in `admin` that follow the same `includes` `assets` structure

Note: Because we moved to using SPL_Autoload you no longer need to split includes between `includes` and `lib` folders. Instead
the system will automatically include files as you attempt to access classes that don't exist. This is both easier to manage
and more efficient since the system only loads classes its actually using on that page load.

#Using Github Updater Plugin
This plugin includes meta lines in the main PHP file. By including the github.com url to your repository you can make 
use of GIT tagging system alongside WordPress update system to `release` your plugin as new stable versions are tagged.

See more about this at:
https://github.com/afragen/github-updater#description

#Boilerpalte Change Log

## 0.1.2
- Moved autolaoding to use spl_autoload for easier access and better performance
- Removed get_custom_option function which doesn't work accross multiple plugins
