## `*`
**Categorie:** Regex 
EX:
cd /ch*

is similar with cd /challenge

_Useful for searching a bunch of folders and files with the same name _


## `?`
**Categorie:** Regex
if we have in directory 
File-a File-b File-cc

ls File-?? => will return File-cc
ls File-? => will return File-A File-B

_Useful for searching a file/directory with a specific pattern_

##`[]`
**Categorie:** Regex

if we have in directory
File-a File-b File-cc

ls File-[ab] => will return File-a File-b 
_Useful for searching a file/directory with a more specific pattern_

##`[^] OR [!]`
**Categorie:** Regex
if we have in directory
file-a file-b file-c

ls file-[!ab] => file-c
ls file-[ab] => file-a file-b
_Useful for searching a file/directory with a specific pattern_

##`<TAB>`
**Categorie:** Autocomplite
if we have in directory
file,idk,idk2
ls f<TAB> => ls file
_Useful for searching a file/directory very fast_
