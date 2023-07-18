Les applications app_back et app_front doivent etre clone dans le meme folder 

Le lancement des 3 containers (back, front, bdd) se fait via le docker-compose.yml de l'application back 

-> cd app_back
-> docker-compose up --build 

cela lancera les 3 containers directement sans avoir besoin de passer par d'autre commande

Le User et Mdp de la base de donnee peuvent etre modifie depuis le docker-compose.yml de l'app_back  

L'application app_back se compose uniquement d'une application Symfony vide. 
L'application app_front se compose uniquement d'une application React vide. 
La base donnee MySQL se compose uniquement d'une table user constitue des attributs suivants : email, mot de passe hashe et roles. (3 users ont deja ete enregistre). 