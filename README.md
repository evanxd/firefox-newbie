# Firefox Newbie
The repo provides documents and config files to help newbies setup development environment and contribute code to Firefox. The document is referred to the [Simple Firefox build][simple-firefox-build] document on [MDN][mdn].

## Get Started
Before start to hack Firefox, you need to setup your development environment to build and run your own Firefox with source code.

### Setup Development Environment
1. Install [homebrew][homebrew] with the `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` command.
2. Run `brew doctor` to ensure there is no warning and show `Your system is ready to brew.` or fix it.
3. [Install the dependencies for Mac OS][macos-dependencies] with the `curl https://hg.mozilla.org/mozilla-central/raw-file/default/python/mozboot/bin/bootstrap.py > bootstrap.py && python bootstrap.py` command.
4. Get the source code of Firefox with the `hg clone https://hg.mozilla.org/mozilla-central` command.

### Build Firefox
1. Download the [mozconfig][mozconfig] file and store it in the `mozilla-central` directory.
2. Run `./mach build`. If you would like to build faster, please run `./mach build faster`.

### Run Firefox
1. Run `./mach run` to launch the Firefox Nightly you just built.

Now, let's start to hack Firefox!

[homebrew]: http://brew.sh
[macos-dependencies]: https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/Build_Instructions/Mac_OS_X_Prerequisites
[mozconfig]: https://github.com/evanxd/firefox-newbie/blob/master/mozconfig
[simple-firefox-build]: https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/Build_Instructions/Simple_Firefox_build
[mdn]: https://developer.mozilla.org
