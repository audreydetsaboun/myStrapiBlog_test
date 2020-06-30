# Strapi application

## Demande client

- un auteur peut écrire des articles
- un article peut avoir plusieurs catégories
- un article contient ses dates de création et de modifications
- un utilisateur peut filtrer les articles par catégorie (priorité)
- un utilisateur peut filtrer les articles par auteur (v2)
- les articles contiennent un titre, un chapeau et un corps
- les utilisateurs voient 2 articles proposés à la suite de l'article en cours (en se basant sur les catégories) (v3)

## Use Cases

|En tant que|Je veux pouvoir| Dans le but de| Sprint |
|---|---|---|---|
|auteur|rédiger un titre, un chapeau et un corps|écrire un article|1|
|auteur|sélectionner une ou plusieurs catégories|catégoriser les articles|1|
|auteur|consulter les dates de crea et modif||1|
|utilisateur|filtrer les articles par catégorie||1|
|utilisateur|filtrer les articles par auteur||2|
|utilisateur|voir 2 articles proposés à la suite de l'article en cours|lire d'autres article de même catégorie|3|

## MCD

AUTEUR: nom

ECRIS, 0N AUTEUR, 11 ARTICLE

ARTICLE: titre, chapeau, corps

POSSEDE, 0N ARTICLE, 0N CATEGORIE

CATEGORIE: nom

## MLD

auteur(id, nom)

article(id, titre, chapeau, contenu, #auteur(id))

categorie(id, nom)

article_has_categorie(id, #article(id), #categorie(id))