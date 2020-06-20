DokuWiki is a simple to use and highly versatile Open Source wiki
software that doesn't require a database. It is loved by users for its
clean and readable syntax. The ease of maintenance, backup and integration
makes it an administrator's favorite. The large number of plugins
contributed by its vibrant community allow for a broad range of use cases
beyond a traditional wiki.

## Sandstorm Upgrade Troubleshooting

If you've upgraded DokuWiki and are now getting PHP errors in your pages,
you may have a plugin that needs to be upgraded or disabled.
See if the script referenced in the error is in `plugins`. If it is:

* Try to disable or remove the plugin from the admin UI.
* If you can't disable/remove the plugin via the admin:
  1. Download a backup of the grain
  2. Unzip the backup into a new folder
  3. Remove the plugin folder from the unzipped backup tree
  4. Rezip up the backup tree, preserving the same base folders
  5. Restore the grain from backup
