<div align="center">

<img src="assets/banner.png" width="100%" alt="Sai Siddharth B S — embedded systems, avionics and defence technology, AI and software. An aircraft cockpit overlooking a runway at dusk.">

<br>

<a href="#selected-work">Selected work</a> &nbsp; / &nbsp;
<a href="#engineering-interests">Engineering interests</a> &nbsp; / &nbsp;
<a href="#toolbox">Toolbox</a> &nbsp; / &nbsp;
<a href="#connect">Connect</a>

<h1>Sai Siddharth B S</h1>

<b>Hardware curiosity. Software craft. Products that work.</b>

I build across applications, applied AI, and data systems.<br>
My interests extend into embedded systems, avionics, and defence technology.

</div>

<br>

## Selected work

Four projects across music, manufacturing knowledge, quantitative research, and voice-driven automation. Each brings together the interface, the underlying engines, and the work needed to connect them.

[OpenWave](#01--openwave) · [Neura1](#02--neura1) · [Agent Alpha](#03--agent-alpha) · [Captain AI](#04--captain-ai)

### 01 / OpenWave

**One music library. Every device.**

<a href="https://github.com/SaiSiddharthBS/OpenWave"><img src="assets/openwave-preview.png" width="100%" alt="OpenWave product preview showing its desktop music player and a phone listening to the same song."></a>

An open-source music player with gapless playback, offline downloads, synced libraries, and shared listening sessions. A Python engine powers desktop apps, Android, an iPhone web app, and self-hosted deployments.

<sub>PYTHON &nbsp; / &nbsp; FASTAPI &nbsp; / &nbsp; JAVASCRIPT &nbsp; / &nbsp; SQLITE &nbsp; / &nbsp; DOCKER</sub>

**[Explore the code ↗](https://github.com/SaiSiddharthBS/OpenWave)** &nbsp; · &nbsp; [Visit the website](https://saisiddharthbs.github.io/OpenWave/) &nbsp; · &nbsp; [Download](https://github.com/SaiSiddharthBS/OpenWave/releases)

<br>

### 02 / Neura1

**Understand what a change touches.**

<a href="https://cdn.jsdelivr.net/gh/SaiSiddharthBS/Neura1@64a8cd8c71cab93df6006766be7dbc44e5d68ec2/docs/demo/neura1-demo.mp4"><img src="assets/neura1-preview.jpg" width="100%" alt="Watch Neura1's three-minute product demonstration: manufacturing knowledge graph, change impact, and planning tools."></a>

A company knowledge graph for hardware manufacturers. Neura1 connects parts, builds, customer orders, people, and past decisions to trace the consequences of a change. Graph queries, planning logic, and AI work together, with facts linked back to their sources.

<sub>PYTHON &nbsp; / &nbsp; FALKORDB &nbsp; / &nbsp; NEXT.JS &nbsp; / &nbsp; MCP &nbsp; / &nbsp; LOCAL INFERENCE</sub>

**[Explore the code ↗](https://github.com/SaiSiddharthBS/Neura1)** &nbsp; · &nbsp; [Watch the demos](https://github.com/SaiSiddharthBS/Neura1#readme) &nbsp; · &nbsp; [Read the evaluation](https://github.com/SaiSiddharthBS/Neura1/blob/main/docs/EVAL.md)

<br>

### 03 / Agent Alpha

<p align="center"><a href="https://github.com/SaiSiddharthBS/Agent_Alpha"><img src="assets/agent-alpha-logo.png" width="144" alt="Original Agent Alpha logo: a metallic alpha symbol with an aircraft detail."></a></p>

**From market data to signals, risk decisions, and a paper-trading arena.**

Agent Alpha is my quantitative research and trading project for Indian equities. It brings market-data ingestion, technical analysis, machine-learning signals, market-regime classification, risk checks, and portfolio monitoring into a connected system. The engineering spans the analytical backend, scheduled jobs, persistent data, desktop interface, and remote monitoring.

<a href="https://github.com/SaiSiddharthBS/Agent_Alpha#system-gallery"><img src="assets/agent-alpha-preview.png" width="100%" alt="Agent Alpha dashboard from the public repository, showing market information, research panels, and system monitoring."></a>

**What the system brings together**

- **Multiple views of the market.** Technical indicators, momentum, machine-learning predictions, institutional flows, options data, and statistical-arbitrage research contribute to the analysis. Ensemble weighting combines signals into a directional assessment.
- **Market context and risk controls.** A four-state Hidden Markov Model classifies market conditions. A separate veto layer can override a signal, while volatility and Kelly-based sizing inform position allocation.
- **Research and simulated execution.** Screening, individual-stock analysis, portfolio views, and a paper-trading arena connect research with simulated positions and outcomes. Backtesting and signal-accuracy views support evaluation of the strategies.
- **An operational interface.** The dashboard is accompanied by an Electron desktop wrapper, a macOS menu-bar utility, and Telegram commands and alerts. These provide different ways to inspect the system and monitor its activity.

<details>
<summary><b>Inside the engineering — models, infrastructure, and reliability</b></summary>

#### Research pipeline

The documented model families cover trend and volatility indicators, momentum, boosted-tree classifiers, sequence models, institutional flows, and pairs research. The regime classifier adds context to those signals: an assessment in a quiet uptrend should be treated differently from one during a volatile drawdown. The risk layer then considers whether a candidate should proceed at all.

#### Compute and delivery

The deployment design separates a Mac-based interface and development workstation from an always-on Windows execution host. Docker services, scheduled scans, a FastAPI backend, PostgreSQL persistence, and Ollama-based language-model analysis support the system. SSH deployment tooling connects the development and execution environments.

#### Reliability work

The repository includes checks for database hangs, portfolio queries, pricing fallbacks, regime logic, statistical calculations, and the paper-trading engine. This matters because a research system depends on both its analytical logic and the quality and availability of the data feeding it.

</details>

<sub>PYTHON &nbsp; / &nbsp; FASTAPI &nbsp; / &nbsp; POSTGRESQL &nbsp; / &nbsp; OLLAMA &nbsp; / &nbsp; ELECTRON &nbsp; / &nbsp; DOCKER</sub>

**[Explore the code ↗](https://github.com/SaiSiddharthBS/Agent_Alpha)** &nbsp; · &nbsp; [Architecture & research](https://github.com/SaiSiddharthBS/Agent_Alpha#readme) &nbsp; · &nbsp; [Interface gallery](https://github.com/SaiSiddharthBS/Agent_Alpha#system-gallery)

<br>

### 04 / Captain AI

<p align="center"><a href="https://github.com/SaiSiddharthBS/Captain_AI"><img src="assets/captain-ai-logo.png" width="420" alt="Original Captain AI wordmark in metallic white, blue, and violet."></a></p>

**A voice interface connected to the screen, the desktop, and the phone.**

Captain AI is my modular assistant project, built around a central intent router that coordinates speech, conversation, screen understanding, and device actions. It combines on-device audio processing with cloud language-model inference and local vision, bringing those capabilities into a desktop overlay and a remote Telegram interface.

<a href="https://github.com/SaiSiddharthBS/Captain_AI#readme"><img src="assets/captain-ai-preview.png" width="100%" alt="Captain AI Ghost HUD: the project's desktop assistant overlay, shown in its public interface gallery."></a>

**What the system brings together**

- **A complete voice loop.** OpenWakeWord detects the trigger, Faster-Whisper transcribes speech, and Piper generates spoken responses. Audio ducking lowers music during an interaction; cached speech output reduces repeated synthesis work.
- **Conversation with retrieved context.** Groq supplies streaming language-model responses, with Wikipedia and DuckDuckGo retrieval providing context for information requests. Ollama and Moondream handle local screen-image analysis.
- **Actions across devices.** Intent handlers connect voice commands to application launching, web navigation, email workflows, music, and Android automation through ADB. Persistent memory, to-do lists, alarms, and timers support everyday tasks.
- **A visible assistant state.** The Ghost HUD uses a frameless PyQt6 window and an HTML/CSS interface. WebSocket messages connect it to the backend, displaying listening, processing, and speaking states. A hotkey summons the overlay; Telegram provides another command channel.

<details>
<summary><b>Inside the engineering — orchestration, audio, and the Ghost HUD</b></summary>

#### One router, multiple engines

The central `Brain` routes input to independent speech, language, vision, and device-control engines. The architecture keeps microphone capture, model calls, audio playback, and interface updates as distinct responsibilities connected through the orchestration layer.

#### More than transcription and a reply

The voice pipeline includes filters for spurious transcription, wake-word sensitivity, speech caching, and coordination between music and spoken output. Android integration uses ADB commands and UI hierarchy parsing. The repository also demonstrates voice-driven email composition and phone workflows.

#### Interface evolution

The project progressed from a CustomTkinter prototype with logs and controls to the Ghost HUD: a compact overlay with a global shortcut and visual feedback for each interaction stage. A WebSocket protocol carries state changes between the Python backend and the interface. The repository includes screenshots of both generations and video demonstrations.

#### Where computation happens

Wake-word detection, speech recognition, speech synthesis, and the Moondream vision path run locally. The documented default conversational model uses Groq, while retrieval and messaging integrations require network access. Windows is the documented setup target; broader platform support remains development work.

</details>

<sub>PYTHON &nbsp; / &nbsp; PYQT6 &nbsp; / &nbsp; WEBSOCKETS &nbsp; / &nbsp; GROQ &nbsp; / &nbsp; OLLAMA &nbsp; / &nbsp; WHISPER &nbsp; / &nbsp; PIPER &nbsp; / &nbsp; ADB</sub>

**[Explore the code ↗](https://github.com/SaiSiddharthBS/Captain_AI)** &nbsp; · &nbsp; [Architecture & demonstrations](https://github.com/SaiSiddharthBS/Captain_AI#readme) &nbsp; · &nbsp; [Watch the Gmail workflow](https://github.com/SaiSiddharthBS/Captain_AI/raw/main/assets/demo_gmail.mp4)

<br>

[Browse all repositories →](https://github.com/SaiSiddharthBS?tab=repositories)

<br>

## Engineering interests

**Embedded systems & avionics**<br>
The intersection of hardware, software, and dependable system behaviour.

**Applied AI & knowledge systems**<br>
Local inference, voice interfaces, graph-backed reasoning, and agents connected to useful tools.

**Product engineering**<br>
Taking an idea through interface design, backend services, packaging, documentation, and releases.

<br>

## Toolbox

**Applications** &nbsp; Python · TypeScript · JavaScript · React · Next.js · Flutter<br>
**Services & data** &nbsp; FastAPI · SQLite · PostgreSQL · FalkorDB<br>
**AI & integration** &nbsp; Ollama · vLLM · Whisper · MCP<br>
**Build & delivery** &nbsp; Git · GitHub Actions · Docker · Cross-platform packaging

<details>
<summary><b>A few things I care about when building</b></summary>

- Interfaces that make the next action obvious.
- Data ownership and practical self-hosting options.
- Traceable outputs and clear limits on what a system knows.
- Documentation and releases that make a project usable beyond my own machine.

</details>

<br>

## Connect

Interested in embedded systems, applied AI, or building useful open-source software?<br>
Start with an issue on the relevant project: **[OpenWave](https://github.com/SaiSiddharthBS/OpenWave/issues)** · **[Neura1](https://github.com/SaiSiddharthBS/Neura1/issues)** · **[Agent Alpha](https://github.com/SaiSiddharthBS/Agent_Alpha/issues)** · **[Captain AI](https://github.com/SaiSiddharthBS/Captain_AI/issues)**.

---

<p align="center"><sub>SAI SIDDHARTH B S &nbsp; / &nbsp; EXPLORING SYSTEMS. BUILDING PRODUCTS.</sub></p>
