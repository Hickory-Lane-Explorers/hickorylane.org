# Hickory Lane Explorers website

A static website made with [Zola](https://www.getzola.org/) 0.23 (Tera 2 templates).

## Commands

| Command | Result |
| --- | --- |
| `zola serve` | A local preview at http://127.0.0.1:1111 that updates when files change |
| `zola build` | The finished website in `public/` |

## Folders

| Path | Contents |
| --- | --- |
| `website-content/` | All words and picture choices, one YAML file for each page. Editors change only this folder. Refer to `website-content/HOW-TO-EDIT.md`. |
| `static/images/photographs/` | Photographs. Zola makes smaller WebP copies during the build. |
| `static/images/icons/` | The icons, the portrait placeholder, and the favicon, all SVG |
| `templates/` | `base.html`, one template for each page, `sections/` for page parts, `partials/` for header, banner, and footer, `components/` for shared Tera components |
| `sass/` | Styles, one partial file for each area. Sizes are in `_tokens.scss`. Colors and fonts are in `website-content/appearance.yaml`, so editors can change them. |
| `content/` | Three small files that connect a web address to a template and a content file |
| `static/admin/` | The Sveltia CMS web editor: the page, and the settings in `config.yml` |

## Web editor setup

[Sveltia CMS](https://sveltiacms.app) is free and runs in the browser at `/admin/`. It connects directly to GitHub with a token. No other server is involved.

1. Make a GitHub account for each editor, and give the account write access to the repository in the organization.
2. Make a fine-grained personal access token. Select the organization as the resource owner, select only this repository, and set **Contents** to **Read and write**.
3. Open https://hickorylane.org/admin/, click **Sign In Using Access Token**, and paste the token. The browser keeps the token until you sign out.

The script version in `static/admin/index.html` is fixed, with a hash that the browser checks. To update Sveltia CMS, change the version and the hash together.

## Icon style

Each icon is a 512 by 512 SVG with the same cream medallion, the same soft shadow, light from the top left, and colors taken from the banner photograph. Copy the medallion part of an existing icon when you draw a new one.
