# Third-Party SDK Setup

This directory contains only dependency setup information. FFmpeg and SDL3 archives, headers, import libraries, DLLs, source code, and license files are intentionally excluded from this repository.

## FFmpeg

The current CMake configuration is tested with the following shared LGPL build:

| Item | Value |
| --- | --- |
| Provider | [BtbN/FFmpeg-Builds](https://github.com/BtbN/FFmpeg-Builds) |
| Release | [autobuild-2026-09-02-13-13](https://github.com/BtbN/FFmpeg-Builds/releases/tag/autobuild-2026-09-02-13-13) |
| Archive | `ffmpeg-n8.1.2-50-g1a748fe2cd-win64-lgpl-shared-8.1.zip` |
| SHA-256 | `46744f3ef783805376fbcc72a3067bacd9f78c929e13882e54b2e2fad5f69966` |
| FFmpeg version | `n8.1.2-50-g1a748fe2cd-20260902` |
| Package license | GNU LGPL version 3 or later |

Download the archive, verify its checksum, and extract it so these files are present:

```text
third_party/ffmpeg/include/libavutil/avutil.h
third_party/ffmpeg/lib/libavutil.dll.a
third_party/ffmpeg/lib/libavformat.dll.a
third_party/ffmpeg/lib/libavcodec.dll.a
third_party/ffmpeg/lib/libswscale.dll.a
third_party/ffmpeg/lib/libswresample.dll.a
third_party/ffmpeg/bin/avutil-60.dll
third_party/ffmpeg/bin/avformat-62.dll
third_party/ffmpeg/bin/avcodec-62.dll
third_party/ffmpeg/bin/swscale-9.dll
third_party/ffmpeg/bin/swresample-6.dll
third_party/ffmpeg/LICENSE.txt
```

Keep the package license file together with the SDK. Inspect the selected build with `ffmpeg -L` and `ffmpeg -buildconf`; FFmpeg license terms depend on its enabled components.

## SDL 3.4.16

| Item | Value |
| --- | --- |
| Provider | [libsdl-org/SDL](https://github.com/libsdl-org/SDL) |
| Release | [release-3.4.16](https://github.com/libsdl-org/SDL/releases/tag/release-3.4.16) |
| Archive | `SDL3-devel-3.4.16-mingw.zip` |
| SHA-256 | `9828bb735cf8a007bcf0ac5aa9f01f3fcb54b7ca67c932e775c905c5d5053a60` |
| License | zlib License |

Download and verify the archive, then place its contents at `third_party/SDL3`. The x64 build must provide:

```text
third_party/SDL3/x86_64-w64-mingw32/include/SDL3/SDL.h
third_party/SDL3/x86_64-w64-mingw32/include/SDL3/SDL_main.h
third_party/SDL3/x86_64-w64-mingw32/lib/libSDL3.dll.a
third_party/SDL3/x86_64-w64-mingw32/lib/cmake/SDL3/SDL3Config.cmake
third_party/SDL3/x86_64-w64-mingw32/bin/SDL3.dll
third_party/SDL3/LICENSE.txt
```

The imported CMake target `SDL3::SDL3` supplies headers and link settings. The build copies `SDL3.dll` beside each executable that needs it.
