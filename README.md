[![Latest Stable Version](https://poser.pugx.org/anime-db/shmop/v/stable.png)](https://packagist.org/packages/anime-db/shmop)
[![Latest Unstable Version](https://poser.pugx.org/anime-db/shmop/v/unstable.png)](https://packagist.org/packages/anime-db/shmop)
[![Build Status](https://travis-ci.org/anime-db/shmop.png)](https://travis-ci.org/anime-db/shmop)
[![Total Downloads](https://poser.pugx.org/anime-db/shmop/downloads.png)](https://packagist.org/packages/anime-db/shmop)
[![License](https://poser.pugx.org/anime-db/shmop/license.png)](https://packagist.org/packages/anime-db/shmop)
[![Code Coverage](https://scrutinizer-ci.com/g/anime-db/shmop/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/anime-db/shmop/?branch=master)

# shmop

Shmop is a simple and small abstraction layer for shared memory manipulation using PHP

## Examples

Creating new block

```php
use AnimeDb\Shmop\FixedBlock;

$sh = new FixedBlock(0xFF /* id for memory block */, 3 /* memory block size */);
$sh->write('foo');
echo $sh->read(); // print 'foo'
```

Reading an existing block

```php
use AnimeDb\Shmop\FixedBlock;

$sh = new FixedBlock(0xFF /* id for memory block */, 3 /* memory block size */);
// print contents of memory block. if block is not exists prints a blank line
echo $sh->read();
```
