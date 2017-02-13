# AOE Technology Radar

A static site generator for AOE Technology Radar

## Installation

```
> git clone git@github.com:AOEpeople/aoe_techradar_node.git
> cd aoe_techradar_node
> npm install
> npm run watch
```
*A new browser tab should open up - wait until last command has finished and refresh.*

## Usage

For a new Technology Radar release, create a folder of the release date (YYYY-MM-DD) under `/radar`. In each release folder create a folder for every quadrant and place the items there.

### Maintaining items

The items are written in Markdown format (.md)

Each file has a [front-matter](https://github.com/jxson/front-matter) header where the attributes of the item are listed:
  ```
  ---
  title:      "React"
  ring:       adopt
  ---

  Text goes here
  ```

Following front-matter attributes are possible:
- **title**: Name of the Item
- **ring**: Ring section in radar. One of `trial`, `assess`, `adopt`, `hold`
- **info**: (optial) A short textual description of the item (visible in overview pages)

The name of the .md file acts as item identifier and may overwrite items with the same name from older releases.

If an item is overwritten in a new release, the attributes from the new item are merged with the old ones and a new history entry is created for that item.

## Todos

-  [ ] Final CSS (Icons, etc)
-  [ ] Better semantic and SEO
-  [ ] Radar View?
-  [ ] Make mobile friendly
-  [ ] Add pjax
