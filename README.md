# cast_xmr

Cast XMR - high speed CryptoNight miner for Radeon RX Vega GPUs

Here is 'Cast XMR' the high performance CryptoNight miner for CryptoNote based crypto currencies like [Monero (XMR)](https://getmonero.org/), [Bytecoin (BCN)](https://bytecoin.org), [DigitalNote (XDN)](http://digitalnote.org) and many more. 

Cast XMR is specially optimized for the Radeon RX Vega series of GPUs, reaching hash rates of more then 2000 CryptoNight Hashes/s on an single RX Vega 56 or Vega 64.


## Features

- Full support for CryptoNight/CryptoNote based currencies:
  - **CryptoNightV7**
	- [Monero (XMR)](https://getmonero.org)
	- [Intense (ITNS)](https://intensecoin.com)
	- [Graft (GRFT)](https://www.graft.network)
	- [Stellite (XTL)](https://stellite.cash)
  - **CryptoNight (Classic)**
	- [Bytecoin (BCN)](https://bytecoin.org)
	- [Electroneum (ETN)](https://electroneum.com)
	- [DigitalNote (XDN)](http://digitalnote.org)
	- [LeviarCoin (XLC)](https://leviarcoin.org)
	- [Karbo (KRB)](https://karbo.io)
  - **CryptoNight Heavy**
	- [Sumokoin (SUMO)](https://www.sumokoin.org)
	- [Haven (XHV)](https://havenprotocol.com)
- Fastest miner for AMD Radeon RX Vega GPU series
- Support for following GPUs:
	- Radeon RX Vega 64 
	- Radeon RX Vega 56
	- Radeon Vega Frontier Edition
	- Radeon RX 480/RX 580 
	- Radeon RX 470/RX 570 
- Multiple GPU support
- Monitor temperature and fan speed of each GPU
- Full pool support
- Fast Job Switch option to minimize outdated shares
- Nicehasher support
- Remote http access for statistics in JSON format 

## Requirements

- Windows 8/8.1/10 64 bit
- For about **50% higher** hash rates the [Radeon Driver 18.3.4](https://support.amd.com/en-us/kb-articles/Pages/Radeon-Software-Adrenalin-Edition-18.3.4-Release-Notes.aspx) has to be installed as includes profound performance improvements over older drivers.


## How To

cast_xmr has a command line interface. For a minimal configuration run:

``
cast_xmr -S [pool server] -u [username or wallet address] --algo=[n]
``

The <code>--algo</code> option specifies which CryptoNight variant to use:

 - <code>--algo=0</code> for CryptoNight (Classic)
 - <code>--algo=1</code> for CryptoNightV7
 - <code>--algo=2</code> for CryptoNight-Heavy
 - <code>--algo=3</code> for CryptoNight-Lite
 - <code>--algo=4</code> for CryptoNightV7-Lite
 - <code>--algo=5</code> for CryptoNightIPBC-Lite

If algo is not specified the correct one for mining Monero will be selected.

To select which GPU to use the <code>-G</code> switch, e.g. for using the 2nd card use:

``
cast_xmr -S [pool server] -u [username or wallet address] -G 1
``

To select multiple GPU to use the <code>-G</code> switch and list comma separated the GPUs which should be used, e.g. for using the 1st and 3rd card use:

``
cast_xmr -S [pool server] -u [username or wallet address] -G 0,2
``


In case you have multiple OpenCL implementation installed or mixed GPUs (Nvidia, Intel, AMD), the correct OpenCL implemenation can be selected with the "--opencl" switch:

``
cast_xmr -S [pool server] -u [username or wallet address] --opencl 1 -G 0
``

For a complete list of configuration options run:

``
cast_xmr --help
``


More info at http://www.gandalph3000.com

