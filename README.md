Memowrite 📝Memowrite is an expressive, beginner-friendly, and expressive programming language built on Python. It offers a clean, English-like syntax paired with an extensive set of built-in standard libraries for graphics, 2D animation, GUI creation, persistent memory, sound synthesis, and interactive desktop application development.⚠️ Platform Notice: Memowrite is built and optimized exclusively for Windows. Win32/Windows-specific APIs, launchers, installer configurations, and desktop GUI integrations require a Windows environment.📋 Table of ContentsOverview & PhilosophyKey FeaturesProject ArchitectureInstallation & SetupPrerequisitesUsing the Windows InstallerRunning from SourceLanguage Tour & SyntaxHello World & BasicsVariables & InputControl Flow & LoopsFunctionsPersistent Memory (File.Memory)Built-In Standard LibrariesMemowrite Studio & ToolingMemowrite Studio IDEVS Code ExtensionIncluded Showcase ExamplesBuilding & PackagingLicense🌟 Overview & PhilosophyMemowrite aims to bridge the gap between simple scripting languages and full-featured application creation. By providing human-readable keywords alongside immediate visual and persistent state capabilities, developers can prototype games, utilities, and desktop GUI tools without juggling heavy external dependencies.⚡ Key FeaturesReadable Syntax: Clear keywords like say, ask, set, repeat, if, and book make code intuitive and self-documenting.Integrated 2D Graphics Engine: Direct support for canvas creation, geometric primitive rendering, color manipulation, and animation loops.Built-In GUI Framework: Construct windows, buttons, input fields, labels, and event listeners directly within Memowrite code.Persistent Key-Value Store (File.Memory): Effortlessly save, load, and manage state across application restarts without managing raw files manually.Audio Synthesis & Effects: Native sound capabilities for playing audio tones and sound effects.Developer Environment Included: Comes bundled with Memowrite Studio (an interactive IDE) and a official VS Code Extension.📦 Project Architecturememowrite-source/
│
├── memowrite/                  # Primary Python implementation
│   ├── stdlib/                 # Standard Library Modules
│   │   ├── colors.py           # Console color & styling formatting
│   │   ├── file_memory.py      # Persistent key-value storage engine
│   │   ├── files.py            # File I/O utilities
│   │   ├── graphics.py         # 2D Canvas & animation rendering engine
│   │   ├── gui.py              # Windows GUI toolkit
│   │   ├── sound.py            # Audio playback & tone synthesis
│   │   ├── system.py           # OS, environment, and system utilities
│   │   └── text_plus.py        # String manipulation & formatting helpers
│   ├── cli.py                  # CLI argument parser & execution handler
│   ├── errors.py               # Runtime & parse error definitions
│   ├── interpreter.py          # Abstract Syntax Tree (AST) evaluator
│   ├── lexer.py                # Lexical scanner & tokenizer
│   ├── parser.py               # Grammatical parser & AST generator
│   ├── studio.py               # Memowrite Studio IDE (Tkinter-based)
│   └── values.py               # Internal representation of runtime values
│
├── examples/                   # 25+ Comprehensive Example Scripts (.mw)
│   ├── 01_hello.mw             # Basic output demo
│   ├── 08_file_memory.mw       # Persistent memory demo
│   ├── 11_calculator_app.mw    # Graphical calculator application
│   ├── 13_drawing.mw           # Interactive drawing canvas
│   ├── 15_bouncing_ball.mw     # 2D physics animation
│   ├── 16_catch_game.mw        # Mini arcade game implementation
│   ├── 17_paint_app.mw         # Full paint application with color pickers
│   ├── 20_clock_app.mw         # Desktop analog/digital clock
│   ├── 24_contact_book.mw      # Interactive database/contact management
│   └── 25_solar_system.mw      # 2D planetary motion simulator
│
├── library/                    # Additional helper modules and drawing primitives
├── launcher/                   # C-compiled Windows binaries (.exe wrappers)
├── installer/                  # NSIS installer configuration script (`memowrite.nsi`)
└── vscode/                     # Official VS Code Extension package (`.vsix`)
🛠️ Installation & SetupPrerequisitesOperating System: Windows 10 or Windows 11 (64-bit recommended)Python Engine: Python 3.8+ (Required when running from source)Using the Windows InstallerNavigate to the installer/ directory or download the latest executable installer.Run MemowriteSetup.exe (generated via NSIS).Follow the installation wizard to install Memowrite, register .mw file associations, and add memowrite to your Windows %PATH%.Running from SourceClone or extract the source workspace on your Windows machine:git clone https://github.com/your-repo/memowrite.git
cd memowrite
Verify your Python installation and run scripts directly via the command prompt:python -m memowrite examples\01_hello.mw
💡 Language Tour & Syntax1. Hello World & Basicssay "Welcome to Memowrite on Windows!"
2. Variables & Inputset name to ask "Enter your name: "
say "Hello, " + name + "! Welcome back."
3. Control Flow & Loopsset score to 85

if score >= 90 then
    say "Grade: Outstanding"
else if score >= 70 then
    say "Grade: Good"
else
    say "Grade: Needs Work"
end

set counter to 1
repeat while counter <= 5
    say "Step: " + counter
    set counter to counter + 1
end
4. Functionsfunction greetUser(username)
    say "Welcome, " + username
end

greetUser("Alex")
5. Persistent Memory (File.Memory)Store data permanently on your Windows disk across program launches without configuring databases:use File.Memory

# Store persistent values
Memory.set("high_score", 5000)
Memory.set("player_name", "CyberKnight")

# Retrieve values in subsequent runs
set current_high_score to Memory.get("high_score")
say "Current High Score: " + current_high_score
📚 Built-In Standard LibrariesLibraryModule PathPurpose / HighlightsColorsmemowrite/stdlib/colors.pyTerminal color styling, text decorations, and ANSI background formatting.TextPlusmemowrite/stdlib/text_plus.pyStrings transformation, padding, pattern searches, and formatting tools.Filesmemowrite/stdlib/files.pyStandard Windows file path resolution, reading, writing, appending, and deleting.File.Memorymemowrite/stdlib/file_memory.pyPersistent disk-backed JSON key-value store for app configuration and game saves.Graphicsmemowrite/stdlib/graphics.py2D canvas drawing routines, primitives, custom shapes, double-buffered frame loops.GUImemowrite/stdlib/gui.pyDesktop GUI toolkit for creating native windows, buttons, input fields, and alerts.Soundmemowrite/stdlib/sound.pyAudio tone playback, sound effect generation, and media handlers.Systemmemowrite/stdlib/system.pyExecution environment inspect, process launchers, Windows command execution.🖥️ Memowrite Studio & ToolingMemowrite Studio IDEMemowrite comes with an integrated IDE designed for fast code iteration and testing.Launch the studio from the command prompt:memowrite-studio
Or run via Python directly:python -m memowrite --studio
Studio Features:Code Editor with syntax highlightingOne-click script runner (F5)Output terminal panel with error highlightingIntegrated example loaderVS Code ExtensionFor developers who prefer Visual Studio Code:Open VS Code.Go to the Extensions sidebar (Ctrl+Shift+X).Click the ... menu at the top right and select Install from VSIX....Select vscode/memowrite-1.0.0.vsix.🎨 Included Showcase ExamplesCheck out the examples/ directory for ready-to-run projects demonstrating various capabilities:11_calculator_app.mw - Functional desktop GUI calculator.13_drawing.mw & 17_paint_app.mw - Full-featured paint and interactive canvas software.15_bouncing_ball.mw - Real-time physics rendering and bounce collision handling.16_catch_game.mw - Keyboard-driven mini arcade game.20_clock_app.mw - Real-time animated graphical clock display.25_solar_system.mw - Multi-body planetary orbit physics simulation.🔨 Building & PackagingTo compile the C executable launchers or generate the NSIS installer:Launcher Binaries: Build executable launchers inside launcher/ using GCC/MinGW on Windows.NSIS Installer: Open installer/memowrite.nsi in NSIS (Nullsoft Scriptable Install System) and click Compile Script to output MemowriteSetup.exe.📄 LicenseThis project is licensed under the MIT License. See the LICENSE.txt file for full terms and conditions.
