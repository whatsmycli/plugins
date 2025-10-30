# whatsmycli Plugins

Official community plugin repository for **[whatsmy](https://github.com/whatsmycli/whatsmy)**.

Verified, open-source plugin binaries for Linux, Windows, and macOS.

## Structure

Each plugin has its own folder with platform-specific binaries:

```
plugins/
└── example/
    ├── linux.so
    ├── windows.dll
    └── macos.dylib
```

The folder name is the command: `whatsmy example`

## Available Plugins

| Plugin | Description | Platforms | Source |
|--------|-------------|-----------|--------|
| **example** | Simple platform detection example | Linux, Windows, macOS | [plugin-template](https://github.com/whatsmycli/plugin-template) |

## Using Plugins

**Install plugins:**
```bash
whatsmy plugin install <name>
```

**List available:**
```bash
whatsmy plugin list
```

**Run plugin:**
```bash
whatsmy <plugin-name>
```

## Contributing

See [plugin-template](https://github.com/whatsmycli/plugin-template) for how to create plugins.

## License

GNU General Public License v3.0 - All plugins must be open source.

## Resources

- [whatsmy](https://github.com/whatsmycli/whatsmy) - Main project
- [plugin-template](https://github.com/whatsmycli/plugin-template) - Create plugins
