# Minecraft x GTA V: community builds

Ready-made downloads of the **Minecraft x GTA V passthrough** example from
[universal-modder](https://github.com/rehan-remade/universal-modder) (`examples/minecraft-gta5-passthrough`),
made by Rehan and the universal-modder contributors and shared under the MIT licence.

The original project publishes source code only. This repository builds it on GitHub's own servers, at a pinned
upstream commit, so players can download the finished files. Nothing is changed in the code. All credit goes to
the original authors; see `NOTICE.txt` and `LICENSE.txt` in each release.

## What's in a release

| File                              | What it is                                                                   |
| --------------------------------- | ---------------------------------------------------------------------------- |
| `minecraft-gta5-<ver>.zip`        | `MCPassthrough.asi` and `reshade-shaders\Shaders\MCPassthrough.fx` for GTA V |
| `minecraft-gta5-fabric-<ver>.jar` | The Fabric mod for Minecraft 26.3                                            |
| `LICENSE.txt`, `NOTICE.txt`       | universal-modder's MIT licence, credits and third-party licences             |
| `SHA256SUMS.txt`                  | Checksums of every file                                                      |

**Not included, ever:** ScriptHookV and its ASI loader (get them from
[dev-c.com](https://www.dev-c.com/gtav/scripthookv/)), the ScriptHookV SDK, ReShade, Fabric, or any game files.

Single-player only: GTA V story mode with BattlEye off. Never use mods in GTA Online.

## Not official

Not made or endorsed by Rehan, Mojang, Microsoft, Rockstar Games or Take-Two.
NOT AN OFFICIAL MINECRAFT PRODUCT. NOT APPROVED BY OR ASSOCIATED WITH MOJANG OR MICROSOFT.

If you're one of the original authors and want this changed or taken down, open an issue and it will be done.

## How a release is made

Actions tab → **Build and release** → Run workflow → enter a tag such as `v0.1.0`. The workflow
(`.github/workflows/build.yml`) checks out universal-modder at the pinned commit, downloads the ScriptHookV SDK
from dev-c.com only to compile against it (it's deleted before packaging), checks every download's SHA-256,
builds with Visual Studio and Gradle, and publishes the files above.
