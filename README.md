# Bazaar Sim Releases

Public release repository for Bazaar Sim, a BepInEx mod for The Bazaar.

This repository is intentionally release-only. It does not contain simulator source code, internal debugging tools, or development workflows. Installable builds are published from the private development repository as GitHub Release assets.

## Current Scope

Bazaar Sim is being developed as a post-lock fight analysis tool. The intended public mod package should:

- run only after a fight has been locked or captured by the game client;
- avoid pre-choice encounter recommendations;
- avoid exposing arbitrary monster or board simulation commands in the shipped mod package;
- keep simulation logic in a bundled worker process rather than inside the game process;
- make local mod activity visible through normal files and logs.

The project is not affiliated with Tempo Games or Tempo Storm.

## Downloads

Use the latest release from the [Releases](https://github.com/Adversarian/bazaar-sim-releases/releases) page.

The release package is expected to contain a `BepInEx` folder. To install, extract the package into your local The Bazaar install directory so that the files land under:

```text
The Bazaar/
  BepInEx/
    plugins/
      BazaarSimExporter.dll
      BazaarSim/
        worker/
          bazaar-sim.exe
```

Restart the game after installing or updating the mod.

## Compliance Direction

The public package is intended to be constrained for post-lock analysis. Development builds may contain broader debugging tools, but those tools are not intended for public release.

If Tempo Games publishes clearer modding or simulation rules, public releases should follow those rules or stop distribution until the package can be made compliant.

## Support

Open an issue in this repository for release packaging problems, install problems, or public mod behavior. Do not post proprietary game data, account credentials, access tokens, or private logs containing sensitive information.
