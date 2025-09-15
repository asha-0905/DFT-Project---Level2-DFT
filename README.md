## 🔹 What is EDT?
**EDT (Embedded Deterministic Test)** is a DFT technique used to reduce test data volume and improve test efficiency.  
It works by compressing the ATPG-generated test patterns before applying them to the scan chains. On-chip decompression logic expands the patterns, and the compacted test responses are collected at the outputs.  

### Why is EDT performed?
- To **reduce test pattern count** and hence **tester memory requirements**.  
- To **decrease test application time** without losing fault coverage.  
- To make large SoCs testable with practical ATE (Automatic Test Equipment) resources.  

### Outcomes of EDT:
- **High fault coverage** comparable to uncompressed tests.  
- **Reduced test cost** due to fewer patterns and faster execution.  
- **Scalable solution** for designs with many scan chains.

---
# DFT-Project-Level2-Case1 – EDT Flow

This project is Level-2 in my DFT learning path. It demonstrates **EDT (Embedded Deterministic Test) compression flow** applied to a scan-inserted design using Mentor Graphics Tessent.

---

## 🛠️ Flow Summary

1. Load scan-inserted netlist & standard cell library  
2. Insert EDT wrapper (decompressor + compactor) around existing scan chains  
3. Generate netlist & constraint file  
4. Run synthesis logging & monitor area/timing reports (no ATPG yet)

---

## 📂 Project Structure
For Structure of Repository, see 
 [project_structure](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/EDT_Repo_srtucture.pdf)

---

## 🚀 Flow Summary  

1. **Setup (Dofile Script)**  
   - Insert EDT (decompressor + compactor) around existing scan chains
   - Generate netlist & constraint file
   - Run synthesis logging & monitor area/timing reports (no ATPG yet)
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

---

## 📊 Results

- 40 scan cells traced into scan chains.  
- EDT decompressor + compactor successfully inserted.  
- No timing violations (slack = 0 in syn log).  
- Constraint file (`.tcd`) generated for compressed ATPG.

---

## 🖼️ Visual Snapshots  

- **EDT Dofile** → `edt_dofile.png`
- ![edt_dofile](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/EDT_Dofile.png)
  
- **EDT Log** → `edt_log.png`
- ![edt_Logfile](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/EDT_Logfile.png?raw=true)
  
- **Synthesis Log** → `syn_log.png`
- ![syn_log](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/EDT_Syn_log.png?raw=true)
  
- **EDT Netlist** → `case1_edt_top_gate.png`
- ![case1_edt_top_gate](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/case1_edt_top_gate.png?raw=true)
  
- **TCD File** → `case1_DmaWr_edt_tcd.png`
- ![case1_DmaWr_edt_tcd](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/case1_DmaWr_edt.tcl1.png?raw=true)
  
- **Terminal Log** → `terminal_log.png`
- ![terminal_log](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/terminal.png?raw=true)

---

## 📖 Detailed Flow Explanation
For a step-by-step breakdown of each screenshot and output, see 
 [docs/Explanation.md](https://github.com/asha-0905/DFT-Project---Level2-DFT/blob/main/EDT_Explanation.pdf)
 
---

## 🔮 Next Steps (Planned Roadmap)  

- **ATPG Pattern Generation** (Stuck-at, TDF, IDDQ)  
- Fault coverage reports & pattern compression analysis  

---

👤 **Author**: Asha Ranabhare  
📧 **Email**: asharanabhare28@gmail.com  
🔗 [LinkedIn](#) | [GitHub](#)  

⭐ If you found this project useful, consider giving the repo a star!

---

#DFT #VLSI #Semiconductors #ScanInsertion #EDT #ATPG #ASIC #DesignForTest #ChipDesign #SoC #TestCompression #DFTEngineering
