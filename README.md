xbmc-fmr : XBMC Fix Movies Rating
=======================

This script intend to keep your movie rating up to date
Currently only work with mysql DB

Changelog
--------------------------
* v0.2

Switch to sequel and sqlite native xbmc database support

* v0.1

Initial release



Supported Ruby version
--------------------------

Develop on Debian testing so ruby 1.9.3

How it works ?
--------------------------

The script take the IMDB id in the database and look if rating need to be adjust against IMDB.
If there's no valid IMDB id for the movie , it try to fix it with the first search matching the movie title.

Required gem
--------------------------
* sequel
* mysql2 or/and sqlite
* imdb
* ruby-progressbar

Configuration
--------------------------
Open the file and edit the mysql connection settings section

Usage
--------------------------

Don't forget to configure Mysql settings !

```Shell
Usage: ./xbmc-fmr [options]
    -a, --all                        All movies rating update.
    -z, --zero                       Only proceed movie with a rating of 0.
    -d, --dry                        Dry run mode, no database update.
    -c, --cron                       Crontab mode , no progress bar.
    -n, --num [VAL]                  Proceed [VAL] random movies rating update (default 10).
        --version                    Display xbmc-fmr version and exit.
    -h, --help                       display this help and exit.
```
