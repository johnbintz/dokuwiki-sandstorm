# DokuWiki Sandstorm

Run [DokuWiki](https://www.dokuwiki.org/dokuwiki) on [Sandstorm](https://sandstorm.io/).
A lightweight wiki for your personal use.

## Details

* Runs in PHP 7 using PHP-FPM and an Nginx reverse proxy
* Uses Sandstorm authentication

### Sandstorm Upgrades

_(last updated 2020-06-26)_

The version in the app store is far behind the current releases of
DokuWiki. In order to minimize the amount of hassle with getting Sandstorm's
DokuWiki up to date with modern DokuWiki, new releases will be rolled out every
two or so weeks, giving existing Sandstorm users enough time to clean up
potentially conflicting plugins and other modifications, which will cause the
most issues when upgrading.

The release plan follows the recommended versions as shown on
the [Download DokuWiki](https://download.dokuwiki.org/) page,
and will be updated as new releases are available in the [App Store](https://apps.sandstorm.io/).

* Previous: 2017-02-19b
* [Currently in App Store](https://apps.sandstorm.io/app/nx3dqcmz2sjjz939vkg4847vvxrzqsatqfjrt3ea50z3jac5kv7h): 2017-02-19g (old stable)
* Next: 2018-04-22c (stable)
* Next: rc-2020-06-09 (recommended version)

## Troubleshooting

### PHP errors in the page, especially after upgrades

You may have a plugin that needs to be upgraded or disabled.
See if the script referenced in the error is in `plugins`.

* Try to disable or remove the plugin from the admin UI.
* If you can't disable/remove the plugin via the admin:
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
# follow the directions echoed from the script
```
