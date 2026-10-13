# Emiro releases

Downloads of Emiro, a self-hosted media server. The source code is not public; this repository
holds only the built packages, published by the build of each component.

| Tag | What it is |
|---|---|
| `server-v<version>` | The Emiro server, in every package below, with `SHA256SUMS`. |
| `m3u-v<version>` | The M3U/XMLTV live TV plugin, as a zip for the server's plugin directory. |

## Installing the server

| Platform | File | |
|---|---|---|
| Windows 10/11, x86-64 or ARM | `emiro-<version>-windows-<amd64\|arm64>.zip` | Unpack anywhere, start `emiro.cmd`. |
| macOS 13+, Apple silicon or Intel | `emiro-<version>-macos-<arm64\|amd64>.tar.gz` | Unpack, then `xattr -dr com.apple.quarantine emiro-*` and `./emiro`. The build is not signed. |
| Ubuntu 24.04 | `emiro_<version>-1_<amd64\|arm64>.deb` | `sudo apt install ./emiro_<version>-1_<arch>.deb` |
| Fedora 44 | `emiro-<version>-1.<x86_64\|aarch64>.rpm` | `sudo dnf install ./emiro-<version>-1.<arch>.rpm` |
| QNAP QTS / QuTS hero 5.0+ | `Emiro_<version>_<x86_64\|arm_64>.qpkg` | App Center → Install Manually. |

The server listens on port 1810: open `http://<machine>:1810` to set it up. On Linux it runs as the
systemd service `emiro`, with its settings in `/etc/emiro/emiro.conf` and its data in
`/var/lib/emiro`.

Transcoding needs a GPU: Intel (QuickSync), NVIDIA (NVENC), AMD (VAAPI, Linux only) or Apple
(VideoToolbox). Without one, and on Windows on ARM, the server plays what a client can take and
remuxes the rest.

## Installing a plugin

In the Emiro admin interface, Plugins → upload the zip, then reload the plugins.

## License

Emiro is proprietary software, free of charge. See [LICENSE](LICENSE).

It is built on open-source components, each under its own license. A running server lists all of
them - with their license texts and, for the LGPL components such as FFmpeg, their complete source
code to download - under **Licenses** in the account menu. A plugin's components are listed there
under the plugin's name.
