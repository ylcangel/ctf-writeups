In `CodeGate 2018 - SuperMarimo` challenge, there is a `heap overflow` vulnerability by which we can leak `malloc@GOT` address in order to find `libc` base address. Using the same vulnerability, we can overwrite `malloc@GOT` (since `Full RELRO` is not enabled) with `One Gadget` address to execute `execve("/bin/sh")`. This is an interesting `heap exploitation` challenge to learn bypassing protections like `NX`, `Canary`, and `ASLR` in `x86_64` binaries.