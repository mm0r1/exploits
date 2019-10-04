# PHP 7.0-7.3 disable_functions bypass

This exploit uses a three year old [bug](https://bugs.php.net/bug.php?id=72530) in PHP garbage collector to bypass `disable_functions` and execute a system command. It was tested on various php7.0-7.3 builds for Ubuntu/CentOS/FreeBSD with cli/fpm/apache2 server APIs and found to work reliably. Feel free to submit an issue if you experience any problems.

## Targets
  - 7.0 - all versions to date
  - 7.1 - all versions to date
  - 7.2 - all versions to date
  - 7.3 - all versions to date

