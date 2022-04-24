<a href="https://bledy-guides.repl.co">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/BOM/Window.md">Next &gt;</a>
<hr>
<h1>Index</h1>
<ul>
  <li><a href="#Index">Index</a></li>
  <li><a href="#Introduction">Introduction</a></li>
  <li><a href="#Usage">Usage</a></li>
  <ul>
    <li><a href="#UTF-8">UTF-8</a></li>
    <li><a href="#UTF-16">UTF-16</a></li>
    <li><a href="#UTF-32">UTF-32</a></li>
  </ul>
  <li><a href="#Encoding">Encoding</a></li>
</ul>
<h1>Introduction</h1>
The byte order mark (BOM) is a particular usage of the Unicode character, <code>U+FEFF ZERO WIDTH NO-BREAK SPACE</code>, whose appearance as a magic number at the start of a text stream can signal several things to a program reading the text:
<ul>
  <li>The byte order, or endianness, of the text stream in the cases of 16-bit and 32-bit encodings;</li>
  <li>The fact that the text stream's encoding is Unicode, to a high level of confidence;</li>
  <li>Which Unicode character encoding is used.</li>
</ul>
BOM use is optional. Its presence interferes with the use of UTF-8 by software that does not expect non-ASCII bytes at the start of a file but that could otherwise handle the text stream.
<br><br>
Unicode can be encoded in units of 8-bit, 16-bit, or 32-bit integers. For the 16- and 32-bit representations, a computer receiving text from arbitrary sources needs to know which byte order the integers are encoded in. The BOM is encoded in the same scheme as the rest of the document and becomes a noncharacter Unicode code point if its bytes are swapped. Hence, the process accessing the text can examine these first few bytes to determine the endianness, without requiring some contract or metadata outside of the text stream itself. Generally the receiving computer will swap the bytes to its own endianness, if necessary, and would no longer need the BOM for processing.
<br><br>
The byte sequence of the BOM differs per Unicode encoding (including ones outside the Unicode standard such as UTF-7, see table below), and none of the sequences is likely to appear at the start of text streams stored in other encodings. Therefore, placing an encoded BOM at the start of a text stream can indicate that the text is Unicode and identify the encoding scheme used. This use of the BOM character is called a "Unicode signature".
<h1>Usage</h1>
If the BOM character appears in the middle of a data stream, Unicode says it should be interpreted as a "zero-width non-breaking space" (inhibits line-breaking between word-glyphs). In Unicode 3.2, this usage is deprecated in favor of the "Word Joiner" character, U+2060. This allows U+FEFF to be used only as a BOM.
<h2>UTF-8</h2>
The UTF-8 representation of the BOM is the (hexadecimal) byte sequence <code>0xEF,0xBB,0xBF</code>.
<br><br>
The Unicode Standard permits the BOM in UTF-8, but does not require or recommend its use. Byte order has no meaning in UTF-8, so its only use in UTF-8 is to signal at the start that the text stream is encoded in UTF-8, or that it was converted to UTF-8 from a stream that contained an optional BOM. The standard also does not recommend removing a BOM when it is there, so that round-tripping between encodings does not lose information, and so that code that relies on it continues to work. The IETF recommends that if a protocol either (a) always uses UTF-8, or (b) has some other way to indicate what encoding is being used, then it "SHOULD forbid use of U+FEFF as a signature."
<br><br>
Not using a BOM allows text to be backwards-compatible with some software that is not Unicode-aware. Examples include programming languages that permit non-ASCII bytes in string literals but not at the start of the file.
<br><br>
UTF-8 is a sparse encoding in the sense that a large fraction of possible byte combinations do not result in valid UTF-8 text. Binary data and text in any other encoding are likely to contain byte sequences that are invalid as UTF-8. Practically the only exceptions to that are when the text consists purely of ASCII-range bytes. Because all modern encodings use ASCII-range bytes to represent ASCII characters, ASCII-only text can be safely interpreted as UTF-8 regardless of what encoding was intended by the system that emitted the bytes. Because of these considerations, heuristic analysis can detect with high confidence whether UTF-8 is in use, without requiring a BOM.
<br><br>
Microsoft compilers and interpreters, and many pieces of software on Microsoft Windows such as Notepad treat the BOM as a required magic number rather than use heuristics. These tools add a BOM when saving text as UTF-8, and cannot interpret UTF-8 unless the BOM is present or the file contains only ASCII. Windows PowerShell (up to 5.1) will add a BOM when it saves UTF-8 XML documents. However, PowerShell Core 6 has added a <code>-Encoding</code> switch on some cmdlets called utf8NoBOM so that document can be saved without BOM. Google Docs also adds a BOM when converting a document to a plain text file for download.
<h2>UTF-16</h2>
In UTF-16, a BOM (<code>U+FEFF</code>) may be placed as the first character of a file or character stream to indicate the endianness (byte order) of all the 16-bit code unit of the file or stream. If an attempt is made to read this stream with the wrong endianness, the bytes will be swapped, thus delivering the character U+FFFE, which is defined by Unicode as a "noncharacter" that should never appear in the text.
<ul>
  <li>If the 16-bit units are represented in big-endian byte order, the BOM will appear in the sequence of bytes as <code>0xFE</code> <code>0xFF</code></li>
  <li>If the 16-bit units use little-endian order, the BOM will appear in the sequence of bytes as <code>0xFF</code> <code>0xFE</code></li>
</ul>
Neither of these sequences is valid UTF-8, so their presence indicates that the file is not encoded in UTF-8.
<br><br>
For the IANA registered charsets UTF-16BE and UTF-16LE, a byte order mark should not be used because the names of these character sets already determine the byte order. If encountered anywhere in such a text stream, U+FEFF is to be interpreted as a "zero width no-break space".
<br><br>
If there is no BOM, it is possible to guess whether the text is UTF-16 and its byte order by searching for ASCII characters (i.e. a 0 byte adjacent to a byte in the 0x20-0x7E range, also 0x0A and 0x0D for CR and LF). A large number (i.e. far higher than random chance) in the same order is a very good indication of UTF-16 and whether the 0 is in the even or odd bytes indicates the byte order. However, this can result in both false positives and false negatives.
<br><br>
Clause D98 of conformance (section 3.10) of the Unicode standard states, "The UTF-16 encoding scheme may or may not begin with a BOM. However, when there is no BOM, and in the absence of a higher-level protocol, the byte order of the UTF-16 encoding scheme is big-endian." Whether or not a higher-level protocol is in force is open to interpretation. Files local to a computer for which the native byte ordering is little-endian, for example, might be argued to be encoded as UTF-16LE implicitly. Therefore, the presumption of big-endian is widely ignored. The W3C/WHATWG encoding standard used in HTML5 specifies that content labelled either "utf-16" or "utf-16le" are to be interpreted as little-endian "to deal with deployed content". However, if a byte-order mark is present, then that BOM is to be treated as "more authoritative than anything else".
<br><br>
Programs that interpret UTF-16 as a byte-based encoding may display a garbled mess of characters, but ASCII characters would be recognizable because the low byte of the UTF-16 representation is the same as the ASCII code and therefore would be displayed the same. The upper byte of 0 may be displayed as nothing, white space, a period, or some other unvarying glyph.
<h2>UTF-32</h2>
Although a BOM could be used with UTF-32, this encoding is rarely used for transmission. Otherwise the same rules as for UTF-16 are applicable.
<br><br>
The BOM for little-endian UTF-32 is the same pattern as a little-endian UTF-16 BOM followed by a NUL character, an unusual example of the BOM being the same pattern in two different encodings. Programmers using the BOM to identify the encoding will have to decide whether UTF-32 or a NUL first character is more likely.
<h1>Encoding</h1>
This table illustrates how the BOM character is represented as a byte sequence in various encodings and how those sequences might appear in a text editor that is interpreting each byte as a legacy encoding (CP1252 and caret notation for the C0 controls):
<table class="ws-table-all notranslate">
  <tr>
    <th>Encoding</th>
    <th>Representation (hexadecimal)</th>
    <th>Representation (decimal)</th>
    <th>Bytes as CP1252 characters</th>
  </tr>
  <tr>
    <td>UTF-8 <code>*</code></td>
    <td><code>EF BB BF</code></td>
    <td><code>239 187 191</code></td>
    <td><code>ï»¿</code></td>
  </tr>
  <tr>
    <td>UTF-16 <b>[BE]</b></td>
    <td><code>FE FF</code></td>
    <td><code>254 255</code></td>
    <td><code>þÿ</code></td>
  </tr>
  <tr>
    <td>UTF-16 <b>[LE]</b></td>
    <td><code>FF FE</code></td>
    <td><code>255 254</code></td>
    <td><code>ÿþ</code></td>
  </tr>
  <tr>
    <td>UTF-32 <b>[BE]</b></td>
    <td><code>00 00 FE FF</code></td>
    <td><code>0 0 254 255</code></td>
    <td><code>^@^@þÿ</code> (<code>^@</code> is the <b>null character</b>)</td>
  </tr>
  <tr>
    <td>UTF-32 <b>[LE]</b></td>
    <td><code>FF FE 00 00</code></td>
    <td><code>255 254 0 0</code></td>
    <td><code>ÿþ^@^@</code> (<code>^@</code> is the <b>null character</b>)</td>
  </tr>
  <tr>
    <td>UTF-7 <code>*</code></td>
    <td><code>2B 2F 76</code> <code>*</code></td>
    <td><code>43 47 118</code></td>
    <td><code>+/v</code></td>
  </tr>
  <tr>
    <td>UTF-1 <code>*</code></td>
    <td><code>F7 64 4C</code></td>
    <td><code>247 100 76</code></td>
    <td><code>÷dL</code></td>
  </tr>
  <tr>
    <td>UTF-EBCDIC <code>*</code></td>
    <td><code>DD 73 66 73</code></td>
    <td><code>221 115 102 115</code></td>
    <td><code>Ýsfs</code></td>
  </tr>
  <tr>
    <td>SCSU <code>*</code></td>
    <td><code>0E FE FF</code> <code>*</code></td>
    <td><code>14 254 255</code></td>
    <td><code>^Nþÿ</code> (<code>^N</code> is the <b>"shift out" character</b>)</td>
  </tr>
  <tr>
    <td>BOCU-1 <code>*</code></td>
    <td><code>FB EE 28</code></td>
    <td><code>251 238 40</code></td>
    <td><code>ûî(</code></td>
  </tr>
  <tr>
    <td>GB-18030 <code>*</code></td>
    <td><code>84 31 95 33</code></td>
    <td><code>132 49 149 51</code></td>
    <td><code>„1•3</code></td>
  </tr>
</table>
<code>*</code> This is not literally a "byte order" mark, since a code unit in these encodings is one byte and therefore cannot have bytes in a "wrong" order. Nevertheless, the BOM can be used to indicate the encoding of the text that follows it.
