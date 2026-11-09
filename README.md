# RenderNames

- updated: it now has a checkbox "Save Changes Globally" which saves your setting overall - so it is not scene dependent but for all blend files.
  If you uncheck it, it works as before.

<img width="188" height="66" alt="image" src="https://github.com/user-attachments/assets/0841e9f4-0a94-4a1a-bc82-9d91b30236b4" />


**Smart render output naming for Blender that actually makes sense.**

Stop manually renaming files. Stop creating folders. Stop losing track of which render is which.

RenderNames gives you **template-based file naming** with live preview, automatic folder organization, and preset management—built right into Blender's Output Properties panel.

![RenderNames Cover](https://github.com/user-attachments/assets/47ef10e7-b964-448b-b4a9-9be0b044becd)

---

## Why This Exists

Blender's render output? It's just a text field. No variables, no organization, no help.

You end up with:
- `untitled.png`, `untitled0001.png`, `final_final_ACTUAL.png` 😅
- Manual folder creation for every project
- No consistency across scenes or cameras
- Constant fear of overwriting your best render

**RenderNames fixes this.** One template, infinite possibilities.

```
{{blend_file}}/{{date}}/{{scene}}_
→ my_project/2025-01-15/Scene_0001.png
```

Blender adds frame numbers automatically. You handle the rest.

---

## Features

🎯 **Template Variables** — Mix `{{scene}}`, `{{camera}}`, `{{date}}`, `{{resolution}}`, and more  
👁️ **Live Preview** — See your output path as you type  
📁 **Auto Folders** — Organize by scene, camera, or date  
💾 **Presets** — Save and share your favorite setups  
🔧 **Blender Native** — Lives in Output Properties (no weird UI)  
⚡ **Non-Destructive** — Enable/disable without losing settings  

![RenderNames Features](https://github.com/user-attachments/assets/803acf15-f12c-4601-b232-d80f96e313c8)

---

## Installation

1. Download the latest `.zip` from [Releases](https://github.com/novincode/rendernames/releases)
2. In Blender 4.2+: `Edit → Preferences → Extensions → Install from Disk`
3. Select the zip, enable the extension
4. Go to Output Properties and start templating

**Need help?** See [Installation Guide →](docs/INSTALL.md)

---

## Quick Start

1. Open **Output Properties** (printer icon)
2. Enable **RenderNames**
3. Pick a preset or edit the template
4. Render — your files land exactly where shown in the preview

---

## Template Variables

| Variable | Output |
|----------|--------|
| `{{scene}}` | Scene name |
| `{{blend_file}}` | Your .blend filename |
| `{{camera}}` | Active camera |
| `{{date}}` | Today's date (YYYY-MM-DD) |
| `{{time}}` | Current time (HH-MM-SS) |
| `{{datetime}}` | Combined date + time |
| `{{resolution}}` | Render resolution (1920x1080) |
| `{{fps}}` | Frame rate |
| `{{format}}` | Output format (png, exr, etc.) |
| `{{engine}}` | Render engine (cycles, eevee) |
| `{{samples}}` | Sample count |

**More variables?** [See full reference →](docs/variables.md)

---

## Example Templates

**Simple:**
```
{{scene}}_
```

**Professional:**
```
{{blend_file}}/{{date}}/{{scene}}_{{camera}}_
```

**Timestamped:**
```
renders/{{datetime}}/{{scene}}_
```

Blender automatically adds frame numbers (0001, 0002, ...) to animations. The preview shows you exactly what you'll get.

---

## Built-in Presets

Default presets ready to go:

- **Simple** — Just scene name
- **Professional** — Full folder structure with date and camera
- **Archival** — Timestamped for versioning
- **By Camera** — Organized by camera name
- **Minimal** — Bare minimum

Create your own custom presets, export as JSON, and unlock consistency across your entire team.

![RenderNames Presets](https://github.com/user-attachments/assets/7016cb90-8fa8-4451-ad40-59fb570c6458)

---

## Documentation

- 📖 [Installation Guide](docs/INSTALL.md) — Setup and troubleshooting
- 📋 [Full Variable Reference](docs/variables.md) — All template variables
- 🏗️ [Architecture](docs/architecture.md) — How it works (for developers)
- 📝 [Changelog](CHANGELOG.md) — Version history
- 👁️ [Design Vision](docs/vision.md) — Why we built it this way

---

## Compatibility

✅ Blender 4.2+  
✅ Blender 5.0+  
❌ Blender 4.1 and earlier (requires extension system)

---

## Support the Project

If RenderNames saves you time, consider supporting development:

- ⭐ **Star on GitHub** — it really helps others find this
- 💬 **Report bugs** or [request features](https://github.com/novincode/rendernames/discussions)
- ❤️ **Sponsor development** → [github.com/sponsors/novincode](https://github.com/sponsors/novincode)

---

## Development

Want to contribute or build from source?

```bash
git clone https://github.com/novincode/rendernames.git
cd rendernames
python3 scripts/build.py
```

[See DEVELOPMENT guide →](docs/DEVELOPMENT.md)

---

## License

GPL-3.0-or-later — Same as Blender.

**Made by humans who got tired of manually naming render files.** 🎬
