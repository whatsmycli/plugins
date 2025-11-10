# GPU Detection Plugin

Cross-platform GPU detection plugin for whatsmycli that displays graphics card information.

## Description

The GPU plugin provides detailed information about graphics cards in your system, including vendor identification, driver versions, and PCI IDs. It supports multiple GPUs and works across Linux, Windows, and macOS.

## Features

- **Active GPU Display**: Show information about the primary/active GPU
- **Multi-GPU Support**: List all GPUs in systems with multiple graphics cards
- **Index Selection**: Query specific GPU by index number
- **Cross-Platform**: Works on Linux, Windows, and macOS
- **Vendor Detection**: Identifies NVIDIA, AMD, Intel, and other GPU vendors
- **Driver Information**: Shows installed driver version (when available)
- **PCI Identification**: Displays PCI vendor and device IDs

## Installation

### Using Plugin Manager (Recommended)

```bash
whatsmy plugin install gpu
```

### Manual Installation

**Linux**:
```bash
mkdir -p ~/.local/share/whatsmy/plugins/gpu
curl -L https://raw.githubusercontent.com/whatsmycli/plugins/main/gpu/linux.so -o ~/.local/share/whatsmy/plugins/gpu/linux.so
```

**Windows**:
```powershell
New-Item -ItemType Directory -Path "$env:PROGRAMFILES\whatsmy\plugins\gpu" -Force
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/whatsmycli/plugins/main/gpu/windows.dll" -OutFile "$env:PROGRAMFILES\whatsmy\plugins\gpu\windows.dll"
```

**macOS**:
```bash
mkdir -p /usr/local/lib/whatsmy/plugins/gpu
curl -L https://raw.githubusercontent.com/whatsmycli/plugins/main/gpu/macos.dylib -o /usr/local/lib/whatsmy/plugins/gpu/macos.dylib
```

## Usage

### Basic Commands

Show active/default GPU:
```bash
whatsmy gpu
```

Show all GPUs:
```bash
whatsmy gpu all
```

Show specific GPU by index:
```bash
whatsmy gpu 0
whatsmy gpu 1
```

Show help:
```bash
whatsmy gpu help
```

## Information Displayed

- **GPU Name**: Model or description with PCI ID
- **Vendor**: NVIDIA, AMD, Intel, or Unknown
- **Driver Version**: Currently installed driver (when available)
- **PCI ID**: Vendor:Device identification in hexadecimal
- **Index**: GPU number in multi-GPU systems
- **Active Status**: Whether the GPU is the primary/active GPU

## Platform-Specific Details

### Linux
- Reads GPU information from `/sys/class/drm/`
- Detects NVIDIA, AMD, and Intel GPUs via PCI IDs
- Extracts NVIDIA driver version from `/proc/driver/nvidia/version`
- Requires read permissions to `/sys/` filesystem

### Windows
- Uses Windows Setup API for device enumeration
- Queries display adapter information from Device Manager
- Shows manufacturer, device description, and driver info
- Parses hardware IDs for PCI vendor/device codes

### macOS
- Uses IOKit framework
- Compatible with both Intel and Apple Silicon Macs
- Detects integrated and discrete GPUs

## Examples

**Single GPU system**:
```bash
$ whatsmy gpu

GPU 0 (Active)
==================================================
  Name: NVIDIA GPU [10DE:1C82]
  Vendor: NVIDIA
  Driver Version: 580.95.05
  PCI ID: 10DE:1C82
```

**Multi-GPU system**:
```bash
$ whatsmy gpu all

All GPUs (2 detected)
==================================================
GPU 0 (Active)
  Name: NVIDIA GPU [10DE:1C82]
  Vendor: NVIDIA
  PCI ID: 10DE:1C82

GPU 1
  Name: Intel GPU [8086:5912]
  Vendor: Intel
  PCI ID: 8086:5912
```

## Version

**Current Version**: 1.0.0

## Source Code

Source code is available at: https://github.com/whatsmycli/plugin-gpu

## License

GPLv3

## Contributing

Contributions are welcome! Please submit issues and pull requests to the [plugin-gpu repository](https://github.com/whatsmycli/plugin-gpu).

## Support

For issues or questions:
- Plugin issues: https://github.com/whatsmycli/plugin-gpu/issues
- General whatsmycli issues: https://github.com/whatsmycli/whatsmy/issues

