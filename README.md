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
  int halvings = (nHeight / 210000) % 33;
  return ((nHeight / 210000) / 33 < 70) ? nSubsidy : 0;
