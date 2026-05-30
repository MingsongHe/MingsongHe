#### 🚀 Core Projects
- **[Lonwindows Platform](链接)** [Hybrid Automation Test Platform]- <img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Main%20UI%202.jpg" width="40" alt="UI P01"><img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Main%20UI%203.jpg" width="40" alt="UI P01"><img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Lonwindows%20Platform%20P-ID%20Window.jpg" width="40" alt="UI P01"><img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Lonwindows%20Platform%20Calibration%20setting%20Window.jpg" width="40" alt="UI P01"><img    src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Lonwindows%20Platform%20Report.jpg" height="30" alt="UI P01">
  <p> 
    
  - **Tech Stack:** `C++ (32-bit)`, `Python (32-bit)`, `PyQt`, `LonWorks`, `RS232`
  - **Key Achievement:** Successfully spearheaded the modernization of a 20-year-old monolithic C++ test system, engineering a modern, sequence-drive (.seq) hybrid automation testing platform that achieved full compatibility with legacy hardware wrappers.
  - **Technical Challenges & Solutions:**
    - **Reverse-engineered legacy protocol:** Executed black-box and white-box reverse-engineering on the losted proprietary, LonWorks communication protocol,meticulously analyzed legacy C++ MFC source code to decipher complex frame structures (0x80 headers, variable length bytes) and precise hardware timing constraints.Re-implemented the protocol stack in Python with seamless integration of legacy 32-bit Win32 APIs (ldv32.dll), ensuring data integrity and backward hardware compatibility without original technical documentation.
    - **.seq-driven test engine:** Developed a high-performance JSON-based sequence parsing engine featuring an advanced finite state machine (FSM) that supports runtime execution control, including real-time test step enabling/disabling, pause/resume, and dynamic step skipping managed through a hierarchical tree UI.Designed a deterministic hybrid sync/async execution architecture to handle massive concurrent I/O.The "pass/fail" logic is handled in the foreground, resulting in a complete test report.
    - **Hybrid async/sync execution:** Engineered a high-frequency background polling thread to buffer data from 64 AI/AO + 192 DI/DO channels at a strict 25ms interval.Utilized optimized foreground QTimer event callbacks for asynchronous hardware loopback validation, decoupling intense data acquisition from the UI to deliver zero-lag performance and comprehensive test analytics.
    - **Note:** *Due to NDA, only high-level architecture and core metrics are disclosed.*
    
  </p>
- **[Universal Leak Tester](链接)** [Hybrid Automation Test Platform]- <img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Univsal%20Leak%20Tester%20Report.jpg" height="30" alt="UI P01">                      <img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Univsal%20Leak%20Tester%20seq%20Flow.jpg" height="30" alt="UI P01">
  <p>
    
  - **Tech Stack:** `Python`, `C#`, `LonWorks`, `TwinCAT`, `EtherCAT`, `RS232`, `Named Pipe`
  - **Key Achievement:** Built a .seq-driven test engine with conditional branching (IF/ELSE/Interrupt). The 64-bit Python directly handles Ethercat communication PCBA, while the 32-bit C# handles Lonworks communication' PCBA via adv32.dll and Named pipe.
  - **Technical Challenges & Solutions:**
    - **Designed a mission-critical .seq-driven leak testing platform:**  JSON parser converts test steps into executable operations; supports auto-execution, conditional branching (if/else/interrupts/checkpoints), Information Prompts，dynamic leak threshold evaluation and flow jumps; managed via dynamic tree UI for intuitive tests step state visualization.
    - **Multi-threaded Data Interaction:**
           -   1)EtherCAT UUTs: data read/write uses Beckhoff TwinCAT's ADS protocol, handled by a background Python thread.
           -   2)Lonworks UUTs: a C# background process communicates with PCBA via ldv32.dll (32-bit) and with the Python main program via Named Pipe.
           -   3)Helium detector: a background thread reads detector data at 4Hz via RS-232.

    - **Main Thread:** Manages the main UI and test windows, loads .seq files per test type (Pallet Test / Final Test), plots real-time data, and controls test flow based on .seq execution. Automatically generates comprehensive compliance reports in Excel, HTML, and XML formats, including real-time trend charts, UI screenshots, and raw data summaries, with pass/fail determination.
    - **Note:** *Due to NDA, only high-level architecture and core metrics are disclosed.*
  </p>


- **[JinRay Test Platform](链接)** [Configurable Multi-Device Test System] <img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/JinRay%20Test%20Platform%20Main%20UI.jpg" width="40" alt="UI P01"><img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/JinRay%20Test%20Platform%20P-ID%20Window.jpg" height="30" alt="UI P01"><img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/JinRay%20Test%20Platform%20P03.jpg" width="40" alt="UI P01"><img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/JinRay%20Test%20Platform%20ui%20Editor%20Working%20Process%20P02.jpg" width="40" alt="UI P01">
  <p>
    
  - **Tech Stack:** `Python`, `TwinCAT (ADS)`, `EtherCAT`, `pyads` `RS-232 Serial`, `Multithreading`
  - **Key Achievement:**Architected and delivered a fully decoupled, hardware-agnostic multi-device testing platform that empowers operators to dynamically configure valves,MFCs,LEDs, pressure sensor and I/O channels via a visual UI, successfully scaling a single software framework to support diverse device ,complete different testing processes variants without code modifications.
  - **Technical Challenges & Solutions:**
    - **Visual UI editor for test configuration:** Engineered a highly intuitive Visual UI Editor enabling drag-and-drop orchestration of industrial widgets onto a background schematic,compiled and serialized into a custom runtime .ui file,（widgets save position, object name, and display label to JSON ） schema for instantaneous layout regeneration.Each widget binds to a component variable name via  dropdown populated from Excel config.linking UI widgets dynamically to variables, object-name collision detection to ensure zero-duplicate channel assignments.
    - **The .seq-based test engine features:** A high-performance JSON-based sequence parsing engine employing an advanced Finite State Machine (FSM);  
supporting automatic execution, conditional branching (if/else/interruption/checkpointing),information prompts, dynamic leak threshold assessment, and flow jumps; managed through a dynamic tree-structured UI for intuitive visualization of test step states.
    - **Cross-type I/O handling:** Unified signal system dispatches 9 PLC data types (USINT/UINT/UDINT/INT/DINT/REAL/BOOL/INT24) to appropriate UI widgets. Special conversions for NI-9220 (±10V scaling) and NI-9208 (24-bit to 20mA).
    - **Note:** *Due to NDA, only high-level architecture and core metrics are disclosed.*
    
  </p>


- **[NC Code Editor & Industrial Communication System ▶️](https://youtu.be/_G05MGl8mwA)** [Left area is a NC editor, right area for graphics] <img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Data%20Editor%20Main%20UI%20P01.jpg" width="40" alt="UI P01"><img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Data%20Editor%20Main%20UI%20P02.jpg" width="40" alt="UI P01">
  <p>
    
  - **Tech Stack:** `C++ (MFC)`, `Win32 API`, `RS-232 Serial`, `Multithreading`, `GDI`
  - **Core Function:** Reads and parses standard G-code, leveraging underlying linear and circular interpolation algorithms to accurately render real-time toolpath graphics on the UI.
  - **Key Contributions:**
    - **Optimized Large-File Rendering:** Resolved UI lag when handling massive NC code files by implementing custom viewport clipping and GDI double-buffering, significantly reducing CPU usage and memory footprint.
    - **Reliable RS-232 Communication:** Implemented dynamic buffering and custom frame validation, overriding background message handling to ensure full-duplex data integrity in noisy shop-floor environments.
    - **Robust "Undo" Mechanism:** Built a multi-level command-pattern undo/redo manager supporting insert, delete, cut, paste, and modify operations across all edit scenarios.
    
  </p>

- **[Agilent Vacuum Pump Controller](链接)** [`LabVIEW`, `VISA`, `RS-232`, `State Machine`] <img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Pump%20Contoller%20V1.0%20Main%20UI.jpg" width="40" alt="UI P01">
  <p>
    
  - **Tech Stack:**  `LabVIEW`, `VISA`, `RS-232`, `State Machine`
  - **Key Technical Highlights:**
    - **State machine architecture:** Implemented LabVIEW state machine with states: Init → Start → Stop → Reset → Status Monitoring. Ensures deterministic transitions and robust error handling.
    - **RS-232 instrument control:** Used NI-VISA to communicate with Agilent vacuum pump over RS-232. Send commands for start, stop, and internal register reset operations.
    - **Real-time status monitoring:** Continuously polls pump status (communication OK, accelerating, start complete) via serial. Displays current state on front panel.

  </p>

- [<b><a href="https://youtu.be/Ng6qhnX2WXk">A-H Monitor ▶️</a></b>] [`C++`, `MFC`, `Win32 API`, `Multithreading`, `GDI`]<img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/A-H%20Monitor%20Main%20UI.jpg" width="40" alt="UI P01"><img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/A-H%20Monitor%20P02.jpg" width="40" alt="UI P01"><img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/A-H%20Monitor%20P03.jpg" width="40" alt="UI P01"><img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/A-H%20Monitor%20P04.jpg" width="40" alt="UI P01">
  <p>
    
  - **Tech Stack:** `C++`, `MFC`, `Win32 API`, `Multithreading`, `GDI`
  - **Key Technical Highlights:**
    - **Multi-threaded data acquisition:** Dedicated thread reads voltage/current/AH/temperature via serial port at configurable intervals (0.017–3600 sec). Main thread triggers visual/audio alarms when thresholds exceeded.
    - **Flicker-free GDI visualization:** Off-screen DC double-buffering enables smooth real-time plotting. Users can drag the chart area (OnLButtonDown + OnMouseMove) to reposition the waveform overlay.
    - **Persistent configuration:** All alarm limits, baud rates, parity, handshaking modes saved to Windows registry via CWinApp::WriteProfileInt/String — auto-loaded on startup.

  </p>

  
