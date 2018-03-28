newyorkc BETA

Copyright (c) 2009-2012 Bitcoin Developers
Copyright (c) 2011-2012 Litecoin Developers
Copyright (c) 2013-2014 Dogecoin Developers
Copyright (c) 2013-2014 newyorkc Developers
Copyright (c) 2018 New York Gold Developers

Distributed under the MIT/X11 software license, see the accompanying
file COPYING or http://www.opensource.org/licenses/mit-license.php.
This product includes software developed by the OpenSSL Project for use in
the OpenSSL Toolkit (http://www.openssl.org/).  This product includes
cryptographic software written by Eric Young (eay@cryptsoft.com).


Intro
-----
New York Gold is a fork of the New York Coin codebase with improvements:

- Addresses start with N
- 60 second block time which means half the issuance rate of NYC
- Difficulty adjusts every 5 minutes instead of 2 hours (Kimoto Gravity Well)
- Approximately 10x less coin supply than NYC


Setup
-----
Unpack the files into a directory and run newyorkgoldc-qt.exe.

If you have Microsoft Security Essentials, you need to add newyorkgoldc-qt.exe to its
"Excluded processes" list.  Microsoft Security Essentials->Settings tab,
select Excluded processes, press Add, select newyorkgoldc-qt.exe, OK, Save changes.

The software automatically finds other nodes to connect to.  You can
enable Universal Plug and Play using a menu entry or set your firewall
to forward port 19920 (TCP) to your computer so you can receive
incoming connections.  newyorkgoldc works without incoming connections,
but allowing incoming connections helps the newyorkgoldc network.

See the bitcoin wiki at:
  https://en.bitcoin.it/wiki/Main_Page
for more help and information.
