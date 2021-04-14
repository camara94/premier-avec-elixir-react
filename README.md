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