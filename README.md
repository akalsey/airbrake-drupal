Airbrake for Drupal
===================

Copyright 2012 [Adam Kalsey](http://kalsey.com)

Implemnts [Airbrake error reporting](http://airbrakeapp.com) for Drupal. Sends reports to Airbrake for PHP Exceptions from any module and watchdog entries of your choice ofseverities (defaults to ERROR and above).

Requirements
------------

* An [Airbrake account](http://airbrakeapp.com) (duh!). 
* [PHP-Airbrake library](https://github.com/nodrew/php-airbrake) 
* [Libraries API module](http://drupal.org/project/libraries) (2.0 or up)

Installation
------------

Place the src folder from the php-airbrake library in `sites/all/libraries/airbrake` or `sites/<your-site>/libraries/airbrake`. If you don't already have a `libraries` folder, create it inside your sites/all directory. You should end up with a directory structure that looks like `sites/<your-directory>/libraries/airbrake/src/Airbrake` with a bunch of files in the `Airbrake` directory.

Go to http://yourdrupalinstall.example.com/admin/config/development/airbrake and set your API key. You can also name you Drupal environment and Airbrake will group your errors together to prevent errors from your local dev environment from polluting your production logging.