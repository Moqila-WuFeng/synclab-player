# Third-Party Notices

SyncLab Player uses APIs provided by FFmpeg and SDL3. These projects are independent from SyncLab Player and retain their respective copyrights, trademarks, and license terms. Their source code, development packages, libraries, and runtime binaries are not included in this repository.

## FFmpeg

- Project: <https://ffmpeg.org/>
- Copyright: the FFmpeg developers and other contributors
- License information: <https://ffmpeg.org/legal.html>

FFmpeg is generally available under GNU LGPL 2.1 or later. Optional components can cause a particular FFmpeg build to be covered by GNU GPL 2 or later. SyncLab Player links dynamically to FFmpeg libraries supplied by the builder.

Before distributing an application binary together with FFmpeg libraries, inspect the exact FFmpeg build with `ffmpeg -L` and `ffmpeg -buildconf`, include the applicable license text and notices, and provide the corresponding FFmpeg source and build information when required by that license. Do not assume that the license of one FFmpeg build applies to another build.

The threading and synchronization model in this project is informed by FFmpeg's `ffplay` reference implementation. FFmpeg is a trademark of Fabrice Bellard, originator of the FFmpeg project.

## SDL3

- Project: <https://www.libsdl.org/>
- Source and license: <https://github.com/libsdl-org/SDL/blob/main/LICENSE.txt>
- Copyright: Sam Lantinga and SDL contributors
- License: zlib License

SDL requests that the origin of its software is represented accurately, altered source versions are marked, and its license notice remains in source distributions. An acknowledgment in product documentation is appreciated by the SDL project.
