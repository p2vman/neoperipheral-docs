# Socket & Modules

**Block ID**: `neoperipheral:socket`  
**Peripheral Type**: `neo_socket` ([API Reference](../pheripherals/socket.md))

The **Socket Block** is a modular chassis capable of housing up to 4 plug-and-play expansion modules (slots 0 through 3). This allows players to combine different peripheral functions into a single block space.

## Available Modules

| Module Name | Item ID | Description |
| :--- | :--- | :--- |
| **Radar Module** | `neoperipheral:radar_module` | Provides sub-level radar scanning capabilities. |
| **Creative Radar Module** | `neoperipheral:creative_radar_module` | Provides creative/admin-grade radar scanning capabilities. |
| **Crypto Module** | `neoperipheral:crypto_module` | Cryptographic processing module (WIP). |

## Managing Modules
Modules can be inserted into or removed from the Socket Block. Connected computers can dynamically query inserted modules, inspect slots, and interact with module-specific methods.
