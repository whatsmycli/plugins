# Example Plugin

A simple example plugin demonstrating platform detection and basic plugin structure.

## Usage

```bash
whatsmy example
```

## Example Output

```
==================================
  Example Plugin for whatsmycli  
==================================

Platform: Linux
System:   Linux 6.17.3-artix1-1

This is a template plugin!
Replace this code with your own implementation.

Tip: Return 0 for success, non-zero for errors.
```

## Purpose

This plugin serves as:
- **Minimal example** for plugin developers
- **Template** for creating new plugins
- **Test case** for the plugin loading system

## Features

- Cross-platform detection (Linux, Windows, macOS)
- System information via `uname()` on Unix and `GetVersionEx()` on Windows
- Simple, readable code structure
- Full exception handling

## Platform Support

- ✅ Linux (fully functional)
- ⏳ Windows (pending testing)
- ⏳ macOS (pending testing)

## Source

This plugin is built from the plugin template: [plugin-template](https://github.com/whatsmycli/plugin-template)

## For Developers

Use this as a starting point for your own plugins. The template includes:
- CMakeLists.txt for cross-platform builds
- Platform detection patterns
- Error handling examples
- Complete documentation

## License

GPLv3

