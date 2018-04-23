---
published: false
---
I wanted to update "Kindle for Mac" app. I have it installed using bask cask.
Notice an application that's out-of-date in Homebrew-Cask? 

	$ brew cask info kindle
	kindle: 48016
	https://www.amazon.com/gp/digital/fiona/kcp-landing-page
	/usr/local/Caskroom/kindle/44182 (64B)
	/usr/local/Caskroom/kindle/48016 (64B)
	From: https://github.com/caskroom/homebrew-cask/blob/master/Casks/kindle.rb
	==> **Name**
	Kindle for Mac
	==> **Artifacts**
	Kindle.app (App)

I looked to see what version of kindle is available and it shows brew cask has version "48016" availible. I went online and saw that the latest version is actually "50131".
In most cases, it's very simple to update it. We have a script that will ask for the new version number, and take care of updating the Cask file and submitting a pull request to us:

	$ brew install vitorgalvao/tiny-scripts/cask-repair
	Updating Homebrew...
	==> **Auto-updated Homebrew!**
	Updated 2 taps (caskroom/versions, caskroom/cask).
	
	==> **Tapping vitorgalvao/tiny-scripts**
	Cloning into '/usr/local/Homebrew/Library/Taps/vitorgalvao/homebrew-tiny-scripts'...
	remote: Counting objects: 33, done.
	remote: Compressing objects: 100% (33/33), done.
	remote: Total 33 (delta 15), reused 3 (delta 0), pack-reused 0
	Unpacking objects: 100% (33/33), done.
	Tapped 29 formulae (86 files, 45.5KB)
	==> **Installing cask-repair from vitorgalvao/tiny-scripts**
	==> **Installing dependencies for vitorgalvao/tiny-scripts/cask-repair: hub, hr**
	==> **Installing vitorgalvao/tiny-scripts/cask-repair dependency: hub**
	==> **Downloading https://homebrew.bintray.com/bottles/hub-2.2.9.high_sierra.bottle.tar.gz**
	######################################################################## 100.0%
	==> **Pouring hub-2.2.9.high_sierra.bottle.tar.gz**
	==> **Caveats**
	Bash completion has been installed to:
	  /usr/local/etc/bash_completion.d

	zsh completions have been installed to:
	  /usr/local/share/zsh/site-functions
	==> **Summary**
	🍺  /usr/local/Cellar/hub/2.2.9: 10 files, 9.4MB
	==> **Installing vitorgalvao/tiny-scripts/cask-repair dependency: hr**
	==> **Downloading https://github.com/LuRsT/hr/archive/1.2.tar.gz**
	==> **Downloading from https://codeload.github.com/LuRsT/hr/tar.gz/1.2**
	######################################################################## 100.0%
	🍺  /usr/local/Cellar/hr/1.2: 5 files, 6.5KB, built in 2 seconds
	==> **Installing vitorgalvao/tiny-scripts/cask-repair**
	==> **Cloning https://github.com/vitorgalvao/tiny-scripts.git**
	Cloning into '/Users/esko/Library/Caches/Homebrew/cask-repair--git'...
	remote: Counting objects: 36, done.
	remote: Compressing objects: 100% (35/35), done.
	remote: Total 36 (delta 1), reused 12 (delta 0), pack-reused 0
	Unpacking objects: 100% (36/36), done.
	==> **Checking out branch master**
	🍺  /usr/local/Cellar/cask-repair/0.36.3: 5 files, 26KB, built in 2 seconds
	$ cask-repair --help
	
	usage: cask-repair [options] <cask_name>
	
	options:
	  -o, --open-home                        Open the homepage for the given cask.
	  -a, --open-appcast                     Open the appcast for the given cask.
	  -v, --cask-version                     Give a version directly, instead of being prompted for it.
	  -u, --cask-url                         Give a URL directly, instead of being prompted for it.
	  -e, --edit-cask                        Opens cask for editing before trying first download.
	  -c <number>, --closes-issue <number>   Adds 'Closes #<number>.' to the commit message.
	  -b, --blind-submit                     Submit cask without asking for confirmation, if there are no errors.
	  -f, --fail-on-error                    If there are any errors with the submission, abort.
	  -w, --allow-warnings                   If set to fail on error and there are only warnings, do not abort.
	  -i, --install-cask                     Installs your updated cask after submission.
	  -d, --delete-branches                  Deletes all local and remote branches named like cask_repair_update-<word>.
	  -h, --help                             Show this help.

	$ cask-repair kindle
	`hub` is not configured.
	To do it, run `cd $(brew --repository) && hub issue`. Your Github password will be required, but is never stored.
    

