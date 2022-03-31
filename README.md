# NSIS INetC plug-in

The [INetC (Internet client) plug-in][1] is a [NSIS][2] plugin downloading and uploading files. It is based on the 
[InetLoad plug-in][4]. The network implementation uses `MS WinInet API`, and supports the `HTTP`, `HTTPS` and `FTP` protocols.

**Note:** There are some unfortunate issues with `MS WinInet API`, as it is based on using parts of the long abandoned Internet Explorer. This means that IE users settings (Proxy settings etc.) will apply to this plugin as well. In addition, it's not exactly up-to-date in many respects - and it will only support TLS 1.1 on Windows XP for example. There now exists an alternative plugin [NSCurl](https://github.com/negrutiu/nsis-nscurl) that uses [libcurl](https://curl.haxx.se/libcurl/) and [OpenSSL](https://www.openssl.org/) instead of `WinInet`. While I haven't personally tried it, this might be a better solution for many.

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
* **1.0.5.6** - Applied changes from upstream `1.0.5.3`: `/tostackconv` supports UTF-8 and UTF-16LE BOM sniffing and conversion.
* **1.0.5.7** - Fixed download progress for files larger than 2 GB (thanks @pjpuchyr) and reverted changes that broke `/WEAKSECURITY`.

Nadahar

  [1]: http://nsis.sourceforge.net/Inetc_plug-in
  [2]: http://nsis.sourceforge.net/Main_Page
  [3]: http://nsis.sourceforge.net/License
  [4]: http://nsis.sourceforge.net/InetLoad_plug-in
