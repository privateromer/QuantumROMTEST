# services.jar Patches

Place any `.patch` or `.diff` files inside this directory.

During the ROM build process:
1. `services.jar` is decompiled.
2. All `*.patch` and `*.diff` files in this directory are automatically applied using `patch` (with `-p1`, `-p0`, `-p2` automatic detection) or `git apply`.
3. `services.jar` is recompiled and integrated into the ROM.

You can also place replacement `.smali` files or `smali_classes*` folders here to overlay directly onto the decompiled `services.jar`.
