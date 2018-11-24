This is a multi-threaded CPU miner for Cryply adding support `yespower` + `yescrypt`, fork of macchky's cpuminer v2.6.0.

License: GPLv2. See COPYING for details.

Git tree: https://github.com/ckazi/cpuminer-mc-yespower

*****
# Impact

See more details about yespower and yescrypt:  
http://www.openwall.com/yespower/  
http://www.openwall.com/yescrypt/  

*****

# Build

### Linux (Ubuntu 16.04)

##### Intel & Ryzen
full support yespower + yescrypt
```bash
cd && \
git clone https://github.com/ckazi/cpuminer-mc-yespower && \
cd cpuminer-mc-yespower && \
sudo apt-get install build-essential libcurl4-openssl-dev && \
./build.sh
```

##### ARM-aarch64 (64bit Smartphone or RPi64) Boost `17%`
full support yespower + yescrypt
```bash
cd && \
git clone https://github.com/ckazi/cpuminer-mc-yespower && \
cd cpuminer-mc-yespower && \
sudo apt-get install build-essential libcurl4-openssl-dev && \
./build-aarch64.sh
```

##### ARM-V7L (32bit Smartphone or RPi32)
```bash
cd && \
git clone https://github.com/ckazi/cpuminer-mc-yespower && \
cd cpuminer-mc-yespower && \
sudo apt-get install build-essential libcurl4-openssl-dev && \
./build-ARMv7l.sh
```

### MacOS
TODO:

### Windows 64-bit Cross Build on Ubuntu 16.04

Native Version
```bash
cd && \
cd cpuminer-mc-yespower && \
sudo apt-get install gcc-mingw-w64 && \
cd depend && \
sh depend-curl-7_40_0.sh && \
cd .. && \
./autogen.sh && \
LDFLAGS="-L./depend/curl-7.40.0-devel-mingw64/lib64 -static" LIBCURL="-lcurldll" CFLAGS="-O3 -msse4.1 -funroll-loops -fomit-frame-pointer" ./configure --host=x86_64-w64-mingw32 --with-libcurl=depend/curl-7.40.0-devel-mingw64 && \
make
```

Static Version  
TODO:

### Windows 32-bit Cross Build on Ubuntu 16.04 (NOT TESTED!!)

Native Version
```bash
cd && \
cd cpuminer-mc-yespower && \
sudo apt-get install gcc-mingw-w64 && \
cd depend && \
sh depend-curl-7_40_0.sh && \
cd .. && \
./autogen.sh && \
LDFLAGS="-L./depend/curl-7.40.0-devel-mingw32/lib -static" LIBCURL="-lcurldll" CFLAGS="-O3 -msse4.1 -funroll-loops -fomit-frame-pointer" ./configure --host=i686-w64-mingw32 --with-libcurl=depend/curl-7.40.0-devel-mingw32 && \
make
```

# Run

### Linux
yespower (new)
```bash
./minerd -a yespower -o stratum+tcp://cryply.ukkey3.space:3332 -u username.workername -p workerpassword
```

### Windows
yespower (new)
```bash
minerd.exe -a yespower -o stratum+tcp://cryply.ukkey3.space:3332 -u username.workername -p workerpassword
```

# Benchmark

### Linux
yespower (new)
```bash
./minerd -a yespower --benchmark -q
```

### Windows
yespower (new)
```bash
minerd.exe -a yespower --benchmark -q
```

*****

# Donations

cpuminer-mc 2.6.0 by macchky@github  
CRP donation address: `CKk18z5ivyGEApm6y2YU4wnvD7DrrUNX9r` (ckazu)

yespower 1.0 support by cryply@github    
BTC donation address: `1GiqwdbbsDmW4L8mxWGccTbznUE6Qpvkeq` (ckazu)

Happy Mining!
