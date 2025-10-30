# whatsmycli Plugins

Official community plugin repository for **[whatsmy](https://github.com/whatsmycli/whatsmy)**.

Verified, open-source plugin binaries for Linux, Windows, and macOS.

## Structure

Each plugin has its own folder with platform-specific binaries:

```
plugins/
└── gpu/
    ├── linux.so
    ├── windows.dll
    └── macos.dylib
```

The folder name is the command: `whatsmy gpu`

## Available Plugins

| Plugin | Description | Platforms | Source |
|--------|-------------|-----------|--------|
| **gpu** | GPU detection and information | Linux | [plugin-gpu](https://github.com/whatsmycli/plugin-gpu) |
| **example** | Simple platform detection example | Linux | [plugin-template](https://github.com/whatsmycli/plugin-template) |

**Note**: Windows and macOS binaries pending. Linux binaries are fully functional.

## Using Plugins

**Install location**:
- Linux: `/usr/lib/whatsmy/plugins/`
- Windows: `C:\Program Files\whatsmy\plugins\`
- macOS: `/usr/local/lib/whatsmy/plugins/`

**Run**: `whatsmy <plugin-name>`

## Contributing

See [plugin-template](https://github.com/whatsmycli/plugin-template) for how to create plugins.

## License

GNU General Public License v3.0 - All plugins must be open source.

## Resources

- [whatsmy](https://github.com/whatsmycli/whatsmy) - Main project
- [plugin-template](https://github.com/whatsmycli/plugin-template) - Create plugins
