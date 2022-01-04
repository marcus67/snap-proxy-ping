![ProxyPing-Logo](doc/proxy_ping_logo_128x128.png)
![Snapcraft-Logo](doc/snapcraft-logo-128x128.png)

# Snapcraft Support for `ProxyPing`

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/proxy-ping)

## Overview

This is the snap available to run ProxyPing. See [here](https://github.com/marcus67/proxy_ping) for details
on the application.

Follow these steps to install and configure the snap:
 
* Install the [snap daemon](https://snapcraft.io/docs/installing-snapd).    

* Install the ProxyPing snap:

      sudo snap install proxy-ping

* Optionally, configure the snap, if the default port `6666` does not work for you:

      sudo snap proxy-ping set port=PORT
 
  where `PORT` is the desired port number.

* Manually connect the required plugs:

      sudo snap connect proxy-ping:network-observe :network-observe

* Restart the snap

      sudo snap proxy-ping restart

and you are all set!

## Change History 

See [here](CHANGES.md)

## Security Details

In order for `ProxyPing` to be able to do its work, the snap has to be allowed to use the 
following plugs:

* `network-observe`: Obtain permission to execute the `ping` binary. 
  See [here](https://forum.snapcraft.io/t/executing-ping-within-a-snap/1540/2) for details.

* `network-bind`: Obtain permission to bind to the port `PORT` to provide the API interface.

These plugs are pre-configured for the snap. However, only the `network-bind` plug is automatically connected. The
other plug has to be connected manually. See Above.
