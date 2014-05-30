Migration
=========

SED Scripts
-----------

* https://github.com/rakshasa/rtorrent/blob/master/doc/scripts/update_commands_0.9.sed

Example
-------

```
for i in `find . -name \*.php -or -name \*.js`; do
  sed -f ~/rtorrent/doc/scripts/update_commands_0.9.sed $i > $i.tmp;
  mv $i.tmp $i;
done
```

Modify the migration files as needed. It contains two sets of the same translations, one ending with a quote and another that ends with equal sign.

Notes
-----

* d.multicall was renamed d.multicall2 and now requires a target. (add a blank string as the first argument)