# CSFS
Cowmonk's Suckless From Scratch Guide

## What does this repository hold?
As I continue to work on the guide, this repository will house certain scripts, patches, and other things that will have to come up.

In the end, there will be a Makefile that will compile a PDF guide, I plan to work on separating this project into multiple LaTeX files.

## Goals
The goal of this is not to create the smallest statically linked "distro", but a guide on how to create a relatively minimal system
which attempts to avoid GNU utilities, use as much suckless utils, minimal enough, and with usability in mind (you can use **some** 
bloated applications without the need for using containers or **fatpak**). Like Linux From Scratch, this is the core system, and there
is a beyond version, and both versions will exist on the same repository. Here are some notable things I plan to do:
- Users have the ability to either use clang/llvm, tcc, cproc, etc if they so chose. Some packages (the linux kernel) will only be able to be compiled with the bloated compiler, and it will be specified which packages.
- Controversely, the guide will provide build guides for Xlibre, say how you will, I won't provide build guides on a dead project. If you don't like Xlibre, the alternative (which I will do) is TinyX.
- On the same topic as above, **NO** wayland. Either build for one server or the other, both are bloated, having both is worse than having one. Also too lazy to provide more support across multiple display servers.
- There is a more suckless part of the guide, and a more bloated suckful part (firefox, gcompat, gaming, discord, etc)
- On coreutils, ubase and sbase are great, but I will provide other alternative builds (toybox, busybox, etc.)
- Other core components: sinit (will provide scripts and other goodies), sdhcp, smdev (alternatives: mdev, mdevd, or oasis approach of none), [eiwd](https://github.com/illiliti/eiwd) (or wpa_supplicant) for wireless networking, etc.

## Other Notes
This won't be the only repository that I create for Suckless From Scratch, I plan to create a pure llvm + musl toolchain cross-compiler.
This project came out of a yearning for a **mostly** GNU-free suckless "distro" (I don't think I'll be able to replace GNU make). 
While I love oasis linux and what it does, there are a
bit of downsides in using oasis (I mean duh), but it's goal of creating a small static distro is extremely honorable. For one, I felt
like it's deviation to using a package manager for everything else kinda sucks (pkgmgr & nix), but yeah maintaining such a huge amount of packages sucks,
which is entirely understandable. Secondly, say how you will, but I don't like wayland, yes it might be "slim", but that's only the protocol;
Xorg is not perfect, but it's a hell of a lot flexible, doesn't break everything, and actually works (also I want to use dwm). Thirdly,
it's boring to have everything automated, that's why I love LFS, but oasis doesn't scratch that itch for me. I want a comprehensible guide
on building it from scratch, not everything being automated with scripts (or well, except for Xorg lol).

Unfortunately, as my goals are also usability, there will be bloated components to my distro, such as some dynamic linking, and scary bad build systems (cmake/meson).
People are able to avoid these by using things like tinyX instead of Xlibre. I love customizability, and I look forward to anyone willing to help contribute and
expand this guide to make it the best suckless guide by far!

# Credits
- [Linux From Scratch](https://www.linuxfromscratch.org/) - thank you for inspiration and such a great guide
- [Suckless](https://suckless.org) - thank you for the indoctrination lol and quality software
- [Oasis Linux](https://github.com/oasislinux/oasis) - thank you for creating such a small amazing distro
- [Xlibre](https://x11libre.net/) - thank you for a maintained xorg
