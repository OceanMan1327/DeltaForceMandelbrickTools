# DeltaForceMandelbrickTools

A local, single-file HTML tool for planning MandelBrick crafts in **Delta Force**.

No installation is required. Open the HTML file in a modern browser and use it locally.

## Features

- **Optimal craft calculation**
  - Selects exactly 20 skins.
  - Finds the highest possible total float that does not exceed the selected limit.
  - Adjustable total limit from **8.00 to 23.00** with **0.01** precision.
  - Fine adjustment buttons support click-and-hold.

- **More Collections mode**
  - Maximizes the number of items from preferred collections.
  - Excludes **Medusa**, **Custom Build**, and **Astromancy** from the priority count.
  - Uses the best total float as the tiebreaker.

- **Custom mode**
  - Manually select up to 20 skins from the list.
  - Click once to add an item, click again to remove it.
  - Shows the live total and craft probability distribution.

- **Craft probability breakdown**
  - Each selected item contributes **5%** to the craft result of its collection.
  - The result panel shows the percentage for every possible craft.

- **Confirm craft**
  - Highlights all skins used by the calculated craft.
  - Confirming removes those exact items from the inventory list.

- **Skin inventory**
  - Add skins by collection and purple skin name.
  - Enter float values with up to 9 decimal places.
  - Automatic sorting from lowest to highest float.
  - `#1` is always the lowest float in the current list.
  - Duplicate float detection.
  - Import/export inventory as JSON.

- **Offer timers**
  - Add a timer by collection and skin.
  - Time format: `2 30` = 2 minutes 30 seconds.
  - Timers are automatically sorted by remaining time.
  - Red warning state during the final 45 seconds.
  - Expired timers disappear automatically.
  - Active timers persist through page reloads using `localStorage`.

## Included Collections

The current built-in collection database includes:

- Spectrum Blitz
- Medusa
- Custom Build
- Fated Trigger
- Meteorology
- Spectrum Blitz 2
- Most Wanted
- Custom Build S2
- Automata
- Astromancy

Each collection stores its craft weapon and available purple skins.

## Usage

1. Download the HTML file.
2. Open it in Chrome, Edge, Firefox, or another modern desktop browser.
3. Click **+ Add** to add skins to your inventory.
4. Enter the float value for each skin.
5. Choose a craft mode:
   - **Best Quality**
   - **More Collections**
   - **Custom**
6. For automatic modes, choose the total limit and click **Calculate**.
7. Review the selected 20 skins and craft probabilities.
8. Click **Confirm Craft** to remove used skins from the inventory.

## JSON Backup

Use the import/export buttons in the Skin List header.

The exported file is named:

```text
skins.json
```

It contains the current skin inventory and can be imported later.

## Local Storage

The app uses browser `localStorage` for:

- skin inventory
- active offer timers

This means your data normally remains available after closing and reopening the HTML file in the same browser.

For backup or moving the inventory to another PC/browser, use JSON export.

## Timer Input Format

Timer input uses:

```text
minutes seconds
```

Examples:

```text
2 30
0 45
12 05
```

## Craft Limits

The interface currently references:

- **S quality:** total float ≤ **8.5**
- **A quality:** total float ≤ **23**

The slider can be adjusted anywhere from **8.00** to **23.00**.

## Planned Features

Future ideas currently planned:

- Collection priority mode
- Undo last craft
- Edit existing skins
- Timer sound notifications

## Version

**v1.1**

- Added automatic offer timer sorting
- English interface

## Disclaimer

This is a community-made utility and is not affiliated with, endorsed by, or officially connected to Delta Force, Team Jade, TiMi Studio Group, or Tencent.
