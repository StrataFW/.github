<div align="center">

<img src="https://raw.githubusercontent.com/StrataFW/strata-recipe/main/.github/assets/banner.png" alt="Strata Framework" width="600">

### A modern, batteries-included FiveM roleplay framework built on `ox_core`.

[![Latest release](https://img.shields.io/github/v/release/StrataFW/strata-recipe?label=framework&color=2b7fff&style=for-the-badge)](https://github.com/StrataFW/strata-recipe/releases/latest)
&nbsp;
[![FiveM](https://img.shields.io/badge/FiveM-cerulean-fd4f48?style=for-the-badge)](https://fivem.net)
&nbsp;
[![Lua](https://img.shields.io/badge/Lua-5.4-2c2d72?style=for-the-badge&logo=lua&logoColor=white)](https://lua.org)
&nbsp;
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178c6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org)
&nbsp;
[![React](https://img.shields.io/badge/React-18-61dafb?style=for-the-badge&logo=react&logoColor=black)](https://react.dev)
&nbsp;
[![Mantine](https://img.shields.io/badge/Mantine-v5-228be6?style=for-the-badge)](https://v5.mantine.dev)

</div>

<br />

## ⚡ Get started

The fastest path is the **txAdmin recipe** &mdash; one URL, full server in
minutes:

```
https://raw.githubusercontent.com/StrataFW/strata-recipe/main/recipe.yaml
```

In txAdmin → **New deployment → Remote recipe**, paste that URL and follow
the prompts. You'll need a Cfx.re `sv_licenseKey` and a MySQL connection
string &mdash; everything else (resources, cfg tree, schema bootstrap) is
handled for you.

Prefer to drop in a frozen bundle? Grab
[`strata-framework-vX.Y.Z.zip`](https://github.com/StrataFW/strata-recipe/releases/latest)
and unzip into your FXServer directory.

<br />

## 📦 Resources

<table>
  <tr><td colspan="2"><b>Foundation</b></td></tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_log"><code>st_log</code></a></td>
    <td>Structured logger &mdash; pretty console, file rotation, NDJSON, Discord webhook, dedup, redaction.</td>
  </tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_bootstrap"><code>st_bootstrap</code></a></td>
    <td>Branded loadscreen + boot summary card.</td>
  </tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_ipl"><code>st_ipl</code></a></td>
    <td>IPL / interior loader with dependency ordering.</td>
  </tr>

  <tr><td colspan="2"><br /></td></tr>
  <tr><td colspan="2"><b>Identity &amp; session</b></td></tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_multichar"><code>st_multichar</code></a></td>
    <td>Character selector &mdash; replaces <code>ox_core</code>'s built-in selector.</td>
  </tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_spawn"><code>st_spawn</code></a></td>
    <td>Spawn / respawn flow with cinematic camera, synced wake-up animation, last-location memory.</td>
  </tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_appearance"><code>st_appearance</code></a></td>
    <td>Appearance editor &mdash; clothing, hair, face, tattoos, outfits, presets, wardrobe, faction uniforms, sharing.</td>
  </tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_apartments"><code>st_apartments</code></a></td>
    <td>Per-character apartments &mdash; routing-bucket isolated rooms with stash + wardrobe (paired with La Puerta MLO).</td>
  </tr>

  <tr><td colspan="2"><br /></td></tr>
  <tr><td colspan="2"><b>Interface</b></td></tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_chat"><code>st_chat</code></a></td>
    <td>Chat NUI replacement &mdash; Mantine UI, channels, slash-command suggestions.</td>
  </tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_admin"><code>st_admin</code></a></td>
    <td>Staff panel &mdash; DB-managed permissions, notes, reports queue, vehicle inspector, ban records.</td>
  </tr>
</table>

### Deploy

<table>
  <tr>
    <td><a href="https://github.com/StrataFW/strata-recipe"><code>strata-recipe</code></a></td>
    <td>One-click txAdmin recipe + fat-bundle CI. Pulls every <code>[cfx]</code>, <code>[ox]</code>, and <code>[strata]</code> resource and ships <code>server.cfg</code> + <code>cfg/</code> in place.</td>
  </tr>
</table>

<br />

## 🧱 Stack

|                |                                                                                |
|----------------|--------------------------------------------------------------------------------|
| **Server**     | FiveM (cerulean / Lua 5.4) on `ox_core` + `oxmysql`                            |
| **Database**   | MariaDB / MySQL (`utf8mb4`) &mdash; tables auto-create on first boot          |
| **NUIs**       | React 18 + TypeScript 5 + Vite + Mantine **v5** (dark / blue / Montserrat)     |
| **Tooling**    | bun · per-resource GitHub Actions release workflow                             |

<br />

## 🎨 Brand

Mantine's default dark palette with `primaryColor: 'blue'`, **Montserrat**
throughout, and `clamp()` fluid sizing on every primitive. Each NUI resource
vendors a copy of the Strata `nui-kit` (theme + shared primitives) so styling
stays consistent without coupling resources at runtime. Reference resource:
[`st_bootstrap`](https://github.com/StrataFW/st_bootstrap).

<br />

## 🔖 Versioning

Each resource is independently semver-tagged (`vMAJOR.MINOR.PATCH`). Pushing
a tag triggers per-resource CI to build, zip, and publish a downloadable
release asset. [`strata-recipe`](https://github.com/StrataFW/strata-recipe)
bundles the latest release of each into a single
`strata-framework-vX.Y.Z.zip`, published weekly and on demand.

<br />

## 🛠 Build your own

NUI resources ship **with source** &mdash; `web/src`, `package.json`,
`vite.config.ts`, `bun.lock`. To iterate:

```bash
cd resources/[strata]/st_chat/web
bun install
bun run build
```

Fork a resource, tag a new `vX.Y.Z`, and CI cuts you a release zip you can
drop straight into your server.

<br />

<div align="center">

[strata-recipe](https://github.com/StrataFW/strata-recipe) · [report a bug](https://github.com/StrataFW/strata-recipe/issues) · [okIndica](https://github.com/okIndica)

<sub>© 2026 Strata. Each repository licensed individually &mdash; see its <code>LICENSE</code>.</sub>

</div>
