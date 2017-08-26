# CentOS 7.0 with switchable PHP version using Apache PHP-FPM 

## How to Use

* If you are using Windows machine install Git Bash.
* If you are using Linux machine install git.
* Open Terminal/Git bash and type below commands<br>
git clone https://github.com/harivenu/Pre-installed-CentOS-7-Apache-with-switchable-PHP-versions-using-PHP-FPM.git my-project<br>
cd my-project<br>
vagrant up</br>
* Go to the link http://192.168.33.10 it will show the public folder contents.
* Open PuTTy/SSH and open the 192.168.33.10 with default port number.

### Credentials
Username: vagrant
Password: vagrant

## Features

* CentOS 7.0
* Web Server - Apache/2.4.6 (CentOS) mod_fcgid/2.3.9 PHP/7.0.21
* Default version of PHP 7.0.19
* MySQL - 5.6.36 MySQL Community Server(root/vagrant)
* phpMyAdmin - 4.4.15 (root/vagrant)
* Composer - Version 1.4.2
* Drush Version - 8.0.0
* httpie - Version 0.9.4
* memcached - Version 1.4.15 (Not For PHP-FPM)
* vsftpd - Version 3.0.2
* Mailcatcher - Version 0.6.4
* git version 1.8.3.1
* openjdk version - 1.8.0_131
* Solr 6.6.0
* PHP_CodeSniffer version 2.9.1 (The installed coding standards are MySource, PEAR, PHPCS, PSR1, PSR2, Squiz, Zend and Drupal)

## Usage Drupal Coder

Just run the command

drupalcs File/Folder path

Eg:
[vagrant@localhost]$ drupalcs book.module
![drupalcs](http://www.ferbine.com/images/drupalcs.png)

## Solr Server

Already running just go http://192.168.33.10:8983

## Mailcatcher Usage

Already running - http://192.168.33.10:1080/

use this command for stop systemctl stop mailcatcher and start with this command systemctl start mailcatcher

## Shared Folder

'public' directory to '/var/www/html'

## Using PHP-FPM version

PHP versions : PHP 5.4, PHP 5.5, PHP 5.6, PHP 7.0 and PHP 7.1


Use autopilot command to specify the PHP version for each project folder.

The folder have .user.ini file to override the php.ini file configuration value.

 Usage:
    autopilot (options ...)

  Options:
    -p,  --project <name>      Required! Name of the project. Autopilot consider this as the machine name.
                               Optional! When you using Autopilot to change the command line version.
    -V,  --php-version         Optional! Define PHP version for this project (Default version is PHP 5.6).
    -c,  --php-cli             Optional! Define PHP command line version(PHP CLI is global).
    -l,  --list                Display the table of information project with PHP version.
    -h,  --help                This small usage guide.

  PHP Versions Directives:
    php54 for PHP 5.4
    php55 for PHP 5.5
    php56 for PHP 5.6
    php70 for PHP 7.0
    php71 for PHP 7.1

  Example:
    Command for setup project folder, assign specific PHP version to the project and change PHP ClI version.
    autopilot -p my_project -V {php54 | php55 | php56 | php70 | php71} -c {php54 | php55 | php56 | php70 | php71}
                  OR
    autopilot --project my_project --php-version {php54 | php55 | php56 | php70 | php71} --php-cli {php54 | php55 | php56 | php70 | php71}

    NOTE: Above command is also used for update PHP version based on the project name(my_project).

    -------------------------------------------------------------------------------------------------------

    Command for change PHP CLI version
    autopilot -c {php54 | php55 | php56 | php70 | php71}
              OR
    autopilot --php-cli {php54 | php55 | php56 | php70 | php71}

    -------------------------------------------------------------------------------------------------------

    Command for getting the project information table
    autopilot -l
         OR
    autopilot --list

  Features Note:
    * Autopilot is taken the Project name as unique ID.
    * Assign PHP version in each PHP projects located in the vagrant shared directory.
    * Update PHP version in each PHP projects located in the vagrant shared directory.
    * Each project directory contains .user.ini file for override the php.ini to each project.
    * Possible to switch PHP CLI version at any time.
    * Autopilot is also provided project information list.

  More information:

  Bug reports and suggestions to <hari.venu@ferbine.com>/<harivenu.v1992@gmail.com>
  
## Enjoy Coding... Thank you...

## This project has some performance issues so anyone interested please tune the configuration.
