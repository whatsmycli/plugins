# 🧩 whatsmycli Plugins

Official community plugin repository for **[whatsmy](https://github.com/whatsmycli/whatsmy)** —  
a fast, minimal, and extensible cross-platform system information CLI.

This repository hosts **verified, open-source plugin binaries** for Linux, macOS, and Windows.  
Contributions are accepted via **Pull Request (PR)**.

---

## 📦 How this repository works

- Each plugin should be added under its own folder:
plugins/
weather/
linux.so
windows.dll
mac.dylib

- Only **compiled binaries** are required.  
- The PR **must include a link** to the plugin's **original source repository**.  
- You are **not required to submit source code** here — only verified, open-source binaries.

> ⚠️ All submissions must be open-source. Proprietary or closed-source binaries will **not** be accepted.

---

## ⚡ Using Plugins

Once a plugin is merged into this repository, it can be invoked from **whatsmycli** using the **plugin folder name** as the command.  

For example, if a plugin is added under:
plugins/weather/
linux.so
windows.dll
mac.dylib


You can call it with:

```bash
whatsmy weather
```

The folder name becomes the plugin command.

Ensure the plugin binaries are correctly placed for your operating system.

---

## 🚀 Contributing a Plugin

1. Fork this repository  
2. Add your plugin binaries to a **new folder** (one folder per plugin)  
3. Make a PR with:
   - Folder containing binaries (`.so`, `.dll`, `.dylib`)  
   - Link to the plugin's **original source repository**  
   - Short description of what the plugin does  

4. Upon review, the maintainers may merge it.  
   - Maintainers may choose to rebuild the plugin themselves from source if needed.

---

## 📜 License

All plugin binaries in this repository are under the **[GNU General Public License v3.0](../LICENSE)**.  
> All plugins must remain open-source and compatible with the main whatsmycli project.

---

### 🤝 Notes

- This repository serves as a **community-curated plugin registry**.  
- For developing new plugins, see the [plugin-template](https://github.com/whatsmycli/plugin-template) repository.  
- Only maintainers merge PRs; contributors submit binaries and source links for verification.

