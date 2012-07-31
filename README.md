chaptermerge
=========
A small script for merging M4V chapter files together (for instance, when you have a two-part movie) into a single file that can then be merged into a final, combined movie.

chaptermerge is designed to be used as part of a workflow in conjunction with tools such as Subler. It really doesn't do a lot on it's own.

Usage
-----
To use chaptermerge, pass in the files as -f's. Each file has a filename and a time, separated by a comma. Time is in the format of hours:minutes:seconds. This is the length of that video segment (and the amount the next series of chapters will be offset).

Pass the file you want written as -o.

    chaptermerge -f file1.txt,2:34:50 -f file2.txt -o file.txt

Workflow
--------
chaptermerge is designed to work as part of your workflow, and can be used in a variety of ways. The way I have used it is like this:

1. Legally rip copies of DVDs that you own. In my case, I wrote this for ***The Ten Commandments***.
2. Feed both copies into a tool such as MetaX, which will merge in chapter names. That's really the only thing you need to add for the time being. Really, you're just doing this to avoid having to create chapter files yourself. You can alwways skip this step if you already have chapter files.
3. Use Subler to extract the individual chapter files from each segment into text files.
4. Use chaptermerge to merge the chapter files together into a single chapter file.
5. Do whatever you'd like to merge the files together and remux the result back into M4V.
6. Use Subler to add the chapter markers back from your merged chapter file.
7. Use MetaX or iDentify to add the remaining metadata.