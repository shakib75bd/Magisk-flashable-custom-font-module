# MFFM v11 — Custom Font Magisk Module (by @shakib75bd)

This repository is based on [mistu01/mffmv11](https://github.com/mistu01/mffmv11) and customized by [@shakib75bd](https://github.com/shakib75bd).  
It provides an easy way to **apply custom fonts (English, Bengali, Emoji, etc.)** system-wide on Android through **Magisk**, without depending on the system `fonts.xml` file.

---

## 🧩 About the Project

This Magisk module lets you replace Android’s default fonts using your own `.ttf` or `.otf` files.  
Unlike the original installer version, **this variant uses direct module mode**, which means it:
- Does **not** require `/system/etc/fonts.xml`
- Works even on ROMs where the font installer fails
- Can mix multiple font types (Latin, Bengali, Emoji, Monospace, etc.)

---

## ⚙️ Requirements

- Rooted Android device  
- **Magisk** (Zygisk enabled)  
- **Font Loader Zygisk module** (required to prevent app crashes)  
- Your desired fonts (`.ttf` or `.otf` format)

---

## 🪶 Font Naming Rules (see the existing example too for practical understanding)

> ⚠️ If you have **.otf** format fonts, just rename the font files to **.ttf** in the extension, it will work fine.

> ⚠️ The `Files/` folder is **included** in the original ZIP, it contains
Dank mono and Kohinoor (Bengali) for now. Change as you wish, you own custom fonts.

| Category | Required filenames | Example |
|-----------|--------------------|----------|
| **English / Latin** | `Regular.ttf`, `Bold.ttf`, `Italic.ttf`, `BoldItalic.ttf` | `DankMono-Regular.otf` → `Regular.ttf` |
| **Bengali** | `Beng-Regular.ttf`, `Beng-Medium.ttf`, `Beng-Bold.ttf` | `SolaimanLipi.ttf` → rename/copy to all three |
| **Optional** | `Emoji.ttf`, `Mono-Regular.ttf`, `Serif-Regular.ttf`, etc. | Add if needed |

If you have only one Bengali font file, duplicate it for the Medium and Bold variants.

---

## 🪄 How to Build and Flash

1. Simply clone this repo.
2. Place and rename your fonts inside `Files/` folder according to the table above.
3. Select all project contents and **zip them** (don’t include an extra parent folder).  
   The ZIP root should show:
   ```
   Files/
   META-INF/
   module.prop
   customize.sh
   ```
4. Flash the ZIP in Magisk → *Modules → Install from storage*.
5. Reboot.

---

## ✅ After Installation

- Your system will now use your selected fonts globally.  
- If fonts do not appear:
  - Ensure **Zygisk** is enabled in Magisk settings.
  - Check that **Font Loader** is installed and active.
  - Force-close or clear cache of affected apps.
  - If Google apps still display the old fonts after flashing, try flashing the KillGMSFont Magisk module: https://github.com/MrCarb0n/killgmsfont. This often resolves Google-app font issues.

---

## ⚠️ Notes

- This module works completely offline; no font extraction or `fonts.xml` parsing.
- Safe to combine with other Magisk visual mods (bootanimation, system theming, etc.).
- Always keep a backup of your working font module before replacing or editing fonts.

---

## 🧑‍💻 Maintainer

**Author:** [@shakib75bd](https://github.com/shakib75bd)  
**Base Project:** [mistu01/mffmv11](https://github.com/mistu01/mffmv11)

Customized for direct Magisk module installation without `fonts.xml`.

---

## 🖋️ License

This project follows the same open-source license as the original [mistu01/mffmv11](https://github.com/mistu01/mffmv11) repository.

---
