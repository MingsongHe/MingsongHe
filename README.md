#### 🚀 Core Projects
- **[Lonwindows Platform](链接)** [Hybrid Automation Test Platform]- <img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Main%20UI%202.jpg" width="40" alt="UI P01">
  <p> 
    
  - **Tech Stack:** `C++ (32-bit)`, `Python (32-bit)`, `PyQt`, `LonWorks`, `RS232`
  - **Key Achievement:** Reverse-engineered the Lost LonWorks protocol from legacy c++.Built a .seq-driven test engine replacing a 20-year-old C++ system. 
  - **Technical Challenges & Solutions:**
  - **Reverse-engineered legacy protocol:** No documentation existed. Analyzed C++ MFC code to infer frame structures (0x80 header, length bytes) and timing. Re-implemented in Python with full hardware and ldv32.dll compatibility.
    - **.seq-driven test engine:** JSON-based sequence parser converting test steps into executable actions. State machine with test auto_run,and test step enable/disable, pause/resume, and runtime skipping — managed through a dynamic tree UI.
    - **Hybrid async/sync execution:** Background thread polls 64 AI/AO + 192 DI/DO at 10ms in data buffer. Foreground engine uses QTimer callbacks for hardware loopback validation. The "pass/fail" logic is handled in the foreground, resulting in a complete test report.
  - **Note:** *Due to NDA, only high-level architecture and core metrics are disclosed.*
    
  </p>
- **[Universal Leak Tester](链接)** [Hybrid Automation Test Platform]- <img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Main%20UI%202.jpg" width="40" alt="UI P01">
  <p>
    
  - **Tech Stack:** `Python`, `C#`, `LonWorks`, `TwinCAT`, `EtherCAT`, `RS232`, `Named Pipe`
  - **Key Achievement:** Built a .seq-driven test engine with conditional branching (IF/ELSE/Interrupt). The 64-bit Python directly handles Ethercat communication' PCBA, while the 32-bit C# handles Lonworks communication' PCBA via adv32.dll and Name pipe.
  - **Technical Challenges & Solutions:**
    - **Conditional test flow engine:** Extended .seq JSON format with IF/ELSE, Interrupt, and Check points. Evaluates string/numeric/bool conditions in real-time, dynamically skipping or executing step blocks — enabling adaptive flows based on leak rate thresholds or detector status.
    - **Dual-thread acquisition:** The data read/write thread processes data using Ethercat/LonWorks and PCBA, while the detector thread reads helium detector data at a frequency of 4Hz via RS-232. The main thread plots real-time trend graphs, controls test procedures, and determines Pass/Fail" and Generates Excel (trend charts + screenshots), HTML, and XML Multi-format report
    - **Modular Configuration:** The program's .ui editor supports drag-and-drop .ui interface generation, intelligent parameter configuration, and facilitates the deployment of various specifications of devices under test, including "Pallet Test" and "Final Test".
  - **Note:** *Due to NDA, only high-level architecture and core metrics are disclosed.*
    
  </p>
- **[NC Code Editor & Industrial Communication System](链接)** [Left area is a full-featured NC editor, right area for graphics] <img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Main%20UI%202.jpg" width="40" alt="UI P01">
  <p>
    
  - **Tech Stack:** `C++ (MFC)`, `Win32 API`, `RS-232 Serial`, `Multithreading`, `GDI`
  - **Core Function:** Reads and parses standard G-code, leveraging underlying linear and circular interpolation algorithms to accurately render real-time toolpath graphics on the UI.
  - **Key Contributions:**
    - **Optimized Large-File Rendering:** Resolved UI lag when handling massive NC code files by implementing custom viewport clipping and GDI double-buffering, significantly reducing CPU usage and memory footprint.
    - **Reliable RS-232 Communication:** Implemented dynamic buffering and custom frame validation, overriding background message handling to ensure full-duplex data integrity in noisy shop-floor environments.
    - **Robust "Undo" Mechanism:** Built a multi-level command-pattern undo/redo manager supporting insert, delete, cut, paste, and modify operations across all edit scenarios.
    
  </p>

- **[JinRay Test Platform](链接)** [Configurable Multi-Device Test System] <img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Main%20UI%202.jpg" width="40" alt="UI P01">
  <p>
    
  - **Tech Stack:** `Python`, `TwinCAT (ADS)`, `EtherCAT`, `pyads` `RS-232 Serial`, `Multithreading`
  - **Key Achievement:** Built a drag-and-drop UI editor allowing operators to configure valves, MFCs, LEDs, and I/O channels without code changes — enabling a single platform to test multiple device variants.
  - **Technical Challenges & Solutions:**
    - **Visual UI editor for test configuration:** Implemented drag-and-drop editor where users place Valve/MFC/LED widgets onto a background schematic. Widgets save position, object name, and display label to JSON — regenerated on load. Supports big-picture mode with scrollable background.
    - **Hardware-agnostic channel mapping:** Each widget binds to a PLC variable name via dropdown populated from Excel config. Used object name tracking to prevent duplicate assignments. Same platform adapts to different UUTs by swapping UI files.
    - **Cross-type I/O handling:** Unified signal system dispatches 9 PLC data types (USINT/UINT/UDINT/INT/DINT/REAL/BOOL/INT24) to appropriate UI widgets. Special conversions for NI-9220 (±10V scaling) and NI-9208 (24-bit to 20mA).
    
  </p>

##### 🚀 Click to expand for more

<details>
  <summary><b>Agilent Vacuum Pump Controller</b>[`LabVIEW`, `VISA`, `RS-232`, `State Machine`]</summary>
  <p>
  
  - **Tech Stack:** `LabVIEW`, `VISA`, `RS-232`, `State Machine`
  - **Key Technical Highlights:**
    - **State machine architecture:** Implemented LabVIEW state machine with states: Init → Start → Stop → Reset → Status Monitoring. Ensures deterministic transitions and robust error handling.
    - **RS-232 instrument control:** Used NI-VISA to communicate with Agilent vacuum pump over RS-232. Send commands for start, stop, and internal register reset operations.
    - **Real-time status monitoring:** Continuously polls pump status (communication OK, accelerating, start complete) via serial. Displays current state on front panel.
  <br>
  <img src="https://githubusercontent.com" width="500" alt="System Preview">
  </p>
</details>

<details>
  <summary><b>A-H Monitor</b> [`C++`, `MFC`, `Win32 API`, `Multithreading`, `GDI`]</summary>
  <p>
  
  - **Tech Stack:** `C++`, `MFC`, `Win32 API`, `Multithreading`, `GDI`
  - **Key Technical Highlights:**
    - **Multi-threaded data acquisition:** Dedicated thread reads voltage/current/AH/temperature via serial port at configurable intervals (0.017–3600 sec). Main thread triggers visual/audio alarms when thresholds exceeded.
    - **Flicker-free GDI visualization:** Off-screen DC double-buffering enables smooth real-time plotting. Users can drag the chart area (OnLButtonDown + OnMouseMove) to reposition the waveform overlay.
    - **Persistent configuration:** All alarm limits, baud rates, parity, handshaking modes saved to Windows registry via CWinApp::WriteProfileInt/String — auto-loaded on startup.
  <br>
  <img src="https://githubusercontent.com" width="500" alt="System Preview">
  </p>
</details>

- **[项目名称](链接)**:

### 🛠️ 工具轮子 (Open Source Tools)
- **[项目名称](链接)**:
