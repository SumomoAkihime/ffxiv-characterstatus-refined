## Project Notes

- `Localization.ja.resx` currently exists but is effectively empty. The build will still emit a `ja` satellite assembly/folder, so do not assume that the presence of a language folder means the plugin is actually translated for that language.
- The "Use Game Language if available" tooltip had fallen out of sync with reality in the existing resources. If localization support changes again, update the tooltip text in every maintained `.resx` file together with the language-switching logic.
- The current solution targets `.NET 10` (`net10.0` / `net10.0-windows`). Building will fail on machines that only have the .NET 8 SDK installed, even though the plugin version itself is still `1.8.5.0`.
- `origin` currently points at `Kouzukii/ffxiv-characterstatus-refined`, which is easy to mistake for the maintainer's own publishing target. Verify or replace the remote before pushing.
- The untracked `release/` directory is not covered by the current `.gitignore`. Treat it as suspicious build output unless there is a deliberate reason to version it.
