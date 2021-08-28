## Linux from Source System

Welcome to the LiSoSy - or the Linux from Source System project. This project is an official project of [The Potabi Foundation](https://foundation.potabi.com).

### Documentation
We have a system for discussing and showing our designs and build systems. It is important to know how we currently have our build system designed. Here is a diagram helping understand how it works. It's mostly designed to function with as few scripts as needed. These folder names are long names, but each one will have a shorter name.

![diagram](https://raw.githubusercontent.com/PotabiFoundation/diagrams/main/lisosy/basediagram.png)

All files (In order):
- `/config/hostname`:
    > Sets the system's hostname.
- `/config/build`:
    > This file is important for various important things to check. This will include Linux kernel version, ISO output name, and various important defaults and autoconfiguration for system tools. 
- `/tarlist/*`
    > The tarlist files are just lists of tar names you set in the `/src/tarbuild` directory. This is where you can enable, disable, comment, and list all tarballs you will use in your builds. The names within this file are important, but more will be part of the src.
- `/src`
    > This directory is still incomplete.
  - `/src/tarbuild`
    > These files have to be named the same as each of the ones listed in `/tarlist`.
    - `/src/tarbuild/tar-build.sample`
        > This file is important, as it shows you how these files work. You can actually read more about these files [here](./tar-build.sample).