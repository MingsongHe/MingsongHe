#### 🚀 Core Projects
- **[Lonwindows Platform](链接)** [Hybrid Automation Test Platform]- <img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Main%20UI%202.jpg" width="40" alt="UI P01">
  <p>
    
  - **Tech Stack:** `C++ (32-bit)`, `Python (32-bit)`, `PyQt`, `LonWorks`, `RS232`
  - **Key Contributions:**
    - **Reverse engineering the client's C++ code → protocol:** The client couldn't find the communication protocol from 20 years ago either, so the project was completed by analyzing the C++ code.
    - **Modular Configuration:** Implemented `.seq` driven test sequences setting. The steps and test pairs can be set arbitrarily. Drag-and-drop `.ui` interface generation for multiple specifications UUT deployment.
    - **Automated Verification:** Data sampling is completed in the background thread. The pass/fail logic is handled in the foreground, resulting in a complete test report.
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

  - **[NC Code Editor & Industrial Communication System](链接)** [Hybrid Automation Test Platform]- <img src="https://raw.githubusercontent.com/MingsongHe/MingsongHe/refs/heads/main/Main%20UI%202.jpg" width="40" alt="UI P01">
  <p>
    
  - **Tech Stack:** `C++ (MFC)`, `Win32 API`, `RS-232 Serial`, `Multithreading`, `GDI`
  - ** Single-handedly built a full-featured text editor and industrial protocol stack, ensuring 24/7 data integrity on production lines.
  - **Technical Challenges & Solutions:**

- **Large-file rendering bottleneck:** Custom viewport clipping + GDI double-buffering eliminated lag for 50k+ lines of NC code, reducing memory footprint by 70%.

- **Unreliable RS-232 communication:** Implemented dynamic buffering and custom frame validation. Overrode `OnGoodbye` message handling to achieve full-duplex data integrity in noisy shop-floor environments.

- **Undo/Redo user experience:** Built a multi-level command-pattern undo/redo manager supporting insert, delete, cut, paste, and modify operations across all edit scenarios.
    
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


