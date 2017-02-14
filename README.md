Operating Systems: From 0 to 1
=============================

This book helps you gain the foundational knowledge required to write an operating system from scratch. Hence the title, 0 to 1.

After completing this book, at the very least:

- How to write an operating system from scratch by reading hardware datasheets. In the real world, it works like that. You won't be able to consult Google for a quick answer.

- Write code independently. It's pointless to copy and paste code. Real learning happens when you solve problems on your own. Some examples are given to kick start, but most problems are yours to conquer. However, the solutions are available online for you to examine after giving a good try.

- A big picture of how each layer of a computer is related to the other, from hardware to software.

- Linux as a development environment and how to use common tools for low-level programming.

- Understand x86 assembly in-depth.

- How a program is structured so that an operating system can run.

- How to debug a program running directly on hardware with gdb and QEMU.

- Linking and loading on bare metal x86_64, with pure C. No standard library. No runtime overhead.

[Download the book](https://github.com/tuhdo/os01/zipball/master)

# The pedagogy of the book

> You give a poor man a fish and you feed him for a day. You teach him to fish and you give him an occupation that will feed him for a lifetime.

This is the guiding principle of the book when I was writing it. The book does not try to teach you everything, but enough to enable you to learn by yourself. The book itself, at this point, is quite "complete": once you master part 1 and part 2 (which consist of 8 chapters), you can drop the book and learn by yourself. At this point, a smart reader should be able to continue on his own. For example, he can continue his journey on [OSDev wiki](http://wiki.osdev.org/Main_Page); or, if he considers developing an OS for fun is impractical, he can continue with a Linux-specific book, such as this free book [Linux Insiders](https://0xax.gitbooks.io/linux-insides/content/), or other popular Linux kernel books.

The book teaches you core concepts, such as x86 Assembly, ELF, linking and debugging on bare metal, etc., but more importantly, where such information comes from. For example, instead of just teaching x86 Assembly, it also teaches you how to use the reference manuals from Intel. Learning to read the official manuals is important because only the hardware manufacturers themselves understand how their hardware work. If you only learn from the secondary resources because it is easier, you will never gain a complete understating of the hardware you are programming for. Have you ever read a book on Assembly, and wonder where does all the information come from? How does the author know everything he says is correct? And how one seems to magically know so much about hardware programming? The book gives a pointer to such questions.

As an example, you should skim through chapter 4, "x86 Assembly and C", to see how it makes use of the Intel manual, Volume 2, when explaining stuffs. And in the process, it guides you how to use the official manuals.

Part 3 is planned as a series of specifications that a reader will implement to complete each operating system component. It will not contain code, aside from a few examples. Part 3 is just there to shorten the reader's time from read the official manuals by giving hints where to read, explaining difficult concepts and how to use the manuals to debug. In sum, the implementation, is up to the reader to work on his own; the chapters are just like university assignments.

# Prerequisites

Know some circuit concepts:
+ Basic Concepts of Electricity: atom, electrons, proton, neutron, current flow.
+ Ohm law

However, if you know absolute nothing, you can quickly learn it here:
http://www.allaboutcircuits.com/textbook/, by reading chapter 1 and chapter 2.

Know some C programming. In particular:

- Variable and functions declaration/definitions

- While and for loops.

- Understand how pointers work.

- Fundamentals of algorithm and data structure in C.

Know Linux basics:

- Know how to navigate directories with the command line

- Know how to invoke a command with options.

- Know how to pipe output to another program.

Know how to touch type. Since we are going to use Linux, touch typing helps. I
know typing speed does not relate to problem -solving, but at least the speed
should be fast enough not to let it get it the way and degrade the learning
experience.

In general, I assume that a reader acquired basic programming knowledge with C,
and can use an IDE at its basic. That is, know how to press the Play button for
building and running a program.

# Status:
* Part 1
- Chapter 1: Complete
- Chapter 2: Complete
- Chapter 3: Almost. Currently, the book relies on the Intel Manual for fully explaining x86 execution environment.
- Chapter 4: Complete
- Chapter 5: Complete
- Chapter 6: Complete
* Part 2
- Chapter 7: Complete
- Chapter 8: Complete
* Part 3
- Chapter 9: Incomplete
- Chapter 10: Incomplete
- Chapter 11: Incomplete
- Chapter 12: Incomplete
- Chapter 13: Incomplete

# Sample OS
[This repository](https://github.com/tuhdo/sample-os) is the sample OS of the book that is intended as a reference material for part 3. It covers 10 chapters of the "System Programming Guide" (Intel Manual Volume 3), along with a simple keyboard and video driver for input and output. However, at the moment, only the following features are implemented:

- Protected mode.
- Creating and managing processes with TSS (Task State Structure).
- Interrupts
- LAPIC.

Paging and I/O are not yet implemented. I will try to implement it as the book progresses.

# Contributing

I will upload the Lyx - Latex source soon, after cleaning it up. In the
meantime, if you find any grammatical issue, please report it using Github
issue. Or, if some sentence or paragraph is difficult to understand, feel free
to open an issue. I really appreciate it.
