## 🖥 VM - Setup

To ensure Macromedia Director 8.5 and this project run smoothly, we recommend using a lightweight Windows 7 virtual machine. 

While Director was originally designed for Windows 98/2000/XP, compatibility mode on Windows 7 provides somewhat stable use.

---

### 💡 Why Use a VM?

- 🧠 **Isolation**: Keeps legacy dependencies and environment changes separate from your main system.
- 💾 **Stability**: Prevents modern OS conflicts with protected mode drivers and Xtras.
- 🧪 **Consistency**: Guarantees a reproducible environment across devs and contributors.
- ⚡ **Lightweight**: Director 8.5 requires very few system resources—ideal for virtualized execution.

![resource_usage](./resource_usage.png 'Idle Resource Usage')

---

### ✅ Recommended Configuration

| Setting            | Value                                 |
|--------------------|----------------------------------------|
| OS                 | [Windows 7 Professional (x64)](https://archive.org/details/Windows7-iso)   |
| RAM                | 4 GB                                   |
| vCPUs              | 2–4                                    |
| VRAM               | 256 MB (3D acceleration enabled)       |
| Storage            | 40–60 GB (SSD-backed if possible)      |
| Display            | 1280x1024 minimum                      |
| Tools              | VMware Tools or VirtualBox Guest Additions |
| Optional           | DirectX 9.0c installed manually        |

> [!NOTE]  
> Make sure to disable Windows Aero and use the **Basic Theme** to reduce graphical overhead and improve compatibility.

Image file for Windows 7 

---

### 🛠 Installation Steps

1. **Install VMware Workstation / VirtualBox**  
  Choose your preferred hypervisor. VMware offers better graphics acceleration for legacy DirectX content.

2. **Create a New Virtual Machine**
  - Select "Windows 7" as the guest OS.
  - Assign 2–4 CPU cores, 4 GB RAM, and 256 MB VRAM.
  - Use a fixed-size virtual disk for performance.

3. **Install Windows 7 Professional x64**
  - You can use any valid ISO with SP1 integrated.
  - Disable Windows Updates post-install to avoid bloat or driver overwrites.

4. **Install Guest Additions / Tools**
  - Enables shared clipboard, folder drag/drop, and 3D acceleration.
  - Reboot the VM after installation.

5. **Install Macromedia Director 8.5**
  - Use a preserved installer (or copy from original media).
  - Install any required Xtras (e.g., `Buddy API`, `FileXtra4`) to `C:\Program Files\Macromedia\Director 8.5\Xtras\` or copy the provided Xtras.

6. **Configure Compatibility Mode**
  - Right-click `Director.exe`
  - `Properties → Compatibility`
  - Check "Run this program in compatibility mode for" → **Windows ME** or **Windows 98** (Windows 2000 works as well)
  - Also check "Run as Administrator" to avoid permission-related crashes.

### 🧪 Troubleshooting

| Issue                         | Solution                                      |
|------------------------------|-----------------------------------------------|
| Director won't launch         | Ensure compatibility mode + admin is enabled |
| Graphical glitches            | Use Basic Theme, disable Aero                |
| Save errors (bitmap bug)      | Loop through all bitmaps before saving       |
| Projector doesn't run         | Make sure all required Xtras are present     |
| Slow rendering                | Enable 3D acceleration + Guest Additions     |


