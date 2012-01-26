Airbrake for Drupal
===================

Copyright 2012 [Adam Kalsey](http://kalsey.com)

Implements [Airbrake error reporting](http://airbrakeapp.com) for Drupal. Sends reports to Airbrake for PHP Exceptions from any module and watchdog entries of your choice of severities (defaults to ERROR and above).

Requirements
------------

* An [Airbrake account](http://airbrakeapp.com) (duh!). 
* [PHP-Airbrake library](https://github.com/nodrew/php-airbrake) 
* [Libraries API module](http://drupal.org/project/libraries) (2.0 or up)

Installation
------------

Place the src folder from the php-airbrake library in `sites/all/libraries/airbrake` or `sites/<your-site>/libraries/airbrake`. If you don't already have a `libraries` folder, create it inside your sites/all directory. You should end up with a directory structure that looks like `sites/<your-directory>/libraries/airbrake/src/Airbrake` with a bunch of files in the `Airbrake` directory. 

You can see if the library is installed correctly by visiting your Status Report in the Drupal admin console (?q=admin/reports/status). The module will only report errors (why clutter the status page with lots of "yes, it works" messages?), so if you have Airbrake enabled and don't see the word "Airbrake on that page, you're good to go.

Go to http://yourdrupalinstall.example.com/?q=admin/config/development/airbrake and set your API key. You can also name you Drupal environment and Airbrake will group your errors together to prevent errors from your local dev environment from polluting your production logging.