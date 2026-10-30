# Local manifests for the Xiaomi Pad 8 Pro (piano)

| | |
| --- | --- |
| Path | `.repo/local_manifests` |
| Android | 17 |

```
git clone https://github.com/xiaomi-pad-8-pro-development/local_manifests -b seventeen .repo/local_manifests
repo sync
```

`piano.xml` has the required trees. For extras, copy files from `optional/` next to it:

| File | Adds |
| --- | --- |
| `piano-xiaomi-parts.xml` | Pen, keyboard, display |
| `piano-alxp-parts.xml` | AirPods, iPhone, Mac |
| `piano-xiaomi-camera.xml` | Xiaomi camera |
| `piano-xiaomi-notes.xml` | Xiaomi Notes |
| `piano-aosp-notes.xml` | AOSP Notes |
| `piano-patches.xml` | ROM patches |
