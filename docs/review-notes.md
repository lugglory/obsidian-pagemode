# Review Notes

## Settings API compatibility

PageMode implements `getSettingDefinitions()` so that Obsidian 1.13.0 and newer can render and search its settings.

The `display()` override remains as a fallback for older versions, preserving the minimum supported Obsidian version of 1.6.6. Both paths share the same definitions and rendering callbacks, including saving, archive-path normalization, and archive-folder visibility updates.

The new settings types are imported only for type checking; no new runtime API is required by the fallback.

See the official [dual-support migration guide](https://docs.obsidian.md/plugins/guides/migrate-declarative-settings).
