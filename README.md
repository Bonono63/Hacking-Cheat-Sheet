# Hacking-Cheat-Sheet

- Easy decoding site
[dcode.fr](https://www.dcode.fr/)

- python library for crypto
[cryptography](https://cryptography.io/en/latest/)

- precomputed hash table site
[crackstation](https://crackstation.net/)

- python print without new line
print(, end='')

- python byte strings to python strings
##
    .decode()

## General text and file formats
- Very simple only 128 characters, how byte strings are encoded in C, encoded in 2^7 (2^8 but probably signed)
[ASCII](https://en.wikipedia.org/wiki/ASCII)
- Millions of potential characters, intended to encode every possible symbol and character in existance, support for likely all written language, encoded in 2^32
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
## hex to bytes
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
