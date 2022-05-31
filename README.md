# karuta-translations
_Keep Karuta translations up to date._

Le principe est le suivant :
1. nous partons du fichier `locale_en.js` contenant les clefs et chaines en __anglais__ à traduire,
2. il est tout d'abord transformé en un fichier `locale_en.xml`, respectant le format [Android](https://support.crowdin.com/file-formats/android-xml/), par l'outil [karuta2xml](https://github.com/eduquenoy/translation-tools),
3. le fichier `locale_en.xml` peut ensuite être envoyé sur la plate-forme de traduction collaborative [Crowdin](https://crowdin.com/project/karuta-eporfolio) via un dépôt Github,
4. une fois les traductions dans différentes langues effectuées, [Crowdin](https://crowdin.com/project/karuta-eporfolio) permet de les déposer automatiquement, sur le même dépôt Github mais sur une nouvelle branche sous la forme d'une série de fichiers `locale_*.xml` (un fichier par langue),
5. les fichiers `locale_*.xml` doivent ensuite être transformés en leur correspondant `locale_*.js`, au format demandé par Karuta et ceci grâce à l'outil [xml2karuta](https://github.com/eduquenoy/translation-tools),
6. il reste à incorporer les `locale_*.js` au dépôt [Karuta](https://github.com/karutaproject/karuta-frontend/tree/master/WebContent/karuta/js/languages).

Voici une description graphique du processus :

![Description du processus](https://eric.duquenoy.org/wp-content/uploads/2022/05/TraductionsKaruta.svg)