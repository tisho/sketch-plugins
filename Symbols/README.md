# Sketch Symbols

## DEPRECATED: Symbols are now part of Sketch 3.

Sketch Symbols is a plug-in for [Sketch](http://bohemiancoding.com/sketch/) that lets you mimic basic Smart Objects / Symbols functionality by automatically syncing changes between layer groups named in a particular way. As an added bonus, you can mark certain text layers in your symbols as dynamic and have their styles replicated, but not their content.

## Demo

[![Demo Video](http://tisho.github.io/sketch-plugins/images/demo-video-thumb.png)](https://vimeo.com/83370438)

## Installation

1. [Download the plugin.](https://github.com/tisho/sketch-plugins/archive/master.zip)
2. Double-click the file `Sync Symbol.sketchplugin` inside `Symbols/`. Sketch should open
   automatically and tell you that a new plugin was installed.

<img src="http://tisho.github.io/sketch-plugins/images/plugin-installed.png" alt="Installed Plugin Message" width="534" />

You should see the **Sync Symbol** entry under the Plugins menu now.

<img src="http://tisho.github.io/sketch-plugins/images/plugin-menu.png" alt="Plugin Menu" width="317" />

## Usage

1. Create a layer group for your symbol. (`Cmd + G`)
2. Add **": symbol-name"** to its name to mark it as a symbol. *E.g.: "signup
   button : button-default".*

    ![Symbol Name Example](http://tisho.github.io/sketch-plugins/images/symbol-name.png)

3. Copy the same symbol to other parts of your document. You
   can change the name before the colon to whatever you like.
E.g.: "ok button : button-default".
4. Make changes to any of the copies of the symbol you've created. With the symbol or one of its layers still selected, press `Cmd + E` to sync these changes with other instances of the symbol.

**Bonus Tip:** Open *Preferences* and under *Layers* uncheck *"Append
'Copy' after duplicated layers"*, so you don't need to tweak the symbol
name after you duplicate it.

## Dynamic Text Layers

Put a `$` in front of the name of any text layer inside a symbol to mark
it as dynamic. When you sync changes between symbols, dynamic text layers will
not be replaced. Their styles, including font size, family and line height will be updated, but their content will remain
intact. This lets you define a single symbol for a button, for example, but use
different copy for each instance of that button.

![Dynamic Layer Name Example](http://tisho.github.io/sketch-plugins/images/dynamic-layer-name.png)

## Changing the Default Keyboard Shortcut

1. Open Sketch's plugins folder. You can do that easily by choosing
   Custom Script from the Plugins menu, then click the gear icon and
choose "Open Plugins Folder".
2. Open the file "Sync Symbols.sketchplugin" in your favorite text
   editor.
3. The shortcut is on the first line:

    ```
    // Syncs all instances of a symbol tagged with ": symbol-name" (cmd e)
    ```

  Change it to whatever you like (ctrl shift s, for example), and you
should be good to go. The following modifiers are all valid: `control ctrl alt option cmd command shift`.

## Updating the Plugin

Right now there's no automated way to update plugins. You'll have to
replace the plugin files manually.

1. [Download the latest version of the plugin.](https://github.com/tisho/sketch-plugins/archive/master.zip)
2. Open Sketch's plugins folder. You can do that easily by choosing
   Custom Script from the Plugins menu, then click the gear icon and
choose "Open Plugins Folder".
3. Replace the file `Sync Symbol.sketchplugin` with its new version from
   the archive you downloaded.

You don't need to restart Sketch. It will pick up the changes
automatically.

## Issues and Questions

[File an issue on Github](https://github.com/tisho/sketch-plugins/issues), send a message to [@tisho](http://twitter.com/tisho) on Twitter, or email <t@tisho.co>.

## Thanks

Bohemian Coding for creating [Sketch](http://bohemiancoding.com/sketch/) in the first place and [@bomberstudios](http://twitter.com/bomberstudios) for the wonderful [sketch-commands bundle](https://github.com/bomberstudios/sketch-commands), which proved a wonderful source for learning and inspiration.

## License

The MIT License (MIT)

Copyright (c) 2013 Tisho Georgiev

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
