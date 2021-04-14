# AFFICHAGE EN TEMPS RÉEL DE MILLIONS D’UTILISATEURS AVEC ELIXIR ET REACT - PARTIE 1: CRÉATION DE L’API REST

## L’idée en fil rouge
L'objectif de cette partie est de construire une application pour visualiser en temps réel la position de milliers (voire millions ?) de joueurs connectés

## De quoi ai-je besoin ?
* Un serveur API Rest construit en Elixir grâce au framework Phoenix

* Une interface Client en React pour consommer notre API et afficher les joueurs sur une carte openstreet
  
  ![elixir et react](images/elixir-react.png)

# Les notions abordées dans cet article
Dans ce premier article, nous allons détailler comment mettre en place une API REST grâce à Phoenix

Les grandes étapes :
* Installation des pré-requis
* Initialisation du projet Phoenix
* Définition des schémas et contexte
* Gestion des routes, contrôleur et vues
* Ajouter des jeux de données
* Documenter son api

## Installation des pré-requis
* erlang / elixir
* une base de donnée (Postgres dans notre cas)

## Initialisation du projet Phoenix
Avant de commencer, il faut d'abord installer **elixir**<br /> [ici pour installer elixir](https://elixir-lang.org/install.html)
Utiliser la commande Phoenix pour généraer un nouveau projet
<code>mix phx.new article-elixir-midgard --app midgard  --no-webpack --no-html</code>

## Installer Postgre
Si vous n'avez pas postgré, vous pouvez l'installer à travers [Cet article](https://www.datacamp.com/community/tutorials/installing-postgresql-windows-macosx?utm_source=adwords_ppc&utm_campaignid=1455363063&utm_adgroupid=65083631748&utm_device=c&utm_keyword=&utm_matchtype=b&utm_network=g&utm_adpostion=&utm_creative=332602034358&utm_targetid=aud-299261629574:dsa-429603003980&utm_loc_interest_ms=&utm_loc_physical_ms=1012760&gclid=Cj0KCQjwpdqDBhCSARIsAEUJ0hO0u5RTbzMNzGrQNDHFjzCfIHOqXfdKLI4ulYFHnknxKVMggpPTmMIaAqHDEALw_wcB)