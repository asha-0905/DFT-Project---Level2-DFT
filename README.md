# DFT-Project-Level2-Case1 – EDT Flow  

This project demonstrates **Level 2 of the DFT Flow** — *Enhanced Deterministic Test (EDT) compression* — using **Mentor Graphics Tessent Shell**.  

It builds upon **Level1 (Scan Insertion)**, where scan chains were created.  
Here, we insert an **EDT wrapper** around those scan chains and generate all required reports, logs, and constraint files.  

---

## 🚀 Flow Summary  

1. **Setup (Dofile Script)**  
   - Loaded scan-inserted netlist  
   - Linked with TSMC13 standard cell library  
   - Configured Tessent EDT  

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
![project_structure](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/DFT_flow.pdf)


## 🖼️ Visual Snapshots  

- **EDT Dofile** → `edt_dofile.png`
- ![edt_dofile](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/terminal.png?raw=true)
  
- **EDT Log** → `edt_log.png`
- ![edt_Logfile](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/EDT_Logfile.png?raw=true)
  
- **Synthesis Log** → `syn_log.png`
- ![syn_log](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/EDT_Syn_log.png?raw=true)
  
- **EDT Netlist** → `case1_edt_top_gate.png`
- ![case1_edt_top_gate](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/case1_edt_top_gate.png?raw=true)
  
- **TCD File** → `case1_DmaWr_edt_tcd.png`
- ![case1_DmaWr_edt_tcd](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/case1_DmaWr_edt.tcl1.png?raw=true)
- ![case1_DmaWr_edt_tcd](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/case1_DmaWr_edt.tcl2.png?raw=true)
- ![case1_DmaWr_edt_tcd](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/case1_DmaWr_edt.tcl3.png?raw=true)
  
- **Terminal Log** → `terminal_log.png`
- ![terminal_log](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/terminal.png?raw=true)


---

## 📖 Detailed Flow Explanation
For a step-by-step breakdown of each screenshot and output, see 
 [docs/Explanation.md](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/EDT_GITHUB.pdf)
 
---

## 🔮 Next Steps (Planned Roadmap)  

- **ATPG Pattern Generation** (Stuck-at, TDF, IDDQ)  
- Fault coverage reports & pattern compression analysis  

---

👤 **Author**: Asha Ranabhare  
📧 **Email**: asharanabhare28@gmail.com  
🔗 [LinkedIn](#) | [GitHub](#)  

⭐ If you found this project useful, consider giving the repo a star!
