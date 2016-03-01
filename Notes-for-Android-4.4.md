Because Android 4.4 KitKat does not allow separate libraries per application on the /system partition, while some Google applications have conflicting dependencies on common libraries; not all recent Google Apps can be installed together on the /system partition.

As provisional solution, Google+, Hangouts, Messenger, Photos and YouTube are installed on on /data instead of /system, to prevent conflicts with the libraries of each other and the Google Search App.
This ensures that these applications will continue to be available in the Open GApps packages.
Difference is, that after installation they will behave just like any application installed from the Play Store, e.g. they can be uninstalled.