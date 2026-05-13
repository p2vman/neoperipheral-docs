# Radar Peripheral API

**Peripheral Type**: `neo_radar`

The `neo_radar` peripheral is exposed by both the standard Radar Block / Module and the Creative Radar Block / Module. It allows computers to scan for nearby Sable physics sub-level structures.

---

## Methods

### `isCreative()`

Checks if the attached radar is a Creative Radar variant.

- **Returns**: `boolean` - `true` if creative/admin tier, `false` otherwise.

---

### `scanForSubLevels([range], [absolute])`

Scans the environment for nearby Sable sub-levels.

- **Arguments**:
  - `range` (*number*, optional): Scan radius in blocks (defaults to server configuration, capped by max range limit).
  - `absolute` (*boolean*, optional): If `true` and the radar is creative, returns absolute world coordinates instead of relative offsets.

- **Returns**: `table` - An array of sub-level data tables. Each sub-level table contains:
  - `id` (*string*): UUID of the sub-level.
  - `x`, `y`, `z` (*number*): Position coordinates (relative offset or absolute).
  - `q_x`, `q_y`, `q_z`, `q_w` (*number*): Quaternion orientation components representing the sub-level's rotation.