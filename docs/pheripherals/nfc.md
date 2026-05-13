# NFC Peripheral API

The NFC suite exposes two distinct peripheral types: `neo_nfc_master` (for writing and managing cards) and `neo_nfc_reader` (for event-based scanning).

---

## `neo_nfc_master`

### `hashCard()`
Checks if an NFC card is currently inserted into the master block.
- **Returns**: `boolean` - `true` if inserted, `false` otherwise.

---

### `getLabel()`
Gets the custom label assigned to the master station.
- **Returns**: `string` - Current label.

---

### `setLabel(label)`
Sets a custom label for the master station.
- **Arguments**: `label` (*string*)

---

### `flash(mode, arg1, [pin])`
Flashes new data or configurations onto the inserted NFC card.

- **Arguments**:
  - `mode` (*string*): Flash mode, either `"DATA"` or `"B4PIN"`.
  - `arg1` (*table* | *string* | *number*): If mode is `"DATA"`, a table of bytes (0-255) or a raw text string (max 1024 bytes). If mode is `"B4PIN"`, the new 4-digit PIN integer.
  - `pin` (*number*, optional): If the card is currently locked with a B4PIN, the correct existing PIN must be passed to authorize the flash.

- **Returns**: `boolean` - `true` on successful flash, `false` otherwise.

---

### `read()`
Reads the raw data payload from the inserted card.
- **Returns**: `table` | `boolean` - A table of byte integers (indexed 1 to N), or `false` if no card/data is present.

---

### Events (`neo_nfc_master`)
- `nfc_master_card_inject` (label): Fired when a card is inserted into the master.
- `nfc_master_card_enject` (label): Fired when a card is removed.

---

## `neo_nfc_reader`

The `neo_nfc_reader` peripheral does not expose callable Lua functions. Instead, it listens for physical interactions and pushes events to attached computers.

### Events (`neo_nfc_reader`)
- `neo_nfc_read` (label, data): Fired when a player interacts with the reader using an NFC card. `label` is the reader's label string, and `data` is a table of the card's stored bytes.
