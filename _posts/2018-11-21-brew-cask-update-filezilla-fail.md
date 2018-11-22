---
published: false
---
## A New Post

> brew cask outdated  
filezilla (3.34.0) != 3.38.1  

> brew cask reinstall filezilla  
==> Satisfying dependencies  
==> Downloading https://download.filezilla-project.org/client/FileZilla_3.38.1_macosx-x86.app.tar.bz2  
######################################################################## 100.0%  
curl: (16) Error in the HTTP2 framing layer  
Error: Download failed on Cask 'filezilla' with message: Download failed: https://download.filezilla-project.org/client/FileZilla_3.38.1_macosx-x86.app.tar.bz2  

> brew cask upgrade filezilla  
==> Upgrading 1 outdated package:  
filezilla 3.34.0 -> 3.38.1  
==> Satisfying dependencies  
==> Downloading https://download.filezilla-project.org/client/FileZilla_3.38.1_macosx-x86.app.tar.bz2  
######################################################################## 100.0%  
curl: (22) The requested URL returned error: 416  
==> Purging files for version 3.38.1 of Cask filezilla  
Error: Download failed on Cask 'filezilla' with message: Download failed: https://download.filezilla-project.org/client/FileZilla_3.38.1_macosx-x86.app.tar.bz2  

> brew config  
**HOMEBREW_VERSION:** 1.8.3-4-g7241156  
**ORIGIN:** https://github.com/Homebrew/brew.git  
**HEAD:** 72411560803d854256a2f75d09409bc5235b3755  
**Last commit:** 3 days ago  
**Core tap ORIGIN:** https://github.com/Homebrew/homebrew-core  
**Core tap HEAD:** e17277a630638792a2bb1ec36babbd784efb2bbd  
**Core tap last commit:** 5 hours ago  
**HOMEBREW_PREFIX:** /usr/local  
**HOMEBREW_VISUAL:** nano  
**CPU:** octa-core 64-bit haswell  
**Homebrew Ruby:** 2.3.7 => /System/Library/Frameworks/Ruby.framework/Versions/2.3/usr/bin/ruby  
**Clang:** 10.0 build 1000  
**Git:** 2.19.1 => /usr/local/bin/git  
**Curl:** 7.54.0 => /usr/bin/curl  
**Java:** 10, 1.8.0_131, 1.8.0_112, 1.8.0_102, 1.8.0_92, 1.8.0_74, 1.8.0_66, 1.8.0_51  
**macOS:** 10.13.6-x86_64  
**CLT:** 10.1.0.0.1.1539992718  
**Xcode:** 10.1  

Enter text in [Markdown](http://daringfireball.net/projects/markdown/). Use the toolbar above, or click the **?** button for formatting help.


Resources:  
https://github.com/Homebrew/homebrew-cask/blob/master/Casks/filezilla.rb  
https://github.com/Homebrew/homebrew-cask/issues/53634  