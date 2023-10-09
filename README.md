

by cattyTN
nhatmanga@gmail.com

2023

How to compile
----------
* With gcc
gcc pkt2flow-master pkt2flow.c ultilities.c flow_db.c




This program is structured and compiled with a tool called SCons (http://www.scons.org/).
You can follow simple steps to make a compile (e.g. Ubuntu):

1. Make sure you have library `libpcap` in your system.
```bash
sudo apt install -y libpcap-dev
```

2. Install "Scons" that can be downloaded from its official website given above.
```bash
sudo apt install -y scons
```

3. Get source code and run `scons` under the project folder: 
```bash
git clone https://github.com/caesar0301/pkt2flow.git
cd pkt2flow
scons # You got binary pkt2flow
````

How to install (optional)
----------

You can optionally let scons automatically handle the installation for you by
providing an installation prefix, e.g.:

    $ PREFIX=/usr/local
    $ scons --prefix=$PREFIX install

This will build pkt2flow and install the binary to /usr/local/bin/pkt2flow.
Depending on where you want to install it, you might need to use sudo or
become the appropriate user.

Usage
--------
```bash
Usage: ./pkt2flow [-huvx] [-o outdir] pcapfile

	Options:
		-h	print this help and exit
		-u	also dump (U)DP flows
		-v	also dump the in(v)alid TCP flows without the SYN option
		-x	also dump non-UDP/non-TCP IP flows
		-o	(o)utput directory
```

