---
title: About
subtitle: Red is a deep, powerful language, inspired by Rebol.<br>Its mission, to fight software complexity.
blocks:
  - template: "media-feature"
    heading: "Red Can Do It All"
    content: |-
      Red is a full-stack, metal to meta, open-source toolchain. It's a 
      relatively new, language created by Nenad Rakocevic. It was directly
      inspired by Rebol, designed by Carl Sassenrath (of Amiga OS fame),
      and has been developed as an open-source project since 2011.
      
      Red was bootstrapped in Rebol, to prove that the language was capable
      of self-hosting. High level Red code compiles to low level Red/System 
      code, which compiles directly to machine code. No C compiler or 
      assembler is needed.
     
    image: "/images/redlang_heroine_planet2.jpg"
    image_position: "left"
    image_shadow: true
  - template: "media-feature"
    heading: "Lean, Nimble, Flexible"
    content: |-
      The entire toolchain, including a full cross compiler and reactive GUI
      system, fits in a single EXE just over 1MB in size. Drop that EXE in a
      folder, and you're good to go. Compile to any platform, from any
      platform. Red doesn't depend on anything besides what came with your OS,
      and the same goes for apps you build with it.
      
      But Red is also flexible. You can compile the runtime to be used externally,
      shared by mutiple apps, or called into from other languages. If you need
      blazing performance, like C, you can program directly in Red/System, getting
      EXEs as small as 7-25K (dependending on the target OS). Or you can mix and
      match. By using the `routine` keyword in Red, you can inline Red/System code
      for performance critical sections.
    image: "/images/redlang_heroine_crouch.jpg"
    image_position: "right"
    image_shadow: true
  - template: "media-feature"
    heading: "Red Makes Life Easy"
    content: |-
      It uses human-friendly syntax, like 31-Jan-2018 / 16:00+8:00 for dates, 
      which is 1517385600 for those of you wearing an epoch seconds watch. What?
      Nobody? That's what we thought. As programmers, we are so used to the pain
      most languages inflict on us, that we never even think there could be a
      better way.
      
      We spend a lot of time on the design side, not just copying designs from
      the past but taking the long view. Your time, and the time for everyone 
      reading and maintaining your code is valuable. Much more valuable than the
      machine's time. A great irony here is that Red can be much more efficient
      while also providing a better user experience.
      
    image: "/images/heroine_hanoi.jpg"
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
      Sure, it's easy to use, a no-brainer to install, and will let you write
      code in your paradigm of choice. But it's not for everyone. It's for 
      rebels or, as we call ourselves, Reducers. Those who think there has to 
      be a better way to write software, who are tired of slow, bloated, complex
      tools. The few who recognize that we've forgotten some of the best and
      most important lessons from the early days, while carrying forward a legacy
      of syntax and limitations tied to machines and thinking from long ago.
    image: "http://via.placeholder.com/500x280"
    image_position: "left"
    button_text: "Learn More"
    button_url: "https://doc.red-lang.org/"
    bg_dark: true
  - template: "action-feature"
    heading: "Are you one of us?"
    content: |-
      Do you feel that there's something wrong with the world? You don't know
      what it is, but it's there, like a splinter in your mind...OK, you do
      know what it is; it's complexity. If you agree, if you dare to follow
      the tradition of the Rebol Forces, we can show you that there is no 
      spoon. Join us, and fight sofware complexity.
    image: "http://via.placeholder.com/500x280"
    image_position: "right"
    button_text: "Start Reducing"
    button_url: "https://gitter.im/red/red"
    bg_dark: true
  - template: "narrow-cta"
---
