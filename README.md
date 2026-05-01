# Camper RF / BSSID Review Notes

This repository is a small public review packet from an owned local sensor project.
The goal is to collect feedback on recurring hidden/named BSSID family patterns and
to prepare for controlled calibration experiments using owned network hardware.

## Scope

- Passive Wi-Fi scan summaries from Windows and Android sensors.
- Hidden/named sibling BSSID families observed over time.
- First-octet changes where the remaining BSSID tail bytes stay stable.
- Current RF/environment comparison metadata from the local PhoneLink stack.
- No deauthentication, association attempts, credential capture, or interaction with
  third-party networks.

## Current Packet

The included compact packet was generated on 2026-04-23 from:

- 8,741 Wi-Fi sweeps
- 1,181,298 BSSID observations
- 244 unique BSSIDs
- 429,635 hidden records
- 751,663 visible records
- 14 first-octet-shift families in the weekly summary

The current live monitor snapshot copied into this packet showed:

- 117 Wi-Fi records
- 44 hidden records
- 52 alerts
- 13 hidden/named family groups
- 13 first-octet-shift groups
- 13 role-flip groups
- 8 persistent unexplained families

## Files

- `packet-summary.json` - compact summary from the original BSSID review packet.
- `bssid-family-summary.csv` - recurring BSSID family summary.
- `current-alert-examples.csv` - example alerts from the packet.
- `latest-wifi-monitor-report.json` - current full Wi-Fi monitor report at packet creation time.
- `latest-rf-environment-comparison.json` - current RF/environment comparison snapshot.
- `bssid-review-packet-20260423-060340.zip` - original compact packet archive.

## Reviewer Questions

1. Are hidden and visible BSSIDs sharing stable tail bytes with first-octet shifts a normal managed Wi-Fi pattern in comparable environments?
2. Do the repeated hidden/named sibling groups look like ordinary controller, mesh, hotspot, or property Wi-Fi infrastructure?
3. What additional metadata would best distinguish managed infrastructure from unusual local RF behavior?
4. Would controlled daily calibration SSIDs from owned equipment be useful as timestamped RF stimuli for comparing hidden-network reactions?

## Next Experiment

The next planned step is to add an owned OpenWrt-capable router as a controlled sensor and calibration source. It will emit one documented calibration SSID during randomly selected windows, then collect synchronized router logs, Wi-Fi scans, SDR snapshots, and PhoneLink presence state.
