PID Log
=======

Color-coded [dlog](https://developer.tizen.org/development/guides/native-application/system/dlog) formatter with filter by process modified for Tizen development.

An update to Jeff Sharkey's excellent [logcat color script][1] which only shows
log entries for processes from a specific application package.

During application development you often want to only display log messages
coming from your app. Unfortunately, because the process ID changes every time
you deploy to the phone it becomes a challenge to grep for the right thing.

This script solves that problem by filtering by application package. Supply the
target package as the sole argument to the python script and enjoy a more
convenient development process.

    pidlog com.oprah.bees.android


Here is an example of the output when running for the Google Plus app:

![Example screen](screen.png)


Install
-------

Get the script:

 *  Download `pidlog.py` and place it on your PATH.


Make sure that `sdb` from the [Tizen SDK][3] is on your PATH. This script will
not work unless this is that case. That means, when you type `sdb` and press
enter into your terminal something actually happens.

To include `sdb` and other android tools on your path:

    export PATH=$PATH:<path to Tizen SDK>/tools

Include these lines in your `.bashrc` or `.zshrc`.

*Note:* `<path to Tizen SDK>` should be absolute and not relative.

 [1]: http://jsharkey.org/blog/2009/04/22/modifying-the-android-logcat-stream-for-full-color-debugging/
 [2]: http://brew.sh
 [3]: https://developer.tizen.org/development/tools/download
