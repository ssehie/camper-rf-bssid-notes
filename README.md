# Compact BSSID Review Packet

Generated: 2026-05-01 13:25:08 -05:00

This packet is a small technical preview for independent review. It is not a raw 802.11 monitor-mode packet capture and it is not the full sealed evidence packet.

## What This Shows

- Passive Wi-Fi scan summaries from the local sensor stack.
- Hidden/named sibling BSSID families.
- First-octet changes while the remaining BSSID tail bytes stay stable.
- Example families where hidden BSSIDs appear adjacent to visible private SSIDs.
- Current alert examples with family keys, SSID labels, first-octet sets, sensors, and RSSI where available.

## Current Monitor Snapshot

- Monitor generated: 2026-05-01T13:20:07.5483846-05:00
- Records in latest sweep: 129
- Hidden records in latest sweep: 47
- Alerts in latest sweep: 49
- First-octet-shift families: 15
- Role-flip families: 13
- Sensors: moto_g_play___2026; windows
- Phone anchor: moto_g_play___2026: ssehorse -25 dBm ch 44

## Week Snapshot

- Week report generated: 2026-04-20T15:52:41.8565236-05:00
- Sweeps: 8741
- BSSID observations: 1181298
- Unique BSSIDs: 244
- Hidden records: 429635
- Visible records: 751663
- First-octet-shift families: 14

## Reviewer Ask

Please sanity-check whether these hidden/named sibling BSSID families and first-octet role shifts are normal managed Wi-Fi infrastructure in your local environment, or whether the pattern warrants deeper investigation.

Specific questions:

1. Do you routinely see hidden and visible BSSIDs sharing the same tail bytes while only the first octet changes?
2. Do you see this around ordinary private SSIDs in your own area?
3. Is there a normal controller/mesh/hotspot/vendor behavior that explains this pattern?
4. What additional capture or metadata would make the observation more useful?

## Files

- bssid-family-summary.csv
- current-alert-examples.csv
- packet-summary.json
- README.md
