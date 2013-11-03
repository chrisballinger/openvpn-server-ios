openvpn-server-ios
==================

Tethering the hard way.

## Setup

Install OpenVPN for Mac OS X:

	$ brew install openvpn
	
Generate a static key:

	$ openvpn --genkey --secret static.key
	
Build the dependencies:

    $ bash build-libssl.sh
    $ bash build-openvpn.sh    
    
## Configuration

Simplest OpenVPN setup: [Static Key Mini-HOWTO](http://openvpn.net/index.php/open-source/documentation/miscellaneous/78-static-key-mini-howto.html)
