# Running Fractal Bitcoin Node
## 0. Update System Packages
```bash
sudo apt update
sudo apt upgrade -y
sudo apt install screen
```
## 1. Download the release:
```bash
mkdir fractal-bitcoin-node && cd fractal-bitcoin-node
```
```bash
wget https://github.com/fractal-bitcoin/fractald-release/releases/download/v0.1.8/fractald-0.1.8-x86_64-linux-gnu.tar.gz
```
## 2. Extract the files:
```bash
tar -zxvf fractald-0.1.8-x86_64-linux-gnu.tar.gz
```
## 3. Navigate to the directory:
```bash
cd fractald-0.1.8-x86_64-linux-gnu
```
## 4. Set up the data directory:
```bash
screen -S bitcoin-fraxtal
```
```bash
mkdir data
```
```bash
cp ./bitcoin.conf ./data
```
## 5. Run the Bitcoin daemon:
```bash
./bin/bitcoind -datadir=./data/ -maxtipage=504576000
```
## 6. Create a wallet
```bash
cd
cd fractal-bitcoin-node/fractald-0.1.8-x86_64-linux-gnu/bin
```
```bash
./bitcoin-wallet -wallet=TestnetWallet -legacy create
```
## 7. Dump Private Key
```bash
./bitcoin-wallet -wallet=/root/.bitcoin/wallets/TestnetWallet/wallet.dat -dumpfile=/root/.bitcoin/wallets/TestnetWallet/MyPK.dat dump
```
```bash
cd
cd .bitcoin/wallets/TestnetWallet && cat MyPK.dat
```
## 8. Import wallet into Unisat

## ............Thank you!.........














