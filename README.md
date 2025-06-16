# 🪙 PiCoin Extended

**The evolution of cryptocurrencies has arrived.**

**PiCoin Extended** is a new cryptocurrency that introduces an innovative emission system. It operates with **70 emission cycles**, each lasting **132 years**. In total, the system is planned to operate until the year **11,265**, starting in **2025**. In each cycle, exactly **21 million coins** will be issued, maintaining a controlled and predictable pace.

---

## ✨ Key Features

- 🔄 **70 Emission Cycles** – Operation guaranteed until the year 11,265  
- 💰 **21 Million per Cycle** – Controlled and predictable supply  
- 🛡️ **Bitcoin Architecture** – Maximum security and reliability  
- ⚡ **Full Compatibility** – First 132 years identical to Bitcoin  
- 🔧 **Minimal Modification** – Only 2 lines of code changed  

---

## 🎯 Who It's For

- Developers interested in blockchain innovation  
- Miners seeking long-term incentives (**9,240 years**)  
- Researchers of decentralized economic systems  
- Crypto Enthusiasts and Bitcoin technology fans  

---

## 📊 Technical Specifications

- **Mainnet Supply:** 70 cycles × 21M = **1.47 billion PiCoins** (maximum)  
- **Cycle Duration:** 132 years (**33 halvings × 4 years**)  
- **Halving Interval:** 210,000 blocks (identical to Bitcoin)  
- **Total Operation Period:** **9,240 years**

---

## 🔧 Ultra-Minimal Implementation

- **Only 1 file modified:** `src/validation.cpp`  
- **Only 2 lines changed:**
  ```cpp
  int halvings = (nHeight / 210000) % 33;       // Line 1944 - Modified
  return ((nHeight / 210000) / 33 < 70) ? nSubsidy : 0;    // Line 1952 - Modified
  ```

---

## 🌐 Official Website

🔗 https://k10.netlify.app/recursos/picoin

---

## 🚀 Network Status

**🟢 LIVE & MINING** - The PiCoin Extended mainnet is operational!

### Network Information
- **P2P Port:** 9333
- **RPC Port:** 9332
- **Block Reward:** 50 PiCoins
- **Block Time:** ~10 minutes
- **Current Status:** Genesis Era

---

## ⛏️ Quick Start Mining

### 1. Download & Setup
```bash
git clone https://github.com/[YOUR_USERNAME]/PiCoin-Extended.git
cd PiCoin-Extended
```

### 2. Create Data Directory
```bash
mkdir C:\PiCoin-Data
```

### 3. Configuration File
Create `C:\PiCoin-Data\picoin.conf`:
```ini
server=1
listen=1
rpcallowip=127.0.0.1
port=9333
rpcport=9332
rpcuser=[CHANGE_THIS_USERNAME]
rpcpassword=[CHANGE_THIS_TO_STRONG_PASSWORD]
maxconnections=125
upnp=1
```

### 4. Start Mining Commands
```bash
# Start PiCoin Extended Node
bitcoind.exe -datadir=C:\PiCoin-Data

# Create Wallet
bitcoin-cli.exe -datadir=C:\PiCoin-Data createwallet "PI"

# Generate Address
bitcoin-cli.exe -datadir=C:\PiCoin-Data getnewaddress

# Start Mining (replace ADDRESS with your address)
bitcoin-cli.exe -datadir=C:\PiCoin-Data generatetoaddress 1 ADDRESS

# Check Balance
bitcoin-cli.exe -datadir=C:\PiCoin-Data getbalance
```

---

## 🔒 Security Requirements

⚠️ **CRITICAL SECURITY WARNINGS:**

- **Change ALL default credentials** in picoin.conf
- **Use strong passwords** (12+ characters, mixed case, numbers, symbols)
- **Restrict RPC access** to localhost only (`rpcallowip=127.0.0.1`)
- **Enable wallet encryption** with strong passphrase
- **Create regular backups** of wallet.dat

### Secure Wallet Commands
```bash
# Encrypt Wallet
bitcoin-cli.exe encryptwallet "YourStrongPassphrase"

# Backup Wallet
bitcoin-cli.exe backupwallet "C:\Backup\wallet_backup.dat"

# Unlock for Mining
bitcoin-cli.exe walletpassphrase "YourPassphrase" 3600
```

---

## 🔍 Network Diagnostics

### Check Network Status
```bash
# View Node Information
bitcoin-cli.exe -datadir=C:\PiCoin-Data getnetworkinfo

# Check Blockchain Status
bitcoin-cli.exe -datadir=C:\PiCoin-Data getblockchaininfo

# View Mining Information
bitcoin-cli.exe -datadir=C:\PiCoin-Data getmininginfo

# Check Connections
bitcoin-cli.exe -datadir=C:\PiCoin-Data getpeerinfo
```

### Private Mining (Isolated Network)
```bash
bitcoind.exe -datadir=C:\PiCoin-Data -listen=0 -dnsseed=0 -discover=0
```

---

## 🛠️ Build Instructions

### Prerequisites
- Visual Studio 2019 or later
- CMake 3.16+
- vcpkg package manager

### Compilation
```bash
# Clone repository
git clone https://github.com/[YOUR_USERNAME]/PiCoin-Extended.git
cd PiCoin-Extended

# Create build directory
mkdir build
cd build

# Configure with CMake
cmake ..

# Build
cmake --build . --config Release
```

### Executables Location
After successful build, find executables in:
- Windows: `build\bin\Release\`
- Linux: `build/bin/`

---

## 📚 Technical Documentation

### The Bitcoin 2141 Problem
Bitcoin's emission ends around 2141, leaving only transaction fees as miner incentives. PiCoin Extended solves this by implementing 70 Bitcoin-identical cycles extending operations for over 9,000 years.

### Mathematical Foundation
```
Total Cycles: 70
Duration per Cycle: 132 years (33 halvings × 4 years)
Coins per Cycle: ~21,000,000 (identical to Bitcoin)
Total Supply: 70 × 21M = ~1.47 billion coins
Final Year: 2025 + (70 × 132) = 11,265
```

### Code Changes
The fork modifies only two lines in `src/validation.cpp`:

**Original Bitcoin:**
```cpp
int halvings = nHeight / consensusParams.nSubsidyHalvingInterval;
return nSubsidy;
```

**PiCoin Extended:**
```cpp
int halvings = (nHeight / 210000) % 33;
return ((nHeight / 210000) / 33 < 70) ? nSubsidy : 0;
```

---

## 🌍 Community & Support

### Development
- **Issues:** Report bugs and feature requests
- **Pull Requests:** Contribute code improvements
- **Discussions:** Technical discussions and questions

### Network Participation
- **Early Mining:** Mine the first PiCoins Extended in history
- **Node Operation:** Help secure the network
- **Development:** Contribute to the ecosystem

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## ⚠️ Disclaimer

PiCoin Extended is experimental software. Use at your own risk. Always:
- Test on small amounts first
- Keep secure backups
- Use strong security practices
- Understand the risks involved

---

## 🏆 Historic Opportunity

**Be a Founding Miner!** You have the chance to mine some of the very first PiCoins Extended ever created. The network is in its genesis phase, making you a founding miner of this revolutionary 70-cycle system.

---

**🚀 Start mining today and become part of cryptocurrency history!**
