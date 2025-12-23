<div align="center">

# EnderCNC

**Transform Your Ender 3 PRO Into a Powerful CNC Machine**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Discord](https://img.shields.io/discord/YOUR_DISCORD_ID?color=7289da&logo=discord&logoColor=white)](https://discord.gg/f6FjTJYpcy)
[![Printables](https://img.shields.io/badge/Printables-Model-orange.svg)](https://www.printables.com/model/1318299-e3cnc-ender-3-pro-based-cnc)
[![GitHub Stars](https://img.shields.io/github/stars/yahyasvm/EnderCNCs?style=social)](https://github.com/yahyasvm/EnderCNCs/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/yahyasvm/EnderCNCs?style=social)](https://github.com/yahyasvm/EnderCNCs/network/members)

![EnderCNC Main Image](https://github.com/user-attachments/assets/df2746be-0fd8-4aa2-b609-81031dc4cfa2)

*Maximum reuse. Minimal cost. Maximum capability.*

[Documentation](#documentation) • [Quick Start](#quick-start) • [Community](#community) • [Download Files](https://www.printables.com/model/1318299-e3cnc-ender-3-pro-based-cnc/files)

</div>

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Project Versions](#project-versions)
- [Specifications](#specifications)
- [Quick Start](#quick-start)
- [Documentation](#documentation)
- [Repository Structure](#repository-structure)
- [Hardware Requirements](#hardware-requirements)
- [Software & Tools](#software--tools)
- [Community & Support](#community)
- [Contributing](#contributing)
- [Credits](#credits)
- [License](#license)

---

## Overview

**EnderCNC** is an open-source project that converts the popular Creality Ender 3 PRO 3D printer into a fully functional CNC machine. Born from a passion for CAD design and a desire to repurpose spare printer parts, this project offers an affordable and accessible entry point into CNC machining.

### Why EnderCNC?

- **Budget-Friendly**: ~$60 BOM cost (excluding Ender 3 PRO and spindle/dremel)
- **Maximum Reuse**: Utilizes frame, steppers, wiring, screws, and more from your existing printer
- **Beginner-Friendly**: Perfect for those new to CNC with extensive documentation
- **Modular Design**: Multiple versions and mods available for different needs
- **Active Community**: Growing Discord community for support and inspiration

---

## Features

### Core Features

- Klipper-Ready: Designed to work with Klipper firmware (GRBL compatible as well)
- Reuses 90%+ of Ender 3 PRO Parts: Frame, motors, MCU, PSU, and more
- Multiple Tool Support: Dremel rotary tools, spindles (Ø52-65mm)
- Linear Rail Z-Axis: Improved accuracy with dual linear rails
- Fusion 360 Compatible: Includes custom post-processor for easy CAM workflow
- Scalable Design: Easy to modify cutting area to your needs
- Open Source CAD: Full Fusion 360 files available for customization

### Advanced Features

- Dust management with optional splash guards
- Electronics enclosure for 4.2.2/SKR Pico boards
- Vacuum attachment support
- Self-upgrading capability (can mill its own aluminum upgrades)
- Klipper macros for zero positioning (XYZ)

---

## Project Versions

### Ender3CNC (Budget Version) - RECOMMENDED

The latest and most cost-effective version, designed around maximizing the use of Ender 3 PRO components.

**Status**: Released & Tested  
**BOM Cost**: ~$60 USD (excluding printer & spindle)  
**Based On**: Ender 3 PRO  

![Ender3CNC](https://github.com/user-attachments/assets/43854a83-0945-4e80-aa53-9ccf8a7e4b0b)

**Key Highlights**:
- Minimal additional parts required
- Uses original frame, motors, electronics
- Dual linear rail Z-axis
- Compatible with Ender 3 PRO (4040 extrusion bed frame)
- Active development with regular updates

[View Ender3CNC Files](Ender3CNC/)

---

### EnderCNC (Original Version)

The first-generation design, now in stable "release" state.

**Status**: Stable Release  
**Based On**: Ender 3 PRO + Ender 4 parts  

![Original EnderCNC](https://github.com/user-attachments/assets/9c401c66-4c9e-4997-86d7-50659553de69)

**Note**: This version is feature-complete and will only receive updates for critical issues.

[View Original EnderCNC Files](EnderCNC%20CAD/)

---

### MGN Version (Coming Soon)

**Status**: In Development  
**Based On**: Ender3CNC with MGN linear rails  
**Features**: Larger cutting area, enhanced rigidity

---

## Specifications

### Ender3CNC (Budget Version)

| Specification | Value |
|--------------|-------|
| **Cutting Area** | ~220mm x 220mm x ~150mm (Z) |
| **Frame** | Ender 3 PRO aluminum extrusions |
| **Linear Motion** | V-wheels (X/Y), Dual MGN12 rails (Z) |
| **Motors** | Original Ender 3 steppers |
| **Controller** | Original Ender MCU (Klipper) or upgraded SKR board |
| **Spindle Support** | Dremel-style rotary tools, Ø52-65mm spindles |
| **Power Supply** | Original Ender 3 PSU |
| **Material Capability** | Wood, plastics, soft metals (aluminum with care) |

### Print Settings (for 3D printed parts)

- **Material**: PLA+ recommended
- **Walls**: 5 perimeters
- **Top/Bottom**: 5 layers
- **Infill**: 40% gyroid pattern

---

## Quick Start

### Prerequisites

- Ender 3 PRO 3D printer (or compatible frame)
- Access to a 3D printer for printed parts
- Basic tools (hex keys, screwdrivers, wrenches)
- Spindle or Dremel rotary tool
- ~$60 USD for additional hardware

### Installation Steps

1. **Download Files**
   - Get STL files from [Printables](https://www.printables.com/model/1318299-e3cnc-ender-3-pro-based-cnc/files)
   - Download CAD files for reference or customization

2. **Print Components**
   - Use recommended print settings (5 walls, 40% infill, PLA+)
   - Refer to [BOM](Ender3CNC/BOM.md) for parts list

3. **Source Hardware**
   - Purchase items from [Bill of Materials](Ender3CNC/BOM.md)
   - Most screws and components reused from Ender 3 PRO

4. **Assembly**
   - Follow the [Build Guide](Ender3CNC/Manual.md) (WIP - community contributions welcome!)
   - Join [Discord](https://discord.gg/f6FjTJYpcy) for build support

5. **Software Setup**
   - Install Klipper firmware (or GRBL if preferred)
   - Set up Fusion 360 with [Post Processor](https://github.com/Zergie/mpcnc_post_processor/blob/main/MPCNC.cps)
   - Import [Klipper macros](Macros/) for easy zeroing

6. **Testing & Calibration**
   - Run test cuts on soft materials first
   - Calibrate steps/mm for your configuration
   - Start with conservative feeds and speeds

---

## Documentation

### Essential Guides

| Document | Description | Link |
|----------|-------------|------|
| **Bill of Materials** | Complete parts list with quantities and sources | [BOM.md](Ender3CNC/BOM.md) |
| **Build Manual** | Step-by-step assembly instructions (WIP) | [Manual.md](Ender3CNC/Manual.md) |
| **Fusion 360 Post Processor** | Setup guide for CAM toolpath generation | [fusion360 post processor.md](Ender3CNC/fusion360%20post%20processor.md) |
| **Klipper Macros** | XYZ zero positioning macros | [Macros/](Macros/) |
| **Changelog** | Project update history | [Changelog.md](Changelog.md) |
| **CAD Information** | Details about design files | [CAD.md](Ender3CNC/CAD/CAD.md) |

### Mods & Upgrades

Explore community modifications and upgrades:

- [2040 Frame Mod](Ender3CNC/Mods/2040_frame_mod/) - For Ender 3 Non-Pro
- [Rod Mod](Ender3CNC/Mods/E3CNC%20RodMod/) - Alternative Z-axis design
- [Faceplate Dremel Mod](Ender3CNC/Mods/Faceplate%20Dremel%20mod/) - Enhanced tool mounting
- [Non-Pro X Gantry](Ender3CNC/Mods/) - Ender 3 Non-Pro compatibility

---

## Repository Structure

```
EnderCNCs/
│
├── README.md                          # This file - project overview
├── Changelog.md                       # Version history and updates
├── LICENSE                            # Project license
│
├── Ender3CNC/                         # Main budget version (RECOMMENDED)
│   ├── readme.md                      # Version-specific info
│   ├── BOM.md                         # Bill of materials
│   ├── Manual.md                      # Build instructions
│   ├── fusion360 post processor.md   # CAM setup guide
│   │
│   ├── CAD/                           # Design files
│   │   ├── E3CNC_18.11.25.f3z        # Fusion 360 archive
│   │   ├── Ender3Pro_cheap_cnc.step  # STEP file
│   │   └── CAD.md                     # CAD documentation
│   │
│   ├── Mods/                          # Community modifications
│   │   ├── 2040_frame_mod/           # Non-Pro frame adaptation
│   │   ├── E3CNC RodMod/             # Alternative Z-axis
│   │   ├── Faceplate Dremel mod/     # Tool mounting options
│   │   └── ender3nonpro stl/         # Non-Pro specific parts
│   │
│   └── User-Builds/                   # Community builds showcase
│
├── EnderCNC CAD/                      # Original version (stable)
│   ├── EnderCNC_release.f3d          # Fusion 360 file
│   └── README.md                      # Original version info
│
└── Macros/                            # Klipper configuration
    ├── E3CNC_ZERO_MACROS.cfg         # Zero position macros
    └── README.md                      # Macro documentation
```

---

## Hardware Requirements

### From Your Ender 3 PRO (Reused)

- Aluminum extrusion frame (4040 bed frame for PRO)
- 4x Stepper motors (X, Y, Z, E becomes A-axis if needed)
- Lead screw + nut + coupler
- MCU board (stock 4.2.x or upgraded SKR)
- Power supply
- V-wheels and spacers
- Most screws, nuts, and bolts
- Wiring (may need extensions)
- LCD screen (optional)

### Additional Parts to Purchase

| Category | Items | Approx. Cost |
|----------|-------|-------------|
| **Linear Rails** | 2x MGN12H rails for Z-axis | $20-30 |
| **Fasteners** | M3/M5 T-nuts, additional screws | $10-15 |
| **Spindle/Tool** | Dremel or 52-65mm spindle | $30-100 |
| **Miscellaneous** | Spoilboard, clamps, wiring | $10-20 |

**Total Additional**: ~$60-80 USD (excluding spindle)

[Complete BOM with links](Ender3CNC/BOM.md)

---

## Software & Tools

### Required Software

| Software | Purpose | Cost | Link |
|----------|---------|------|------|
| **Fusion 360** | CAD/CAM design | Free (Personal) | [Autodesk](https://www.autodesk.com/products/fusion-360/) |
| **Klipper** | Machine control firmware | Free | [Klipper3d](https://www.klipper3d.org/) |
| **Mainsail/Fluidd** | Web interface for Klipper | Free | [Mainsail](https://docs.mainsail.xyz/) |

### Alternative Options

- **GRBL**: Alternative firmware for CNC control
- **UGS / CNCjs**: GRBL-compatible control software
- **FreeCAD**: Open-source CAD alternative

### Post Processor

- Custom Fusion 360 post processor (Klipper-compatible)
- Credit: [Zergie](https://github.com/Zergie/mpcnc_post_processor/)
- Installation guide: [fusion360 post processor.md](Ender3CNC/fusion360%20post%20processor.md)

---

## Community

### Get Help & Share Your Build

[![Join Discord](https://img.shields.io/badge/Discord-Join%20Server-7289da?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/f6FjTJYpcy)

- **Discord Server**: Active community for questions, troubleshooting, and sharing builds
- **GitHub Issues**: Report bugs or request features
- **Printables Comments**: Share your makes and ask questions

### Show Your Build

We'd love to see your EnderCNC in action! Share photos and videos:
- Upload your build to [User-Builds](Ender3CNC/User-Builds/)
- Post in Discord #build-showcase
- Tag your Printables make

---

## Contributing

Contributions are welcome! Here's how you can help:

### Ways to Contribute

1. **Report Issues**: Found a bug? Open an issue with details
2. **Improve Documentation**: Submit PRs for clearer guides
3. **Share Mods**: Create and share your custom modifications
4. **Document Your Build**: Help others with photo build guides
5. **Suggest Features**: Share ideas for improvements

### Contribution Guidelines

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingMod`)
3. Commit your changes (`git commit -m 'Add amazing mod'`)
4. Push to the branch (`git push origin feature/AmazingMod`)
5. Open a Pull Request

---

## Credits

### Project Creator

- **Original Creator**: [Futtawuh](https://github.com/Futtawuh)

### Contributors & Community

- **Shadowphyre**: BEEFY dremel clamps, front corner 20mm mod
- **Ravenspecial**: Rod mod contributions
- **Zergie**: Fusion 360 post processor
- **Community**: Discord members for testing, feedback, and mods

### Inspirations

- [MPCNC](https://www.v1engineering.com/) - Mostly Printed CNC
- [Ender3dent](https://github.com/yell3D/Ender3dent) - Ender Trident mod

---

## License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

### What This Means

- Free to use for personal and commercial projects
- Modify and distribute as you wish
- Attribution appreciated but not required
- Provided "as is" without warranty

---

## Contact & Links

### Project Maintainer

- **GitHub**: [@yahyasvm](https://github.com/yahyasvm)
- **Discord**: ravenkeeper

### Project Links

- **GitHub Repository**: [EnderCNCs](https://github.com/yahyasvm/EnderCNCs)
- **Printables**: [E3CNC Model](https://www.printables.com/model/1318299-e3cnc-ender-3-pro-based-cnc)
- **Discord Community**: [Join Server](https://discord.gg/f6FjTJYpcy)

---

<div align="center">

### Star this project if you find it useful!

**Made by the EnderCNC Community**

*From 3D Printer to CNC Machine - The Ultimate Upcycle*

</div>
