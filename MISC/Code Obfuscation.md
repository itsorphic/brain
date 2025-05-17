___
Obfuscation is a technique used to make code more difficult to read by humans, but allowing it to function the same way (though performance may be slower).

# Commands
```bash
# Base64 Encode
echo orphic | base64
# Base 64 Decode
echo ENCODED_B&$ | base64 -d

# Hex Encode
echo orphic | xxd -p
# Hex Decode
echo ENCODED_HEX | xxd -p -r

# Rot13 Encode
echo orphic | tr 'A-Za-z' 'N-ZA-Mn-za-m'
# Rot13 Decode
echo ENCODED_ROT13 | tr 'A-Za-z' 'N-ZfgA-Mn-za-m'
```



# Obfuscation Techniques

## Basic

### JavaScript
A `packer` obfuscation tool attempts to convert all words and symbols into a list or a dictionary and then refer to them using the `(p,a,c,k,e,d)` function to re-build the original code during execution. However, it usually contains a certain order in which the words and symbols of the original code were packed to know how to order them during execution.

[BeautifyTools](https://beautifytools.com/javascript-obfuscator.php#)

## Advanced

### JavaScript

Change **String Array Encoding** to `Base64`:
[JavaScript Obfuscator Tool](https://obfuscator.io/)

There are many other JavaScript obfuscators, however they usually make code execution/compilation very slow, and are only recommended to be used for very specific reasons, like bypassing web filters or restrictions:
[JSFuck](http://www.jsfuck.com/)
[JJ Encode](https://utf-8.jp/public/jjencode.html)
[AA Encode](https://utf-8.jp/public/aaencode.html)



# Deobfuscation Websites
[JS Console](https://jsconsole.com/)
[Prettier](https://prettier.io/playground/)
[Beautifier](https://beautifier.io/)
[JSNice](http://www.jsnice.org/)
[UnPacker](https://matthewfl.com/unPacker.html)
