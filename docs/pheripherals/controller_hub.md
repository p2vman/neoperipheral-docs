# Linked Controller Hub Peripheral API

**Peripheral Types**: `linked_controller_hub`, `tweaked_linked_controller_hub`, `controller_hub`

Exposed by the **Linked Controller Hub Block** (Create / Create Tweaked Controllers integration). Allows computers to read wireless button presses from bound Linked Controllers.

---

## Methods

### `getButton(key)`
Checks if a specific controller button is currently pressed.
- **Arguments**: `key` (*string*): The button identifier string (e.g., `"keyUp"`, `"keyJump"`).
- **Returns**: `boolean` - `true` if pressed, `false` otherwise.

---

### `getButtons(table)`
Populates a provided Lua table with the boolean states of all bound controller buttons.
- **Arguments**: `table` (*table*): Target table to populate.
- **Returns**: `nil` (Mutates the passed table in-place).

---

### `getKeys()`
Returns an array of all available button identifier strings supported by the hub.
- **Returns**: `table` - `{"keyUp", "keyDown", "keyLeft", "keyRight", "keyJump", "keyShift"}`
