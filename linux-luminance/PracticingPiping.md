## `>`
**Categorie:** Redirect

echo PWN > file.txt

_Util cand vrei sa transporti outputul intr-un alt fisier_


##`>>`
**Categorie:** Truncate
Daca fisierul avea deja scris ceva in el cu ajutorul >> mapam restul infromatiei 
echo PWN >> file.txt
_Util cand vrei sa transporti outputul fara a strica continutul_

##`File Descriptor in Linux`
**Categorie:** Teorie

FD0:Standard Input
FD1:Standard Output
FD2:Standard Error

Cand folosim ">" acesta comuta File descriptorul in input/output putem folosi
"1>" pentru a preciza explicit ce file Descriptor avem FD1

Ex:

/challenge/run > myflag 2> instructions

_Util cand vrei sa salvezi errorile sau sa parsezi diferit_


##`<`
**Categorie:** INPUT

echo COLLEGE > PWN
cat PWN
COLLEGE

/challenge/run < PWN <- parseaza val din PWN in run

_Util cand ai un set mare de date de parsat ca si input_

##`|`
**Categorie:** Pipe
Ex:
/challenge/run <- imi va returna o multime de valori (*)

/challenge/run | grep pwn <- imi va trimite outputul din (*) ca input in grep 

_Util pentru transfer rapid de date de la output la input si vice versa_

##`>&`
**Categorie** Redirection of a file descriptor

Transfera un file descriptor intr-un alt file descriptor


##`2>&1`
**Categorie** Parsare
Transfera errorile din primul file descriptor ca input in urmatorul file
descriptor
Ex:
/challenge/run 2>&1 | grep pwn <- transfera outputul de errori din 
/challenge/run ca input in grep pentru a fii filtrare

_Util cand vrei sa verific errorile si sa gasesti una anume_


##`grep -v`
**Categorie:** Filtrare
Daca "grep" returneaza liniile care respecta un pattern
grep -v returneaza liniile care nu respecta un pattern 

_Util cand ai multe "DECOIES" date de care nu ai nevoie_

##`sed`
**Categorie:**
EX:
sed "s/oldword/newWord/g"

s/-substitute
oldword-word to replace
newWord - word to replace with
/g - global <- cauta pentru toate cunvintele care sunt oldword sa le faca
newWord 
_Util cand vrei sa schimbi anumite cuvinte in alte cunvinte sau sa le stergi_


##`tee`
**Categorie:** Debug

EX:
command1| command2

OUTPUT:command2 failed

command1 | tee comand1_output | command2

cat comand1_output

OUTPUT:command1 need --flag

comand1 --flag | command2
SUCCES	

_Utila cand vrei sa faci debug intre pipe-uri_

##`<(COMMAND)`
**Categorie** Pipe
Ex:
echo <(echo hi)
OUTPUT: /dev/fd/63 <- acesta este path-ul of the named pipe file
__
