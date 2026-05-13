#`PERMISSIONS`
**Categori:**Permission Types
	|OWNER|GROUP|PUBLIC|
READ	|400  |40   |4     |
WRITE	|200  |20   |2     |
EXECUTE	|100  |10   |1     |
READ-WRITE-EXECUTE 077 pentru GROUP-PUBLIC 
READ-WRITE 064 - READ-WRITE pentru GROUP Read pentru Public

_Doar coduri pentru permisiuni la fisiere_


#``
**Categorie:**TEORIE
Authorization vs Access Control

Authorization is the policy
Access Control is the mechanism


MODELING ACCESS CONTROL
Subjects S
-Things in the system that can act

Objects O
-Assets or objects in the system

Rights R
-What can the subject do to the object


SIMPLIFIED UNIX MODEL
Subjects are processes
Files are objects
Rights(read,write,execute,append,own)
-r,w,x,a,o



#`chown [username] [file]`
**Categorie:**Add owner
mkdir pwn_directory
touch college-file
ls -l
-rw-r--r...
chown hacker college-file
_Util cand vrei sa oferi privilegi cuiva pt un file/directory_

**Categorie:**Teorie
Character device -> interacting with it results in changes to the 
display output rather than changes to disk storage as for a normal file

crw-rw---- 1 root video 29

#`chgrp [username] [file]`

**Categorie:**Add group

_Util cand vrei sa adaugi privilegi cuiva_


r - user/group/other can read the file (or list the directory)
w - user/group/other can modify the files (or create/delete files in the directory)
x - user/group/other can execute the file as a program (or can enter the directory, e.g., using `cd`)
- - nothing 


#`chmod [OPTIONS] MODE FILE`
**Give permission**
u+r give user read permissions
g+wr give group write/read permissions
o-w other remove write permissions
a-rwx removes all rwx permissions


ex:
chmod u-r,g+rw,o-x ...
chmod u=r,g=rw,o=x ...
__
