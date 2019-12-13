---
title: Roadmap
subtitle: "This is the current roadmap for Red 1.0. You can find a more detailed roadmap on our [Trello board](https://trello.com/b/FlQ6pzdB/red-tasks-overview)."
roadmap_entries:
  - section: "Bootstrap"
    items:
      - item: Write Red/System compiler in REBOL
        percentage: 100
      - item: Write Red/System linker in REBOL
        percentage: 100
      - item: Write Red runtime in Red/System
        percentage: 95
        sub_items:
          - item: Memory Allocator
            percentage: 100
          - item: Garbage collector
            percentage: 50
          - item: Run-time lexical scanner
            percentage: 100
          - item: Datatypes
            percentage: 95
      - item: Actions
        percentage: 75
      - item: Natives
        percentage: 87
      - item: Interpreter
        percentage: 100
      - item: File I/O
        percentage: 90
      - item: Network I/O
        percentage: 20
      - item: Compile-time lexical scanner
        percentage: 100
      - item: GUI support
        percentage: 60
        sub_items:
          - item: Cross-Platform GUI Engine
            percentage: 100
          - item: GUI DSL
            percentage: 100
          - item: Vector 2D DSL
            percentage: 100
          - item: Windows backend
            percentage: 100
          - item: Android backend
            percentage: 20
          - item: GTK3 backend
            percentage: 10
          - item: MacOSX backend
            percentage: 98
          - item: iOS backend
            percentage: 0
      - item: Write Red static compiler in REBOL
        percentage: 95
      - item: Write Red standard library in Red (mezzanine code)
        percentage: 85
  - section: Self-Hosted
    items:
    - item: Rewrite Red/System compiler in Red
      percentage: 0
    - item: Rewrite Red compiler (both AOT and JIT) in Red
      percentage: 0
  - section: Code backends
    items:
    - item: IA-32
      percentage: 100
      sub_items:
      - item: PIC support
        percentage: 100
    - item: ARMv5
      percentage: 100
      sub_items:
      - item: PIC support
        percentage: 100
    - item: "[AVR](http://www.atmel.com/products/AVR/)"
      percentage: 8
      sub_items:
      - item: AVR 8-bit
        percentage: 15
      - item: AVR 32-bit
        percentage: 0
    - item: JVM
      percentage: 0
    - item: CLR
      percentage: 0
    - item: x86-64
      percentage: 0
  - section: File formats emitters
    items:
    - item: PE/COFF
      percentage: 66
      sub_items:
      - item: Code+data segments
        percentage: 100
      - item: Imports segment
        percentage: 100
      - item: PIC support
        percentage: 100
      - item: Shared dynamic library (.dll)
        percentage: 100
      - item: Static library (.lib)
        percentage: 0
      - item: Object format (.o)
        percentage: 0
    - item: ELF
      percentage: 66
      sub_items:
      - item: Code+data segments
        percentage: 100
      - item: Imports segment
        percentage: 100
      - item: PIC support
        percentage: 100
      - item: Shared dynamic library (.dll)
        percentage: 100
      - item: Static library (.lib)
        percentage: 0
      - item: Object format (.o)
        percentage: 0
    - item: Mach-o
      percentage: 66
      sub_items:
      - item: Code+data segments
        percentage: 100
      - item: Imports segment
        percentage: 100
      - item: PIC support
        percentage: 100
      - item: Shared dynamic library (.dll)
        percentage: 100
      - item: Static library (.lib)
        percentage: 0
      - item: Object format (.o)
        percentage: 0
    - item: "[Intel-HEX](http://en.wikipedia.org/wiki/Intel_HEX)"
      percentage: 100
      sub_items:
      - item: Code+data
        percentage: 100
  - section: Bridges
    items:
    - item: JVM / Android
      percentage: 90
    - item: CLR / .NET
      percentage: 50
---

<content>
