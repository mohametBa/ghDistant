Entrer "y" si vous voulez committer les modifications
Sinon tapez "n" pour quitter le commit
Voici le code shell qui permet d'exécuter un commit detaillé
.
.
.
#!/bin/bash
read -p "ajouter le fichier de suivi de commit (y/[n]) ?" yn < /dev/tty
yn=${yn:n}
case $yn in
 [Yy]* )
 date=$(date +"%Y-%m-%d %T")
 echo "commit verifie le $date" > suivi/commitInfo.txt
 git add suivi/commitInfo.txt
 exit 0;;
 [Nn]* )
 exit 0;;
esac
exit 0