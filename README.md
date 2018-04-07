# Kaleidoscope-Emoji
Emoji Keys for Kaleidoscope

![status][st:experimental]

 [st:stable]: https://img.shields.io/badge/stable-✔-black.svg?style=flat&colorA=44cc11&colorB=494e52
 [st:broken]: https://img.shields.io/badge/broken-X-black.svg?style=flat&colorA=e05d44&colorB=494e52
 [st:experimental]: https://img.shields.io/badge/experimental----black.svg?style=flat&colorA=dfb317&colorB=494e52



## Installation

Install this plugin as you would any other 3rd-party plugin.  Specifically:

1. __Find your plugin directory.__  This is wherever you normally put plugins; it
should be `$SKETCHBOOK_DIR/hardware/keyboardio/avr/libraries`, or at least
accessible from there via symlink.  (If you don't know what a symlink is, don't
worry - just use the `libraries` directory directly.)  `$SKETCHBOOK_DIR` is your
Arduino sketchbook directory, perhaps `$HOME/Arduino` or `$HOME/Documents/Arduino`.
2. __Install this plugin into your plugin directory__ using one of the below options.
* __(Option 1 - using Git)__ Clone this Git repo into your plugin directory.  This can
be done from the command line - just navigate to your plugin directory and type
`git clone https://github.com/jjochen/Kaleidoscope-Emoji`.
* __(Option 2 - no Git or command-line required)__ Click the green "Clone or download"
button at the top right of this page, and select "Download ZIP".  Then, unzip the
folder in your plugin directory.

You're done!  It was that easy.

## Adding the plugin to your sketch

To activate the plugin, you need to include the header, tell Kaleidoscope to `use`
the plugin, and place the `Key_Emoji...` keys in your keymap.

In general, this plugin desires to be as early as possible in the
`Kaleidoscope.use()` order, so that it can catch all keypresses before other
plugins try to handle them. There may be exceptions.

### Setup operations in the firmware sketch (example):

```c++
#include <Kaleidoscope.h>
#include <Kaleidoscope-Emoji.h>

void setup (){
  Kaleidoscope.use(&Emoji);
  Kaleidoscope.setup();
}
```

### Emoji Keys

...


## Dependencies

* [Kaleidoscope-Unicode](https://github.com/keyboardio/Kaleidoscope-Unicode)

## Further reading

The [example][plugin:example] is a working sketch using Kaleidoscope-Emoji.

 [plugin:example]: https://github.com/jjochen/Kaleidoscope-Emoji/blob/master/examples/Emoji/Emoji.ino
