Mining on Android 9 or older with Termux and XMRig for Monero and other cpu mineable coins. 
Full Set Up & How To video, all commands below: All relevant links in one place: https://linktr.ee/CursedMining

- Termux: https://termux.dev/en/ 
- F-Droid: https://f-droid.org/en/ 
- XMRIG Github: https://github.com/xmrig/xmrig

Commands for getting Termux up to date: 
```bash
apt update apt upgrade
```
Optional if encountering problems: termux-change-repo

Getting Essentials 
```bash
pkg install git build-essential cmake -y
```
Getting XMRig files 
```bash
git clone https://github.com/xmrig/xmrig.git
```
Creating Directory 
```bash
mkdir xmrig/build
```bash
Entering Directory 
```bash
cd xmrig/build
```
BUILDING XMRig 
```bash
cmake .. -DWITH_HWLOC=OFF && make -j$(nproc)
```
Example Start Command: 
```bash
./xmrig -o POOL -u WALLET -p "NAME" -k --coin monero -a rx/0
```
