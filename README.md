# All Saints Fermentery — Recipe Template

This is the official template repository for creating new recipe repositories for [All Saints Fermentery](https://allsaintsfermentery.github.io).

## How to use this template

1. Click **"Use this template"** → **"Create a new repository"** at the top of this page.
2. Name your new repository after the beer (e.g. `st-arnold-pale-ale`).
3. Add the **`recipe`** topic to your new repository (Settings → General → Topics). This is required for the sync workflow to discover it.
4. Edit `beer.yml` in your new repository with your beer's details.
5. That's it — the nightly [sync workflow](https://github.com/allsaintsfermentery/allsaintsfermentery.github.io/blob/main/.github/workflows/sync-beers.yml) will automatically pick up your recipe and include it in the website inventory.

## beer.yml schema

| Field | Required | Values |
|-------|----------|--------|
| `name` | ✅ | String — the beer's name |
| `style` | ✅ | String — e.g. `American Pale Ale` |
| `abv` | ✅ | Number — e.g. `5.0` |
| `description` | ✅ | String — a short description of the beer |
| `status` | ✅ | One of: `Available`, `Seasonal`, `Coming Soon` |

A single repo can contain multiple beers by using a YAML list (see `beer.yml` for an example).
