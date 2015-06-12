Because Android 4.4 KitKat does not allow separate libraries per application on the /system partition, while some Google applications have conflicting dependencies on common libraries; not all recent Google Apps can be installed together on the /system partition.

As provisional solution, Google+, Hangouts, Photos and YouTube are installed on on /data instead of /system, to prevent conflicts with the libraries of each other and the Google Search App.
This ensures that these applications will continue to be available in the Open GApps packages.
Difference is, that after installation they will behave just like any application installed from the Play Store, e.g. they can be uninstalled.

This hack did break the current space-calculations in the install-script, since the space-calculation still assumes all applications would be installed on /system. This should only have a very limited impact, since now it can only refuse installation, but never let your device run out of space. Also it should not impact many users, since those with a small /system partition wouldn't install full or stock with a manual configuration-file anyhow.