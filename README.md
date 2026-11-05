# My Own MCP downloads

Installers for My Own MCP, a Windows app that keeps your knowledge on your own PC and lets you choose which AI apps
and people may use it. About the app: https://www.myownmcp.com

This repository holds release files only. The app's source code is not here.

## Latest: 0.1.3 signed test build

**This is a test build.** It is signed, and so far it has been tried only on the developer's own PC. Expect rough
edges, and install it only on a PC you test with.

- File: `MyOwnMCP-Setup-0.1.3.exe` (143 MB), on the [Releases](../../releases) page
- SHA-256: `86ED157323D3CB977D44216C077907C83712A0BF404763CE414CB2C54816F725`
- Signed by Wei Yuan, through Microsoft's Artifact Signing service

Check the file in PowerShell before you run it. If your browser saved it in your Downloads folder, run this; the
hash it prints must match the one above:

    Get-FileHash "$HOME\Downloads\MyOwnMCP-Setup-0.1.3.exe"

To check the signature, right-click the file, select Properties, then Digital Signatures, select Wei Yuan,
then Details: Windows should say "This digital signature is OK."

## Which Windows versions

| Windows | Works? |
|---|---|
| Windows 11 on an Intel or AMD PC (x64) | Made for it. So far this test build has been tried only on the developer's own PC |
| Windows 10 version 22H2, 64-bit (x64) | The installer accepts it, but it is not tested yet. Microsoft ended support for Windows 10 on 14 October 2025. |
| Windows on ARM PCs | No: the installer refuses them |
| 32-bit Windows, Windows 10 before version 22H2, Windows 8.1 and older | No |
| Windows in S mode | No: S mode runs only apps from the Microsoft Store |

The app and the installer are in English. My Own MCP installs for your Windows account only, so installing it needs
no administrator rights. There is no Mac or Linux version. A Mac version is planned.

## What to expect when you install it

- Your browser may warn that the file isn't commonly downloaded (Chrome shows "Suspicious download blocked").
  Keep it (in Chrome, choose Download suspicious file), then check its SHA-256 before you run it, and delete it
  if it doesn't match.
- Windows may show "Windows protected your PC". Select More info, check that the publisher is Wei Yuan, then
  select Run anyway.
- New downloads can get these two warnings until enough people have downloaded them, even when they're
  signed.
- When Microsoft's cloud service can't tell whether an app is safe, Smart App Control lets it run if it has
  a valid signature, so it shouldn't block this signed build, but that isn't tried yet on a PC with Smart
  App Control turned on.

## After installing

My Own MCP runs on your PC, and you use it in your browser. The first Google account that signs in becomes the
hub's owner. For now Google's sign-in screen says "to continue to connector", from the app's earlier name, Connector
Hub: that is this app. MCP, the part that lets your own AI app, such as Claude, use your Memories (in testing; ChatGPT is being
confirmed), stays off until you turn it on in the app's MCP tab.

## Source code of open-source parts

Some open-source parts of My Own MCP come under licenses that ask for their source code to be available. The
source of GNU libiconv and lxml is at https://www.myownmcp.com/source; THIRD-PARTY-NOTICES.txt, in the folder
My Own MCP installs to, says where the rest is.

## Licence

My Own MCP is proprietary software. The installer shows its licence before you install.

## Older builds

The app was called Connector Hub up to 0.1.2. 0.1.2 was its first signed test build and 0.1.1 an unsigned one. Use 0.1.3
instead: it installs over either of them, stays in the folders it finds and is made to keep your data (tried over 0.1.2,
on a PC with no Memories yet; not yet tried over 0.1.1).
