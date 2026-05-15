<div align="center">

# Strata

**A modern FiveM roleplay framework.**

Built on `ox_core` · React + Mantine NUIs · MariaDB

[![Website](https://img.shields.io/badge/stratafw.com-228be6?style=for-the-badge)](https://stratafw.com)
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

The fastest path is the **txAdmin recipe** — one URL, full server in minutes:

```
https://raw.githubusercontent.com/StrataFW/strata-recipe/main/strata-recipe.yaml
```

In txAdmin → **Setup → Remote URL Recipe**, paste that URL and follow the
prompts. You'll need your `sv_licenseKey`, a Steam API key, and DB credentials.

Prefer manual? Each resource ships as a tagged release with a downloadable
zip — drop into `resources/[strata]/<name>/` and `ensure` it in `server.cfg`.

<br />

## 📦 Resources

<table>
  <tr><td><b>Foundation</b></td><td></td></tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_lib"><code>st_lib</code></a></td>
    <td>Shared helpers exposed via <code>@st_lib/init.lua</code>. Required by most resources.</td>
  </tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_log"><code>st_log</code></a></td>
    <td>Buffered structured logger with optional Discord webhook delivery.</td>
  </tr>
  <tr><td colspan="2"><br /></td></tr>
  <tr><td><b>Identity & session</b></td><td></td></tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_bootstrap"><code>st_bootstrap</code></a></td>
    <td>Loadscreen — minimal, on-brand boot UI with live server stats.</td>
  </tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_multichar"><code>st_multichar</code></a></td>
    <td>Character selector — replaces <code>ox_core</code>'s default selector.</td>
  </tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_spawn"><code>st_spawn</code></a></td>
    <td>Spawn selector with cinematic camera and synced wake-up animation.</td>
  </tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_appearance"><code>st_appearance</code></a></td>
    <td>Clothing, outfits, wardrobe slots, faction uniforms, marketplace, share codes.</td>
  </tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_apartments"><code>st_apartments</code></a></td>
    <td>La Puerta apartments — routing-bucket isolated rooms with stash + wardrobe.</td>
  </tr>
  <tr><td colspan="2"><br /></td></tr>
  <tr><td><b>Interface</b></td><td></td></tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_ui"><code>st_ui</code></a></td>
    <td>HUD — vitals, compass, minimap frame, vehicle dashboard, death overlay.</td>
  </tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_chat"><code>st_chat</code></a></td>
    <td>Chat NUI replacement.</td>
  </tr>
  <tr>
    <td><a href="https://github.com/StrataFW/st_admin"><code>st_admin</code></a></td>
    <td>Admin menu — DB-managed permissions, command palette, reports queue.</td>
  </tr>
</table>

<br />

### Shared & deploy

<table>
  <tr>
    <td><a href="https://github.com/StrataFW/nui-kit"><code>nui-kit</code></a></td>
    <td>Mantine v5 theme + shared NUI primitives. Published as <code>@strata/nui-kit</code>.</td>
  </tr>
  <tr>
    <td><a href="https://github.com/StrataFW/strata-recipe"><code>strata-recipe</code></a></td>
    <td>One-click txAdmin recipe. Pulls every resource, sets up the schema, drops <code>server.cfg</code> in place.</td>
  </tr>
</table>

<br />

## 🧱 Stack

|       |                                                                              |
| :---- | :--------------------------------------------------------------------------- |
| **Server**   | FiveM (cerulean / Lua 5.4) on `ox_core` + `oxmysql`                   |
| **Database** | MariaDB                                                               |
| **NUIs**     | React 18 + TypeScript + Vite + Mantine **v5** (dark / blue / Montserrat) |
| **Tooling**  | bun                                                                   |

<br />

## 🎨 Brand

Mantine's default dark palette with `primaryColor: 'blue'`, Montserrat
throughout, and `clamp()` fluid sizing on every primitive. Shared via the
[`@strata/nui-kit`](https://github.com/StrataFW/nui-kit) package — drop it
into a new NUI to inherit the look.

<br />

## 🔖 Versioning

Each resource is independently semver-tagged (`vMAJOR.MINOR.PATCH`). Pushing
a tag triggers CI to build, zip, and publish the asset.
[`strata-recipe`](https://github.com/StrataFW/strata-recipe) pins specific
resource versions so a recipe install is always reproducible.

<br />

<div align="center">

[stratafw.com](https://stratafw.com) · [stratafivem@gmail.com](mailto:stratafivem@gmail.com)

<sub>© 2026 Strata. Each repository licensed individually — see its <code>LICENSE</code>.</sub>

</div>
