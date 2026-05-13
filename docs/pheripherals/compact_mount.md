# Compact Cannon Mount Peripheral API

**Peripheral Types**: `compact_mount`, `neo_compact_mount`

Exposed when a computer connects to a **Create Big Cannons** Fixed/Compact Cannon Mount. Allows full automated control over assembly, aiming, and firing.

---

## Methods

### `assemble()`
Attempts to assemble the cannon structure attached to the mount.
- **Returns**: `boolean` - `true` if assembly was successfully initiated, `false` if already running.

---

### `disassemble()`
Disassembles the currently running cannon structure.
- **Returns**: `boolean` - `true` if disassembled successfully, `false` if not running.

---

### `fire()`
Fires the assembled cannon. Rate-limited per tick.
- **Returns**: `nil` (Throws an error if the cannon is not assembled or cannot fire).

---

### `isRunning()`
Checks if the cannon mount is currently assembled and running.
- **Returns**: `boolean`

---

### `getYaw()`
Gets the current yaw orientation angle of the mount.
- **Returns**: `number`

---

### `getPitch()`
Gets the current pitch elevation angle of the mount.
- **Returns**: `number`

---

### `setYaw(yaw)`
Sets the target yaw orientation angle.
- **Arguments**: `yaw` (*number*)

---

### `setPitch(pitch)`
Sets the target pitch elevation angle.
- **Arguments**: `pitch` (*number*)

---

### `getX()`, `getY()`, `getZ()`
Gets the exact block coordinate of the cannon controller.
- **Returns**: `number`

---

### `getDirection()`
Gets the horizontal facing direction of the cannon mount controller block.
- **Returns**: `string` (e.g., `"north"`, `"south"`, `"east"`, `"west"`)