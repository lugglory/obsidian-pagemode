# Review Notes

## Settings API compatibility

PageMode implements `getSettingDefinitions()` so that Obsidian 1.13.0 and newer can render and search its settings.

The `display()` override remains as a fallback for older versions, preserving the minimum supported Obsidian version of 1.6.6. Both paths share the same definitions and rendering callbacks, including saving, archive-path normalization, and archive-folder visibility updates.

The new settings types are imported only for type checking; no new runtime API is required by the fallback.

See the official [dual-support migration guide](https://docs.obsidian.md/plugins/guides/migrate-declarative-settings).

## Styles

All plugin CSS lives in `styles.css`, which Obsidian loads automatically. The plugin never creates `<style>` elements; it only toggles classes. The archive folder is hidden by adding `pagemode-archive-folder-hidden` to the matching `.nav-folder` in File explorer, re-applied through a `MutationObserver` on the explorer container.
