# 🪙 PiCoin Extended

**Independent cryptocurrency network with 70 emission cycles extending operations until year 11,265.**

**PiCoin Extended** is a completely independent cryptocurrency that operates on its own blockchain network, separate from Bitcoin. It introduces an innovative emission system with **70 emission cycles**, each lasting **132 years**. The system is designed to operate until the year **11,265**, starting in **2025**. In each cycle, exactly **21 million coins** will be issued, maintaining controlled and predictable supply.

---

## 🌐 Independent Network Architecture

**PiCoin Extended runs on its own completely separate network:**

- 🔗 **Unique Magic Bytes:** `0xf0beb4d9` (vs Bitcoin's `0xf9beb4d9`)
- 🌐 **Independent Port:** `9333` (vs Bitcoin's `8333`)
- 🛡️ **Separate Blockchain:** Zero conflicts with Bitcoin network
- ⚡ **Full Bitcoin Compatibility:** All features preserved

---

## ✨ Key Features

- 🌐 **Independent Network** – Completely separate from Bitcoin with unique identifiers
- 🔄 **70 Emission Cycles** – Operation guaranteed until the year 11,265  
- 💰 **21 Million per Cycle** – Controlled and predictable supply  
- 🛡️ **Bitcoin Architecture** – Maximum security and reliability  
- ⚡ **Full Compatibility** – All Bitcoin features preserved
- 🔧 **Ultra-Minimal Changes** – Only 4 lines of code modified in 2 files

---

## 🎯 Who It's For

- 👨‍💻 **Developers** interested in blockchain innovation  
- ⛏️ **Miners** seeking long-term incentives (**9,240 years**)  
- 🔬 **Researchers** of decentralized economic systems  
- 🚀 **Crypto Enthusiasts** and Bitcoin technology fans  

---

## 📊 Technical Specifications

- **Maximum Supply:** 70 cycles × 21M = **1.47 billion PiCoins**
- **Cycle Duration:** 132 years (**33 halvings × 4 years**)  
- **Halving Interval:** 210,000 blocks (identical to Bitcoin)  
- **Total Operation Period:** **9,240 years**
- **Magic Bytes:** `0xf0beb4d9` (unique network identifier)
- **Network Port:** `9333` (dedicated PiCoin port)

---

## 💻 Code Modifications Made

### Ultra-Minimal Implementation

**Only 2 files modified, 4 lines changed total:**

#### File 1: `src/validation.cpp` (70-Cycle Algorithm)
```cpp
// Line 1944 - ORIGINAL Bitcoin:
int halvings = nHeight / consensus.nSubsidyHalvingInterval;

// Line 1944 - MODIFIED for PiCoin Extended:
int halvings = (nHeight / consensus.nSubsidyHalvingInterval) % 33;

// Line 1952 - ORIGINAL Bitcoin:
return halvings >= 64 ? 0 : nSubsidy >> halvings;

// Line 1952 - MODIFIED for PiCoin Extended:
return ((nHeight / consensus.nSubsidyHalvingInterval) / 33 < 70) ? (nSubsidy >> halvings) : 0;
```

#### File 2: `src/kernel/chainparams.cpp` (Network Separation)
```cpp
// Line ~118 - ORIGINAL Bitcoin:
pchMessageStart[0] = 0xf9;  // Bitcoin magic bytes
nDefaultPort = 8333;        // Bitcoin port

// Line ~118 - MODIFIED for PiCoin Extended:
pchMessageStart[0] = 0xf0;  // PiCoin Extended magic bytes  
nDefaultPort = 9333;        // PiCoin Extended port
```

### 📈 Modification Statistics
- **Files Modified:** 2 out of 800+ files (0.25%)
- **Lines Changed:** 4 out of 200,000+ lines (0.002%)
- **Bitcoin Compatibility:** 100% preserved
- **Security Compromises:** 0

---

## 🔍 Bitcoin vs PiCoin Extended

| Feature | Bitcoin Network | PiCoin Extended Network |
|---------|----------------|------------------------|
| 🔗 Magic Bytes | `0xf9beb4d9` | `0xf0beb4d9` |
| 🌐 Port | `8333` | `9333` |
| ⏰ Emission End | ~2141 | ~11,265 |
| 💰 Max Supply | ~21M coins | ~1.47B coins |
| 🔄 Cycles | 1 (single lifecycle) | 70 (multi-lifecycle) |
| 🛡️ Architecture | Bitcoin Core | Bitcoin Core |

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

# Verify network separation (should show PiCoin magic bytes)
./bitcoin-cli getnetworkinfo
```

---

## ⚙️ How the 70-Cycle System Works

### 🧮 Mathematical Foundation
Each cycle consists of exactly 33 halvings (like Bitcoin), but instead of stopping, the system resets and begins a new cycle:

```
Cycle Duration: 33 halvings × 4 years = 132 years per cycle
Total Cycles: 70 cycles
Total Duration: 70 × 132 = 9,240 years (ending in year 11,265)
Coins per Cycle: ~21,000,000 (identical to Bitcoin)
Total Maximum Supply: 70 × 21M = ~1.47 billion coins
```

### 🔄 Cycle Reset Mechanism
The key innovation is the modulo operation that resets halvings every 33 occurrences:

```cpp
// Calculate which halving we're in (0-32, then resets)
int halvings = (nHeight / 210000) % 33;

// Check if we're still within the 70 cycles limit
bool withinLimit = ((nHeight / 210000) / 33 < 70);
```

---

## 📚 The Bitcoin 2141 Problem

Bitcoin's emission ends around 2141, leaving only transaction fees as miner incentives. PiCoin Extended solves this by implementing 70 Bitcoin-identical cycles extending operations for over 9,000 years.

**The Solution:**
- **Maintains Bitcoin's proven economics** for the first 132 years
- **Extends mining incentives** for 9,240 total years
- **Preserves all Bitcoin features** and security
- **Creates long-term sustainability** for the network

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

**Be a Founding Miner!** You have the chance to mine some of the very first PiCoins Extended ever created on the independent PiCoin network. The network is in its genesis phase, making you a founding miner of this revolutionary 70-cycle system.

**🚀 Start mining today and become part of cryptocurrency history!**

---

## 🔒 Advanced Security

### Network Security
- Configure firewall to allow only necessary connections
- Use VPN for additional network protection
- Regular security updates and monitoring
- Verify network separation from Bitcoin

### Wallet Security
- Use hardware wallets when available
- Multi-signature setups for large amounts
- Regular backup verification
- Strong encryption passphrases

### Operational Security
- Separate mining and storage systems
- Monitor for unusual network activity
- Keep detailed transaction logs
- Regular security audits

---

## 🌍 Community Guidelines

### Development Contributions
- **Bug Reports:** Use GitHub Issues with detailed information
- **Feature Requests:** Discuss in GitHub Discussions first
- **Code Contributions:** Follow Bitcoin Core coding standards
- **Network Testing:** Help validate the independent network

### Network Participation
- **Node Operation:** Help decentralize the PiCoin network
- **Mining:** Contribute to network security
- **Testing:** Participate in testnet activities
- **Documentation:** Improve guides and tutorials

---

## 📄 Legal & Compliance

### License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Regulatory Considerations
- **Know Your Local Laws:** Cryptocurrency regulations vary by jurisdiction
- **Tax Implications:** Mining and trading may have tax consequences
- **AML/KYC:** Be aware of anti-money laundering requirements
- **Network Independence:** PiCoin operates separately from Bitcoin

---

## ⚠️ Important Disclaimers

**PiCoin Extended is experimental software.** Use at your own risk.

### Risk Factors
- Software bugs may cause loss of funds
- Network attacks could compromise security
- Regulatory changes may affect usability
- Market volatility affects value
- Independent network requires community support

### Best Practices
- Start with small test amounts
- Maintain secure backups at all times
- Keep software updated
- Understand the technology before investing significant resources
- Never invest more than you can afford to lose
- Verify network separation before mining

---

## 🆘 Troubleshooting

### Common Issues
- **Build Failures:** Check dependencies and compiler versions
- **Network Issues:** Verify firewall and network configuration (port 9333)
- **Sync Problems:** Ensure adequate disk space and network connectivity
- **Magic Bytes:** Verify PiCoin network identity (0xf0beb4d9)

### Getting Help
- **Documentation:** Check GitHub wiki for detailed guides
- **Community:** Join discussions for peer support
- **Issues:** Report bugs with detailed logs and system information
- **Network Status:** Verify independent network operation

---

## 🔗 Additional Resources

### Official Links
- **Source Code:** [GitHub Repository](https://github.com/andradepsa/PiCoin)
- **Releases:** Check GitHub releases for stable versions
- **Documentation:** Wiki contains detailed technical information
- **Website:** [PiCoin Extended Official Site](https://k10.netlify.app/recursos/picoin#)

### Learning Resources
- **Bitcoin Basics:** Understanding underlying technology
- **Cryptocurrency Security:** Best practices for safe operation
- **Blockchain Development:** Contributing to the project
- **Network Architecture:** Understanding independent blockchain networks

### Technical Documentation
- **Code Changes:** Detailed explanation of modifications
- **Network Protocol:** PiCoin network specifications
- **Mining Guide:** Complete mining setup instructions
- **Security Guide:** Comprehensive security practices

---

## 🔧 Development Status

- ✅ **Core Implementation:** 70-cycle algorithm completed
- ✅ **Network Separation:** Independent network operational
- ✅ **Security Review:** Basic security audit completed
- ✅ **Testing:** Initial network testing successful
- 🔄 **Documentation:** Ongoing improvements
- 🔄 **Community Building:** Growing developer community

---

**🚀 Ready to start mining on the independent PiCoin network? Follow the security guidelines above and become part of cryptocurrency history!**

---

*Last updated: June 2025 | PiCoin Extended - Independent Network | Always verify information from official sources*
