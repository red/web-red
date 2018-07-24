---
title: Getting Started
subtitle: Everything you need to know to install Red locally and begin writing your first project.
---

## Installing Red locally

Here is a step by step guide of how to install Red locally:

1. Download the correct Red binary version for your computer [from here](/download/) (takes only a few seconds, it's less than 1MB). Save into a suitable folder.
2. For Windows users, run it by double-clicking on the Red binary file. It will then automatically build the Red GUI-console. Next time you double-click on the file, the GUI-console will automatically open.
3. For Linux/OSX users, you need to open a terminal app to be able to run Red. Once you have opened the terminal app, change to the directory in which you saved Red. Now do a: `chmod u+x <red-binary>` which will make sure that Red can be run on your computer. After that simply run Red using `./<red-binary>`. This will build the Red console. Next time you run Red, the console will automatically open.

Done! No installer, no setup, no dependencies(*)! What, that's all? Yes, there was a time when software used to be done right, that's what we aim at bringing back. ;-)

_(*) We have a temporary dependency on `libcurl3` for Linux platform, so in case it is not installed or if you are running a 64-bit Linux, please check extra instructions from our [download page](/download/)._

## Making a "Hello World"

Red comes with a interpreter in addition to the compiler, which can be easily accessed using the built-in REPL. Calling Red binary with no argument will open the console and allow you to interact with the language in live:

```
red>> print "Hello World!"
Hello World!
```

If you are running Red from Windows, you can also use the built-in GUI system and make a more appealing HelloWorld:

```
red>> view [text "Hello World!"]
```

Now try something more sophisticated:

```
red>> view [name: field button "Hi" [print ["Hi" name/text]]]
```

Yes, GUI programming can be that easy! See more about GUI capabilities in this GUI [release post](http://www.red-lang.org/2016/03/060-red-gui-system.html) and have a look into the View [reference documentation](https://doc.red-lang.org/gui/View.html).


## Compiling a "Hello World"

You can also compile your Red programs and get a single binary with no dependencies. You don't have to install anything else, the Red binary you have downloaded already contains a complete toolchain for native compilation! Here is how to use it:

1. In a code or text editor, write the following Hello World program:

        Red [Title: "Simple hello world script"]
    
        print "Hello World!"

2. Save it under the name: hello.red

3. From a terminal (works from DOS too), type:

        $ red -c hello.red
        $ ./hello

        or from DOS:
        > red -c hello.red
        > hello

4. You should see the Hello World! output.

5. Want to cross-compile to another supported platform?

        $ red -c -t Windows hello.red
        $ red -c -t Darwin hello.red
        $ red -c -t Linux-ARM hello.red

Cross-compilation done right: checked! ;-)

Here is a list of currently supported platforms:

```
MSDOS        : Windows, x86, console (+ GUI) applications
Windows      : Windows, x86, GUI applications
WindowsXP    : Windows, x86, GUI applications, no touch API
Linux        : GNU/Linux, x86
Linux-ARM    : GNU/Linux, ARMv5, armel (soft-float)
RPi          : GNU/Linux, ARMv5, armhf (hard-float)
Darwin       : macOS Intel, console-only applications
macOS        : macOS Intel, applications bundles
Syllable     : Syllable OS, x86
FreeBSD      : FreeBSD, x86
Android      : Android, ARMv5
Android-x86  : Android, x86
```

## Compiling a GUI "Hello World"

Save the following code in hello-gui.red file:

```
Red [Needs: 'View]
    
view [text "Hello World!"]
```

Compile and run it the same way as the first hello.red script (just replace the filename with hello-gui.red). Notice that compiled GUI apps requires a `Needs: 'View` declaration in the Red header block. This tells the compiler to import the View module, which contains all the GUI supporting code.

## Going further...

You can now continue your journey discovering all the great features of Red through the following links:

* A user-friendly [introduction to Red](http://redprogramming.com/Home.html) (including some history).
* Learning about Red core concepts using the [Rebol documentation](http://www.rebol.com/docs/core23/rebolcore.html) ([mirror](http://web.archive.org/web/20160322081114/http://www.rebol.com/docs/core23/rebolcore.html)).
* A [introduction to Parse](http://www.red-lang.org/2013/11/041-introducing-parse.html) DSL with an example of creating a simple DSL.
* [Chatting](https://gitter.im/red/red) with the Red community and asking questions to the Red contributors.
* Explore the [red/red](https://github.com/red/red) repository on Github and have a look at the source code.
* Try some of the samples in [red/code](https://github.com/red/code).
* Install the [Visual Studio Code](https://code.visualstudio.com/) IDE with the [Red extension](https://marketplace.visualstudio.com/items?itemName=red-auto.red).

Happy coding/hacking and have fun...that's the whole point! ;-)
