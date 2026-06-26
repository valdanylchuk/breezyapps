# BreezyBox apps

**Notice:** This repo is outdated; moved to [valdanylchuk/breezybox/apps](https://github.com/valdanylchuk/breezybox/tree/main/apps)

These are some ELF apps compatible with [BreezyBox](https://github.com/valdanylchuk/breezybox) shell running on ESP32-S3.

Some can also be compiled with gcc to run on POSIX-compatible systems, e.g. Mac OS:

- [plasma](plasma/) - ANSI console full-screen "plasma" effect
- [termbench](termbench/) - small vterm benchmark
- [vi](vi/) - minimal vi clone

Some depend on specific exports being available from your ESP-IDF firmware, usually via BreezyBox:

- [gzip](gzip/gzip.c) - gzip compressor
- [gunzip](gzip/gunzip.c) - gzip decompressor
- [wget](wget/) - minimal wget downloader clone

## Installation in BreezyBox
(for the whole bundle):
```
eget valdanylchuk/breezyapps
```

## Building from source

POSIX versions for your Mac can be built literally like this:

```
gcc vi.c
```

For ESP32 builds, there is usually buildelf.sh included, with the build commands I used. You will need xtensa-esp32s3-elf-gcc from the xtensa-esp-elf toolkit. [Espressif IDF Tools documentation](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/api-guides/tools/idf-tools.html) provides a good starting point on where to get and how to install that.

You do not need a full ESP-IDF CMakeLists.txt and idf.py based setup for this.

## More BreezyBox apps elsewhere:

- [xcc700](https://github.com/valdanylchuk/xcc700) - mini C compiler

## License
This is free software under [MIT License](LICENSE).
