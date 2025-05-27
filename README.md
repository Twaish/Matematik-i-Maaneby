# Måneby Preservation Project

Unprotected files for educational game Matematik i Maaneby by Bitfrost Interactive I/S and later associated with **Darkhill Games**. The game was built using **Macromedia Director** and distributed as a standalone Shockwave projector executable.

![game_preview](docs/game_preview.png 'Game Preview')

## 🗂️ Contents

The repository contains:

- Unprotected `.dir` files containing original game assets and scripts
- Configuration files (e.g. `BrugerT.txt`)
- Original Xtras used by the game (e.g. Buddy API, FileXtra4)
- Projector executables (`Maaneby.exe`, `MaanebyV.exe`) for analysis

## 🛠️ Tools Used

- [ProjectorRays](https://github.com/ProjectorRays/ProjectorRays): for decompiling protected Director `.dcr` files
- [Macromedia Director 8.5](https://archive.org/details/macromediadirector85): for inspecting `.dir` files including Serial Number (key) for activating the software

## 🧪 Setting Up the Development Environment

> [!NOTE]  
> **Macromedia Director 8.5** was released during the era of Windows 98 and Windows ME. 


1. **Install Macromedia Director 8.5**
  - To run effectively on a newer Windows version, set the compatibility mode for the Macromedia Director executable to Windows 2000, through properties menu.

2. **Use a Virtual Machine (Recommended)**
  - See `/docs/vm_setup.md` for instructions on creating a stable VM.
  - Ensure 3D acceleration is enabled if using legacy Xtras that depend on DirectX.

3. **Required Xtras**
   - Confirm that the included `Xtras/` folder is present **in the same directory** as the `.dir` files or linked via Director’s search paths.
   - Key Xtras: `Buddy API`, `FileXtra4`, `DirectOS`, etc.

## 🧩 Opening the Project

To explore the game's structure and logic:

1. Open **Macromedia Director 8.5** or a compatible version.
2. Use `File > Open` to load any of the unprotected `.dir` files from this repository.
3. You can browse the movie timeline, inspect cast members, and read or edit the original Lingo scripts and textures.

> [!WARNING]  
> Ensure the included `Xtras/` folder is accessible from Director’s search path for full functionality (e.g., Buddy API, FileXtra4).

![editor_preview](docs/editor_preview.png 'Editor Preview')

From here you can edit the game how you like. **[INGAME]**
![modded_preview](docs/modded_preview.png 'Modded Preview')

### 🛠 Known Issue: Save Failures Due to Unloaded Bitmaps

**Problem:**  
Macromedia Director may occasionally fail to save the project correctly if not all bitmap assets have been rendered or "seen" in the cast window or playback. This behavior is due to how Director lazily loads certain media elements.

**Workaround:**  
Before saving, ensure that all bitmap assets have been loaded at least once.

**Quick Method:**

1. Open a bitmap from the asset inspector.
2. **Hold down the Left or Right Arrow key** on your keyboard to cycle through the timeline.
3. Let the playback loop briefly to force-load all bitmap elements.
4. Once all bitmaps have been visually rendered at least once, you can safely save the project.

This ensures all media are fully initialized and prevents corruption or asset loss during the save process.


## 🎯 Purpose

This project exists to:

- Enable educational use and possible reinterpretation or reimplementation of the game's ideas

## 📜 License & Legal

All content is provided **for archival, educational, and non-commercial use only**. The rights to *Måneby* remain with the original developers and publishers. If you are the rights holder and wish to request changes or takedown, please contact the repository maintainer.

## 🙌 Credits

- Original Developers: **Bitfrost Interactive I/S**, possibly in collaboration with **Darkhill Games**