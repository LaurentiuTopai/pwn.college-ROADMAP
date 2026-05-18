The Fork Bomb

!!!OBSERVATIE trebuie facut intr-un mediu controlat

ai un fisier .sh
si se auto apeleaza pana ramai fara procese de creat
ex:

bomb.sh

_______________________________________________
#!/bin/bash

echo "BOMBBBB!"
./bomb.sh &
./bomb.sh &

chmod +x bomb.sh





2.
inlocuitor de cat /flag
in caz de rm -rf /
este:
print '%s'"$(</flag)"
