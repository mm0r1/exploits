# PHP 7.0-7.4 disable_functions bypass

This exploit uses a two year old [bug](https://bugs.php.net/bug.php?id=76047) in debug_backtrace() function. We can trick it into returning a reference to a variable that has been destroyed, causing a use-after-free vulnerability. The PoC was tested on various php builds for Debian/Ubuntu/CentOS/FreeBSD with cli/fpm/apache2 server APIs and found to work reliably.

## Targets
  - 7.0 - all versions to date
  - 7.1 - all versions to date
  - 7.2 - all versions to date
  - 7.3 < 7.3.15 (released 20 Feb 2020)
  - 7.4 < 7.4.3 (released 20 Feb 2020)
