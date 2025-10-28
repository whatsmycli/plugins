# GPU Plugin

Detects and displays GPU (graphics card) information.

## Usage

```bash
whatsmy gpu
```

## Example Output

```
GPU Information
==================================================

Name:           NVIDIA GeForce GTX 1050 Ti
Vendor:         NVIDIA
PCI ID:         0x10de:0x1c82
Driver Version: 580.95.05  Tue Sep 23 10:11:16 UTC 2025
```

## Features

- **Linux**: Reads from `/sys/class/drm/` and `/proc/driver/nvidia/version`
- **Windows**: Uses Setup API for device enumeration
- **macOS**: Planned - IOKit framework integration

## Platform Support

- ✅ Linux (fully functional)
- ⏳ Windows (pending testing)
- ⏳ macOS (pending implementation)

## Source

Full source code and build instructions: [plugin-gpu](https://github.com/whatsmycli/plugin-gpu)

## License

GPLv3

