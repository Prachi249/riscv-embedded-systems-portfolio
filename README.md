# RISC-V Embedded Systems Projects

A small portfolio of low-level embedded systems projects written in **RISC-V assembly** for a SiFive-based microcontroller platform. The projects demonstrate direct GPIO control, memory-mapped I/O, deterministic timing, lookup-table encoding, interrupt handling, and register-level programming.

> **Academic-work note:** These projects originated as collaborative university laboratory coursework. Personal identifying information has been removed from the public-facing source. Before making this repository public, verify that your course/institution permits publication of completed lab code and that any collaborator is comfortable with the shared work being published.

## Projects

### 1. [Morse Code Translator](./morse-code-translator)
Converts ASCII characters into Morse-code LED patterns using a compact 16-bit lookup table and RISC-V assembly routines for table indexing, bit-level decoding, GPIO output, and timing.

**Highlights:** RISC-V assembly · ASCII indexing · lookup tables · memory addressing · GPIO · subroutines · stack/return-address management · timing loops

### 2. [Interrupt-Driven Binary Countdown Timer](./interrupt-binary-countdown)
Uses a GPIO pushbutton interrupt to enter an ISR, generate a randomized countdown interval, and display the remaining value in binary on an LED bar. The implementation configures RISC-V machine interrupts and the PLIC directly in assembly.

**Highlights:** RISC-V assembly · external interrupts · PLIC · CSRs · ISR context save/restore · memory-mapped GPIO · pseudo-random generation · binary LED display

## Hardware / Tooling

- SiFive RISC-V microcontroller platform
- SparkFun RED-V Thing Plus / `sparkfun_thing_plus_v` PlatformIO target
- PlatformIO
- Freedom E SDK
- LED bar and pushbutton GPIO peripherals

## Repository Structure

```text
riscv-embedded-systems-portfolio/
├── README.md
├── .gitignore
├── morse-code-translator/
│   ├── README.md
│   ├── platformio.ini
│   └── src/
│       └── morse_code_translator.S
└── interrupt-binary-countdown/
    ├── README.md
    ├── platformio.ini
    └── src/
        └── interrupt_binary_countdown.S
```

## Portfolio Focus

These projects are included to demonstrate low-level embedded fundamentals relevant to firmware and controls engineering: translating requirements into deterministic state/bit logic, interacting directly with physical I/O, debugging at the register level, and understanding how processor architecture maps to real hardware behavior.
