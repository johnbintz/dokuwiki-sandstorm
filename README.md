# DokuWiki Sandstorm

Run [DokuWiki](https://www.dokuwiki.org/dokuwiki) on [Sandstorm](https://sandstorm.io/).
A lightweight wiki for your personal use.

## Details

* Runs in PHP 7 using PHP-FPM and an Nginx reverse proxy
* Uses Sandstorm authentication

## Troubleshooting

### PHP errors in the page

* See if the script referenced in the error is in `plugins`. You may have a
  plugin that needs to be upgraded or disabled.
  * If you can't disable/remove the plugin via the UI:
    1. Download a backup of the grain
    2. Unzip the backup into a new folder
    3. Remove the plugin folder from the unzipped backup tree
    4. Rezip up the backup tree, preserving the same base folders
    5. Restore the grain from backup

## Building a new version

### Requirements

* git
* VirtualBox
* Vagrant
* [vagrant-spk](https://docs.sandstorm.io/en/latest/vagrant-spk/installation/)

### Setup & Commands

```
git submodule init
git submodule update
bin/upgrade_dokuwiki <target git tag from https://github.com/splitbrain/dokuwiki>
# follow the directions printed from the script
```
