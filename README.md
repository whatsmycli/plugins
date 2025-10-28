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

| Plugin | Description | Source |
|--------|-------------|--------|
| *(coming soon)* | Be the first to contribute! | - |

## Using Plugins

**Install location**:
- Linux: `/usr/lib/whatsmy/plugins/`
- Windows: `C:\Program Files\whatsmy\plugins\`
- macOS: `/usr/local/lib/whatsmy/plugins/`

**Run**: `whatsmy <plugin-name>`

## Contributing

### Requirements
- Binaries for all three platforms (Linux, Windows, macOS)
- Link to public source repository
- GPLv3-compatible license

### Process
1. Fork this repository
2. Create folder: `plugins/yourplugin/`
3. Add binaries: `linux.so`, `windows.dll`, `macos.dylib`
4. Update this README table
5. Open Pull Request with source link

See [plugin-template](https://github.com/whatsmycli/plugin-template) for development guide.

## Guidelines

- **API**: Implement `plugin_run()` function
- **Naming**: Lowercase folder names, no spaces
- **Binaries**: Exact names: `linux.so`, `windows.dll`, `macos.dylib`
- **Source**: Must be publicly available
- **License**: GPLv3-compatible

## License

GNU General Public License v3.0 - All plugins must be open source.

## Resources

- [whatsmy](https://github.com/whatsmycli/whatsmy) - Main project
- [plugin-template](https://github.com/whatsmycli/plugin-template) - Create plugins
