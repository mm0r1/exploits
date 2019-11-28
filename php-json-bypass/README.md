# PHP 7.1-7.3 disable_functions bypass

**Check out my [php7-gc-bypass](https://github.com/mm0r1/exploits/tree/master/php7-gc-bypass) exploit which uses another [bug](https://bugs.php.net/bug.php?id=72530) that works on all php 7.0-7.3 versions released as of 28.11.2019.**

___

![not an issue](https://i.imgur.com/Hta6ggy.png)
___

This exploit utilises a use after free [vulnerability](https://bugs.php.net/bug.php?id=77843) in json serializer in order to bypass `disable_functions` and execute a system command. It should be fairly reliable and work on all server apis, although that is not guaranteed.

## Targets
  - 7.1 - all versions to date
  - 7.2 < 7.2.19 (released: 30 May 2019)
  - 7.3 < 7.3.6 (released: 30 May 2019)

<br />

Credits to [@cfreal](https://github.com/cfreal) for the original bug discovery.
