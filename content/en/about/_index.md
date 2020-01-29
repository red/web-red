---
title: About
subtitle: Red is a deep, powerful language, inspired by Rebol.<br>Its mission, to fight software complexity.
blocks:
  - template: "media-feature"
    heading: "Red Can Do It All"
    content: |-
      It's a metal to meta, open-source toolchain created by Nenad Rakocevic,
      directly inspired by Rebol (designed by Carl Sassenrath of Amiga OS
      fame), and actively developed as an open-source project since 2011.
      
      Bootstrapped in Rebol, to prove that the language was capable
      of self-hosting, high level Red code compiles to low level Red/System 
      code, which compiles directly to machine code. No C compiler or 
      assembler is needed.
     
    image: "/images/can-do-it-all.jpg"
    image_position: "left"
    image_shadow: true
  - template: "media-feature"
    heading: "Lean, Nimble, Flexible"
    content: |-
      The entire toolchain, including a full cross compiler and reactive GUI
      system, is in a single EXE just over 1MB in size. Drop it in a folder
      and go. Compile <i>to</i> any platform, <i>from</i> any platform. Red 
      depends only on your OS; the same goes for what you build.
      
      Make standalone EXEs, or compile the runtime to be used externally and
      called into from other languages. Need C speed? Write your app in 
      Red/System (EXEs as small as 7K), or inline Red/System code just for
      performance critical sections.
    image: "/images/lean-nimble.jpg"
    image_position: "right"
    image_shadow: true
  - template: "media-feature"
    heading: "Red Knows You're Human"
    content: |-
      As one example, you write dates like this: `31-Jan-2018/16:00+8:00`, which
      is `1517385600` for those of you wearing an epoch seconds watch. What?
      Nobody? That's what we thought. As programmers, we are so used to the pain
      most languages inflict on us, that we can't even see there could be a
      better way.
      
      We spend a lot of time on design, taking a long view. Human time is more
      valuable than machine time. You win because Red can be more efficient while
      also providing a better user experience.
      
    image: "/images/red-knows.jpg"
    image_position: "left"
    image_shadow: true
  - template: "grid-list"
    num_cols: 4
    grid_items:
      - title: Single File
        description: One EXE. Drop it on your system and go.
      - title: No Dependencies
        description: Red only uses what your OS provides.
      - title: Native GUI System
        description: Built right in; Red syntax in an eDSL.
      - title: VSCode Plugin
        description: Supports help and autocomplete.

      - title: High-level Scripting
        description: Think Python, Ruby, or Javascript abstraction level.
      - title: Modern Syntax
        description: Legacy syntax models don't support things we use all the time.
      - title: Built-in Datatypes
        description: Around 50 of them. Many have direct lexical forms. 
      - title: Homoiconic
        description: Code is data. Red's ancestor, Rebol, was designed as a messaging language. Red is great even if used only as a data interchange format.

      - title: Garbage Collected
        description: You shouldn't have to manage memory.
      - title: Symbolic
        description: Words and context are central elements. 
      - title: Object Support
        description: Prototype based objects, like Javascript and Self.
      - title: Reactivity
        description: Declarative dataflow model; works on objects and GUI elements.
        
      - title: Dynamic and Strongly Typed
        description: Values are strongly typed, variables are not.
      - title: PEG Parser DSL
        description: Works at both the string and Red value level. e.g., you can parse by datatype.
      - title: Macro System
        description: Fully hygienic; compile time or runtime.
      - title: Bridging to the JVM
        description: Android coming soon (experimental now)

      - title: Native Code
        description: Compile to machine code; no C or ASM needed.
      - title: Highly Embeddable
        description: Call into the Red runtime from C or other langs.
      - title: Cross-compilation
        description: Compile to any platform, from any platform.
      - title: Low-level Programming
        description: Red/System is a C-level dialect of Red; built-in.
        
      - title: Concurrency
        description: Informed by many models. One size does not fit all.
      - title: Higher Order Functions
        description: Rethought from the ground up, for the modern world.
      - title: Command Line Support Made Easy
        description: A CLI lib like no other.
      - title: Modules and Packages
        description: Coming soon!
        
        
  - template: "accordion"
    accordion_items:
      - title: How do I install Red?
        description: |-
          It's easy! Go to https://beta.red-lang.org/download/ and follow the instructions.
          Happiness awaits.
      - title: How is Red supported?
        description: |-
          Red has a great community, with most of our chat taking place at https://gitter.im/red/red.
          But you can find all the Red rooms via https://gitter.im/red/home.
      - title: Where is Red going?
        description: |-
          To Infinity and a NaN! Seriously, there are no limits in either direction.
          Whether you use it for writing desktop applications, sys-admin and data 
          analysis tools, microservices, or simply as a data interchange format, Red
          is your faithful companion, your superhero sidekick. The question isn't 
          where Red is going, but where you're going to take it.
  - template: "action-feature"
    heading: "Red isn't for everyone"
    content: |-
      Sure, it's easy to use, a no-brainer to install, and has superpowers, but
      it's not for everyone. It's for rebels or, as we call ourselves, Reducers.
      Those who think there has to be a better way to create software. The few
      who see that we're encumbered by a legacy of limitations from a time gone
      by, yet we've forgotten important lessons of the past. You, who are not
      doomed to repeat it.
    image: "/images/isnt-for-everyone.jpg"
    image_position: "left"
    button_text: "Learn More"
    button_url: "https://doc.red-lang.org/"
    bg_dark: true
  - template: "action-feature"
    heading: "Are you one of us?"
    content: |-
      Do you feel that there's something wrong with the world? You don't know
      what it is, but it's there, like a splinter in your mind...OK, you do
      know what it is; it's complexity. If you agree, take the Red pill. Join
      us, and fight software complexity.
    image: "/images/one-of-us.jpg"
    image_position: "right"
    button_text: "Start Reducing"
    button_url: "https://gitter.im/red/red"
    bg_dark: true
  - template: "narrow-cta"
---
