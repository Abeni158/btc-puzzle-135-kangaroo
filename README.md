# btc-puzzle-135-kangaroo₿ BTC Puzzle #135 — Pollard Kangaroo Solver
A full UI toolkit for attacking Bitcoin Puzzle #135 using the Pollard Kangaroo algorithm.
Includes a Windows desktop dashboard and an Android mobile monitor.
🎯 Target
Field
Value
Puzzle
#135
Bit Range
2¹³⁴ → 2¹³⁵
Reward
1.35 BTC
Algorithm
Pollard Kangaroo
Complexity
~2⁶⁷·⁵ operations
Public Key
Known ✅
Public Key (compressed):
Code
📁 Files
File
Description
btc135-windows.html
Desktop solver dashboard — config, live stats, log, checkpoint save
btc135-android.html
Mobile companion app — monitor progress, alerts, redemption guide
README.md
This file
🖥️ Windows App — Features
Live ops counter, speed, distinguished points, collisions
Configurable wild/tame kangaroo count
Distinguished Point bit selector (14 / 16 / 20)
Auto-checkpoint save every N seconds (localStorage + downloadable JSON)
Auto-saves private key to file the moment it is found
Full scrollable solver log with export
Redemption warning modal (MARA Slipstream)
Open: Just double-click btc135-windows.html in any browser.
📱 Android App — Features
Native Android-style UI (works in Chrome mobile)
Dashboard, Config, and Info tabs
Real-time stats: ops, speed, DP points, collisions
Progress bar with ETA
Live activity log
Auto-downloads key file instantly when found
Step-by-step redemption guide built in
Open: Open btc135-android.html in Chrome on Android.
⚡ Real GPU Solving (Required for actual solve)
The HTML apps simulate the algorithm for tracking and UI purposes.
For real solving you need JeanLucPons Kangaroo with an NVIDIA GPU.
Setup
Bash
Create puzzle135.txt
Code
Run
Bash
Flag
Meaning
-gpu
Enable CUDA GPU acceleration
-t 8
8 CPU threads
-d 16
Distinguished point bits (16)
-o result.txt
Save result here when found
💰 When the Key is Found
⚠️ CRITICAL — Read this before redeeming!
Bots monitor the mempool 24/7. If you broadcast a transaction normally, they will steal the funds within seconds using a higher fee.
Safe Redemption Steps
Import the WIF private key into Electrum wallet
Create a transaction to your own address
Sign it but DO NOT broadcast
Go to slipstream.mara.com
Paste the raw signed transaction hex
Submit — MARA mines it directly, bypassing the public mempool
🦘 How Pollard Kangaroo Works
Code
The public key being known is what makes this possible —
puzzles without exposed public keys (like #71) cannot use this shortcut.
📊 Estimated Time (Real GPU)
Hardware
Estimated Time
1× RTX 4090
~Thousands of years
100× RTX 4090
~Decades
Large GPU cluster
Years (coordinated pool)
This is why distributed solving (many people contributing ranges) is the only realistic approach.
🔗 Resources
Bitcoin Puzzle Transaction
JeanLucPons Kangaroo
MARA Slipstream
BTC Puzzle Search
⚖️ Disclaimer
This project is for educational and research purposes.
The Bitcoin puzzles are public challenges created intentionally for the community to solve.
The public keys and ranges are publicly available information.
Good luck. 🦘
