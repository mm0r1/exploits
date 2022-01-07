# PHP 7.3-8.1 disable_functions bypass [concat_function]

This exploit uses a [bug](https://bugs.php.net/bug.php?id=81705) in a function that handles string concatenation. A statement such as `$a.$b` might result in memory corruption if certain conditions are met. The bugreport provides a very thorough analysis of the vulnerability. 

The PoC was tested on various php builds for Debian/Ubuntu/CentOS/FreeBSD with cli/fpm/apache2 server APIs and found to work reliably.

## Targets
  - 7.3 - all versions to date
  - 7.4 - all versions to date
  - 8.0 - all versions to date
  - 8.1 - all versions to date

## Fix
Stop relying on `disable_functions` (or any other php.ini settings) for security.

## Additional info
The underlying issue is present in all PHP7 versions. However, older (<7.3) releases have another [bug](https://github.com/php/php-src/commit/5898583e94462a6808b981b06dece2316979c8c1) that prevents memory from being freed correctly in some parts of the code, including `concat_function`. This exploit relies heavily on that functionality to work properly, so in a way, a memleak prevented the exploitability of a memory corruption vulnerability. Neat!