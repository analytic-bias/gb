# Convert Word documents to markdown with pandoc
I use [pandoc](https://pandoc.org) to convert masses of Word documents to markdown. Still working on a generic script, but for now
here's the "gist" of what I type into the terminal: 

```bash
$ myfilename="example"
$ pandoc \
-t markdown_strict \
--extract-media='./attachments/$myfilename' \
$myfilename.docx \
-o $myfilename.md
```
Pandoc markdown is nice, but with Word documents it often _adds_ odd things in translation.
Stick to markdown_strict to avoid that.

I try to organize media (images, etc) embedded in documents under an attachments subdirectory with folders named for each file.
This helps avoid "collision" between media file names and makes conversion out of markdown into other formats (HTML, PDF)
less messy.
