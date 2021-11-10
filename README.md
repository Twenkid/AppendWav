# AppendWav

-- Todor Arnaudov's WaveAppender --
-- Version 0.01, 12/12/2009 --

http://artificial-mind.blogspot.com
http://research.twenkid.com


-- FREEWARE and NO WARRANTY -- 
-- For Windows XP+ --

How to append/join/concatenate/merge wav segments/files into one?


Appending two or a few Wav files is easy with sound editors such as Audacity, Cool Edit and SoundForge. However, what if you need to join hundreds of files in different folders? Doing this manually is insane. 

Recently I needed to do this with a bunch of records in Italian I wanted to put in my mp3-player. I found only a commercial solution, but I decided to code mine. 

Todor's WaveAppender 0.01 

- Unzip files. 
- Open scan.bat and edit the second string to point the path to the base folder with Wav files. E.g.: 

scan.exe l:\italian\wave\1\ >list.txt 

scan.exe your_full_path_here >list.txt 

- Run scan.bat - it generates list.txt. 
- Open list.txt and put on top a line pointing to the target directory. The merged files will be created there, e.g.: 
- 
```
l:\wav 

l:\italian\wave\0\1b.wav 
l:\italian\wave\0\1i.wav 
l:\italian\wave\0\2b.wav 
l:\italian\wave\0\2i.wav 
l:\italian\wave\0\3b.wav 
l:\italian\wave\0\3i.wav 
l:\italian\wave\0\4b.wav 
l:\italian\wave\0\4i.wav 
l:\italian\wave\0\5b.wav 
l:\italian\wave\0\5i.wav 

# 
$ 
```

- Run append.bat 
- Voila! Files from each folder will be merged in 1.wav (first folder in the list), 2.wav, ... N.wav. 

You can create list files manually. The syntax is: 

First line - target path 
Next - N lists of path to files to be merged in N.wav. A list ends with "#". 
The file ends with "$". 

Eg.: 
```
l:\wav 

l:\italian\wave\0\1b.wav 
l:\italian\wave\0\1i.wav 
l:\italian\wave\0\2b.wav 
l:\italian\wave\0\2i.wav 
l:\italian\wave\0\3b.wav 
l:\italian\wave\0\3i.wav 
l:\italian\wave\0\4b.wav 
l:\italian\wave\0\4i.wav 
l:\italian\wave\0\5b.wav 
l:\italian\wave\0\5i.wav 

# 
l:\italian\wave\2\1b.wav 
l:\italian\wave\2\1i.wav 
l:\italian\wave\2\2b.wav 
l:\italian\wave\2\2i.wav 
l:\italian\wave\2\3b.wav 
l:\italian\wave\2\3i.wav 
l:\italian\wave\2\4b.wav 
l:\italian\wave\2\4i.wav 
l:\italian\wave\2\5b.wav 
l:\italian\wave\2\5i.wav 
l:\italian\wave\2\6b.wav 
l:\italian\wave\2\6i.wav 
l:\italian\wave\2\7b.wav 
l:\italian\wave\2\7i.wav 
l:\italian\wave\2\8b.wav 
l:\italian\wave\2\8i.wav 
l:\italian\wave\2\9b.wav 
l:\italian\wave\2\9i.wav 
l:\italian\wave\2\10b.wav 
l:\italian\wave\2\10i.wav 

# 
$ 
```
NB: Files in each folder (each merge group) should have the same format. Code is pretty simple yet. 


Thanks to Srinivas Varukala (basic code for scanning directories in C#) and Vasian Cepa (Numeric Sorter in C#) for the Scan part, you can find their code in CodeProject. Appender code is in C++, written by me.
