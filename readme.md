<div align="center">
<!-- Title: -->
  <a href="https://github.com/AstroJUS/CSCBE">
    <img src="/img/CSCBE.png" height="200">
  </a>
  <h1><a href="https://github.com/AstroJUS/CSCBE">CSCBE</a></h1>
<!-- Labels: -->
  <!-- First row: -->
 <!--  <a href="https://www.paypal.me/TheAlgorithms/100">
    <img src="https://img.shields.io/badge/Donate-PayPal-green.svg?logo=paypal&style=flat-square" height="20" alt="Donate">
  </a>-->
</div>

QUALIFIED - 18th </br> Our solution
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










