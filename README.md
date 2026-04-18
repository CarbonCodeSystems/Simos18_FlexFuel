## VAG Flex Fuel Crisis Relief

This repository provides custom **.bdc** binary flash files for Volkswagen Audi Group (VAG) vehicles equipped with **SIMOS18** Engine Control Units (ECUs). 

The goal of this project is to provide a community-driven solution for fuel flexibility. By enabling Flex Fuel functionality, vehicle owners can utilize alternative fuel sources (such as E85 or ethanol blends) that may be more accessible or cost-effective during periods of fuel instability or economic crisis.

---

### 📂 Repository Structure

Files are organized by ECU generation and identified by their Calibration ID (**CALID**) and Software ID (**SWID**). This ensures you select the correct binary for your specific vehicle software version.

Each supported version includes both the stock reference and the modified Flex Fuel calibration:

* `SIMOS18_[CALID]_[SWID]_Original.bdc` – The untouched factory binary.
* `SIMOS18_[CALID]_[SWID]_Flex_Fuel_Calibration.bdc` – The modified binary with enabled Flex Fuel logic.

---

### 🛠 Technical Specifications

* **Target ECU:** Continental/VDO SIMOS18.x
* **File Format:** .bdc (Binary Data Container)
* **Functionality:** Enables ethanol content scaling and ignition/fuel mapping adjustments for high-ethanol blends.

---

### ⚠️ Important Safety & Legal Disclaimer

**Use these files at your own risk.** 1.  **Hardware Requirements:** Proper Flex Fuel operation usually requires an ethanol content sensor and associated wiring integrated into the ECU. Running high ethanol blends without supporting hardware or fuel system upgrades (e.g., HPFP) can lead to engine lean-out or mechanical failure.

2.  **Flashing Risks:** Writing to an ECU carries the risk of "bricking" the module if the process is interrupted or the checksums are incorrect. Ensure you are using reliable slave/master tools (such as Autotuner, bFlash, or Flex).

3.  **Compliance:** Modifying engine software may violate local emissions laws or void vehicle warranties. This repository is provided for educational and emergency resource purposes.

---

### 🤝 Contributing

If you have successfully tested a calibration for a SWID not listed here, feel free to submit a Pull Request or open an Issue with the log data. 

> **Note:** Always keep a backup of your original `_Original.bdc` file before attempting any flash operations.