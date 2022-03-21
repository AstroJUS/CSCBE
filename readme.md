<div align="center">
<!-- Title: -->
  <a href="https://github.com/AstroJUS/CSCBE">
    <img src="/img/CSCBE.png" height="200">
  </a>
  <h1><a href="https://github.com/AstroJUS/CSCBE">CSCBE</a></h1>
<!-- Labels: -->
  <!-- First row: -->

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










