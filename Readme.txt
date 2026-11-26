# Basic Forks and C Style Development

This project contains the C programs from Lab 5 (Process Management) of the Operating Systems course (CSE233).

It shows how to create processes, use the linker, and understand how the loader works in Linux.

## Description

This project covers three main topics:

- **Process Creation:** `process_creation.c` uses `fork()` to create a child process. The parent and child print different messages.
- **Linker:** `file1.c` contains a function, and `file2.c` calls this function. Both files are connected to create one program.
- **Loader:** `simple_program.c` is a simple program. We use `ldd` to check the libraries it needs.

The file `answers.txt` contains the code explanations, theory answers, and Linux terminal exercises.

## Project Files

| File | Purpose |
|---|---|
| `process_creation.c` | Creates a child process using `fork()` |
| `file1.c` | Contains the `hello()` function |
| `file2.c` | Calls the `hello()` function |
| `simple_program.c` | Simple program used to test the loader |
| `Makefile` | Builds and runs the programs |
| `answers.txt` | Contains explanations and answers |
| `LICENSE` | MIT License |

## Badges

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

![Language: C](https://img.shields.io/badge/language-C-blue.svg)

## Screenshots

The `screenshots` folder contains pictures of compiling and running the programs.

## Installation

You need Linux, GCC, and Make to run this project.

First, install GCC and Make:

```bash
sudo apt install gcc make
```

Download the project from GitHub:

```bash
git clone <your-repository-url>
cd <repository-folder>
```

Build all programs:

```bash
make
```

This command creates three programs:

- `process_creation`
- `output_program`
- `simple_program`

## Usage

To build and run all programs, use:

```bash
make run
```

You can also run each program separately:

```bash
./process_creation
./output_program
./simple_program
```

To check the shared libraries used by `simple_program`:

```bash
make ldd
```

**Testing the Linker:**

Open `file1.c` and change the message to something like:

```c
printf("Hello from Banana!\n");
```

Then run:

```bash
make
./output_program
```

You will see the new message without changing `file2.c`.

**Note:** The parent and child messages may appear in a different order each time. Their process IDs (PIDs) also change every time we run the program.

To delete the compiled programs, use:

```bash
make clean
```

## Support

If the project does not work, check that GCC and Make are installed:

```bash
gcc --version
make --version
```

## Authors  
   ** Hassan Yasser Elgouhary **

## License

This project uses the MIT License.

## Project Status

Finished. This project was created as a university assignment
