#`tr`
**Categorie:** Modificare
echo OWN | tr O P
PWN
modifica litera O in P pentru cuvantul primit ca output

echo PWM.COLLAGE | tr MA NE
PWN.COLLEGE

_Util cand vrei sa faci anumite modificari_

#`-d`
**Categorie:** Delete
echo PAWN | tr -d A
PWN
tr -d A va sterge toate litere care sunt egale cu A
_Util cand vrei sa modifici un string direct in terminal_

#`head`
**Categorie:** Search

cat /file_long | head
this
is
just
the
first
ten
lines
of
the
file
Va afisa primele 10 Cuvinte din el

cat /flige_long | head -n 2
this
is

_Util cand vrei doar o anumita parte din continutul dintr-un file_

#`cut`
**Categorie:**Search
hacker@dojo:~$ cat scores.txt
hacker 78 99 67
root 92 43 89

cut -d " " -f 1 scores.txt
hacker
root

cut -d " " -f 2 scores.txt
78
92
_Util cand vrei doar o cloana anume de date_


#`sort`
**Categorie:**Sortare
hacker@dojo:~$ cat names.txt
  hack
  the
  planet
  with
  pwn
  college
hacker@dojo:~$ sort names.txt
  college
  hack
  planet
  pwn
  the
  with

sort -r <-reverse (Z to A)
sort -n <-numeric (sort for numbers)
sort -u <-uniq (lines remove duplicates)
sort -R <-random order!

_Util cand vrei doar anumite date_
