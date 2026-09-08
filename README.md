# Strata preview selection evidence

Synthetic text files captured on an isolated Xvfb display, GTK 4.22.4.

- Before: upstream `916095ac27f097d72863883ca5c3b1aae25540e3`.
- After: fix `8a6b5e9`.
- Open `notes.txt` with Space, then select `report.txt` with Down (List) or Right (Icons).
- Before, the preview remains on `notes.txt`; after, the preview follows `report.txt`.

These images are review attachments for lgse/strata#609, not application assets.
