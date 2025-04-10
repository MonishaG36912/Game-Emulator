# Game-Emulator
## Team Members

- Ryan Welter
- Wyatt Avilla
- Monisha Garika
- Michelle Gurovith
- Michael Kamensky

# CSE 111 Emulator with Ethan Sifferman at UCSC
The Banana Emulator is a custom-built emulator for a fictional video game console, developed as part of the CSE 111 course. The project involves creating both the low-level and high-speed components of the emulator, which includes parsing binary ROM files, implementing a CPU, GPU, and memory system, and rendering the game output at high frame rates. The emulator also supports controller input, making it capable of running various games on the Banana platform. 
## How to Build and Run

In the root of a freshly cloned repo run:

```sh
git submodule update --init --recursive
mkdir build
cd build
cmake ..
make -j$(nproc)
```

This will create an executable `emulator` in the current directory.

### Build Options

You can change the behavior of the emulator by passing `-DCMAKE_BUILD_TYPE=<build_type>` to Cmake.

The `Release` option is passed by default, and the `Headless` option builds the emulator without a
GUI.

| Cmake Option        | Clang flags                    |
| ------------------- | ------------------------------ |
| `Debug`             | `-ggdb -O0`                    |
| `Release` (default) | `-O3 -Werror`                  |
| `Headless`          | `-O3 -Werror -DHEADLESS_BUILD` |

