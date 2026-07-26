# 1Hour1Life Resource Pack

Public distribution repository for the Minecraft resource pack used by **MC-Generations**, a Paper plugin inspired by *One Hour One Life*.

Learn more at [1hour1life.net](https://1hour1life.net).

## Purpose

This repository contains deployable resource-pack ZIP files for Minecraft clients and Minehut servers.

The editable resource-pack source remains inside the private MC-Generations project. ZIP files in this repository are generated and uploaded automatically by the project’s deployment tool.

## Published packs

Generated resource packs are stored under:

```text
packs/
└── mc-generations-resourcepack-<sha1>.zip
```

Every filename contains the SHA-1 hash of that exact ZIP file. A changed resource pack therefore receives a new filename and URL, preventing stale downloads from being served from a cache.

Example download URL:

```text
https://raw.githubusercontent.com/1Hour1Life/1Hour1Life-Resourcepack/main/packs/mc-generations-resourcepack-<sha1>.zip
```

The corresponding Minecraft server configuration is:

```properties
resource-pack=<raw GitHub URL>
resource-pack-sha1=<sha1 from the filename>
```

## Important

- Files under `packs/` are generated artifacts.
- Do not modify or replace published ZIP files manually.
- Older files may remain available because existing Minecraft clients or server configurations can still reference them.
- The currently active URL and SHA-1 are managed by the MC-Generations deployment process.

## Deployment

Resource packs are packaged, uploaded, and verified from the private MC-Generations project.

The deployment process:

1. Packages the resource-pack source.
2. Calculates the ZIP’s SHA-1.
3. Uploads the hash-named ZIP to this repository.
4. Verifies the public download against the calculated SHA-1.
5. Updates the server configuration and project documentation.

## Project

MC-Generations implements gameplay inspired by *One Hour One Life* for Minecraft using Paper.

Website: [1hour1life.net](https://1hour1life.net)
