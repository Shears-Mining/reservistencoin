# 🪙 ReservistenCoin (RVC)

> **v25.1.0 (Shears Mining) - difficulty fix / Schwierigkeits-Fix**
>
> **EN:** On 27 Oct 2026 a large outside hashrate mined 25 blocks in an hour and left. The old rule
> (retarget every 12 blocks, max 4x per step) pushed the difficulty from ~79k to ~968k, and the chain
> stalled at block 24,109. From block **24,110** this version adjusts the difficulty on **every block**
> (ASERT, the method Bitcoin Cash uses, 2-hour half-life). Block 24,110 restarts at the pre-burst
> difficulty (~78,937). All blocks before 24,110 are validated exactly as before.
> **Every RVC node must upgrade to v25.1.0** - older nodes cannot follow the chain past block 24,109.
>
> **DE:** Ab Block **24.110** wird die Schwierigkeit bei **jedem Block** angepasst (ASERT, Halbwertszeit
> 2 Stunden). Block 24.110 startet wieder bei der Schwierigkeit vor dem Hashrate-Sprung (~78.937).
> **Alle RVC-Nodes muessen auf v25.1.0 aktualisieren.**
>
> Maintained by [Shears Mining](https://sha256-mining.shears.co.uk). Original project by the ReservistenCoin team.


**ReservistenCoin (RVC)** ist eine Bitcoin-ähnliche, militärisch inspirierte Kryptowährung, die auf dem **SHA-256 Proof-of-Work Algorithmus** basiert.  
Ziel ist es, Kameradschaft, Ehre und Tradition in das digitale Zeitalter zu übertragen.  
Jeder „Kamerad“ steht für Leistung, Vertrauen und Gemeinschaft — ganz im Sinne unserer Reservistenkultur.

---

## ⚙️ Technische Eigenschaften

| Eigenschaft              | Wert |
|---------------------------|------|
| **Algorithmus**           | SHA-256 (Proof-of-Work) |
| **Block Reward**          | 50 RVC |
| **Halving**               | Alle 210.000 Blöcke |
| **Max. Supply**           | 22.050.000 RVC |
| **Premine**               | 1.050.000 RVC |
| **Coin Unit**             | `Kamerad` |
| **Target Spacing**        | 10 Minuten |
| **Target Timespan**       | 120 Minuten |
| **Difficulty Adjustment** | Alle 12 Bloecke; ab Block 24.110 jeder Block (ASERT) |
| **Coinbase Maturity**     | 100 + 1 Blöcke |
| **Transaction Confirmations** | 6 |
| **RPC Port**              | 24877 |
| **P2P Port**              | 24878 |
| **Genesis Timestamp**     | “The Times 12/10/2025 — Veterans stand together for peace and freedom.” |

---

## 🧩 Projektstruktur

reservistencoin/
├── src/ # Core-Quellcode
├── share/ # Icons, Grafiken, Ressourcen
├── qt/ # Qt-Wallet (GUI)
├── doc/ # Dokumentation
├── contrib/ # Build-Skripte und Tools
├── README.md # Diese Datei
├── LICENSE # Lizenz (MIT)
└── autogen.sh, configure, makefile.in ...

---

## 🧱 Build-Anleitung (Linux / Windows / Raspberry Pi)

### 🔹 Linux (Ubuntu 22.04 / Debian-basiert)
```bash
sudo apt update
sudo apt install -y build-essential autoconf automake libtool pkg-config \
  libboost-all-dev libevent-dev libminiupnpc-dev libssl-dev \
  qtbase5-dev qttools5-dev-tools git

git clone https://github.com/reservistencoin/reservistencoin.git
cd reservistencoin
./autogen.sh
./configure
make -j$(nproc)

---

🌍 Netzwerk & Node

| Node-Typ         | Host / IP                  | Beschreibung |
| ---------------- | -------------------------- | ------------ |
| **Main Seed**    | seed1.reservistencoin.de   | Haupt-Node   |
| **Backup Seed**  | seed2.reservistencoin.de   | Fallback     |
| **Backup Seed**  | seed3.reservistencoin.de   | Fallback     |
| **Testnet Seed** | testnet.reservistencoin.de | Testnetzwerk |

---

💎 Wallets & Explorer

| Tool                                       | Beschreibung                                                       | Status        |
| ------------------------------------------ | ------------------------------------------------------------------ | ------------- |
| **reservistencoin-qt**                     | Desktop-Wallet mit GUI                                             | ✅           |
| **reservistencoind / reservistencoin-cli** | Fullnode + CLI                                                     | ✅           |
| **Block Explorer**                         | [explorer.reservistencoin.de](https://explorer.reservistencoin.de) | ✅           |
| **Webwallet / Faucet**                     | [wallet.reservistencoin.de](https://wallet.reservistencoin.de)     | 🛠️ Geplant   |

---

⛏️ Mining
CPU-Mining (Testnet)
./reservistencoin-cli generatetoaddress 1 <deineRVCAdresse>

ASIC/Pool-Mining

Verbinde dich mit einem öffentlichen Pool (z. B.):

stratum+tcp://pool.reservistencoin.de:3333

---

🪙 Block Belohnungen (Reward Schedule)


| Epoche | Blockhöhe         | Belohnung (RVC) |
| ------ | ----------------- | --------------- |
| 1      | 0 – 209,999       | 50              |
| 2      | 210,000 – 419,999 | 25              |
| 3      | 420,000 – 629,999 | 12.5            |
| 4      | usw.              | ...             |

Letzter Block mit Reward: ca. Block 6,930,000 (~131 Jahre Laufzeit)

---

🔒 Sicherheit

SHA-256 Hashing wie Bitcoin

Coinbase Maturity: 100 + 1 Blöcke

Netzwerk validiert automatisch Difficulty & Timestamp

Kein zentraler Einfluss, dezentrales Peer-to-Peer-System

Prüfsummen, Signaturen & Safe RPC-Mechanismen integriert

---

🧭 Projektlinks :

🌐 Website: https://www.reservistencoin.de

💬 Bitcointalk: https://bitcointalk.org/index.php?topic=5565354

🧰 GitHub: https://github.com/reservistencoin/reservistencoin

⚙️ Explorer: https://explorer.reservistencoin.de

💦 Faucet: (in Planung)

---

📜 Lizenz

Dieses Projekt steht unter der MIT-Lizenz.
Details siehe LICENSE.

---

🪖 Motto

„Treue, Kameradschaft und Verantwortung – auch in der digitalen Welt.“

