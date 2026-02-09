<div align="center">

# 🤖 irobot

### *Intelligent. Modular. Build-Free.*

The central software ecosystem for the **iHuman Lab**, designed to decouple robotics hardware from algorithmic research.

</div>

---

## 🎯 What is irobot?

In the **Intelligent Human-Machine Nexus Lab**, we believe researchers should spend their time on *intelligence*, not *infrastructure*.

**irobot** is a "Nexus" repository. It uses **Sugarcoat** to allow students and researchers to build complex, multi-file robotics projects in **pure Python**. No more waiting for `colcon build` every time you change a line of code.

## ✨ Key Features

| Feature | Benefit |
| --- | --- |
| ⚡ **Zero-Build Momentum** | Save your Python file and run. No compilation required. |
| 🧱 **Project Isolation** | Every project lives in its own folder with its own logic. |
| 🤖 **Robot-Agnostic** | Write an algorithm once; run it on any lab robot. |
| 🎛️ **Live Parameter Tuning** | Use auto-generated Web UI sliders to tweak math on the fly. |
| 🧩 **Nexus Utility Library** | Shared lab safety, math, and human-interaction tools. |

## 🚀 Quick Start

### Installation

```bash
# Clone the nexus
git clone https://github.com/iHuman-Lab/irobot.git
cd irobot

# One-time setup: Add src to your Python path
echo "export PYTHONPATH=\$PYTHONPATH:\$(pwd)/src" >> ~/.bashrc
source ~/.bashrc

# Install the framework
pip install sugarcoat-robotics

```

### Run Your First Nexus Project

```python
# src/projects/example_nexus/main_recipe.py
from sugar.launcher import Launcher
from src.common_lab.robot_configs import LabMobileBase
from .modules.brain import MyAlgorithm

# 1. Grab a standard lab robot
launcher = LabMobileBase(name="Nexus_Bot_01")

# 2. Inject your logic (the "Mind")
launcher.add_component(MyAlgorithm())

# 3. Enable the tuning dashboard
launcher.enable_ui()

# 4. Bring it to life!
launcher.bringup()

```

## 📁 Project Structure

```text
irobot/
├── drivers/             # 🏗️ HARDWARE: Built once (LIDAR, Motors, etc.)
└── src/                 # 🧠 LOGIC: Pure Python (The "Nexus")
    ├── common_lab/      # 🤝 SHARED: Robot configs & safety logic
    └── projects/        # 🚨 RESEARCH: Your independent projects
        ├── human_intent/
        ├── rescue_grid/
        └── [your_project]/

```

## 🧪 The iHuman Workflow

1. **Branch:** `git checkout -b project/your-project-name`
2. **Develop:** Create your 10+ files in your project subfolder.
3. **Execute:** Run `python3 main_recipe.py`.
4. **Iterate:** Change logic, save, and re-run. **Total time: < 2 seconds.**

## 📄 License

MIT License - Feel free to use this for your research!

---

<div align="center">

**Intelligent Human-Machine Nexus Lab**

*Bridging the gap between human intent and machine action.*

</div>
