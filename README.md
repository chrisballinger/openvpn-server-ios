openvpn-server-ios
==================

Tethering the hard way.

It turns out that Apple doesn't allow you to use `<net/if_utun.h>` unless you pay them a lot of money so we need to use [tunemu](https://github.com/friedrich/hans/blob/master/src/tunemu.c), a tun emulator that works over ppp.

## Setup

Install GNU libtool and automake:

	$ brew install libtool automake
	
Generate a static key and place it in `/configuration`: 

	$ openvpn --genkey --secret static.key
	
Build the dependencies:

    $ bash build-libssl.sh
    $ bash build-openvpn.sh
    
## Clean

To clean the `Submodules/openvpn` build folder:
	
	$ cd /Submodules/openvpn
    $ git clean -f && git clean -f -X
    
## Configuration

Simplest OpenVPN setup: [Static Key Mini-HOWTO](http://openvpn.net/index.php/open-source/documentation/miscellaneous/78-static-key-mini-howto.html)



