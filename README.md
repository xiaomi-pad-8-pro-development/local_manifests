# Local manifests for the Xiaomi Pad 8 Pro (piano)

Adds the Xiaomi Pad 8 Pro trees to an Android 17 ROM checkout.

`piano.xml` has the trees every build needs: the device, common and kernel
trees and the vendor blobs. Each optional part has its own file in
`optional/`; copy the ones you want next to `piano.xml`:

| File | What it adds |
| --- | --- |
| `optional/piano-xiaomi-parts.xml` | Xiaomi Parts: pen, keyboard cover and display settings |
| `optional/piano-alxp-parts.xml` | ALXP Features: AirPods switching, iPhone notifications, Mac link |
| `optional/piano-xiaomi-camera.xml` | Xiaomi camera |
| `optional/piano-xiaomi-notes.xml` | Xiaomi Notes |
| `optional/piano-patches.xml` | ROM source patches: stylus laser, keyboard cover, Settings |

```
git clone https://github.com/xiaomi-pad-8-pro-development/local_manifests \
    -b seventeen .repo/local_manifests
cp .repo/local_manifests/optional/piano-xiaomi-parts.xml .repo/local_manifests/
repo sync
```

`repo` reads only the top level of `.repo/local_manifests`, so files left in
`optional/` are ignored. The device tree includes each optional part only
when it is synced. `hardware/xiaomi` comes from the ROM's own manifest.
