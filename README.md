# 🎲 Dames Chinoises en OCaml

## 📝 Description
Implémentation du jeu des **Dames Chinoises** (Chinese Checkers) en **OCaml**. Le jeu se déroule sur un plateau hexagonal en forme d'étoile où les joueurs déplacent leurs pions en effectuant des sauts simples ou multiples pour atteindre le camp adverse.

## ✨ Fonctionnalités
- Plateau hexagonal avec système de coordonnées cubiques
- Création et manipulation de configurations initiales
- Validation des coups (déplacements et sauts)
- Gestion des sauts simples et multiples (enchaînements)
- Rotation et transformation de configurations
- Support multijoueur avec gestion des couleurs

## 🎯 Règles du jeu
- Chaque joueur commence avec ses pions dans un triangle
- Objectif : déplacer tous ses pions dans le triangle opposé
- Déplacements possibles : case adjacente ou saut par-dessus un pion
- Les sauts peuvent être enchaînés

## 🔧 Technologies
- **OCaml** : Programmation fonctionnelle
- Structures de données algébriques
- Système de coordonnées hexagonales (cubiques)

## 🚀 Installation et Utilisation

### Prérequis
- OCaml installé sur votre machine

### Exécution
```bash
ocaml
#use "PROJET.ml";;
```

## 📖 Exemples d'utilisation

**Initialisation d'une configuration :**
```ocaml
let conf_1 = ([((0,0,0), Jaune)], [Jaune], 2);;
affiche conf_1;;
```

**Vérification d'un coup :**
```ocaml
let conf_reggae = ([((0,-1,1), Vert); ((0,0,0), Jaune); ((0,1,-1), Rouge)], 
                   [Vert; Jaune; Rouge], 1);;
est_coup_valide conf_reggae (Du((1, 0, -1), (1, 1, -2)));;
```

**Mise à jour après un coup :**
```ocaml
let nouvelle_config = mettre_a_jour_configuration conf_reggae 
                      (Du((0, -1, 1), (-1, -1, 2)));;
affiche nouvelle_config;;
```
