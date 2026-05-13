# Sable Engine Peripheral API

**Peripheral Type**: `neo_sable_engine`

The `neo_sable_engine` peripheral allows computers to interact directly with the **Sable** physics engine when mounted on a moving sub-level structure.

---

## Telemetry Methods

### `getUUID()`
Gets the unique UUID of the containing sub-level.
- **Returns**: `string` | `nil`

---

### `isOnSubLevel()`
Checks if the engine block is currently situated on an active Sable sub-level structure.
- **Returns**: `boolean`

---

### `getName()`
Retrieves the assigned name of the sub-level structure.
- **Returns**: `string` | `nil`

---

### `getMass()`
Returns the total combined mass of the sub-level rigid body.
- **Returns**: `number`

---

### `getPosition()`
Retrieves the logical position of the sub-level structure in absolute world space.
- **Returns**: `table` - `{x = number, y = number, z = number}`

---

### `getOrientation()`
Retrieves the quaternion orientation of the sub-level structure.
- **Returns**: `table` - `{x = number, y = number, z = number, w = number}`

---

### `getLinearVelocity()`
Gets the current linear velocity vector of the sub-level.
- **Returns**: `table` - `{x = number, y = number, z = number}`

---

### `getAngularVelocity()`
Gets the current angular velocity vector of the sub-level.
- **Returns**: `table` - `{x = number, y = number, z = number}`

---

### `getCenterOfMass()`
Retrieves the exact coordinates of the sub-level's center of mass.
- **Returns**: `table` | `nil` - `{x = number, y = number, z = number}`

---

## Physical Impulse Methods

> [!NOTE]  
> All impulse methods are rate-limited per tick to prevent server instability and physics exploitation.

### `applyLinearImpulse(x, y, z)`
Applies an instantaneous linear momentum vector to the center of mass.
- **Arguments**: `x`, `y`, `z` (*number*)
- **Returns**: `boolean` - `true` on success.

---

### `applyAngularImpulse(x, y, z)`
Applies rotational torque (angular impulse) along the given vector.
- **Arguments**: `x`, `y`, `z` (*number*)
- **Returns**: `boolean` - `true` on success.

---

### `applyImpulseAtPoint(px, py, pz, fx, fy, fz)`
Applies a force vector `(fx, fy, fz)` at a specific absolute world coordinate `(px, py, pz)`.
- **Arguments**: `px`, `py`, `pz`, `fx`, `fy`, `fz` (*number*)
- **Returns**: `boolean` - `true` on success.

---

### `applyImpulseAtRelativePoint(rx, ry, rz, fx, fy, fz)`
Applies a force vector `(fx, fy, fz)` at a position offset `(rx, ry, rz)` relative to the Sable Engine Block's coordinates.
- **Arguments**: `rx`, `ry`, `rz`, `fx`, `fy`, `fz` (*number*)
- **Returns**: `boolean` - `true` on success.

---

## Events
- `engine_tick`: Fired during each simulation tick update.
