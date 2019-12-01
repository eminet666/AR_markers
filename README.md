PROCEDURE INSTALLATION SERVEUR HTTPS DE TEST

1_NODEJS
- télécharger à partir de : https://nodejs.org/en/
- Installer le package (mac : applications->Utilitaires->Terminal)
- ouvrir terminal
- taper node -v pour vérifier l’installation
- taper npm - v pour vérifier installation npm

2_INSTALLER HTTP-SERVER
- regarder la page : https://www.npmjs.com/package/http-server
- dans le terminal, taper la commande : sudo npm install http-server -g
- démarrer le serveur http-server

3_INSTALLER NGROK
- regarder la page : https://www.npmjs.com/package/ngrok
- dans le terminal, taper la commande : sudo npm install --unsafe-perm -g ngrok
(npm install -g ngrok sur windows)
- démarrer le serveur ngrok http 8080

Vérifier l'installation des packages npm / http-server / ngrok en tapant la commande : npm list -g --depth=0
Arrêter les 2 fenêtres

Télécharger le zip, le décompresser.

4_DEMARRER EMULATION SERVEUR
- se déplacer dans le répertoire …/markers/test_patterns (*)
- relancer le server http-server
- puis exposer localhost  ngrok http 8080
- copier dans le presse-papier l’adresse générée en https
( par exemple : https://2080cc21.ngrok.io)
- tester l’adresse ci dessus dans un navigateur

5_CREER UN NOUVEAU MARKER
- utiliser l’outil à l’adresse : https://jeromeetienne.github.io/AR.js/three.js/examples/marker-training/examples/generator.html
- importer la photo en 512px, générer le fichier pattern, l’image et le PDF à imprimer.
- copier le fichier pattern dans le répertoire test/marker/patterns
- mettre à jour le nom du pattern dans le fichier index.html

6_ TESTER LA RECONNAISSANCE AR
- entrer l’adresse : https://2080cc21.ngrok.io/index.html
(dans la barre d’adresse d’un navigateur _ ne marche pas sur chrome avec un iPhone)
- vérifier que le fichier pattern a bien été chargé dans la fenêtre ngrok (sinon cela ne marchera pas !)

+ CREATION D’UN QR CODE (détection automatique avec appareil photo iPhone)
- dans le répertoire QR_code, lancer le fichier generate.html puis cliquer sur le lien ‘recommencer’
- entrer l’adresse https://2080cc21.ngrok.io/index.html

(*) pour ouvrir un shell/terminal directement à partir d'un dossier de l'explorateur(pc) ou du finder (mac)
- pc : taper shift+ clic droit dans le dossier, selectionner "ouvrir la fenetre PowerShell ici"
- mac : il faut d'abord une configuration dans les "préférences système" :
      -> clavier -> onglet raccourci -> liste : Services
      -> cliquer sur "nouveau terminal au dossier" puis affecter un raccourci, par exemple "ctrl+alt+cmd+T"
      dans le Finder, cliquer dans le répertoire choisi et taper le raccourci !
