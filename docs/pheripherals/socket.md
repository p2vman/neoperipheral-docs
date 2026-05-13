# Socket Peripheral API

**Peripheral Type**: `neo_socket`

The `neo_socket` peripheral allows computers to query and interact with expansion modules housed inside a Socket Block.

---

## Methods

### `hashModule(slot)`

Checks if a module is currently present in the specified socket slot.

- **Arguments**:
  - `slot` (*number*): Slot index (0 to 3).
- **Returns**: `boolean` - `true` if a module is present, `false` otherwise.

---

### `getModule(slot)`

Retrieves the peripheral wrapper for the module in the specified slot.

- **Arguments**:
  - `slot` (*number*): Slot index (0 to 3).
- **Returns**: `table` | `nil` - The module peripheral table (allowing direct calls to module methods like `scanForSubLevels`), or `nil` if empty.

---

### `findModule(module_type)`

Searches for the first installed module matching the specified type string.

- **Arguments**:
  - `module_type` (*string*): Module type identifier (e.g., `"neo_radar"`).
- **Returns**: `table` | `nil` - The module peripheral table, or `nil` if not found.
