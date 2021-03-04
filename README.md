<h1 align="center"><i>BUI</i></h1>
<p align="center">UI and colors management that <i>SuperB</i></p>
<p align="center"><a href="http://pndsndn.blog79.fc2.com/blog-entry-207.html"><img src="https://blog-imgs-132.fc2.com/p/n/d/pndsndn/nyaberin.gif"></a></p>
<h6 align="center">Artwork by <a href="https://www.pixiv.net/en/users/3605217">いのふとん</a></h6>
<p align="center"><a href="https://github.com/NNBnh/bui/blob/main/LICENSE"><img src="https://img.shields.io/github/license/NNBnh/bui?labelColor=585858&color=F7CA88&style=for-the-badge" alt="License: GPL-3.0"></a> <img src="https://img.shields.io/github/last-commit/NNBnh/bui?labelColor=585858&color=F7CA88&style=for-the-badge"></p>
<p align="center"><a href="https://github.com/NNBnh/bui/watchers"><img src="https://img.shields.io/github/watchers/NNBnh/bui?labelColor=585858&color=F7CA88&style=flat-square"></a> <a href="https://github.com/NNBnh/bui/stargazers"><img src="https://img.shields.io/github/stars/NNBnh/bui?labelColor=585858&color=F7CA88&style=flat-square"></a> <a href="https://github.com/NNBnh/bui/network/members"><img src="https://img.shields.io/github/forks/NNBnh/bui?labelColor=585858&color=F7CA88&style=flat-square"></a> <a href="https://github.com/NNBnh/bui/issues"><img src="https://img.shields.io/github/issues/NNBnh/bui?labelColor=585858&color=F7CA88&style=flat-square"></a></p>

## About
***BUI*** is a UI and colors management method that export the colors hex through environment variables so any program that can read environment variables can used it.

## Features
`#TODO`

## Contents
- [About](#about)
- [Features](#features)
- [Contents](#contents)
- [Setup](#setup)
  - [UI](#ui)
  - [Font](#font)
  - [Colors](#colors)
    - [Elements](#elements)
    - [Base16](#base16)
    - [Terminal](#terminal)
- [Example](#example)
- [Integrate](#integrate)
- [Resources](#resources)

## Setup
### UI
Set the user interface:

|Value                      |Invalid                                                                                                                                                                 |Default                      |Description            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|-----------------------|
|`BUI_GTK_THEME`            |`string`                                                                                                                                                                |`$GTK_THEME` (`Adwaita`)     |GTK theme              |
|`BUI_GTK_TOOLBAR_STYLE`    |`(GTK_TOOLBAR_ICONS\|` `\|GTK_TOOLBAR_TEXT\|` `\|GTK_TOOLBAR_BOTH\|` `\|GTK_TOOLBAR_BOTH_HORIZ)`                                                                        |`GTK_TOOLBAR_BOTH`           |GTK toolbar style      |
|`BUI_GTK_TOOLBAR_ICON_SIZE`|`(GTK_ICON_SIZE_MENU\|` `\|GTK_ICON_SIZE_SMALL_TOOLBAR\|` `\|GTK_ICON_SIZE_LARGE_TOOLBAR\|` `\|GTK_ICON_SIZE_BUTTON\|` `\|GTK_ICON_SIZE_DND\|` `\|GTK_ICON_SIZE_DIALOG)`|`GTK_ICON_SIZE_LARGE_TOOLBAR`|GTK toolbar icon size  |
|`BUI_ICON_THEME`           |`string`                                                                                                                                                                |`Adwaita`                    |Icon theme             |
|`BUI_MOUSE_CURSOR_THEME`   |`string`                                                                                                                                                                |`Adwaita`                    |Mouse cursor theme     |
|`BUI_MOUSE_CURSOR_SIZE`    |`<number>`                                                                                                                                                              |`0.0`                        |Border size            |
|`BUI_BUTTON_IMAGES`        |`(true\|false)`                                                                                                                                                         |`true`                       |Button images          |
|`BUI_MENU_IMAGES`          |`(true\|false)`                                                                                                                                                         |`true`                       |Menu images            |
|`BUI_EVENT_SOUNDS`         |`(true\|false)`                                                                                                                                                         |`true`                       |Event sounds           |
|`BUI_INPUT_FEEDBACK_SOUNDS`|`(true\|false)`                                                                                                                                                         |`true`                       |Input feedback sounds  |
|`BUI_GAPS_SIZE`            |`<number>`                                                                                                                                                              |`0.0`                        |Gaps size              |
|`BUI_BORDER_SIZE`          |`<number>`                                                                                                                                                              |`1.0`                        |Border size            |
|`BUI_OPACITY`              |`(0.0 - 1.0)`                                                                                                                                                           |`1.0`                        |Background opacity     |

### Font

|Value                      |Invalid                                                                                                                                                                 |Default                      |Description            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|-----------------------|
|`BUI_CURSOR`               |`(block\|beam\|underline)`                                                                                                                                              |`block`                      |Text cursor shape      |
|`BUI_CURSOR_BLINK`         |`(true\|false)`                                                                                                                                                         |`true`                       |Text cursor blink      |
|`BUI_FONT_FAMILY`          |`string`                                                                                                                                                                |`Sans`                       |Font family            |
|`BUI_FONT_SIZE`            |`<number>`                                                                                                                                                              |`10.0`                       |Font size              |
|`BUI_FONT_MONO_FAMILY`     |`string`                                                                                                                                                                |`Monospace`                  |Fixed-width font family|
|`BUI_FONT_MONO_SIZE`       |`<number>`                                                                                                                                                              |`10`                         |Fixed-width font size  |
|`BUI_FONT_ANTIALIAS`       |`(true\|false)`                                                                                                                                                         |`true`                       |Font antialias         |
|`BUI_HINT_STYLE`           |`(none\|slight\|medium\|full)`                                                                                                                                          |`full`                       |Hint style             |
|`BUI_SUBPIXEL`             |`(none\|rgb\|bgr\|vrgb\|vbgr)`                                                                                                                                          |`none`                       |Subpixel               |

### Colors
First set the hex value of all the colors: `BUI_COLOR_<NAME>="#<HEX>"`.

As for me, I put all the color names that match the [Minecraft wool palette](https://minecraft.gamepedia.com/Wool) (i mean 16 colors with 4 of them being grayscale, looks kinda fit with the terminal color palette)

> ![Minecraft wool](https://static.wikia.nocookie.net/minecraft_gamepedia/images/f/fc/JE_1.12_Dev_Wool_and_concrete.jpg/revision/latest/scale-to-width-down/800?cb=20210222155408)

```
BUI_COLOR_BLACK
BUI_COLOR_GRAY
BUI_COLOR_GREY
BUI_COLOR_WHITE
BUI_COLOR_BROWN
BUI_COLOR_RED
BUI_COLOR_ORANGE
BUI_COLOR_YELLOW
BUI_COLOR_LIME
BUI_COLOR_GREEN
BUI_COLOR_TEAR
BUI_COLOR_CYAN
BUI_COLOR_BLUE
BUI_COLOR_PURPLE
BUI_COLOR_MAGENTA
BUI_COLOR_PINK
```

Then you can just associate the colors of the elements with their hex: `export BUI_COLOR_<ELEMENT>="$BUI_COLOR_<NAME>`.

This is a good practice as it makes the colors more readable (it shows the color name not the hex) and avoids duplication.

#### Elements
Set the color of the elements so that any program can get it:

|Value|Description|
|-|-|
|`BUI_COLOR_FOREGROUND`|Foreground color|
|`BUI_COLOR_BACKGROUND`|Background color|
|`BUI_COLOR_FOREGROUND_ALT`|Alternative foreground color|
|`BUI_COLOR_BACKGROUND_ALT`|Alternative background color|
|`BUI_COLOR_CURSOR`|Cursor or focus element color|
|`BUI_COLOR_CURSOR_ALT`|Alternative cursor or unfocus element color|
|`BUI_COLOR_SELECTION`|Selection color|

#### Base16
With function and syntax, [Base16](chriskempson.com/projects/base16) is the best architecture as it work on most all color scheme:

|Value|Color|
|-|-|
|`BUI_COLOR_BASE00`|![Base00](https://placehold.it/64x24/181818?text=+)|
|`BUI_COLOR_BASE01`|![Base01](https://placehold.it/64x24/282828?text=+)|
|`BUI_COLOR_BASE02`|![Base02](https://placehold.it/64x24/383838?text=+)|
|`BUI_COLOR_BASE03`|![Base03](https://placehold.it/64x24/585858?text=+)|
|`BUI_COLOR_BASE04`|![Base04](https://placehold.it/64x24/B8B8B8?text=+)|
|`BUI_COLOR_BASE05`|![Base05](https://placehold.it/64x24/D8D8D8?text=+)|
|`BUI_COLOR_BASE06`|![Base06](https://placehold.it/64x24/E8E8E8?text=+)|
|`BUI_COLOR_BASE07`|![Base07](https://placehold.it/64x24/F8F8F8?text=+)|
|`BUI_COLOR_BASE08`|![Base08](https://placehold.it/64x24/AB4642?text=+)|
|`BUI_COLOR_BASE09`|![Base09](https://placehold.it/64x24/DC9656?text=+)|
|`BUI_COLOR_BASE0A`|![Base0A](https://placehold.it/64x24/F7CA88?text=+)|
|`BUI_COLOR_BASE0B`|![Base0B](https://placehold.it/64x24/A1B56C?text=+)|
|`BUI_COLOR_BASE0C`|![Base0C](https://placehold.it/64x24/86C1B9?text=+)|
|`BUI_COLOR_BASE0D`|![Base0D](https://placehold.it/64x24/7CAFC2?text=+)|
|`BUI_COLOR_BASE0E`|![Base0E](https://placehold.it/64x24/BA8BAF?text=+)|
|`BUI_COLOR_BASE0F`|![Base0F](https://placehold.it/64x24/A16946?text=+)|

#### Terminal
Set the terminal color:

|Value|Name|Color|
|-|-|-|
|`BUI_COLOR_TERMINAL000`|`black`|![Black](https://placehold.it/64x24/000000?text=+)|
|`BUI_COLOR_TERMINAL001`|`red`|![Red](https://placehold.it/64x24/800000?text=+)|
|`BUI_COLOR_TERMINAL002`|`green`|![Green](https://placehold.it/64x24/008000?text=+)|
|`BUI_COLOR_TERMINAL003`|`yellow`|![Yellow](https://placehold.it/64x24/808000?text=+)|
|`BUI_COLOR_TERMINAL004`|`blue`|![Blue](https://placehold.it/64x24/000080?text=+)|
|`BUI_COLOR_TERMINAL005`|`magenta`|![Magenta](https://placehold.it/64x24/800080?text=+)|
|`BUI_COLOR_TERMINAL006`|`cyan`|![Cyan](https://placehold.it/64x24/008080?text=+)|
|`BUI_COLOR_TERMINAL007`|`white`|![White](https://placehold.it/64x24/C0C0C0?text=+)|
|`BUI_COLOR_TERMINAL008`|`bright_black`|![Bright black](https://placehold.it/64x24/808080?text=+)|
|`BUI_COLOR_TERMINAL009`|`bright_red`|![Bright red](https://placehold.it/64x24/FF0000?text=+)|
|`BUI_COLOR_TERMINAL010`|`bright_green`|![Bright green](https://placehold.it/64x24/00FF00?text=+)|
|`BUI_COLOR_TERMINAL011`|`bright_yellow`|![Bright yellow](https://placehold.it/64x24/FFFF00?text=+)|
|`BUI_COLOR_TERMINAL012`|`bright_blue`|![Bright blue](https://placehold.it/64x24/0000FF?text=+)|
|`BUI_COLOR_TERMINAL013`|`bright_magenta`|![Bright magenta](https://placehold.it/64x24/FF00FF?text=+)|
|`BUI_COLOR_TERMINAL014`|`bright_cyan`|![Bright cyan](https://placehold.it/64x24/00FFFF?text=+)|
|`BUI_COLOR_TERMINAL015`|`bright_white`|![Bright white](https://placehold.it/64x24/FFFFFF?text=+)|
|`BUI_COLOR_TERMINAL016`|`16`|![16](https://placehold.it/64x24/000000?text=+)|
|`BUI_COLOR_TERMINAL017`|`17`|![17](https://placehold.it/64x24/00005F?text=+)|
|`BUI_COLOR_TERMINAL018`|`18`|![18](https://placehold.it/64x24/000087?text=+)|
|`BUI_COLOR_TERMINAL019`|`19`|![19](https://placehold.it/64x24/0000AF?text=+)|
|...|...|...|
|`BUI_COLOR_TERMINAL255`|`255`|![255](https://placehold.it/64x24/EEEEEE?text=+)|

###### Foreground, background and cursor are explained in [Elements](#elements).

## Example

```sh
# UI
export BUI_CURSOR="block"
export BUI_OPACITY="0.8"
export BUI_FONT_FAMILY="Iosevka Extended"
export BUI_FONT_SIZE="12.0"

# Colors
export BUI_COLOR_DARK="#181818"
export BUI_COLOR_DARK_ALT="#282828"
export BUI_COLOR_BLACK="#383838"
export BUI_COLOR_GRAY="#585858"
export BUI_COLOR_GREY="#B8B8B8"
export BUI_COLOR_WHITE="#D8D8D8"
export BUI_COLOR_LIGHT_ALT="#E8E8E8"
export BUI_COLOR_LIGHT="#F8F8F8"
export BUI_COLOR_BROWN="#A16946"
export BUI_COLOR_RED="#AB4642"
export BUI_COLOR_ORANGE="#DC9656"
export BUI_COLOR_YELLOW="#F7CA88"
export BUI_COLOR_LIME="#A1B56C"
export BUI_COLOR_CYAN="#86C1B9"
export BUI_COLOR_BLUE="#7CAFC2"
export BUI_COLOR_MAGENTA="#BA8BAF"

# Elements
export BUI_COLOR_MAIN="$BUI_COLOR_YELLOW"
export BUI_COLOR_MAIN_ALT="$BUI_COLOR_GREY"
export BUI_COLOR_FOREGROUND="$BUI_COLOR_WHITE"
export BUI_COLOR_BACKGROUND="$BUI_COLOR_DARK"
export BUI_COLOR_FOREGROUND_ALT="$BUI_COLOR_GRAY"
export BUI_COLOR_BACKGROUND_ALT="$BUI_COLOR_DARK_ALT"
export BUI_COLOR_CURSOR="$BUI_COLOR_MAIN"
export BUI_COLOR_CURSOR_ALT="$BUI_COLOR_MAIN_ALT"
export BUI_COLOR_SELECTION="$BUI_COLOR_GRAY"

# Base16
export BUI_COLOR_BASE00="$BUI_COLOR_DARK"
export BUI_COLOR_BASE01="$BUI_COLOR_DARK_ALT"
export BUI_COLOR_BASE02="$BUI_COLOR_BLACK"
export BUI_COLOR_BASE03="$BUI_COLOR_GRAY"
export BUI_COLOR_BASE04="$BUI_COLOR_GREY"
export BUI_COLOR_BASE05="$BUI_COLOR_WHITE"
export BUI_COLOR_BASE06="$BUI_COLOR_LIGHT_ALT"
export BUI_COLOR_BASE07="$BUI_COLOR_LIGHT"
export BUI_COLOR_BASE08="$BUI_COLOR_RED"
export BUI_COLOR_BASE09="$BUI_COLOR_ORANGE"
export BUI_COLOR_BASE0A="$BUI_COLOR_YELLOW"
export BUI_COLOR_BASE0B="$BUI_COLOR_LIME"
export BUI_COLOR_BASE0C="$BUI_COLOR_CYAN"
export BUI_COLOR_BASE0D="$BUI_COLOR_BLUE"
export BUI_COLOR_BASE0E="$BUI_COLOR_MAGENTA"
export BUI_COLOR_BASE0F="$BUI_COLOR_BROWN"

# Terminal
export BUI_COLOR_TERMINAL000="$BUI_COLOR_DARK_ALT"
export BUI_COLOR_TERMINAL001="$BUI_COLOR_RED"
export BUI_COLOR_TERMINAL002="$BUI_COLOR_LIME"
export BUI_COLOR_TERMINAL003="$BUI_COLOR_YELLOW"
export BUI_COLOR_TERMINAL004="$BUI_COLOR_BLUE"
export BUI_COLOR_TERMINAL005="$BUI_COLOR_MAGENTA"
export BUI_COLOR_TERMINAL006="$BUI_COLOR_CYAN"
export BUI_COLOR_TERMINAL007="$BUI_COLOR_GREY"
export BUI_COLOR_TERMINAL008="$BUI_COLOR_GRAY"
export BUI_COLOR_TERMINAL009="$BUI_COLOR_RED"
export BUI_COLOR_TERMINAL010="$BUI_COLOR_LIME"
export BUI_COLOR_TERMINAL011="$BUI_COLOR_YELLOW"
export BUI_COLOR_TERMINAL012="$BUI_COLOR_BLUE"
export BUI_COLOR_TERMINAL013="$BUI_COLOR_MAGENTA"
export BUI_COLOR_TERMINAL014="$BUI_COLOR_CYAN"
export BUI_COLOR_TERMINAL015="$BUI_COLOR_LIGHT_ALT"
```

###### See my [Environment variables](https://github.com/NNBnh/dots/blob/master/home/.config/env#L60) for more information and explanations.

## Integrate
- [`bui-appearance`](https://github.com/NNBnh/bui-appearance): for widget toolkit ([GTK](https://www.gtk.org))
- [`bui-terminal`](https://github.com/NNBnh/bui-terminal): for terminal
- [`bui.kak`](https://github.com/NNBnh/bui.kak): for [Kakoune](http://kakoune.org)

## Resources
- [ANSI escape code](https://en.wikipedia.org/wiki/ANSI_escape_code#8-bit)
- [Base16](chriskempson.com/projects/base16) by [Chris Kempson](http://chriskempson.com)
