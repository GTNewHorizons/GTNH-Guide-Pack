# GTNH-Guide-Pack

Overview
----
GTNH-Guide-Pack is a documentation and template repository designed for use with GuideNH — a Markdown-driven, in‑game guide framework for Minecraft 1.7.10. This repository supplies GT-New-Horizons–style guide templates, examples, and authoring workflows so contributors can create polished, searchable, in-game documentation that players can read without leaving Minecraft.

GTNH players currently rely on fragmented external resources — the Wiki, Discord, videos, spreadsheets, and scattered forum posts. There is no single in‑game system that presents long‑form documentation, interactive content, searchable recipes, and structured progression in one place. That fragmentation makes discovery and learning harder for new and returning players.

GuideNH is an in‑game guide framework that solves the fragmentation problem by rendering Markdown content inside Minecraft (1.7.10). It is a framework only — documentation content (machines, progression, tutorials) is written by contributors and distributed as resource packs or mod assets.

Key idea and project links:
- Repository: https://github.com/GTNewHorizons/GuideNH
- Wiki: https://github.com/GTNewHorizons/GuideNH/wiki

Features
----
- Full Markdown rendering (tables, admonitions/alerts, code blocks, lists)
- Custom interactive tags: item links, tooltips, internal and external links
- NEI recipe integration embedded in guide pages (look up recipes without leaving the guide)
- Interactive 3D multiblock previews and model viewers
- Automatic page discovery via standard resource pack locations (no manifest required)
- Native multi-language support with fallback to English
- Live preview and hot‑reload for content authors (fast edit -> test loop)

Quick Start
----
1. Clone this repo and read [getting-started.md](https://github.com/GTNewHorizons/GuideNH/blob/master/wiki/Getting-Started.md) for the authoring basics and [ContributionGuide.md](https://github.com/GTNewHorizons/GTNH-Guide-Pack/blob/master/CONTRIBUTING.md) for contribution guidelines.
2. Write guide pages in Markdown under docs/ following the provided templates.
3. Test locally with GuideNH live preview (see GuideNH repo for preview tool) or package into a resource pack and drop into the client resourcepacks/ directory.
4. Submit content via PR to this repository or another GuideNH-enabled project.

Authoring Conventions
----
- File format: Markdown (UTF-8), begin each page with a top-level H1.
- Keep pages focused: short introduction, clear objectives, prerequisites, step-by-step instructions, tips, and optional troubleshooting.
- Use fenced code blocks for commands or JSON (```bash, ```json).
- Cite sources for recipes and numeric values (mod name + recipe origin).
- Include image alt text and captions for accessibility.

Localization
----
- Place language files under .../_<lang>/ (e.g., en_us.md, zh_cn.md).
- Use the same filename and folder structure across languages; GuideNH loads per‑page translations and falls back to English.

Releases
----
Releases use semantic versioning and are cut by pushing a bare version tag (no `v` prefix):

```bash
git tag 1.0.1
git push origin 1.0.1
```

The `release-tags.yml` workflow then stamps the tag into `pack.mcmeta` (`gtnh_resource_pack_updater.pack_version`), builds `GTNH-Guide-Pack-<version>.zip`, generates a `gtnh-pack-update.json` metadata asset, and publishes a GitHub release for the tag (replacing any existing release for that tag).

Distribution:
- DreamAssemblerXXL is registered to track this repo's releases, so each GTNH daily bundles the newest release automatically.
- GTNHLib's in-game ResourcePackUpdater notifies players (chat link, no auto-install) when a newer compatible release exists. Targeting is controlled by `gtnh_resource_pack_updater.pack_game_version` in `pack.mcmeta` (the GTNH line, e.g. `2.9.X`, or `2.8.X;2.9.X` for both) - this is the GTNH line, not the Minecraft version. Beta and stable within one minor (e.g. 2.9-beta and 2.9) cannot be targeted separately.

License
----
[![CC BY-NC-SA 4.0](https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

This work is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.

You are free to:

- Share — copy and redistribute the material in any medium or format
- Adapt — remix, transform, and build upon the material

Under the following terms:

- Attribution — You must give appropriate credit.
- NonCommercial — You may not use the material for commercial purposes.
- ShareAlike — If you remix, transform, or build upon the material, you must distribute your contributions under the same license.

For full license text, check LICENSE.txt or go to [Creative Commons](https://creativecommons.org/licenses/by-nc-sa/4.0/).

### Developers

Thanks to the following developers for their contributions to GTNH-Guide-Pack:

<a href="https://github.com/GTNewHorizons/GTNH-Guide-Pack/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=GTNewHorizons/GTNH-Guide-Pack&max=1000" alt="contributors" />
</a>

Disclaimer
----
GuideNH does not provide the distribution of the server guidance.
