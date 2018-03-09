# NSIS INetC plug-in

The [INetC (Internet client) plug-in][1] is a [NSIS][2] plugin downloading and uploading files. It is based on the 
[InetLoad plug-in][4]. The network implementation uses `MS WinInet API`, and supports the `HTTP`, `HTTPS` and `FTP` protocols.

[NSIS (Nullsoft Scriptable Install System)][2] is a professional open source system to create Windows installers.
It is designed to be as small and flexible as possible and is therefore very suitable for internet distribution.

This is a modified version of `1.0.5.2`. Since I couldn't find a source repository, I've created a Git repository and 
committed the downloaded source files. These changes would otherwise have been submitted as a pull request or patch.
I couldn't find an explicit license for [INetC plug-in][1], which means that this is licensed implicitly with the `zLib License`
according to the [NSIS license][3].

The changes in this version is that a fourth download dialog has been created (`/MODERNPOPUP`). I found the
existing `/POPUP` dialog to be visually outdated and with a strange organization of the download information.
No functionality related to the download itself has been changed.

Nadahar

  [1]: http://nsis.sourceforge.net/Inetc_plug-in
  [2]: http://nsis.sourceforge.net/Main_Page
  [3]: http://nsis.sourceforge.net/License
  [4]: http://nsis.sourceforge.net/InetLoad_plug-in
