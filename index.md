---
layout: product
title: Visor is a system-wide terminal accessible via a hot-key
product: visor
product_title: Visor
product_subtitle: a system-wide terminal on a hot-key
download: http://totalterminal.binaryage.com
downloadtitle: Switch to TotalTerminal
buttonicon: warning
downloadsubtitle: Visor has been renamed to TotalTerminal
repo: http://github.com/darwin/visor
meta_title: Visor is a system-wide terminal accessible via a hot-key
meta_keywords: visor,terminal,osx,simbl,binaryage,productivity,software
meta_description: Visor is just a light-weight plugin for Terminal.app (SIMBL)
meta_image: http://www.binaryage.com/base/img/icons/visor-256.png
facebook: 1
retweet: 1
buzz: 1
fbsdk: 1
flattr: http://visor.binaryage.com
ogmeta: {
    site_name: "BinaryAge website",
    description: "Visor is a system-wide terminal for OSX available on a hot-key",
    email: "support@binaryage.com",
    type: "product",
    title: "Visor",
    url: "http://visor.binaryage.com",
    image: "http://www.binaryage.com/base/img/icons/visor-256.png"
}
shots: [{
    title: "Visor Terminal with nice colors!",
    thumb: "/base/img/visor-mainshot.png",
    full: "/base/img/visor-mainshot-full.png"
}]
---

## What's up?

#### Please note that I've changed the name of the program some time ago.

#### Visor has a [new home](http://totalterminal.binaryage.com) and it is called **TotalTerminal** now.

#### Don't worry it is still open-source and I will continue to support TotalTerminal in the future.

## Installation

  1. **[Install SIMBL](http://www.culater.net/software/SIMBL/SIMBL.php)** and <span style="color:#d22">make sure you have latest SIMBL 0.9.x</span>
  2. Place Visor.bundle into `~/Library/Application Support/SIMBL/Plugins` (create this directory if it does not already exist)
  3. Relaunch Terminal.app - You should now see the Visor Status Menu Item
  4. Configure your keyboard trigger by selecting the Visor Status Menu Item -> `Visor Preferences ...` and edit your keyboard `hot-key`

#### You can now trigger Visor with your hot-key from any application to get an instant terminal session. 

To hide Visor, you can either:

  * re-trigger with your key-combo
  * optionally, you can click off the Visor window

### Compatibility
 
  * **Visor 2.2** is tested to work with 
    * SIMBL 0.9.x on Snow Leopard (both 32-bit and 64-bit)
    * SIMBL 0.8.x on Leopard (32-bit)

  * **Visor 2.1** is tested to work with 
    * SIMBL 0.9.x on Snow Leopard (both 32-bit and 64-bit)
    * SIMBL 0.8.x on Leopard (32-bit)
    
  * **Visor 2.0** is tested to work with
    * SIMBL 0.8.x on Snow Leopard but Terminal.app has to be forced to run in 32-bit mode
    * SIMBL 0.8.x on Leopard
    
  * **Visor 1.9** is tested to work with
    * SIMBL 0.8.x on Leopard

**[Where can I get older versions?](http://github.com/darwin/visor/downloads)**

## Source

### Installation from source

#### Prerequisities:

  * [SIMBL](http://www.culater.net/software/SIMBL/SIMBL.php)
  * ruby + rubygems
  * XCode 3.2+
  * zip/unzip

#### Custom installation steps:

    git clone git://github.com/darwin/visor.git
    cd visor
    rake
    rake install

Feel free to [fork and contribute][contribute].

Source code licensed under [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0)

## FAQ

#### I like the idea, but I want to use Terminal.app features. Do you plan to support tabs/unicode/whatever?
> Visor is just a light-weight plugin for Terminal.app (SIMBL). You should be able to use most of Terminal.app features with Visor. The only broken feature is "Windows Groups".

#### Does Visor work on OSX 10.6 (Snow Leopard)?
> 64-bit Terminal.app in Snow Leopard is supported by Visor 2.1 and later.

#### Does Visor work on OSX 10.5 (Leopard)?
> Leopard is supported by Visor 1.5 and later, the best version is Visor 2.1.

#### Does Visor work on OSX 10.4 (Tiger)?
> Tiger was supported by early Visors (pre 1.5). It was in the days when I was a young Windows hacker. I will never look back, so your only chance is to upgrade to (Snow) Leopard.

#### How do I uninstall Visor?
> Visor is a standard SIMBL plugin. Remove `Visor.bundle` from `~/Library/Application Support/SIMBL/Plugins`:

    rm -rf ~/Library/Application\ Support/SIMBL/Plugins/Visor.bundle

> Or alternatively you can run `rake uninstall` task if you have a cloned git repo.

#### Where are Visor settings stored?
> Visor settings are stored with Terminal.app settings. You can `open ~/Library/Preferences/com.apple.Terminal.plist` and tweak the values (better to do this when Terminal.app is not running). 
If you have troubles with Visor settings or the generated Visor profile, delete this file and restart Terminal.app. The file will be recreated with default values.

#### My Visor menu-bar icon is dimmed out. My hot-key doesn't work and just beeps. What's wrong?
> There can be only one visor-ed terminal window in the system. If you close this terminal window (for example `Control+D` or typing exit in shell), Visor gets into the disabled state you are describing. Just open a new terminal window and it gets visor-ed again. You can do this for example by clicking on Terminal.app icon in the Dock.

#### How can I open a new terminal window the old way, as a classic OSX window?
> If there is a visor-ed terminal window (Visor menu-bar icon is active) every new terminal window will be opened as a classic OSX window. In other words, open at least two terminal windows. The second one will be classic terminal window for sure.

#### How can I change the height of Visor?
> Go to Terminal.app's Preferences -> Window -> Rows

#### How can I stick Visor to left screen edge?
> Look for the "Position" option in Visor Preferences and pick "Left-Stretch" window placement.

#### How can I change the width of Visor?
> By default Visor window stretches to the full screen width. Set some non-stretching positioning for Visor window in Visor Preferences, then Go to Terminal.app's Preferences -> Window -> Columns.

#### Is it possible to show Visor only on a secondary monitor?
> Go to Visor Preferences -> Screen

#### Is it possible to see Visor on every Space?
> Visor 1.6 does not respect Spaces settings ([Issue 52](http://code.google.com/p/blacktree-visor/issues/detail?id=52)). Visor 1.7+ forces its window to be visible on every space. 
You may disable this in Visor Preferences. Note: Spaces configuration for Terminal.app doesn't apply to the visor-ed terminal window, it is effective only for other (classic) terminal windows.

#### I want to keep different preferences for Visor and other (classic) terminal windows. What is the best way manage this?
> Well this was quite a pain point in older Visor releases. From Visor 2.0 there must be a profile in Terminal.app called "Visor". Visor-ed window always use the "Visor" profile for opening new tabs 
(regardless of "default profile" or "startup profile" settings in Terminal.app). To make your life easier Visor creates this profile for you if it does not exist and fills in Darwin's preferred Visor settings (black background with fine colors, 90% opacity).

#### How can I revert to Darwin's Visor profile?
> You can always delete (or better rename) the "Visor" profile and relaunch Terminal.app. Visor will then create a new "Visor" profile from scratch with Darwin's preferred settings.

#### Do I need to install TerminalColours SIMBL with Visor?
> No, TerminalColours is integrated into Visor 2.0 and later. My motivation was to allow people to get cool Visor colors out of the box (with generated Visor profile).

#### Do I need to install CopyOnSelect SIMBL with Visor?
> No, CopyOnSelect is integrated into Visor 2.0 and later. It is a configurable option in Visor Preferences (disabled by default).

## Changelog

#### The original Visor 1.5 brought to you by Alcor ([Blacktree](http://blacktree.com)), kudos man!

### History

* **v2.2** (26.09.2009) code name: **Stable Visor**
  * [[darwin][darwin]] fixed crash when [changing display settings](http://github.com/darwin/visor/issues/closed#issue/37) or [fast-switching user](http://github.com/darwin/visor/issues/closed#issue/38)
  * [[darwin][darwin]] fixed some [redrawing issues](http://github.com/darwin/visor/issues/closed#issue/33)
  * [[darwin][darwin]] using new API on Snow Leopard for returning focus to previous application (not using applescript => faster!)
  * [[darwin][darwin]] fixed rake tasks, xcodebuild might fail in some rare situations

* **v2.1** (21.09.2009) code name: **Lovely Visor** <= [Google's QSB](http://code.google.com/p/qsb-mac/) codebase made this release possible!
  * [[darwin][darwin]] support for SIMBL 0.9.x
  * [[darwin][darwin]] 64-bit version for 64-bit Terminal.app in Snow Leopard
  * [[darwin][darwin]] embedded Visor preferences pane into Terminal.app Preferences Window
  * [[darwin][darwin]] you can activate Visor by double tapping Control key (disabled by default)
  * [[darwin][darwin]] generated Visor profile does not use bold bright fonts
  * [[darwin][darwin]] resetting window size is performed only in rare cases of visor reconfiguration (fixed [headaches with 'jumping lines'](http://github.com/darwin/visor/issues/closed#issue/27), also fixed [performance issue](http://github.com/darwin/visor/issues/closed/#issue/13))
  * [[darwin][darwin]] 'restore app key focus' applescript checks if app which has to be restored is still alive (prevents [reopening closed app when leaving Visor](http://github.com/darwin/visor/issues/closed#issue/8))
  * [[darwin][darwin]] removed dependency on QuartzCore.framework
  * [[darwin][darwin]] XCode project cleanup, executable now includes binaries for x86_64, i386 and ppc architectures

* **v2.0.1** (11.09.2009)
  * [[darwin][darwin]] Fixed resizing issue ([Issue #22](http://github.com/darwin/visor/issues/closed#issue/22))

* **v2.0** (06.09.2009) code name: **Snow Visor**
  * [[darwin][darwin]] Compatibility with OSX 10.6 (Snow Leopard)
  * [[ciaran][ciaran]+[evanphx][evanphx]+[darwin][darwin]] integrated [Terminal Colours SIMBL](http://ciaranwal.sh/2007/11/01/customising-colours-in-leopard-terminal)
  * [[darwin][darwin]] Visor uses profile "Visor" or creates a new one if it does not exist ([Issue 57](http://code.google.com/p/blacktree-visor/issues/detail?id=71), [Issue #19](http://github.com/darwin/visor/issues/closed#issue/19)).
  * [[darwin][darwin]] "Visor" profile is created with finest settings from Darwin's Visor profile including setup for Terminal Colours (black background with fine colors, 90% opacity)
  * [[darwin][darwin]] Visor stays hidden after Terminal.app launch (seamless experience when including Terminal.app into startup items)
  * [[genki][genki]+[darwin][darwin]] integrated [CopyOnSelect SIMBL](http://github.com/genki/terminalcopyonselect)

* **v1.9.1** (14.04.2009)
  * [[darwin][darwin]] Fixed missing "Visor Preferences..." menu item (thanks [gestes](http://github.com/gestes)).

* **v1.9** (14.04.2009)
  * [[darwin][darwin]] Fixed bottom window is off-screen in left-stretch/right stretch mode ([Issue 60](http://code.google.com/p/blacktree-visor/issues/detail?id=60)).
  * [[darwin][darwin]] Window size gets properly reset during switching Position in Preferences.
  * [[darwin][darwin]] Added "Full Screen" option into Positions in Preferences ([Issue 57](http://code.google.com/p/blacktree-visor/issues/detail?id=57)).
  * [[darwin][darwin]] Debug messages are not being logged in Release builds.
  * [[darwin][darwin]] Visor restores focus of previous app only in case of closing with hotkey or ESC key ([Issue 67](http://code.google.com/p/blacktree-visor/issues/detail?id=67)).
  * [[darwin][darwin]] Visor does not hang when trying to return focus to a hanging application ([Issue 64](http://code.google.com/p/blacktree-visor/issues/detail?id=64)).
  * [[darwin][darwin]] Going to an empty space no more triggers visor terminal to appear ([Issue 58](http://code.google.com/p/blacktree-visor/issues/detail?id=58)).
  * [[darwin][darwin]] Menu item changes title to "Hide Visor" when Visor is opened ([Issue 43](http://code.google.com/p/blacktree-visor/issues/detail?id=43)).
  * [[darwin][darwin]] Fixed: Switching Space let Visor show and hide in an infinite loop ([Issue 61](http://code.google.com/p/blacktree-visor/issues/detail?id=61)).
  * [[darwin][darwin]] Removed option "Main Screen" from Preferences/Screen ([Issue 59](http://code.google.com/p/blacktree-visor/issues/detail?id=59)).
  * [[darwin][darwin]] Removed pin icon, toggle added under status menu ([Issue 56](http://code.google.com/p/blacktree-visor/issues/detail?id=56)).

* **v1.8.1** (05.03.2009)
  * [[darwin][darwin]] Fixed "NSUserDefaults setString:ForKey:" crash on startup (affected upgrading users from 1.7 to 1.8). Reported by [Kleinman][kleinman], thanks.
  * [[darwin][darwin]] Compilation from sources clears previous build folder (this could possibly make troubles for people developing Visor and then doing release [like me]).

* **v1.8** (04.03.2009)
  * [[darwin][darwin]+[cglee][cglee]] Visor can be positioned to other screen edges. Also non-stretching mode is possible. See Position in Visor Preferences. 
  * [[darwin][darwin]] Visor window can be pinned, so it doesn't auto-hide (see icon in the top-right window corner).
  * [[darwin][darwin]] Better behavior of confirmation sheets (Previously, sheet might appear on different space or might be hidden behind Visor window).
  * [[darwin][darwin]] Custom build from sources is marked as "Custom", no need to specify version.

* **v1.7** (12.02.2009)
  * [[darwin][darwin]] Visor appears on every space by default. You may disable it in Visor Preferences.
  * [[darwin][darwin]] Visor is correctly hidden in fullscreen mode.
  * [[darwin][darwin]] Visor plays nicely when screen resolution changes.
  * [[pumpkin][pumpkin]] Fixed extra shadow under menu-bar.
  * [[blinks][blinks]] Fixed rake install task for case there is no SIMBL plugins directory.

* **v1.6** (03.02.2009)
  * [[darwin][darwin]] Build infrastructure.
  * [[darwin][darwin]] It is possible to specify on which screen visor will appear - see preferences ([Issue 15](http://code.google.com/p/blacktree-visor/issues/detail?id=15)).
  * [[darwin][darwin]] Visor exits gratefully without locking UI ([Issue 50](http://code.google.com/p/blacktree-visor/issues/detail?id=50)).
  * [[darwin][darwin]] Visor becomes inactive when you close visor-ed terminal window or exit it's shell (fixes [Issue 10](http://code.google.com/p/blacktree-visor/issues/detail?id=10)).
  * [[darwin][darwin]] When inactive, Visor eats next coming terminal window (right click terminal.app icon and select "new window").
  * [[darwin][darwin]] Re-implemented window sliding animation using standard NSWindow functions, should fix weird bugs with mouse cursor state.
  * [[darwin][darwin]] Removed support for Quartz powered backgrounds (want simpler codebase!).
  * [[darwin][darwin]] Gentle terminal window hijacking (solves [Issue 5](http://code.google.com/p/blacktree-visor/issues/detail?id=5), [Issue 6](http://code.google.com/p/blacktree-visor/issues/detail?id=6) and related problems. What more? It properly enables [applescript automation in visor-ed terminal](http://onrails.org/articles/2007/11/28/scripting-the-leopard-terminal), which was my original motivation to get dirty with Visor internals).
  * [[darwin][darwin]] Whenever you open Visor window, it steals focus and you may start typing without touching mouse. Visor is a good guy and returns the focus back to original app when being hidden. I said ... don't touch that mouse!
  * [[torsten][torsten]] Fixed the "White Line Bug" ([Issue 16](http://code.google.com/p/blacktree-visor/issues/detail?id=16)).
  * [[torsten][torsten]] Added the option to hide Visor on Escape press. Press Shift+Escape, if you need a "Escape" in the Terminal.
  * [[torsten][torsten]] If you start Visor you get now initial focus. ([Issue 20](http://code.google.com/p/blacktree-visor/issues/detail?id=20)).

* **v1.5a1** (Nov 2007?)
  * Leopard Support

* **v1.2.1**
  * Fixed Choose File button

* **v1.2**
  * Added Animation Speed Preferences
  * Added Transition Preferences for Slide and Fade (both optional)
  * Menu Item is optional
  * Fix for users with Dock on top left or right (Visor appears above the dock)
  * Fixes animation glitches from alternate unsupported version.
  * New icon
  * No longer forked code - one version.
  
* **v1.1** (drparallax's unsupported version?)
  * Dismissing visor now 'slides up'
  * Options for animation
  * New icon

* **v1.0**
  * Initial release
  
  ... hic sunt leones ...

## Links

#### Source code
  * [sources are hosted at GitHub](http://github.com/darwin/visor)

#### Original Visor 1.5
  * [Blacktree Homepage](http://blacktree.com)

### Articles
  * **[Donnez du style à votre terminal avec Visor](http://maxime.sh/2010/01/donnez-du-style-a-votre-terminal-avec-visor)** by Maxime
  * **[Quake like Terminal on Mac OS X: Visor Plugin](http://www.rngtng.com/2009/08/14/quake-like-terminal-on-mac-os-x-visor-plugin/)** by Tobi
  * **[Visor Terminal on Snow Leopard](http://www.metaskills.net/2009/8/18/visor-terminal-on-snow-leopard)** by Ken Collins
  * **[Getting Terminal Visor for OSX working with Snow Leopard](http://aralbalkan.com/2366)** by Aral Balkan
  * **[Re-enabling Visor in Snow Leopard](http://terrychay.com/blog/article/visor-in-snow-leopard.shtml)** by Terry Chay
  * Featured Project in **[Rebase #13](http://github.com/blog/346-github-rebase-13)**, thanks [qrush](http://github.com/qrush)!
  
## Special Guest

### Ben Stiglitz about Terminal.app

<div>Ben is the author of Terminal.app. Kudos!</div>
<embed src='http://rubyconf2008.confreaks.com/player.swf' height='260' width='640' allowscriptaccess='always' allowfullscreen='true' flashvars='file=http%3A%2F%2Frubyconf2008.confreaks.com%2Fvideos%2Fterminalapp-small.mp4&image=images%2Fterminalapp-preview.jpg&plugins=viral-1'/>

[darwin]: http://github.com/darwin
[torsten]: http://github.com/torsten
[pumpkin]: http://github.com/pumpkin
[blinks]: http://github.com/blinks
[cglee]: http://github.com/cglee
[kleinman]: http://github.com/kleinman
[genki]: http://github.com/genki
[ciaran]: http://github.com/ciaran
[evanphx]: http://github.com/evanphx
[contribute]: http://github.com/darwin/visor