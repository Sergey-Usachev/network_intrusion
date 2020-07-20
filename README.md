# Détection d'intrus

![intrusion](https://github.com/vperrinfr/network_intrusion/blob/master/images/intrusion.png)

Cher joueur, vous revenez de recevoir cet email.

## Email

Bonjour,

Nous avons régulièrement des attaques sur notre réseau informatique. Mais aujourd'hui, nous savous qu'un espion a eu accès 
à un de nos sites. Nous avons besoin de votre aide. Nous avons récuperer les informations sur les trames pour chacun des 4 sites.
Pourriez vous nous dire sur quel site se trouve l'espion ? 

Notre équipe IT vous a exporté un fichier d'historique de connexion provenant de notre IDS (Intrusion Dectection System).
Nos sites ouvrent dans 10 minutes, une nouvelle intrusion de l'espion pourrait nous couter cher.

La situation étant sensible, les sites sont référencés par leurs noms de code: Alpha, Bravo, Charlie, Delta

Pour info, il semblerait qu'il existe une solution d'automatisation de conception de modèle de Machine Learning qui fasse des merveilles: [IBM AutoAI](https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/autoai-overview.html)

Merci d'avance de votre discrétion

Bonne chance on compte sur vous...

## Fichiers

Historique de log: [données analysée](https://github.com/vperrinfr/network_intrusion/blob/master/data/Train_data.csv)

Les trames à évaluer: 

- Alpha: [0,"tcp","http","SF",233,2239,0,0,0,0,0,1,0,0,0,0,0,0,0,0,0,0,3,3,0,0,0,0,1,0,0,255,197,0.77,0.02,0,0,0,0,0,0]

- Bravo: [31,"tcp","telnet","SF",197,1608,0,0,0,1,0,1,1,0,0,1,2,1,0,0,0,0,1,1,0,0,0,0,1,0,0,248,32,0.13,0.03,0,0,0,0,0,0]

- Charlie: [0,"tcp","systat","S0",0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,239,20,1,1,0,0,0.08,0.07,0,255,20,0.08,0.08,0,0,1,1,0,0]

- Delta: [0,"tcp","http","SF",277,4968,0,0,0,0,0,1,0,0,0,0,0,0,0,0,0,0,13,13,0,0,0,0,1,0,0,13,255,1,0,0.08,0.01,0,0,0,0]

## Post-Analyse

Il vous faut ensuite saisir dans l'interface le nom du site.












