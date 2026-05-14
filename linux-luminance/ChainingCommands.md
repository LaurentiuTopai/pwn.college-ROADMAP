#`&&`
&& merge doar daca comanda anterioara s-a executat cu succes

command1 && command2

#`||`
|| merge doar daca prima comanda esueaza

command1 || command2


____________________________________________________________

		BASH SCRIPT
____________________________________________________________


#!/bin/bash <- important ca sa poti folosi ./ <- trebui adaugat si permisiune

ex:

touch script.sh
chmod +x script.sh

____________________________________________________________

		CONTINUT
____________________________________________________________
Problema: vom primi ca parametru la fisier 1 cuvant
1. daca cuvantul este pwn atunci va afisa "college" daca nu va afisa "nope"

#!/bin/bash

if [ "$1" == "pwn" ]
then
	echo "college"
else
	echo "nope"
fi

$1 <- primul argument 
$2 <- al doilea argument
..
$n <- al n-lea argument



Problema: vom primi ca parametru la fisier 1 cuvant
1. daca e "pwn" va afisa "college"
2. daca e "hack" va afisa "the planet"
3. daca e "learn" va afisa "linux"
4. daca e orice altceva va afisa "unknown"

#!/bin/bash

if [ "$1" == "pwn" ]
then 
	echo "college"
elif [ "$1" == "hack" ]
then
	echo "the planet"
elif [ "$1" == "learn" ]
then
	echo "linux"
else
	echo "unknown"
fi 
