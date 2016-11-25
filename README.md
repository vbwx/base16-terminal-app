# Base16 for Terminal.app

These profiles bring the [base16 colors](https://github.com/chriskempson/base16) to the Terminal of macOS.

## Installation

Just open the downloaded `profiles` folder in the Finder (or `profiles-256` if your Terminal
supports the ANSI-256 colorspace), select the profiles you want to install, right-click on the files
and click *Open* (in order to circumvent [Gatekeeper](https://support.apple.com/en-us/HT202491)).

## Customization

Since `.terminal` files contain a bunch of settings in addition to the color definitions, you
probably want these profiles to inherit all settings from a profile of your choice.

1. Download [my fork of the base16 Builder](https://github.com/vbwx/base16-builder-php).

2. In Terminal, choose *Shell* > *Export Settings&hellip;* and save the file into the folder you
   just downloaded. (You can also export profiles in the *Profiles* section of the *Preferences*
window.)

3. Execute the following commands. (Replace &ldquo;MyProfile&rdquo; with the name of your profile.)
```sh
cd ~/Downloads/base16-builder-php-master  # the folder you downloaded in step 1
composer install  # depends on your Composer setup
php Builder.php update
php Builder.php -p MyProfile.terminal
cd templates/terminal-app/profiles  # or profiles-256 if your Terminal supports the ANSI 256 colorspace
open *.terminal  # or whichever profiles you like
```

## Demo

![Tomorrow Night profile](assets/tomorrow-night.png)

For this screenshot, I used *Tomorrow Night* with *DejaVu Sans Mono for Powerline* (12pt) as font,
along with [Prezto](https://github.com/vbwx/prezto) (my favorite Zsh configuration framework).
