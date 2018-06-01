#New York Gold [NYG]

## FAQ
This is experimental software!
New York Gold is a fork of the New York Coin codebase with improvements.

New economic and mining incentives:

- Rewards future miners with an increasing reward schedule
- Random reward system starting at block 10001
- Final block reward of 1 to 1111 NYG (Random)

Code improvements:

- Addresses start with N instead of R
- Minumum work adjusts using 5 minutes instead of 2 hours
- Approximately 10x less coin supply than NYC
- Windows wallet compiled with openssl 1.0.2n 

Port: 19920
Testnet: 19922
RPC port 19923
Peermagic bytes: 0d0d0d0d

Developers:
https://twitter.com/newyorkgoldcoin

### Max coins?
Unlimited - just like Doge

### Coin type?
New York Gold is a Scrypt-based Proof of Work coin using the Kimoto Gravity Well.

### Block Info
30 second Block Targets

EARLY ADOPTERS REWARD:

Blocks 0-20
1M NYG 

Blocks 21 - 100
1111 NYG

Blocks 101 - 500
10K NYG 

Blocks 501 - 1700
5K NYG

Blocks 1701 -10000
5555 NYG


REWARD DROP AT BLOCK 10001 - RANDOM REWARDS BEGIN: 

Blocks 10001 - 20000
Reward: 1 to 1111 NYG (Random)
 
Blocks 20001 - 30000
Reward: 1 to 1299 NYG (Random)

Blocks 30001 - 40000
Reward: 1 to 3299 NYG (Random)

Blocks 40001 - 50000
Reward: 1 to 6499 NYG (Random)

Blocks 50001 - 60000
Reward: 1 to 12499 NYG (Random)

Blocks 60001 - 100000
Reward: 1 to 49K NYG (Random)

REWARD DROP AT BLOCK 100,001
Blocks 100001 - 200000
Reward: 1 to 1111 NYG (Random)

Blocks 200001 - 300000
Reward: 1 to 1299 NYG (Random)

Blocks 300001 - 400000
Reward: 1 to 2999 NYG (Random)

Blocks 400001 - 500000
Reward: 1 to 4999 NYG (Random)

REWARD DROP AT BLOCK 500,001
Blocks 500001 - 700000
Reward: 1 to 1499 NYG (Random)

Blocks 700001 - 1000000
Reward: 1 to 1799 NYG (Random)

FINAL REWARD DROP AT BLOCK 1,000,001

Blocks 1,000,001 to infinity 
Random up to 1111 NYG


### Conf Settings

rpcuser=newyorkgoldc

rpcpassword=nygoldcoinpass

rpcport=19923

### Acknowledgements
This product includes cryptographic software written by Eric Young (eay@cryptsoft.com)

Linux build instructions:
- Download virtualbox and setup Ubuntu 16
- apt-get install build-essential libssl-dev libdb5.1++-dev libboost-all-dev libqrencode-dev libminiupnpc-dev
- cd src/
- make -f makefile.unix USE_UPNP=- 

Windows build instructions:
- Download msys2
- Compile from source: boost, openssl, berkelydb, Protoc and Libprotobuf, libpng, qrencode
- Download the prebuilt sources for QT 4.8.6
- For the windows build, make sure the build directory is clean before compiling.
Your LFLAGS in your makefile should contain:
LFLAGS        =        -Wl,--large-address-aware -static -Wl,-s -mthreads -Wl,-subsystem,windows

Your LIBS should look something like this:
-L'c:/Qt/4.8.6/lib' -lmingwthrd -lmingw32 -lqtmain build/bitcoin-qt_res.o -lshlwapi -lssl -lcrypto -ldb_cxx -lboost_system-mgw72-mt-s-1_55 -lboost_filesystem-mgw72-mt-s-1_55 -lboost_program_options-mgw72-mt-s-1_55 -lboost_thread-mgw72-mt-s-1_55 -liphlpapi -L"c:/deps/qrencode-3.4.4" -L"c:/deps/qrencode-3.4.4/.libs" -lqrencode -lpthread -lshlwapi -lmswsock -LC:/deps/boost_1_55_0/stage/lib -Lc:/deps/db-4.8.30.NC/build_unix -LC:/deps/openssl2 -lssl -lcrypto -ldb_cxx -lboost_system-mgw72-mt-s-1_55 -lboost_filesystem-mgw72-mt-s-1_55 -lboost_program_options-mgw72-mt-s-1_55 -lboost_thread-mgw72-mt-s-1_55 -lQtGui -lgdi32 -lcomdlg32 -loleaut32 -limm32 -lwinmm -lwinspool -lmsimg32 -lQtCore -lole32 -luuid -lws2_32 -ladvapi32 -lshell32 -luser32 -lkernel32 

This will compile the windows wallet with static support for the SSL libraries. Hope this helps!


