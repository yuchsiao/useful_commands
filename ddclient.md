# ddclient commands

The following commands work in Ubuntu 14.04.

## Test ddclient setup

ddclient keeps cache of the current ip in the file `/var/cache/ddclient/ddclient.cache`
If you would like to test whether ddclient is working, and does not want the cached ip interferes the mechanisms, 
then it is recommended to remove the cache first:
```
sudo rm /var/cache/ddclient/ddclient.cache
```
And then test by 
```
sudo ddclient -daemon=0 -debug -verbose -noquiet
```

## Update to DNS right away

Use the following command
```
sudo rm /var/cache/ddclient/ddclient.cache
sudo service ddclient restart
```

## Reference

1. [ddclient usage](http://sourceforge.net/p/ddclient/wiki/usage/)
2. [tutorial by dyn](https://help.dyn.com/ddclient/)
3. [cache](https://community.namecheap.com/forums/viewtopic.php?f=6&t=8669)
