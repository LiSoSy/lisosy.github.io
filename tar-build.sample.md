# Example TarBuild Script
[`home`](/)

Welcome to TarBuild scripts, a simple shell script that allows for the installation of whatever software you want. This is a KEY COMPONENT in making a system using LiSoSy. Here is the sample for extracting and installing a TAR file. The location and build are automated, however, with most software and even developers having completely different methods of building software, we have made files you can create to build the software you need to.

To make a TarBuild script, just go with three steps:
1. Add the tar's build name to the correct Tarlist file. EX: `SomeTarFile`
    > This name does NOT have to be the exact name as the tar file, as long as it is the same as the TarBuild's file name
1. Create the tar's build script. EX: `SomeTarFile-build.sh`
1. Make sure to add the TARURL, and TAREXTRACT variables.
    - You need the TARURL to get the tar file itself
    - You need the TAREXTRACT to extract the tar file (Some tars need specific arguments, or maybe it isn't even a tar file and needs a different command altogether!)
1. Make sure to add the build function: EX: `function build-SomeTarFile`
    > This needs to end in the same name as the tarlist file.

Once you have followed the instructions, something like this should exist:

`/path/to/LiSoSy/src/tarbuild/SomeTarFile-build.sh`
```sh
export TARURL="https://example.com/some-tar-file.tar.xz"
export TAREXTRACT="tar xvf some-tar-file.tar.xz"

function build-SomeTarFile {
    make
    make install
}
```

Once you are done, it is already ready to function in your next LiSoSy build
