Zoin
=============================
[![Build Status](https://travis-ci.org/zoinofficial/Zoin.svg?branch=master)](https://travis-ci.org/zoinofficial/Zoin)

What is Zoin?
-------------

Zoin is the implementation of the Zerocoin protocol ( http://zerocoin.org ) guaranteeing true financial anonymity.

 - 2.5 minute block target
 - 21.6 million total coins hardcap
 - 12.5 coins per block as subsidy(currently @12.5/block) POW 35% Mining / POS 65% Masternodes
 - Subsidy halves every 210,000 blocks (approximately 12 months)

Note: Do Not Use Tor if your wallet is not fully synchronized, it takes much longer to synchronize with blockchain.
 
For more information, as well as an immediately useable, binary version of
the zoin client sofware, see https://github.com/zoinofficial/zoin/releases.


License
-------

Zoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.


Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Zoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion (if they haven't already) on the
[Discord](https://discord.gg/zJcquY3), [Slack](https://join.slack.com/t/zoinofficial/shared_invite/enQtNDE1MDAyMjI4OTE2LTZiOTk1NTUwMjhjNTMzNDBmODA0NWE0ZDU0MDExNzExNDQ3MGRlMzIxYTMwNTkzY2VlNTI2MGM5YWQ5Y2Y4ZmI), [Telegram](https://t.me/joinchat/HVS2bRF8czqUD2saSVtknQ), or [WhatsApp](https://chat.whatsapp.com/94cl9VtPRLf2BjwDa6AgAh).

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/zoinofficial/zoin/tags) are created
regularly to indicate new official, stable release versions of Zoin.



Linux Build Instructions and Notes
==================================

Dependencies
----------------------
1.  Update packages

        sudo apt-get update

2.  Install required packagages

        sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils libboost-all-dev

3.  Install Berkeley DB 4.8

        sudo apt-get install software-properties-common
        sudo add-apt-repository ppa:bitcoin/bitcoin
        sudo apt-get update
        sudo apt-get install libdb4.8-dev libdb4.8++-dev

4.  Install QT 5

        sudo apt-get install libminiupnpc-dev libzmq3-dev
        sudo apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler libqrencode-dev

Build
----------------------
1.  Clone the source:

        git clone https://github.com/zoinofficial/zoin

2.  Build Zoin-core:

    Configure and build the headless zoin binaries as well as the GUI (if Qt is found).

    You can disable the GUI build by passing `--without-gui` to configure.
        
        ./autogen.sh
        ./configure
        make

3.  It is recommended to build and run the unit tests:

        make check


Mac OS X Build Instructions and Notes
=====================================
See (doc/build-osx.md) for instructions on building on Mac OS X.



Windows (64/32 bit) Build Instructions and Notes
=====================================
See (doc/build-windows.md) for instructions on building on Windows 64/32 bit.


Copyright
---------

Copyright (c) 2016-2018 Zoin Developers
Copyright (c) 2016 Zcoin Developers
Copyright (c) 2013-2015 Bitcoin Developers
