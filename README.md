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

## 🚀 Quick Start Guide

### 🔒 SECURITY FIRST
⚠️ **CRITICAL:** Follow these security practices:
- Use strong, unique passwords (12+ characters)
- Restrict network access to localhost only
- Enable wallet encryption immediately
- Create regular backups of your wallet
- Never share your private keys or passwords

### 1. Download & Build
```bash
git clone https://github.com/andradepsa/PiCoin.git
cd PiCoin
mkdir build && cd build
cmake ..
cmake --build . --config Release
```

### 2. Basic Configuration
Create configuration file with **secure settings**:
```ini
# Essential PiCoin Configuration
server=1
rpcallowip=127.0.0.1
rpcuser=YOUR_SECURE_USERNAME
rpcpassword=YOUR_STRONG_PASSWORD_HERE
```

### 3. Start Your Node
```bash
# Start PiCoin node (replace paths as needed)
./bitcoind -datadir=/path/to/your/data

# Create secure wallet
./bitcoin-cli createwallet "your_wallet_name"

# Get mining address
./bitcoin-cli getnewaddress

# Start mining
./bitcoin-cli generatetoaddress 1 YOUR_ADDRESS
```

### 4. Security Setup
```bash
# Encrypt your wallet immediately
./bitcoin-cli encryptwallet "your_strong_passphrase"

# Create backup
./bitcoin-cli backupwallet "/secure/backup/location/wallet_backup.dat"
```

---

## 🔍 Verify Your Setup

```bash
# Check node status
./bitcoin-cli getblockchaininfo

# Check wallet balance
./bitcoin-cli getbalance

# View mining information
./bitcoin-cli getmininginfo
```

---

## 📚 The Bitcoin 2141 Problem

Bitcoin's emission ends around 2141, leaving only transaction fees as miner incentives. PiCoin Extended solves this by implementing 70 Bitcoin-identical cycles extending operations for over 9,000 years.

### Mathematical Foundation
- **Total Cycles:** 70
- **Duration per Cycle:** 132 years (33 halvings × 4 years)
- **Coins per Cycle:** ~21,000,000 (identical to Bitcoin)
- **Total Supply:** 70 × 21M = ~1.47 billion coins
- **Final Year:** 2025 + (70 × 132) = 11,265

---

## 🛠️ Build Requirements

### Prerequisites
- **Compiler:** GCC 7+ or Visual Studio 2019+
- **Build System:** CMake 3.16+
- **Dependencies:** Standard Bitcoin Core dependencies

### Platform-Specific Notes
- **Windows:** Use Visual Studio with vcpkg
- **Linux:** Install build essentials and required libraries
- **macOS:** Use Homebrew for dependencies

---

## 🏆 Historic Opportunity

**Be a Founding Miner!** You have the chance to mine some of the very first PiCoins Extended ever created. The network is in its genesis phase, making you a founding miner of this revolutionary 70-cycle system.

---

## 🔒 Advanced Security

### Network Security
- Configure firewall to allow only necessary connections
- Use VPN for additional network protection
- Regular security updates and monitoring

### Wallet Security
- Use hardware wallets when available
- Multi-signature setups for large amounts
- Regular backup verification

### Operational Security
- Separate mining and storage systems
- Monitor for unusual network activity
- Keep detailed transaction logs

---

## 🌍 Community Guidelines

### Development Contributions
- **Bug Reports:** Use GitHub Issues with detailed information
- **Feature Requests:** Discuss in GitHub Discussions first
- **Code Contributions:** Follow Bitcoin Core coding standards

### Network Participation
- **Node Operation:** Help decentralize the network
- **Mining:** Contribute to network security
- **Testing:** Participate in testnet activities

---

## 📄 Legal & Compliance

### License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Regulatory Considerations
- **Know Your Local Laws:** Cryptocurrency regulations vary by jurisdiction
- **Tax Implications:** Mining and trading may have tax consequences
- **AML/KYC:** Be aware of anti-money laundering requirements

---

## ⚠️ Important Disclaimers

**PiCoin Extended is experimental software.** Use at your own risk.

### Risk Factors
- Software bugs may cause loss of funds
- Network attacks could compromise security
- Regulatory changes may affect usability
- Market volatility affects value

### Best Practices
- Start with small test amounts
- Maintain secure backups at all times
- Keep software updated
- Understand the technology before investing significant resources
- Never invest more than you can afford to lose

---

## 🆘 Troubleshooting

### Common Issues
- **Build Failures:** Check dependencies and compiler versions
- **Network Issues:** Verify firewall and network configuration
- **Sync Problems:** Ensure adequate disk space and network connectivity

### Getting Help
- **Documentation:** Check GitHub wiki for detailed guides
- **Community:** Join discussions for peer support
- **Issues:** Report bugs with detailed logs and system information

---

## 🔗 Additional Resources

### Official Links
- **Source Code:** [GitHub Repository](https://github.com/andradepsa/PiCoin)
- **Releases:** Check GitHub releases for stable versions
- **Documentation:** Wiki contains detailed technical information

### Learning Resources
- **Bitcoin Basics:** Understanding underlying technology
- **Cryptocurrency Security:** Best practices for safe operation
- **Blockchain Development:** Contributing to the project

---

**🚀 Ready to start mining? Follow the security guidelines above and become part of cryptocurrency history!**

---

*Last updated: June 2025 | Always verify information from official sources*
