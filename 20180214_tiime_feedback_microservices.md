# Retour d'expérience : _Microservices_

## Contexte
* From scratch Tech
* Schéma Début vs Fin
* /!\ Disclaimer : Vision Produit / Orga / Équipe

## Découpage en services
- Monolith first (only), le plus longtemps possible même si l'organisation bouge

## Loi de Conway 
* Monolith First et vite dévié vers une explosion en _micro_services, car l'organisation / l'équipe nous a contraint
* Eviter l'anticipation des problèmes => Over Engineering
* Multiplication des repos, se faire une raison, tu ne verras pas tout ce qui est développé => Importance de la communication

## Gestion des versions et Communication entre les services
- Carte d'identité du service
    - Nom (ajouté du fun, un univers particulier)
    - Ce qu'il fait, Ce qu'il ne fait pas
    - Qui le maintient ? Faut il un PM ?
    - 
- Messages (RabbitMq) : Autre paradigme de développement
- HTTP
- Les services sont censés être indépendants, difficile à assurer à cause de la communication (Messages / API)
- Consul / Docker Swarm (pas dingue)

## Tests automatisés
- Doivent être bloquant pour toute MEP
- En isolation, très simple , tout en respectant la pyramide des tests
- Pour un lot de services, les choses se compliquent
- Environnement dédié pour la CI et executable en local => /!\ temps de cycle
    + 

## Gestion des sujets de fond / transverses / Outillage
- Dette technique transverse
- Services commun
- Expérimentations
    - Equipe transverse avec objectif court terme, très précis
    - Backlog commun puis Intégration dans les sprints des squads
- Là encore la communication est importante (lib commune, conduite du changement, ...)

##  Take Away
- *Communiquer et encore communiquer pour clarifier et éviter l'over engineering* - Loi de Conway
- *Automatiser pour gagner en fiabilité / sérenité / productivité*
- *Collecter / Analyser pour anticiper / décider*

## Annexe
* Produit existant _développé__ et _maintenu_ depuis 8 ans avec +10k clients (Access, Windev, MySQL, tout sous Windows)
* Objectifs : Scale x10 + nouvelle vision (Mobile, DataScience, Renouvellement des outils internes)