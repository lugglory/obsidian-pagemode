# Review Notes

This document records intentional decisions around Obsidian plugin review warnings that are currently left unresolved.

## `PluginSettingTab.display()` Deprecation

Obsidian marks `PluginSettingTab.display()` as deprecated since Obsidian `1.13.0` and recommends `getSettingDefinitions()`.

PageMode intentionally keeps `display()` for now.

Using `getSettingDefinitions()` would require raising `minAppVersion` to `1.13.0`. PageMode currently supports Obsidian `1.6.6` and newer. Keeping `display()` preserves compatibility with older supported Obsidian versions.

This recommendation is accepted until PageMode is ready to require Obsidian `1.13.0` or newer.
