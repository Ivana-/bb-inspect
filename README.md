# BB inspect

Clojure data GUI inspector, (like clojure.inspector on steroids).

This project shares simple standalone inspection module, which also is a part of
[bb-clj](https://github.com/Ivana-/bb-clj) and [bb-debug](https://github.com/Ivana-/bb-debug)
projects, but can be used separately without having deal with VScode plugin or debugger.

## Setup

You can use any way for it - from local build and adding to lein profile deps up to just copypaste one file to your project and use directly.

## Usage

Single namespace provides only one public method `inspect` which opens a GUI window with data representation. Very usable is to set the hotkey with repl command `(inspect *1)` in your editor/IDE. Some popup window features: nested fields are clickable/expandable, hotkeys work (horisontal arrows for expanding/collapsing etc), copy-paste on any nested level pasted full path and value of selected node, lazy-seqs doesn't fires stackoverflow and shows by chunks, etc. You can open any amount of inspection windows at the time.

There are some settings you can alter directly in the code (font size, colors, lazy-seq limits, etc).

## Examples

### HTTP request result (regular map)

![alt text](https://user-images.githubusercontent.com/10473034/55596814-41d6a980-5753-11e9-86cd-a07e659b8757.png "HTTP request result (regular map)")

### Datomic entity (even with cycle links)

![alt text](https://user-images.githubusercontent.com/10473034/55596818-47cc8a80-5753-11e9-93fe-64a458c90767.png "Datomic entity (even with cycle links)")

### Datomic db itself :)

btw, please do not expand millions of datoms into GUI view, they'l strictly fit the tree and freeze the view - maybe I'l fix it in later release if this tool would be commonly used

![alt text](https://user-images.githubusercontent.com/10473034/55596818-47cc8a80-5753-11e9-93fe-64a458c90767.png "Datomic db itself :)")


## License

Copyright © 2022

Distributed under the Eclipse Public License either version 1.0 or (at your option) any later version.
