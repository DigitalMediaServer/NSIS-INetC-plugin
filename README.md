# NSIS INetC plug-in

The [INetC (Internet client) plug-in][1] is a [NSIS][2] plugin downloading and uploading files. It is based on the 
[InetLoad plug-in][4]. The network implementation uses `MS WinInet API`, and supports the `HTTP`, `HTTPS` and `FTP` protocols.

[NSIS (Nullsoft Scriptable Install System)][2] is a professional open source system to create Windows installers.
It is designed to be as small and flexible as possible and is therefore very suitable for internet distribution.

This is a modified version of `1.0.5.2`. Since I couldn't find a source repository, I've created a Git repository and 
committed the downloaded source files. These changes would otherwise have been submitted as a pull request or patch.
I couldn't find an explicit license for [INetC plug-in][1], which means that this is licensed implicitly with the `zLib License`
according to the [NSIS license][3].

Changes in this fork are:
* **1.0.5.3** - Added options `/TEXTCOLOR "RRGGBB"` and `/BGCOLOR "RRGGBB"`
* **1.0.5.4** - Created a 4th download dialog `/MODERNPOPUP`
* **1.0.5.5** - Created option `/NOSSL` which prevents redirects from HTTP to HTTPS

Nadahar

  [1]: http://nsis.sourceforge.net/Inetc_plug-in
  [2]: http://nsis.sourceforge.net/Main_Page
  [3]: http://nsis.sourceforge.net/License
  [4]: http://nsis.sourceforge.net/InetLoad_plug-in
