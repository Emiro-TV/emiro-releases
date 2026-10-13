# Emiro releases

Downloads of Emiro, a self-hosted media server. The source code is not public; this repository
holds only the built packages, published by the build of each component.

| Tag | What it is |
|---|---|
| `server-v<version>` | The Emiro server, as a QNAP package (`.qpkg`, x86-64). |
| `m3u-v<version>` | The M3U/XMLTV live TV plugin, as a zip for the server's plugin directory. |

## Installing

- **QNAP:** App Center → Install Manually → choose the `.qpkg`.
- **Plugin:** in the Emiro admin interface, Plugins → upload the zip, then reload the plugins.

## License

Emiro is proprietary software, free of charge. See [LICENSE](LICENSE).

It is built on open-source components, each under its own license. A running server lists all of
them - with their license texts and, for the LGPL components such as FFmpeg, their complete source
code to download - under **Licenses** in the account menu. A plugin's components are listed there
under the plugin's name.
