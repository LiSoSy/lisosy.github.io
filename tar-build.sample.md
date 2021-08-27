# Example TarBuild Script
[`home`](/)

Welcome to TarBuild scripts, a simple shell script that allows for the installation of whatever software you want. This is a KEY COMPONENT in making a system using LiSoSy. Here is the sample for extracting and installing a TAR file. The location and build are automated, however, with most software 

```sh
export TARURL="https://example.com/some-tar-file.tar.xz
export TAREXTRACT="tar xvf some-tar-file.tar.xz"

function build-SomeTarFile {
    make
    make install
}
```
