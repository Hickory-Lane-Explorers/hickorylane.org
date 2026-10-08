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
| `.pages.yml` | Settings for the Pages CMS web editor |

## Web editor setup

[Pages CMS](https://pagescms.org) is free and edits the files in a GitHub repository.

1. Put this project in a GitHub repository and connect a host that runs `zola build` after each change.
2. Sign in at https://app.pagescms.org with GitHub and open the repository. Pages CMS reads `.pages.yml`.
3. Invite editors by email in the collaborator settings. Editors do not need a GitHub account.

## Icon style

Each icon is a 512 by 512 SVG with the same cream medallion, the same soft shadow, light from the top left, and colors taken from the banner photograph. Copy the medallion part of an existing icon when you draw a new one.
