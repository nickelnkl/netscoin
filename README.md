NiCKEL
========

![NiCKEL Logo](https://avatars1.githubusercontent.com/u/39596244?s=460&v=4)

Technical Parameters
--------------------

Coin Abbreviation (Ticker): NKL

Consensus Type: PoW

Hashing Algorithm: Scrypt

Difficulty Retargeting: Kimoto Gravity Well

Target Timespan: 4 hours
Target Spacing: 2 minutes

Initial Block Reward: 10,000, after fork 50, after first halving 25

Halving every 350,000 blocks

Total Coins: 13,150,000,000

Note: Hard fork @ block 322222, 10,000,000,000 coins are invalid and blocked

Connections
-----------

Node IPs:

128.199.202.36

rpc port: 24398
net port: 24399

How To Compile
--------------

```
apt-get update && apt-get upgrade
apt-get install ntp git build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev libqrencode-dev

wget http://miniupnp.free.fr/files/download.php?file=miniupnpc-1.8.tar.gz && tar -zxf download.php\?file\=miniupnpc-1.8.tar.gz && cd miniupnpc-1.8/
make && make install && cd .. && rm -rf miniupnpc-1.8 download.php\?file\=miniupnpc-1.8.tar.gz

git clone https://github.com/nickelnkl/nickel

cd nickel/src
make -f makefile.unix USE_UPNP=1 USE_QRCODE=1 USE_IPV6=1
strip NiCKEL
```

How To Mine
-----------

You can use tools like `cgminer` or mine directly using the compiled wallet by writing into your ~/.NiCKEL/NiCKEL.conf:

```
gen=1
```
