This level mainly helps in understanding and learning about linux.
<br>

*	filenames starting with a dash(-):
	<br>shell considers '-' for receiving argument
	<br>to use dashed files use <code>./-{filename}</code>or <code>-- -{filename}</code>
* dealing with spaces in filenames:
	* put filenames in quotes
	* use tab to complete entering filename
* hidden files:
	<br>Dot(.) is appended at the beggining of a filename to make it "hidden".
	<br>Default listing command do not show such files.
	<br>Use -a argument to while using <code>ls</code> to show hidden files.
* <a href="https://en.wikipedia.org/wiki/Find_(Unix)">find</a> - a CLI utility for searching files
*	<a href="https://en.wikipedia.org/wiki/Grep">grep</a> - a CLI utility for searching plain-text data sets for lines that match a regular expression
*	<a href="https://en.wikipedia.org/wiki/Uniq">uniq</a> - uniq is a Unix utility which, when fed a text file or STDIN, outputs the text with adjacent identical lines collapsed to one, unique line of text.
* <a href="http://www.linfo.org/pipes.html">Pipes in linux</a>
* <a href="https://en.wikipedia.org › wiki › Regular_expression">Regular Expression</a>
* <a href="https://en.wikipedia.org/wiki/Base64">base64 encoding</a>
*	<a href="https://en.wikipedia.org/wiki/Tr_(Unix)">tr</a> - it is an abbreviation of translate or transliterate, indicating its operation of replacing or removing specific characters in its input data set
* Compression Programs
	* <a href="https://en.wikipedia.org/wiki/Bzip2">gzip</a> : format - .gz, header magic number - 1f 8b
	* <a href="https://en.wikipedia.org/wiki/Gzip">bzip2</a> : format - .bz2, header magic number - BZ(or 5a 42)
	* <a href="https://linux.die.net/man/1/tar">tar</a>
* For creating a <a href="https://en.wikipedia.org/wiki/Hex_dump">hexdump</a>
	* <a href="https://www.tutorialspoint.com/unix_commands/xxd.htm">xxd</a>
	* hexdump