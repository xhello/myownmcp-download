# Connector Hub downloads

Installers for Connector Hub, a Windows app that keeps your knowledge on your own PC and lets you choose which AI apps
and people may use it. About the app: https://www.myownmcp.com

This repository holds release files only. The app's source code is not here.

## Latest: 0.1.1 test build

**This is a test build.** It is not signed, and it has not been installed on any PC yet. Expect rough edges, and
install it only on a PC you test with, as the installer itself says.

- File: `ConnectorHub-Setup-0.1.1-unsigned.exe` (142 MB), on the [Releases](../../releases) page
- SHA-256: `9699FFC8B8AD428A4707EE1DBA693F51B0460B271B4881DD4D8DBDCC49951727`

Check the file in PowerShell before you run it. The hash it prints must match the one above:

    Get-FileHash .\ConnectorHub-Setup-0.1.1-unsigned.exe

## Which Windows versions

| Windows | Works? |
|---|---|
| Windows 11, 64-bit (x64) | Made for it, but this test build hasn't been installed on any PC yet |
| Windows 10 version 22H2, 64-bit (x64) | The installer accepts it, but it is not tested yet. Microsoft ended support for Windows 10 on 14 October 2025. |
| Windows on ARM PCs | No: the installer refuses them |
| 32-bit Windows, Windows 10 before version 22H2, Windows 8.1 and older | No |
| Windows in S mode | No: S mode runs only apps from the Microsoft Store |

The app and the installer are in English. Connector Hub installs for your Windows account only, so installing it needs
no administrator rights. Mac and Linux versions don't exist yet.

## Installing an unsigned test build

- Your browser may warn that the file isn't commonly downloaded. Keep it, then check its SHA-256 before you run
  it, and delete it if it doesn't match.
- Windows may show "Windows protected your PC". Select More info, then Run anyway.
- If Smart App Control is on, Windows blocks this test build. Wait for the signed build.

## After installing

Connector Hub runs on your PC, and you use it in your browser. The first Google account that signs in becomes the
hub's owner. MCP, the part that lets Claude or ChatGPT use your Memories, stays off until you turn it on in the app's
MCP tab.

## Licence

Connector Hub is proprietary software. The installer shows its licence, which is still a draft for legal review
and not in effect.
