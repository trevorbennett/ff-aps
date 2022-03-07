# Firefox AWS Plugin Searchbox
This plugin creates a searchbox and keyboard functionality to easily log into AWS from their account selection screen. Live your fanciest life with this plugin.

*Installing this unsigned extension requires you to be running Firefox Extended Support Release, Developer Edition, or Nightly version! Chrome may work as well.*

## Project Anatomy
```
icons/                  Delicious icon
output/                 Where pkg.cmd/pkg.sh drops installable extension
fancy_searchbox.js      The goods (self-contained javascript of all logic/styling)
license-gnugplv3.txt    Applies to everything here, except icons (I do not own it)
manifest.json           Meta file for Firefox/Chrome to understand extension
README.md               You are here
```

## Latest changes
```
2022-03-07 Version 1.1
    Add tags to accounts for filtering and grouping

2022-03-04 Version 1.0
    Space-delimited, word-based, 'AND' filtering through an input box
    Arrow keys to select a high-level account
    Enter to log in once selected
    Escape key to re-focus on and clear out input box
    Delicious drumstick logo
```

## Create the unsigned, loadable Firefox extension .zip from this folder

  1. Zip folder without .git/ either [manually](https://stackoverflow.com/a/31043045), or using the provided pkg.cmd, or *(TODO)* pkg.sh on unix-based/macos systems

  1. *(Optional)* Rename zip to to have an .xpi extension -- zip is fine though.

  1. Verify the .zip file shows up under the output directory called **ff-aps-ext.zip**

## Permanently load unsigned extension from .zip

  1. Verify you're running a compatible [Firefox version](https://support.mozilla.org/en-US/kb/add-on-signing-in-firefox?as=u&utm_source=inproduct#w_what-are-my-options-if-i-want-to-use-an-unsigned-add-on-advanced-users): Firefox Browser (ESR), Developer Edition, or Nightly, and NOT simply 'Firefox Browser'
  
  1. Go to about:config, click through the warnings, and change `xpinstall.signatures.required` to false

  1. Click the hamburger (3 lines) button at the top right in Firefox and click Add-ons and Themes (ctrl+shift+a)

  1. On the left click "Extensions"

  1. On the right click the small gear icon 

  1. Click "Install Add-on From File..."

  1. Select the zip

  1. Enjoy your fancy new life

## Temporarily load this extension in developer mode
  
  1. Go to about:debugging in a new Firefox tab

  1. Click "This Firefox" on the left

  1. Under "Temporary Extensions", click "Load Temporary Add-on..."

  1. Select the zip file

  1. Log into AWS via the go URL
  
## Chrome Support

  1. Go to hamburger (3 lines) button at the top right

  1. Drill down into "More Tools" -> "Extensions"

  1. Click "Developer Mode" at the top right to turn it on

  1. Click "Load unpacked" and add this entire folder

  1. Enjoy your Chrome version of ff-aps, aka chr-aps! :)