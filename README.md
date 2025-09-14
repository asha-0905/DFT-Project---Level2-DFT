# DFT-Project-Level2-Case1 – EDT Flow  

This project demonstrates **Level 2 of the DFT Flow** — *Enhanced Deterministic Test (EDT) compression* — using **Mentor Graphics Tessent Shell**.  

It builds upon **Level1 (Scan Insertion)**, where scan chains were created.  
Here, we insert an **EDT wrapper** around those scan chains and generate all required reports, logs, and constraint files.  

---

## 🚀 Flow Summary  

1. **Setup (Dofile Script)**  
   - Loaded scan-inserted netlist  
   - Linked with TSMC13 standard cell library  
   - Configured Tessent ATPG/EDT  

2. **EDT Insertion**  
   - 40 scan cells traced into scan chains  
   - Decompressor + compactor wrapper inserted  
   - Warnings: X-state handling & scan init expansion (normal)  
   - Netlist + reports generated  

3. **Synthesis Report**  
   - Area: ~1361 units  
   - Slack: 0 (no timing violations)  

4. **Outputs Generated**  
   - Post-EDT netlist (`case1_edt_top_gate.v`)  
   - Tessent core description (`case1_DmaWr_edt.tcd`)  
   - Logs & reports  

---

## 📊 Results  

✅ EDT wrapper successfully added  
✅ 4 scan chains compressed into EDT channels  
✅ Clean synthesis log (no critical errors)  
✅ Netlist, reports, constraints generated  

---

## Project Structure
DFT-EDT-Flow/
│── README.md
│── docs/
│ └── Explanation.md
│── src/
│ ├── case1_scan.v # From Level1
│ ├── case1_edt_top_gate.v # Post-EDT netlist
│ └── library.v
│── scripts/
│ ├── case1_atpg.dofile # Dofile script
│ └── run_edt.tcl
│── reports/
│ ├── edt_log.txt # Tessent summary
│ ├── syn_log.txt # Area/timing report
│ └── terminal.log
│── outputs/
│ ├── case1_edt_top_gate.v
│ ├── case1_DmaWr_edt.tcd
│ └── edt_wrapper.v
│── screenshots/
│ ├── atpg_dofile.png
│ ├── edt_log.png
│ ├── syn_log.png
│ ├── case1_edt_top_gate.png
│ ├── case1_DmaWr_edt_tcd.png
│ └── terminal_log.png

## 🖼️ Visual Snapshots  

- **ATPG Dofile** → `atpg_dofile.png`  
- **EDT Log** → `edt_log.png`  
- **Synthesis Log** → `syn_log.png`  
- **EDT Netlist** → `case1_edt_top_gate.png`  
- **TCD File** → `case1_DmaWr_edt_tcd.png`  
- **Terminal Log** → `terminal_log.png`  

---

## 🔮 Next Steps (Planned Roadmap)  

- **ATPG Pattern Generation** (Stuck-at, TDF, IDDQ)  
- Fault coverage reports & pattern compression analysis  

---

👤 **Author**: Asha Ranabhare  
📧 **Email**: asharanabhare28@gmail.com  
🔗 [LinkedIn](#) | [GitHub](#)  

⭐ If you found this project useful, consider giving the repo a star!
