check\_httpd\_limits.pl compares the size of running Apache httpd processes, the configured prefork / worker / event MPM limits, and the server's available memory. The script exits with a warning (or error message) if the configured limits exceed the server's available memory.

The script does not use any 3rd-party perl modules, unless the `--save/days/max` command-line options are used, in which case you will need to have the DBD::SQLite module installed. It should work on any UNIX server that provides /proc/meminfo, /proc/`*`/exe, /proc/`*`/stat, and /proc/`*`/statm files. You will probably have to run the script as root for it to read the /proc/`*`/exe symbolic links.

See the Wiki <a href='https://code.google.com/p/check-httpd-limits/wiki/Documentation'>Documentation</a> page for additional information.

You can view the original release announcement, and leave comments or suggestions, on <a href='http://surniaulula.com/2012/11/09/check-apache-httpd-prefork-or-worker-limits/'>the author's blog page</a>.

