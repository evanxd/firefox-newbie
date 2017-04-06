# Firefox Newbie
The repo provides documents and config files to help newbies setup development environment and contribute code to Firefox. The document is referred to the [Simple Firefox build][simple-firefox-build] document on [MDN][mdn].

## Get Started
Before start to hack Firefox, you need to setup your development environment to build and run your own Firefox with source code.

### Setup Development Environment
1. Install [homebrew][homebrew] with the `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` command.
2. Run `brew doctor` to ensure there is no warning and show `Your system is ready to brew.` or fix it.
3. [Install the dependencies for Mac OS][macos-dependencies] with the `curl https://hg.mozilla.org/mozilla-central/raw-file/default/python/mozboot/bin/bootstrap.py > bootstrap.py && python bootstrap.py` command.
4. Run `brew install mercurial` to install Mercurial (HG).
5. Run `brew link mercurial` to link Mercurial.
6. Run `brew link git` to link Git.
7. Get the source code of Firefox with the `hg clone https://hg.mozilla.org/mozilla-central` command.

### Build Firefox
1. Download the [mozconfig][mozconfig] file and store it in the `mozilla-central` directory.
2. Run `./mach build`. If you would like to build faster, please run `./mach build faster`.

### Run Firefox
* Run `./mach run` to launch the Firefox Nightly you just built.

Now, let's start to hack Firefox!

## Run Test
Please ensure Firefox is closed before run test.

### Run All Tests
* Run `./mach test`.

### Run A Specific Test
* Run `./mach test <path_to_test_file>`. For example, run `./mach test devtools/client/shared/components/test/mochitest/test_reps_grip.html` to run the `Rep test - grip` test.

### Run Test on Debug Mode
1. Add `debugger` in somewhere.
2. Run `./mach mochitest --jsdebugger ./toolkit/components/passwordmgr/test/browser/browser_capture_doorhanger.js`.

## Send Try Request
1. Get your commit access(level 1) by fired a [bugzilla][bugzilla] bug. For example, [Bug 988801][bug-988801] is the bug I got my commit access.
2. Download the [config][try-config] file and store it in `~/.ssh` directory to setup try info.
3. Change `your@email.com` to your commit access email in the [config][try-config] file.
4. Generate the try command on TryChooser Syntax Builder[trychooser-syntax-builder].
5. Run the command generated by the [builder][trychooser-syntax-builder]. For example, run `./mach try -b do -p linux -u all -t none` to run all unit test suites for Linux platform.

## Reivew
* [Module Owner List][module-owner-list]
* Push a [MozReview][moz-review]: `hg push review`

## Mercurial
* [Mercurial][mercurial]

## Search Code
* [Searchfox][searchfox]

## Bugs
Check [bug list][bug-list] here.

## Tips
* [Dev Tools][devtools]

[homebrew]: http://brew.sh
[macos-dependencies]: https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/Build_Instructions/Mac_OS_X_Prerequisites
[mozconfig]: https://github.com/evanxd/firefox-newbie/blob/master/mozconfig
[simple-firefox-build]: https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/Build_Instructions/Simple_Firefox_build
[mdn]: https://developer.mozilla.org
[try-config]: https://github.com/evanxd/firefox-newbie/blob/master/config
[trychooser-syntax-builder]: http://trychooser.pub.build.mozilla.org
[bugzilla]: https://bugzilla.mozilla.org
[bug-988801]: http://bugzil.la/[bug-988801
[devtools]: https://github.com/evanxd/firefox-newbie/blob/master/dev-tools.md
[mercurial]: https://github.com/evanxd/firefox-newbie/blob/master/mercurial.md
[bug-list]: https://github.com/evanxd/firefox-newbie/blob/master/bugs.md
[searchfox]: http://searchfox.org
[module-owner-list]: https://wiki.mozilla.org/Modules/All
[moz-review]: http://mozilla-version-control-tools.readthedocs.io/en/latest/mozreview.html
