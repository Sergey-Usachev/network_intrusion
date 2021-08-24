# Обнаружение нарушителя

![intrusion](https://github.com/Sergey-Usachev/network_intrusion/blob/master/images/intrusion.png)

Уважаемый участник, вы вернулись и получили это письмо.

## Email

Привет,

У нас регулярно происходят атаки на нашу компьютерную сеть. Но сегодня мы знаем, что шпион получил доступ к одному из наших сайтов. Нам нужна твоя помощь. Мы получаем информацию о фреймах для каждого из 4 сайтов. Не могли бы вы сказать нам, на каком сайте находится шпион?

Наша ИТ-команда экспортировала вам файл истории подключений из нашей IDS (системы обнаружения вторжений). Наши сайты открываются через 10 минут, повторное вторжение со стороны шпиона может дорого обойтись.

В связи с деликатной ситуацией сайты упоминаются под кодовыми названиями: Alpha, Bravo, Charlie, Delta.

Заранее благодарим вас за ваше усмотрение

Удачи, мы на тебя рассчитываем ...

## Fichiers

Historique de log: [données analysée](https://github.com/vperrinfr/network_intrusion/blob/master/data/Train_data.csv)

Les trames des différents sites à évaluer: 

- **Alpha** : 0,"tcp","http","SF",233,2239,0,0,0,0,0,1,0,0,0,0,0,0,0,0,0,0,3,3,0,0,0,0,1,0,0,255,197,0.77,0.02,0,0,0,0,0,0

- **Bravo** : 31,"tcp","telnet","SF",197,1608,0,0,0,1,0,1,1,0,0,1,2,1,0,0,0,0,1,1,0,0,0,0,1,0,0,248,32,0.13,0.03,0,0,0,0,0,0

- **Charlie** : 0,"tcp","systat","S0",0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,239,20,1,1,0,0,0.08,0.07,0,255,20,0.08,0.08,0,0,1,1,0,0

- **Delta** : 0,"tcp","http","SF",277,4968,0,0,0,0,0,1,0,0,0,0,0,0,0,0,0,0,13,13,0,0,0,0,1,0,0,13,255,1,0,0.08,0.01,0,0,0,0

## Pour commencer

Aller dans l'interface Watson Studio, les données ont été uploadés dans le projet **Network_Intrusion_XX**

[Indice 1](https://github.com/vperrinfr/network_intrusion/blob/master/indice1.md)

[Indice 2](https://github.com/vperrinfr/network_intrusion/blob/master/indice2.md)

## Post-Analyse

Il vous faut ensuite saisir dans l'interface le nom du site.
