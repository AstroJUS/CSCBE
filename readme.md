<div align="center">
<!-- Title: -->
  <a href="https://github.com/AstroJUS/CSCBE">
    <img src="/img/CSCBE.png" height="200">
  </a>
  <h1><a href="https://platform.cybersecuritychallenge.be/scoreboard">CSCBE</a></h1>
<!-- Labels: -->
  <!-- First row: -->
 <!--  <a href="https://www.paypal.me/TheAlgorithms/100">
    <img src="https://img.shields.io/badge/Donate-PayPal-green.svg?logo=paypal&style=flat-square" height="20" alt="Donate">
  </a>-->
</div>

</br> Our solution
## ROTERDAM

</br><img src="/img/1.png"></br>
Connaissant l’erreur 400 et son message, on détermine un décalage de césar de 13.
On obtient:
</br><img src="/img/2.png"></br>
On peut donc utiliser burpSuite pour envoyer nos requêtes HTTP codées en rot 13.
Cette requête qu’on envoie :
</br><img src="/img/3.png"></br>
Devient alors:
</br><img src="/img/4.png"></br>
On reçoit une réponse:
</br><img src="/img/5.png"></br>
On la déchiffre pour que le navigateur la comprenne et on obtient ce formulaire sur le navigateur:
</br><img src="/img/6.png"></br>
On répond “10”, on chiffre la requête POST toujours en césar, et finalement le serveur nous répond avec cette requête déchiffrée:
</br><img src="/img/7.png"></br>

## REVERSE ME 101

</br><img src="/img/8.png"></br>
</br><img src="/img/9.png"></br>
</br><img src="/img/10.png"></br>

## REVERSE ME LUATIC

String du file, on obtient un long calcul qu’on exécute sur pycharm et il nous sort un ensemble de chiffre :
(67, 83, 67, 66, 69, 123, 84, 101, 115, 116, 95, 76, 117, 97, 95, 79, 98, 102, 117, 115, 99, 97, 116, 111, 114, 125)
On convertit cet ensemble de nombre en hexadécimal ce qui nous donne
43 53 43 42 45 7b 54 65 73 74 5f 4c 75 61 5f 4f 62 66 75 73 63 61 74 6f 72 7d
et on convertit ces chiffre en ASCII et nous obtenons le flag

## PikaPad

J’ai d’abord installé un émulateur android, installé l’app et nous avons vu que l’app nous demandait un code à 6 chiffres.

Nous avons d’abord cherché le “Main activity” de l’app et j'ai trouvé ce code.
</br><img src="/img/11.png"></br>
Nous avons analysé le code et trouve la connection comme suit :
</br><img src="/img/12.png"></br>
Nous rentrons donc le code : 274169 et l’app nous donne donc le flag

## Hideout
On ouvre le fichier pcap avec wireshark et on extrait les object http.
</br><img src="/img/13.png"></br>
On ignore le rick roll
</br><img src="/img/13.5.png"></br>
Et on save le fichier ci-dessous:
</br><img src="/img/14.png"></br>
Ce fichier contient un pastebin qui contient le flag
</br><img src="/img/15.png"></br>

## Over 9000

Nous avons installé l'appli sur votre machine virtuelle, nous devons cliquer sur les sangoku pour obtenir + de 9000 points sauf que les points bloquent à 7612, nous essayons donc de modifier les valeurs grâce à “Game Guardian”

C’etait bien ca la solution, nous avons modifié les values to 9001 et nous obtenons le flag

## headers masters

Pour réussir ce challenge nous devions modifier les http header, voici les header que nous avons utilisé
referer: reddit.com
X-Forwarded-For: 10.13.37.0
Authorization: Basic YWRtaW46YWRtaW4=
Date: Wed, 21 Oct 1900 07:28:00 GMT
nous avons également utilisé user-agent switcher avec l’user agent :Mozilla/5.0 (CrKey armv7l 1.5.16041) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/31.0.1650.0 Safari/537.36 et nous recevons donc le flag

## Unstable Serial Killer

C’est un fichier logic 2
Faut analyser les fréquences, le flag était dedans en ASCII, un peu facile, il fallait juste savoir qu’un fichier .sal était utilisé par logic 2

## Telemaze

Il faut coder une appli qui communique avec le netcat et qui résout le labyrinthe.
Exemple d’un essai qui a fonctionné :
</br><img src="/img/16.png"></br>
La réponse était “UURDRURRRDLDRRRDLLLDU”
</br><img src="/img/17.png"></br>
Aperçu du code
</br><img src="/img/18.png"></br>

## Complex encoding

Grâce au module codext on trouve que le texte de base est de la base 62 ce qui donne :
begin 666 <data>
M'XL( /H^)V("__-)SBB-<O7*+#;,K8PL\/ H\C#UR2LP= H)C0@-RZ\*"P@M
M\"T-\*@(#\]V\<A,*R^W\"@I,W9Q-,LU\8XR=$XM*TYR3PG,2G)+RO P#_'.
?"LRJS#)US0X(KPJH<$U.J@P(<TGR  #3A(K<90

end

On convertit ce résultat en fichier binaire grâce à http://uuencode.online-domain-tools.com/

On l’ouvre en .zip et on obtient un fichier texte qui contient “LchuZEJis1myYpHHrH5Lnp1BTUXUVozVPUpMuPHxWWkDHifww8Htv3DA6m4KZ1CevsbGdQjbFbhH7TKjQjyj5EkPWzPxEcbyPVDbH”
C’est de la base58 qui donne “D712273346274386F54713F53733B643D6F53727339743C6F533C6071347C657D6B7343534 	
”.
Ce qui mène vers une impasse, mais un programme à été capable de crack ce dernier cipher, c’est “Ciphey”.

</br><img src="/img/19.png"></br>

Ce qui donne le flag après plusieurs cycles.
Key or Pin ?
On upload le fichier sur [CyberChef](https://gchq.github.io/CyberChef/)
</br><img src="/img/20.png"></br>
On choisit le “Xor bruteforce” en mettant qu’on connaît la chaîne “csc”.

## Vault

Nous recevons un fichier “vault” en l’ouvrant, nous trouver une string “upx” donc je suppose que le fichier est crypté avec un upx packer, avec ce tool : https://github.com/upx/upx

Avec la commande upx -d vault, notre fichier est décrypte, ensuite je constate que le fichier est un fichier “ELF” qui est un fichier source, je l’ouvre avec IDA, j’ai essayé avec x64dbg au debut mais ca fonctionnait pas, avec IDA je trouve la fonction main_main et c’est là que tout se passe, voici qque screen. 

</br><img src="/img/21.png"></br>

Et en fait, le mot de passe github et discord étaient des phrases “troll” en base 64, alors que les encadrés en rouge, étaient le flag, il fallait xor chaque phrase avec la clé qui était “C” et ca nous donnait le flag. 

## Near future

Nous avons un fichier challenge.exe, nous le decompilon avec instxractor : https://github.com/extremecoders-re/pyinstxtractor
pour obtenir des fichiers, nous trouvons challenge.pyc qui est un fichier python compile, nous utilisons donc un decompiler, decompyle3 :
https://pypi.org/project/decompyle3/
Ce qui nous donne donc le code python en clair.
Voici le code python non modifié. 

</br><img src="/img/22.png"></br>
Et la date, en hash, était la date du 2077-10-12 (référence a cyberpunk je suppose ?)
Nous modifions donc le code comme suit, et le code nous donne le flag





