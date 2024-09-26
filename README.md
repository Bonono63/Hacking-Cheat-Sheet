# Hacking-Cheat-Sheet

- Easy decoding site
(dcode.fr)[https://www.dcode.fr/]


- python print without new line
print(, end='')

- python byte strings to python strings
##
    .decode()

[base64 wikipedia](https://en.wikipedia.org/wiki/Base64)
- Base 64 encodes data to within a 2^6 size, Often used in web
python
##
    import base64 as b64
##
    b64.b64encode()
##
    b64.b64decode()

(hexidecimal wikipedia)[https://en.wikipedia.org/wiki/Hexadecimal]
- Base 16 or hexidecimal: encoded within 2^4, frequenty used to represent memory addresses
python
## hex to bytes
    bytes.fromhex()

(fundamental types cppreference)[https://en.cppreference.com/w/cpp/language/types#Modifiers]
- long is at least 32 bits, base 10, most c primitive types are base 10 (printed memory addresses will be in hex
##
    import Crypto.Util.Number as cum
##
    cum.long_to_bytes()
##
    cum.bytes_to_long()
