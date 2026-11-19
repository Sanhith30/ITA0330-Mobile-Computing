# Smart Shield Wi-Fi 🛡️📶
### A Mobile Computing Framework for Intelligent Wi-Fi Trust Assessment

**Course**: ITA0330 — Mobile Computing  
**Institution**: SIMATS Engineering, Saveetha Institute of Medical and Technical Sciences, Chennai  
**Supervisor**: Dr. Meganathan Elumalai, Professor, SIMATS Engineering  

**Team Members**:
- **T. Sanhith** (Reg. No: 192311228) — *Project Lead & Security Engine Architect*
- **P. Veeraswami** (Reg. No: 192311253) — *Spectrum & Presentation Specialist*
- **P. Jawed Khan** (Reg. No: 192311263) — *Gateway Probing & Analytics Lead*

---

## 📁 Capstone Project Deliverables

| File / Directory | Description |
| :--- | :--- |
| [`Smart Shield Wifi/`](Smart%20Shield%20Wifi/) | Native Android application (Java, MVVM, Room DB, Material Design 3) and Streamlit dashboard |
| [`Capstone_Project_Report_SmartShield_WiFi.docx`](Capstone_Project_Report_SmartShield_WiFi.docx) | Full formal Capstone Project Report following SIMATS Engineering Sep 2026 format (~6 MB) |
| [`MC-ppt.pptx`](MC-ppt.pptx) | Complete Capstone Presentation slide deck (17 slides) |
| [`SmartShield-Wifi.apk`](SmartShield-Wifi.apk) | Compiled and ready-to-install Android Debug Application (~6.28 MB) |
| [`report_assets/`](report_assets/) | High-resolution architecture diagrams, module schematics, and mobile screenshots |
| [`Capstone Project Report - New Format - Sep 2026 (1).pdf`](Capstone%20Project%20Report%20-%20New%20Format%20-%20Sep%202026%20(1).pdf) | Institutional project report format template reference |

---

## 🌟 Key Features

1. **4-Tier MCDA Trust Assessment Engine**:
   - Calculates a normalized 0–100 Trust Score based on:
     $$\text{Score} = \text{Security (40)} + \text{Similarity (30)} + \text{Known/Vendor (20)} + \text{Signal (10)}$$
   - Generates transparent, explainable audit trails (*"Why should I trust this network?"*).

2. **Evil Twin & SSID Spoofing Guard**:
   - Computes **Levenshtein Distance** ($\le 2$) to detect lookalike network names.
   - Flags security cipher mismatches (e.g., Open vs WPA2/WPA3) as critical rogue AP threats.

3. **Spectrum & Channel Interference Analyzer**:
   - Custom canvas rendering parabolic signal curves across 2.4 GHz and 5 GHz frequency bands.
   - Detects co-channel and adjacent-channel congestion and recommends optimal channels.

4. **Active Gateway Probe**:
   - Dispatches RFC 6585 HTTP 204 checks (`connectivitycheck.gstatic.com/generate_204`) to detect captive portal redirection and SSL traffic interception.

5. **Safe QR Code Scanner**:
   - Integrated ZXing camera scanner auditing Wi-Fi credentials before connecting.

---

## 🚀 How to Run & Test

### Android App
```bash
cd "Smart Shield Wifi"
./gradlew assembleDebug
```
Install the generated APK onto your phone:
```bash
adb install SmartShield-Wifi.apk
```

### Streamlit Threat Analytics Dashboard
```bash
cd "Smart Shield Wifi"
pip install streamlit
streamlit run streamlit_app.py
```
