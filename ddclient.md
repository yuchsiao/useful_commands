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
