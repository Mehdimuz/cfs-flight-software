# Core Flight System (cFS) Flight Software

This repository contains the modular flight software architecture for a space mission using NASA's Core Flight System (cFS). The structure supports scalable app development for various mission needs such as attitude control, thermal management, and payload handling.

## 📁 Project Structure

- `bsp/` – Board Support Package (startup code, platform-specific)
- `build/` – CMake scripts and toolchain configuration
- `config/` – Mission- and platform-specific constants and tables
- `core_apps/` – Core cFS apps like Executive Services, Software Bus, etc.
- `mission_apps/` – Mission-specific logic like ADCS, thermal control, power
- `platform_services/` – Hardware drivers and HAL
- `fs_data/` – Flight file system structure (logs, tables)
- `safe_mode/` – Safe boot and watchdog handling
- `test/` – Unit, integration, and HIL testing
- `ground_interface/` – Telemetry/command definitions and ground system tools

## 🚀 How to Build

This project uses CMake. Example:

```bash
mkdir -p build
cd build
cmake ..
make

[200~
---

### ✅ 2. **Create `.gitignore`**
```bash
cat > .gitignore << 'EOF'
# C/C++ build files
build/
*.o
*.out
*.exe
*.a
*.so
*.swp

# CMake
CMakeCache.txt
CMakeFiles/
Makefile
cmake_install.cmake
compile_commands.json

# Editor/OS clutter
.DS_Store
Thumbs.db
.vscode/
.idea/

# Logs or output
*.log
*.bin
*.elf
*.map
