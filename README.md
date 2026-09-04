# About

Plugin for Sublime Text 3 - toggle words with support for user defined arrays.

```
 true -> false
  yes -> no
   on -> off
    0 -> 1
 left -> right
  top -> bottom
   up -> down
width -> height
```

and this automatically understand original words and ->

```
false <-> true
False <-> True
FALSE <-> TRUE
```

# Usage

Set cursor on word or select word and press: <kbd>alt</kbd>+<kbd>w</kbd>, <kbd>alt</kbd>+<kbd>t</kbd>



## Installation

### By Package Control

1. Download & Install **`Sublime Text 3`** (https://www.sublimetext.com/3)
1. Go to the menu **`Tools -> Install Package Control`**, then,
    wait few seconds until the installation finishes up
1. Now,
    Go to the menu **`Preferences -> Package Control`**
1. Type **`Add Channel`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    input the following address and press <kbd>Enter</kbd>
    ```
    https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
    ```
1. Go to the menu **`Tools -> Command Palette...
    (Ctrl+Shift+P)`**
1. Type **`Preferences:
    Package Control Settings – User`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    find the following setting on your **`Package Control.sublime-settings`** file:
    ```js
    "channels":
    [
        "https://packagecontrol.io/channel_v3.json",
        "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
    ],
    ```
1. And,
    change it to the following, i.e.,
    put the **`https://raw.githubusercontent...`** line as first:
    ```js
    "channels":
    [
        "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
        "https://packagecontrol.io/channel_v3.json",
    ],
    ```
    * The **`https://raw.githubusercontent...`** line must to be added before the **`https://packagecontrol.io...`** one, otherwise,
      you will not install this forked version of the package,
      but the original available on the Package Control default channel **`https://packagecontrol.io...`**
    > [!WARNING]
    > Placing this custom channel before the default channel changes Package Control's resolution globally.
    > Packages from this channel with the same name will override versions from the default channel.
    >
    > You can review the channel contents here:
    > https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
1. Now,
    go to the menu **`Preferences -> Package Control`**
1. Type **`Install Package`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    search for **`ToggleWords`** and press <kbd>Enter</kbd>

See also:

1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


# Configure

## Keys

You may redefine the key bindings in your sublime-keymap with command `toggle_word`.


## User defined arrays

You can define lists of words, which will be cycled through in order.

Example file `ToggleWords.sublime-settings`:

```
{
    // User defined words
    "toggle_words_dict": [
        ["left", "right"],
        ["up", "down"],
        ["top", "bottom"],
        ["width", "height"],
        ["red","orange","yellow","green","blue","purple"],
        ["true", "false"],
        ["yes", "no"],
        ["on", "off"],
        ["0", "1"]
    ]
}
```

If installed using `Package Control` dictionary file should be located in `<data_path>/Packages`. To get there select `Preferences -> Browse Packages...` in Sublime menu. Create one if it does not exist.
