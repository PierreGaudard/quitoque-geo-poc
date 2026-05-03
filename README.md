# Quitoque - POC Optimisation GEO

POC qui démontre l'ajout d'éléments GEO (Generative Engine Optimization) dans un article du blog Quitoque, **sans toucher au reste du contenu ni au design original**.

**Article de référence** : [9 recettes de grand-mère](https://www.quitoque.fr/blog/article/recettes-grand-mere-plats-traditionnels)

## Aperçu en ligne

L'article avec les éléments GEO est consultable directement via GitHub Pages.

## Principe

Le HTML, le CSS et la structure originale du blog Quitoque sont conservés à l'identique. Seuls **4 éléments GEO ont été injectés** pour maximiser la citation par les moteurs IA (ChatGPT, Perplexity, Google AI Overviews, Gemini).

## Les 4 éléments GEO ajoutés

### 1. Encart "En bref" (Answer-First)
- **Position** : début de l'article, juste avant la section "Les entrées de grand-mère"
- **Style** : bandeau vert clair avec bordure verte à gauche
- **Contenu** : réponse synthétique à la question principale + liste structurée des 9 recettes par catégorie
- **Objectif** : les LLMs extraient en priorité ce qui est en haut de l'article et formaté comme une réponse directe

### 2. Tableau récapitulatif des 9 recettes
- **Position** : juste après l'encart "En bref"
- **Contenu** : recette / catégorie / temps / difficulté / nombre de personnes
- **Objectif** : les tableaux comparatifs sont massivement repris par les LLMs lors de requêtes de type "comparer", "quel est le meilleur...", "liste de..."

### 3. Liste à puces "Les ingrédients incontournables"
- **Position** : juste après le tableau, avant la première section recette
- **Style** : encart crème avec liste sur 2 colonnes
- **Contenu** : 8 ingrédients de base de la cuisine traditionnelle
- **Objectif** : les listes structurées sont parfaitement extractibles par les moteurs IA et améliorent la lisibilité pour le lecteur

### 4. FAQ classique
- **Position** : fin de l'article, juste avant le formulaire de newsletter Quitoque
- **Contenu** : 6 questions/réponses sur les recettes de grand-mère
- **Schema markup JSON-LD `FAQPage`** intégré dans la page
- **Objectif** : les FAQ avec schema markup sont 3x plus citées par les moteurs IA. Elles déclenchent aussi l'affichage des Q/R dans les SERP Google classiques

## Pourquoi cette approche

L'article actuel du blog Quitoque génère un trafic massif mais n'est pas optimisé pour la nouvelle vague des moteurs IA. Avec l'arrivée de ChatGPT Search, Perplexity et Google AI Overviews, le SEO classique ne suffit plus pour rester visible.

Ce POC démontre qu'on peut intégrer 4 éléments GEO efficaces sans dégrader l'expérience de lecture, en respectant la charte graphique existante.

## Structure des fichiers

```
quitoque-geo-poc/
├── index.html       # Article original + 4 éléments GEO injectés
├── assets/          # Tous les fichiers CSS, JS, images du blog Quitoque
├── .nojekyll        # Désactive Jekyll pour servir les fichiers en statique
└── README.md        # Ce fichier
```

## Différences vs la version Conversion

Ce POC est complémentaire au repo `quitoque-conversion-poc` :
- **`quitoque-conversion-poc`** : ajout de CTAs visuels pour pousser à la conversion vers les paniers
- **`quitoque-geo-poc`** (ce repo) : ajout d'éléments structurels pour optimiser la citation par les moteurs IA

Les deux approches peuvent être combinées en production sur le même article.

## Bonus inclus

- Schema markup JSON-LD `FAQPage` (extractible par les moteurs IA)
- Listes à puces structurées (formats favorisés par les LLMs)
- Tableau comparatif (extractible)
- Encart Answer-First en début de page

---

POC réalisé par datashake dans le cadre de l'audit SEO + GEO Quitoque.
