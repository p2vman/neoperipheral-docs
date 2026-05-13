# Entity Radar Peripheral API

**Peripheral Type**: `neo_entity_radar`

The `neo_entity_radar` peripheral tracks living entities and players in the surrounding area.

---

## Methods

### `scanForEntities([range])`

Scans for all living entities within the specified radius.

- **Arguments**:
  - `range` (*number*, optional): Scan radius in blocks (defaults to 16, capped by server limit).

- **Returns**: `table` - An array of entity data tables. Each entry contains:
  - `id` (*number*): Unique integer ID of the entity.
  - `type` (*string*): Entity resource location (e.g., `"minecraft:cow"`).
  - `x`, `y`, `z` (*number*): Exact world coordinates.
  - `xRot`, `yRot` (*number*): Pitch and yaw viewing angles.
  - `health`, `maxHealth` (*number*): Current and maximum health points.

---

### `scanForPlayers([range])`

Scans specifically for nearby players.

- **Arguments**:
  - `range` (*number*, optional): Scan radius in blocks (defaults to 16, capped by server limit).

- **Returns**: `table` - An array of player data tables. Each entry contains:
  - `username` (*string*, optional): Player's username (if enabled in server config).
  - `x`, `y`, `z` (*number*): Exact world coordinates.
  - `xRot`, `yRot` (*number*): Pitch and yaw viewing angles.
  - `health`, `maxHealth` (*number*): Current and maximum health points.
