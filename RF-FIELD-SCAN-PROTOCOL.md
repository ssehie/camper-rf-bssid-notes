# RF Field Scan Protocol

Purpose: collect repeatable passive evidence that can separate place-tied infrastructure from device-tied or travel-correlated RF behavior.

## Rules

- Passive collection only. Do not associate with, probe, deauth, attack, or authenticate to third-party networks.
- Record observations, not attribution. Use "observed", "correlated", and "unexplained"; avoid claims about intent unless the evidence proves it.
- Keep raw local evidence sealed in the PhoneLink evidence chain before sharing public summaries.
- Public packets should be sanitized summaries unless a reviewer specifically asks for raw files.

## Minimum Field Set

For every scan window, write down:

- Date and local time.
- Rough location bucket, for example `home`, `walmart parking lot`, `truck stop`, `campground`, or `highway pull-off`.
- Sensor list, for example Windows laptop, Moto dev phone, iPhone app, Bluetooth scanner, SDR.
- Device state: normal, airplane mode, Wi-Fi off, Bluetooth off, hotspot on/off, powered off, isolated.
- Movement state: arrived, parked, walking inside, leaving, away for 10 minutes, returned.
- Notes about nearby obvious infrastructure: apartments, store Wi-Fi, hotel, cell tower, vehicle hotspot, public Wi-Fi.

## Standard Window

Use the same shape every time:

1. `before`: scan for 3 to 5 minutes before arrival or before changing device state.
2. `arrival`: scan during arrival or while walking in.
3. `settle`: scan 5 to 10 minutes after stopping.
4. `control`: scan after phone/devices are off, airplane mode, or isolated.
5. `leave`: scan while leaving and 5 to 10 minutes after leaving.

If time is short, do `arrival`, `control`, and `leave`.

## What Counts Most

Strong evidence:

- Same exact BSSID family tails across unrelated places.
- Same unexplained family appearing only when a specific device or vehicle is present.
- Hidden/named sibling families changing within minutes of arrival or departure.
- Repeated RSSI shifts in the same family around the same device-state transition.
- Device-off/control window reduces or removes the suspicious pattern.

Weak evidence by itself:

- Hidden networks exist nearby.
- First-octet flips exist in one dense Wi-Fi environment.
- Common SSID names repeat in different towns.
- Bluetooth devices appear without stable identifiers or RSSI.

## Phone Scan Notes

When scanning from phones:

- Capture screenshots or exports with visible time.
- Note whether randomized MAC is enabled.
- Note whether hotspot is on.
- Note whether Wi-Fi and Bluetooth scanning are enabled even while Wi-Fi/Bluetooth toggles appear off.
- If possible, use two different phones in the same window and label them separately.

## Reviewer Framing

Ask reviewers to evaluate:

1. Whether the same BSSID-family behavior is normal for managed Wi-Fi in comparable places.
2. Whether same-tail first-octet shifts are expected for the observed vendors or SSIDs.
3. What control data would distinguish controller/mesh infrastructure from unusual mobile correlation.
4. Whether the dataset is sufficient to justify monitor-mode capture or additional sensors.

