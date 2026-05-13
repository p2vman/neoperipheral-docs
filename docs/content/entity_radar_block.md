# Entity Radar

**Block ID**: `neoperipheral:entity_radar`  
**Peripheral Type**: `neo_entity_radar` ([API Reference](../pheripherals/entity_radar.md))

The **Entity Radar Block** scans the surrounding environment for living entities and players. It provides real-time tracking data including precise coordinates, look orientation (pitch and yaw), health statistics, and entity types.

## Functionality
- **Entity Scanning**: Returns a structured list of all living entities within range.
- **Player Scanning**: Specifically tracks players, optionally returning usernames (based on server configuration).
