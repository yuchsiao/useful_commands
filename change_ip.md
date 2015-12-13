# How to change ip addresses

1. Modify network configuration file

  ```
  /etc/network/interfaces
  ```
2. Restart the networking service. If remotely, you will be 'bounced'

  ```
  #sudo service networking restart  # this does not work anymore in Ubuntu 14.04
  screen
  #sudo service networking stop; sudo service networking start  # not working either
  ifconfig eth0 down && ifconfig eth0 up
  ```
  
3. Hopefully your new network interface configuration is correct.


## Reference

1. [RESTARTING NETWORK INTERFACES IN UBUNTU 14.04](http://bryanapperson.com/blog/restarting-network-interfaces-in-ubuntu-14-04/)
2. [What is the preferred method to restart networking in Ubuntu and Debian](http://serverfault.com/questions/269921/what-is-the-preferred-method-to-restart-networking-in-ubuntu-and-debian)
