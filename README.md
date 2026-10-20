# Local manifests for the Xiaomi Pad 8 Pro (piano)

Add every Xiaomi Pad 8 Pro tree to an Android 17 ROM checkout:

```
git clone https://github.com/xiaomi-pad-8-pro-development/local_manifests \
    -b seventeen .repo/local_manifests
repo sync
```

`hardware/xiaomi` comes from the ROM's own manifest. Remove the
`android_device_xiaomi_piano-alxp-parts` line to build without ALXP Features.
