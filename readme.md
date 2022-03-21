<div align="center">
<!-- Title: -->
  <a href="https://github.com/AstroJUS/CSCBE">
    <img src="/img/CSCBE.png" height="200">
  </a>
  <h1><a href="https://github.com/AstroJUS/CSCBE">CSCBE</a></h1>
<!-- Labels: -->
  <!-- First row: -->
  <a href="https://www.paypal.me/TheAlgorithms/100">
    <img src="https://img.shields.io/badge/Donate-PayPal-green.svg?logo=paypal&style=flat-square" height="20" alt="Donate">
  </a>
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









