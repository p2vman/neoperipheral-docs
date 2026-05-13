# NFC Blocks & Items

The NFC technology suite in NeoPeripheral provides robust mechanisms for storing, reading, and verifying data on portable smart cards.

## NFC Master

**Block ID**: `neoperipheral:nfc_master`  
**Peripheral Type**: `neo_nfc_master` ([API Reference](../pheripherals/nfc.md))

The **NFC Master Block** is a writer and programmer station. It holds a single NFC Card, allowing connected computers to format data, encode text strings, set security PIN codes (B4PIN), and configure custom display labels.

## NFC Reader

**Block ID**: `neoperipheral:nfc_reader`  
**Peripheral Type**: `neo_nfc_reader` ([API Reference](../pheripherals/nfc.md))

The **NFC Reader Block** is an access control scanner. When a player right-clicks or taps an NFC Card against the reader, it triggers Lua events on attached computers containing the card's stored data payload and label.

## NFC Card

**Item ID**: `neoperipheral:nfc_card`

A portable data card capable of storing up to 1024 bytes of information. Cards maintain persistent data across sessions and can be secured against unauthorized overwriting via a 4-digit verification PIN.
