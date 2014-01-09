## FloatingIP

Script to allow [heartbeat](http://linux-ha.org/wiki/Heartbeat) to allocate and deallocate a floating IP to/from an OpenStack instance.

The intention of this script is to simulate the VirtualIP floating mechanism for High Availability services that is blocked within OpenStack by quantum's anti-spoofing firewall rules.

### Files

   + **FloatingIP-wrapper:** Shell script entry point for heartbeat; typically it will reside under ```/etc/ha.d/resource.d/```. Needs to be renamed to ```FloatingIP```.

   + **FloatingIP:** Actual allocation/deallocation script; typically it will reside under ```/usr/lib/ocf/resource.d/heartbeat/```.

   + **nova.conf:** Sample configuration file, all fields are required. The name and location of this file is not enforced as the full path to it must be specified on ```/etc/ha.d/haresources``` but you would typically want it to reside under /etc/openstack/.
