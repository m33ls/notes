# Ad-Hoc Ethernet
Set up an ad-hoc connection between two computers over an ethernet cable

## Steps
* connect ethernet cable between computers

* manually set an ip for each
  eg. 169.254.0.1 and 169.254.0.2

* set bits after the main address to /16
  eg. 169.254.0.1/16

* set both computers to the same subnet
  e.g. 255.255.0.0;
  this can be done under network properties in windows
  or on linux with `sudo ifconfig INTERFACE netmask MASK`

* ping to check connection
