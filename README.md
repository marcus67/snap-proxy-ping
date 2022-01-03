![ProxyPing-Logo](doc/proxy_ping_logo_128x128.png)
![Snapcraft-Logo](doc/snapcraft-logo-128x128.png)

# Snapcraft Support for `ProxyPing`

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/proxy-ping)

## Overview

There is a snap available to run ProxyPing. See [here](https://github.com/marcus67/proxy_ping) for details
on the application.

Follow these steps to install and configure the snap:
 
* Install the [snap daemon](https://snapcraft.io/docs/installing-snapd).    

* Install the ProxyPing snap:

      sudo snap install proxy-ping

* Optionally, configure the snap, if the default port `6666` does not work for you:

      sudo snap proxy-ping set port=PORT
 
  where `PORT` is the desired port number.

* Restart the snap

      sudo snap proxy-ping restart

and you are all set!

## Security Details

In order for `ProxyPing` to be able to do its work, the snap has to be allowed to use the 
following plugs:

* `network-bind`: Obtain permission to bind to the port `PORT` to provide the API calls.

This plug is pre-configured for the snap and the `network-bind` plug is automatically connected.
