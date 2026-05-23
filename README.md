#### 🚀 Core Projects
- **[Lonwindows Platform](链接)** [Hybrid Automation Test Platform]- <img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Main%20UI%202.jpg" width="40" alt="UI P01">
  <p> 
    
  - **Tech Stack:** `C++ (32-bit)`, `Python (32-bit)`, `PyQt`, `LonWorks`, `RS232`
  - **Key Achievement:** Reverse-engineered the Lost LonWorks protocol from legacy c++.Built a .seq-driven test engine replacing a 20-year-old C++ system. 
  - **Technical Challenges & Solutions:**
    - **Reverse-engineered legacy protocol** No documentation existed. Analyzed C++ MFC code to infer frame structures (0x80 header, length bytes) and timing. Re-implemented in Python with full hardware and ldv32.dll compatibility.
    - **.seq-driven test engine:** JSON-based sequence parser converting test steps into executable actions. State machine with step auto_run,enable/disable, pause/resume, and runtime skipping — managed through a dynamic tree UI.
    - **Hybrid async/sync execution:** Background thread polls 64 AI/AO + 192 DI/DO at 10ms in data buffer. Foreground engine uses QTimer callbacks for hardware loopback validation. The "pass/fail" logic is handled in the foreground, resulting in a complete test report.
  - **Note:** *Due to NDA, only high-level architecture and core metrics are disclosed.*
    
  </p>
- **[Universal Leak Tester](链接)** [Hybrid Automation Test Platform]- <img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Main%20UI%202.jpg" width="40" alt="UI P01">
  <p>
    
  - **Tech Stack:** `Python`, `C#`, `TwinCAT`, `LonWorks`, `EtherCAT`, `RS232`
  - **Key Contributions:**
    - **Cross-Architecture Communication:** Resolved interoperability challenges between 32-bit C# (Communication Layer) and 64-bit Python (Logic Layer). RS232 completes communication with the helium detector.
    - **Modular Configuration:** Implemented `.seq` driven test sequences setting. The steps and test pairs can be set arbitrarily. Drag-and-drop `.ui` interface generation for multiple specifications UUT deployment.
    - **Automated Validation:** The test process can branch based on intermediate results. It integrates robust pass/fail logic. Test reports are provided in Excel, PDF, and XML formats, including test steps and screenshots.
  - **Note:** *Due to NDA, only high-level architecture and core metrics are disclosed.*
    
  </p>
- **[NC Code Editor & Industrial Communication System](链接)** [Left area is a full-featured NC editor, right area for graphics] <img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Main%20UI%202.jpg" width="40" alt="UI P01">
  <p>
    
  - **Tech Stack:** `C++ (MFC)`, `Win32 API`, `RS-232 Serial`, `Multithreading`, `GDI`
  - **Core Function:** Reads and parses standard G-code, leveraging underlying linear and circular interpolation algorithms to accurately render real-time toolpath graphics on the UI.
  - **Key Contributions:**
    - **Optimized Large-File Rendering:** Resolved UI lag when handling massive NC code files by implementing custom viewport clipping and GDI double-buffering, significantly reducing CPU usage and memory footprint.
    - **Reliable RS-232 Communication:** Implemented dynamic buffering and custom frame validation, overriding background message handling to ensure full-duplex data integrity in noisy shop-floor environments.
    - **Robust "Undo" Mechanism:**  Built a multi-level command-pattern undo/redo manager supporting insert, delete, cut, paste, and modify operations across all edit scenarios.
    
  </p>

##### 🚀 Click to expand for more

<details>
  <summary><b>Hybrid Automation Test Platform (C# / Python / LonWorks)</b></summary>
  <p>
  
  - **Tech Stack:** `C# (32-bit)`, `Python (64-bit)`, `LonWorks`, `PyQt`
  - **Key Contributions:**
    - **Cross-Architecture Communication:** Resolved interoperability challenges between 32-bit C# (Communication Layer) and 64-bit Python (Logic Layer).
    - **Modular Configuration:** Implemented `.seq` driven test sequences setting. Drag-and-drop `.ui` interface generation for multiple specifications UUT deployment.
    - **Automated Validation:** Integrated robust Pass/Fail logic ensuring data consistency and rigorous testing cycles.
  - **Note:** *Due to NDA, only high-level architecture and core metrics are disclosed.*
  <br>
  <img src="https://githubusercontent.com" width="500" alt="System Preview">
  </p>
</details>

<details>
  <summary><b>Project Name 2 (Brief One-line Description)</b></summary>
  <p>
  
  - **Tech Stack:** `Your Tech`
  - **Key Contributions:** Detail 1, Detail 2.
  </p>
</details>

- **[项目 B 名称](链接)**: 基于 Python 的自动化脚本。

### 🛠️ 工具轮子 (Open Source Tools)
- **[项目 C 名称](链接)**: 一个轻量级的 CSS 框架。
- <br>
  <img src="https://raw.githubusercontent.com/MingsongHe/ADataEdit/refs/heads/main/PCBA%20Family%20all%20include%20Main%20UI%20P02.jpg" width="40" alt="项目预览">


