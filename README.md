# Hacking-Cheat-Sheet

## Table of contents
- [general resources](https://github.com/Bonono63/Hacking-Cheat-Sheet/blob/main/README.md#resources)
- [python scripting](https://github.com/Bonono63/Hacking-Cheat-Sheet/blob/main/README.md#python-scripting)
- [linux cli](https://github.com/Bonono63/Hacking-Cheat-Sheet/blob/main/README.md#linux-cli)
- [encoding formats](https://github.com/Bonono63/Hacking-Cheat-Sheet/blob/main/README.md#general-text-and-file-formats)
- [pwning](https://github.com/Bonono63/Hacking-Cheat-Sheet/blob/main/README.md#pwning)
- [assembly](https://github.com/Bonono63/Hacking-Cheat-Sheet/blob/main/README.md#assembly)
- [software security](https://github.com/Bonono63/Hacking-Cheat-Sheet/blob/main/README.md#software-security)
- [web](https://github.com/Bonono63/Hacking-Cheat-Sheet/blob/main/README.md#web-exploits)

## Resources
- Easy decoding site
[dcode.fr](https://www.dcode.fr/en)

- python library for crypto
[cryptography](https://cryptography.io/en/latest/)

- precomputed hash table site
[crackstation](https://crackstation.net/)

- General purpose CTF handbook
[ctf 101](https://ctf101.org/)

- Practice materials
[pwn college](https://pwn.college/)

- Bootcamp CTF hosted by OSU cyberclub
[bootcamp CTF](https://bootcamp.osucyber.club/)

- flag format
##
    osuctf{...}

## Python scripting

- python print without new line
print(, end='')

- python byte strings to python strings
##
    .decode()

## Linux CLI

- Enter hex editor mode in vim (Make sure xxd is installed if using neovim)
##
    %!xxd

-reverse any string in linux cli
##
    rev

- the perl exiftool reads all image metadata and prints it
##
    exiftool

## General text and file formats

- Very simple only 128 characters, how byte strings are encoded in C, encoded in 2^7 (8th bit in a byte is sometimes used for parity)
[ASCII](https://en.wikipedia.org/wiki/ASCII)

- Unicode is the organization that has standardized text encoding, they are responsible for UTF-8, UTF-16, and UTF-32.
- There are currently 250,000 unique characters built into the UTF standard.
- UTF-8 is the most common for regular files
[UTF-8](https://en.wikipedia.org/wiki/UTF-8)

[base64 wikipedia](https://en.wikipedia.org/wiki/Base64)
- Base 64 encodes data to within a 2^6 size, Often used in web
python
##
    import base64 as b64
##
    b64.b64encode()
##
    b64.b64decode()
linux
##
    man base64
##
    base64 -d file

[hexidecimal wikipedia](https://en.wikipedia.org/wiki/Hexadecimal)
- Base 16 or hexidecimal: encoded within 2^4, frequenty used to represent memory addresses
python
##
    bytes.fromhex()

[fundamental types cppreference](https://en.cppreference.com/w/cpp/language/types#Modifiers)
- long is at least 32 bits, base 10, most c primitive types are base 10 (printed memory addresses will be in hex
##
    import Crypto.Util.Number as cum
##
    cum.long_to_bytes()
##
    cum.bytes_to_long()

[octet wikipedia](https://en.wikipedia.org/wiki/Octet_(computing))
- octet is 8 bits, basically just another way to refer to a byte, octal means base 8

## PWNing
- Potential attack vector for very specific cases
(OBO)[https://en.wikipedia.org/wiki/Off-by-one_error]

- Common entry point for Arbitrary code execution
(stack buffer overflow wikipedia)[https://en.wikipedia.org/wiki/Stack_buffer_overflow]

- heap pwning
[heap-exploitation](https://heap-exploitation.dhavalkapil.com/)

## Assembly
- Intel64 and AMD64 are practically identical so just pick up either manual and read it.
(Intel 64 manual download)[https://www.intel.com/content/www/us/en/developer/articles/technical/intel-sdm.html]

## Software Security

- Makes certain memory sections read only
(RELRO intro)[https://ctf101.org/binary-exploitation/relocation-read-only/]
(Enabling RELRO)[https://www.redhat.com/en/blog/hardening-elf-binaries-using-relocation-read-only-relro]

- Marks the stack as being Non-Executable
("NX" wikipedia)[https://en.wikipedia.org/wiki/Executable-space_protection]

- Randomizes the address space positions
(ASLR)[https://en.wikipedia.org/wiki/Address_space_layout_randomization]

- PIE, Position Independent Executables, ASLR adjacent info
(PIE wikipedia)[https://en.wikipedia.org/wiki/Position-independent_code#Position-independent_executables]

- Stack Canary, adds a "nonce" after a buffer on a stack to monitor for buffer overflows
[Stack Canary wikipedia](https://en.wikipedia.org/wiki/Buffer_overflow_protection#Canaries)

- Shadow Stack, creates a seperate non executable memory region for return addresses
[Shadow Stack wikipedia](https://en.wikipedia.org/wiki/Shadow_stack)

## Web Exploits
- TCP packet fabrication
[inc0x0](https://inc0x0.com/tcp-ip-packets-introduction/tcp-ip-packets-3-manually-create-and-send-raw-tcp-ip-packets/)
