The Nextcloud Client reads a configuration file.  You can locate this configuration file as follows:

On Linux distributions:
        ``$HOME/.config/Nextcloud/nextcloud.cfg``

On Microsoft Windows systems:
        ``%APPDATA%\Nextcloud\nextcloud.cfg``

On MAC OS X systems:
        ``$HOME/Library/Preferences/Nextcloud/nextcloud.cfg``


The configuration file contains settings using the Microsoft Windows .ini file
format. You can overwrite changes using the Nextcloud configuration dialog.

.. note:: Use caution when making changes to the Nextcloud Client configuration
   file.  Incorrect settings can produce unintended results.

Some interesting values that can be set on the configuration file are:

+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| ``[Nextcloud]`` section                                                                                                                                  |
+=================================+===============+========================================================================================================+
| Variable                        | Default       | Meaning                                                                                                |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+
| ``remotePollInterval``          | ``30000``     | Specifies the poll time for the remote repository in milliseconds.                                     |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+
| ``forceSyncInterval``           | ``7200000``   | The duration of no activity after which a synchronization run shall be triggered automatically.        |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+
| ``fullLocalDiscoveryInterval``  | ``3600000``   | The interval after which the next synchronization will perform a full local discovery.                 |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+
| ``notificationRefreshInterval`` | ``300000``    | Specifies the default interval of checking for new server notifications in milliseconds.               |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+


+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| ``[General]`` section                                                                                                                                    |
+=================================+===============+========================================================================================================+
| Variable                        | Default       | Meaning                                                                                                |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+
| ``chunkSize``                   | ``5242880``   | Specifies the chunk size of uploaded files in bytes.                                                   |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+
| ``promptDeleteAllFiles``        | ``true``      | If a UI prompt should ask for confirmation if it was detected that all files and folders were deleted. |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+
| ``maxLogLines``                 | ``20000``     | Specifies the maximum number of log lines displayed in the log window.                                 |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+
| ``timeout``                     | ``300``       | The timeout for network connections in seconds.                                                        |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+
| ``moveToTrash``                 | ``false``     | If non-locally deleted files should be moved to trash instead of deleting them completely.             |
|                                 |               | This option only works on linux                                                                        |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+
| ``showExperimentalOptions``     | ``false``     | Whether to show experimental options that are still undergoing testing in the user interface.          |
|                                 |               | Turning this on does not enable experimental behavior on its own. It does enable user inferface options that can be used to opt in to experimental features. |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+


+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| ``[Proxy]`` section                                                                                                                                      |
+=================================+===============+========================================================================================================+
| Variable                        | Default       | Meaning                                                                                                |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+
| ``host``                        | ``127.0.0.1`` | The address of the proxy server.                                                                       |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+
| ``port``                        | ``8080``      | The port were the proxy is listening.                                                                  |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+
| ``type``                        | ``2``         | ``0`` for System Proxy.                                                                                |
+                                 +               +--------------------------------------------------------------------------------------------------------+
|                                 |               | ``1`` for SOCKS5 Proxy.                                                                                |
+                                 +               +--------------------------------------------------------------------------------------------------------+
|                                 |               | ``2`` for No Proxy.                                                                                    |
+                                 +               +--------------------------------------------------------------------------------------------------------+
|                                 |               | ``3`` for HTTP(S) Proxy.                                                                               |
+---------------------------------+---------------+--------------------------------------------------------------------------------------------------------+
