openvpn-server-ios
==================

Tethering the hard way.

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


