# Magic Userscript+

> [09/09/21] Greasy Fork version may not work due to userscript library being removed. Use [GitHub](https://raw.githubusercontent.com/magicoflolis/Userscript-Plus/master/dist/magic-userjs.user.js) version for now.

*Fork of [Userscript+ : Show Site All UserJS](https://greasyfork.org/scripts/24508-userscript-show-site-all-userjs). Source code & authors information found [here](https://github.com/jae-jae/Userscript-Plus#userscript).*

> Finds available UserJS for current site.

![Preview](https://raw.githubusercontent.com/magicoflolis/Userscript-Plus/master/resources/preview.png)

***

| Version | Link | Note | Alternative | Build |
|:----------:|:----------:|:----------:|:----------:|:----------:|
Chrome | ~~Install [Chrome Web Store]~~ | **There are no excluded websites, use at your own risk.** *Must be installed [manually](#manual-install).* | [Install [GitHub]](https://github.com/magicoflolis/Userscript-Plus/releases) | [Extension](#build-setup)
Firefox | [Install [Firefox Add-ons]](https://addons.mozilla.org/addon/userscript-plus) | **There are no excluded websites, use at your own risk.** *Can be installed [manually](#manual-install).* | [Install [GitHub]](https://github.com/magicoflolis/Userscript-Plus/releases) | [Add-on](#build-setup)
Userscript | [Install](#install-area) | The userscript **WON'T** work for all websites, [info](#known-bugs). | [Install [GitHub]](https://raw.githubusercontent.com/magicoflolis/Userscript-Plus/master/dist/magic-userjs.user.js) | [Userscript](#build-setup)

***

## Features

**_Optional_** *install [Greasyfork Search with Sleazyfork Results include](https://greasyfork.org/scripts/23840).*

> Currently [Userscript+](https://github.com/jae-jae/Userscript-Plus#userscript) can only find userscripts through __GreasyFork__, I've added support for __SleazyFork__ along with a few additional features and tweaks!

* Tested and compatible with TamperMonkey n ViolentMonkey.
* Trimmed / moved some @resources to this build.
* Added [SleazyFork](https://sleazyfork.org).
* Added Dark Theme.
* Added extra @excludes.
* Added built-in [Greasyfork Search with Sleazyfork Results include](https://greasyfork.org/scripts/23840).

```bash
let sleazyfork_redirect = false; // "true" to enable, "false" to disable
```

## Known bugs

* [ User Script ] *May* conflict with a few running user scripts. (Example: [Twitter External Translator](https://greasyfork.org/scripts/421643))
* [ All ] May leave a opened tab when installing user scripts.
* [ User Script ] Found count may not appear.
* [ User Script ] In some sites below the plug-in interface icon is not displayed

> **Reason**???This is because the security policy of these sites to prevent the plug-in icon font file loading, resulting in the icon does not display properly.

## Manual Install

Chromium

* Download and unzip [latest release](https://github.com/magicoflolis/Userscript-Plus/releases) into desired folder.
* Go to chromium/chrome *Extensions*.
* Click to check *Developer mode*.
* Click *Load unpacked extension...*.
* In the file selector dialog:
  * Select the directory `userscript_for_tampermonkey-*` / desired folder.
  * Click *Open*.

Firefox

> See: [Temporary installation in Firefox](https://extensionworkshop.com/documentation/develop/temporary-installation-in-firefox)

* Download and unzip [latest release](https://github.com/magicoflolis/Userscript-Plus/releases) into desired folder.
* Copy and paste `about:debugging#/runtime/this-firefox` into your URL.
* Click *Load Temporary Add-on???*.
* In the file selector dialog:
  * Select the directory `userscript_for_tampermonkey-*` / desired folder.
  * Click *Open*.

## Build Setup

> Developed using [VSCodium](https://vscodium.com).

| Help Links |
|:----------:|
[web-ext documentation](https://extensionworkshop.com/documentation/develop/getting-started-with-web-ext/) |
[http-server](https://github.com/http-party/http-server) |
[How to edit scripts with your favorite editor?](https://violentmonkey.github.io/posts/how-to-edit-scripts-with-your-favorite-editor/#install-a-local-script) |

```bash
# Install dependencies ( if error use npm i --force )
npm i
# [ Production ] Builds both User Script and Browser Extension
npm run build:all
# [ Development ] User Script
# Recommend bookmarking for faster deployment
# http://localhost:8080/magic-userjs.user.js
npm run dev:user
npm run http-server
# [ Development ] Browser Extension
# For Firefox use web-ext
# Recommended to create additional profile about:profiles
web-ext run -p <profile>
npm run dev:browser
# For Chrome load unpacked, REPLACE manifest.json with chrome-manifest.json
```

## Source Code

* [GitHub](https://github.com/magicoflolis/Userscript-Plus)

### License

MIT

### Contacts

[GitHub](https://github.com/magicoflolis)

[Twitter](https://twitter.com/for_lollipops)

[Greasy Fork](https://greasyfork.org/users/166061)
