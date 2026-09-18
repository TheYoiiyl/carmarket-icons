# CarMarket vehicle icons

Vehicle renders for the CarMarket Unturned plugin, served over GitHub Pages.

Each file is a 512px transparent PNG rendered from the game's own vehicle models by
`Assets/Editor/CarMarket/CarMarketIconRenderer.cs` in the VehicleShop project.

Two names per vehicle:

- `<slug-of-display-name>.png` - matches the catalog `Key` the plugin looks for by default
- `<guid>.png` - the same image, for pointing at with `IconUrl` when display names collide

`icons.csv` maps folder -> GUID -> name -> file.

The plugin fetches these client-side via `EffectManager.sendUIEffectImageURL`, so this just
needs to be reachable over HTTPS from players' machines.
