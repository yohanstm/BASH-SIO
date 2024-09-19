#### TP - BASH

### Création d'une arborescence (structure hiérarchique)
1. Créez un répertoire avec votre nom de famille à la racine du répertoire courant
```bash
mkdir ./SAINTMARC
``` 
2. Créez dedans les deux répertoires TRAVAIL et 117
```bash
cd SAINTMARC
mkdir TRAVAIL
mkdir 117
``` 
ou
```bash
mkdir SAINTMARC/TRAVAIL
mkdir SAINTMARC/117
``` 

3. Créez dans le répertoire TRAVAIL le sous-répertoire TEMP
```bash
cd TRAVAIL
mkdir TEMP
ou
``` 
```bash
mkdir SAINTMARC/TRAVAIL/TEMP
``` 
4. Créez dans le répertoire 117 le sous-répertoire identifiant chaque marguerite (par
exemple 117_M1 désigne la marguerite 1 de la salle 117)
```bash
cd ..
cd 117
mkdir 117_M3
``` 
ou
```bash
mkdir SAINTMARC/117/117_M3
``` 
5. Créez dans le répertoire précédemment créé (par exemple 117_M1) les deux sous-répertoires
suivants : INFO1 et INFO2
```bash
cd 117_M3
mkdir INFO1
mkdir INFO2
``` 
ou
```bash
mkdir SAINTMARC/117/117_M3/INFO1 SAINTMARC/117/117_M3/INFO2

``` 
6. Placez-vous dans le répertoire INFO1, puis créez les répertoires suivants : SHELL, LINUX,
WORD, EXCEL
```bash

cd SAINTMARC/117/117_M3/INFO1
mkdir SHELL LINUX WORD EXCEL

ou 
```bash
mkdir SAINTMARC/117/117_M3/INFO1/SHELL
mkdir SAINTMARC/117/117_M3/INFO1/LINUX
mkdir SAINTMARC/117/117_M3/INFO1/WORD
mkdir SAINTMARC/117/117_M3/INFO1/EXCEL

``` 

7. Sans changer de répertoire courant, créez dans le répertoire SHELL le sous-répertoire TEMP
N.B. : Pour faciliter les manipulations qui suivent, schématisez l’arborescence sur papier.
```bash
mkdir SAINTMARC/117/117_M3/INFO1/SHELL/TEMP
``` 
### Manipulations (le répertoire courant est INFO1)
1. Listez le contenu du répertoire courant, puis voir une aide sur la commande LS
```bash
ls
man ls -> pour l'aide
``` 
2. Listez les noms des fichiers et des répertoires du répertoire courant, qui commencent par W,
puis ceux commençant par W suivi de trois caractères.
```bash
ls W*
ls W???
``` 
3. Sans changer de répertoire courant, listez-le contenu de /etc avec une pause
```bash
ls / etc   A REFAIRE POUR LA PAUSE 
``` 
4. Sans changer de répertoire courant, listez tous les noms des fichiers de la racine ayant
l'extension .conf
ls / | grep ".conf$"
```bash
ls / | grep ".conf$"
``` 
5. Créez dans le répertoire courant (INFO1) les fichiers liste1.txt, liste2.txt et liste3.txt
comme suit :
je me trouve dans mon répertoir SAINTMARC 
```bash
touch 117/117_M3/INFO1/liste1.txt 117/117_M3/INFO1/liste2.txt 117/117_M3/INFO1/liste3.txt
``` 

5.1. Placez le contenu du répertoire courant dans le fichier liste1.txt.
```bash
echo "Contenu contenu " > texte.txt


``` 
5.2. Placez le contenu du répertoire /etc dans le fichier liste2.txt (la liste doit être
ordonnée selon la taille des fichiers). Affichez le contenu du fichier liste2.txt
```bash
ls -lS ./etc > 117/117_M3/INFO1/liste2.txt

cat 117/117_M3/INFO1/liste2.txt


``` 
5.3. Placez tous les noms des fichiers, d'extension .conf, du répertoire /etc dans le
fichier liste3.txt
```bash
find /etc -type f -name "*.conf" > 117/117_M3/INFO1/liste3.txt


cat 117/117_M3/INFO1/liste3.txt


``` 

6. Affichez le contenu du répertoire courant, puis le contenu du fichier liste3.txt
```bash
cd 117/117_M3/INFO1
ls
cat 117/117_M3/INFO1/liste3.txt

``` 
7. Copiez les fichiers liste1.txt, liste2.txt et liste3.txt dans le répertoire TEMP de SHELL
```bash
cp liste1.txt liste2.txt liste3.txt SHELL/TEMP/

``` 
8. Allez dans le répertoire TEMP de SHELL, puis vérifiez son contenu
```bash
cd ./
mkdir SAINTMARC/TRAVAIL/SHELL
ls

``` 
9. Modifiez le nom de liste1.txt du répertoire courant en l'appelant file1.txt
```bash
cd SAINTMARC/TRAVAIL/SHELL
mv liste1.txt files1.txt

``` 
10. Dans le répertoire courant, dupliquez file1.txt en file11.txt, puis file12.txt, puis file13.txt
```bash
cp file1.txt file11.txt
cp file1.txt file12.txt
cp file1.txt file13.txt

``` 
11. En une seule commande SHELL, copiez les fichiers file11.txt, file12.txt et file13.txt dans le
répertoire TRAVAIL
```bash
cp file11 file12 file13 ../TRAVAIL

``` 
12. En une seule commande SHELL, copiez le fichier file1.txt dans le répertoire TRAVAIL en le
renommant fiche1.txt. Affichez le contenu du répertoire TRAVAIL
```bash
cp file11  ../TRAVAIL/fiche1.txt
ls ../TRAVAIL

``` 
13. Sans changer de répertoire courant, ajoutez dans le fichier fiche1.txt (de TRAVAIL) le
contenu du répertoire courant. Affichez le contenu du fichier fiche1.txt
```bash
ls >> ../TRAVAIL/fiche1.txt
cat ../TRAVAIL/fiche1.txt
``` 
14. Supprimez les fichiers du répertoire courant qui commencent par la lettre F
```bash
rm -r F*

``` 
15. Sans changer de répertoire courant, effacez le répertoire TRAVAIL
```bash
rm -r ../TRAVAIL


``` 
16. En une seule commande SHELL, affichez le contenu du répertoire 117 ainsi que ses sous
répertoires
```bash
tree -a

``` 
17. Fermer la session SHELL =>Tapez la commande EXIT
```bash

exit
``` 