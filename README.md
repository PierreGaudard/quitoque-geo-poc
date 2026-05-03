# Quitoque - POC d'optimisation GEO

POC de refonte d'un article du blog Quitoque selon les bonnes pratiques GEO (Generative Engine Optimization), pour maximiser la citation par les moteurs IA (ChatGPT, Perplexity, Google AI Overviews, Gemini).

**Article de référence** : [9 recettes de grand-mère](https://www.quitoque.fr/blog/article/recettes-grand-mere-plats-traditionnels)

## Aperçu en ligne

L'article optimisé est consultable directement via GitHub Pages : `index.html`

## Les 5 piliers GEO appliqués

### 1. Title et méta description optimisés
- **Avant** : "9 recettes de grand-mère : des plats réconfortants et authentiques | Quitoque"
- **Après** : "Recettes de grand-mère : 9 plats traditionnels faciles à cuisiner | Quitoque"
- La nouvelle formulation place le mot-clé principal en début et reste descriptive.

### 2. Answer-First (les 300 premiers mots)
Ajout d'un encart "Réponse rapide" en début d'article qui répond directement à la question principale en 3-5 phrases, avec liste structurée des 9 recettes par catégorie. Ce format est massivement extrait par les LLMs lors de la génération de réponses.

### 3. FAQ structurée GEO
Ajout d'une section FAQ avec 6 questions fréquentes et leurs réponses synthétiques :
- Qu'est-ce qu'une recette de grand-mère ?
- Quels sont les plats traditionnels français les plus emblématiques ?
- Comment réussir un hachis parmentier maison ?
- Quels ingrédients de base pour la cuisine traditionnelle ?
- Combien de temps faut-il pour cuisiner un plat de grand-mère ?
- Comment recevoir les ingrédients pour cuisiner ces recettes ?

Chaque question est intégrée dans un schema markup `FAQPage` (JSON-LD), ce qui multiplie par 3 les chances d'être citée par les moteurs IA.

### 4. Tableaux comparatifs et blocs d'info
- Tableau récapitulatif des 9 recettes (catégorie, temps, difficulté, nombre de personnes), idéal pour les requêtes comparatives
- Encarts "Ingrédients clés" et "L'astuce de grand-mère" pour chaque recette, en formats extractibles

### 5. Listes à puces et structure extractible
- Sommaire cliquable au début (table des matières)
- Liste des ingrédients en bullet points pour chaque recette
- Liste des arguments Quitoque en bullet points dans le CTA
- Conversion des paragraphes denses en formats structurés

## Schema.org JSON-LD ajoutés

- `Article` (avec author, datePublished, image, publisher)
- `FAQPage` (les 6 Q/R en format extractible)
- `BreadcrumbList` (fil d'Ariane structuré)

## Structure des fichiers

```
quitoque-geo-poc/
├── index.html       # Article optimisé GEO
├── style.css        # CSS clean inspiré de la palette Quitoque
└── README.md        # Ce fichier
```

## Gain attendu

L'optimisation GEO appliquée à cet article devrait :
- Augmenter la probabilité de citation dans les réponses ChatGPT, Perplexity, Google AI Overviews
- Améliorer le CTR organique grâce au schema markup (FAQ visibles dans les SERP)
- Réduire le bounce rate grâce à la structure Answer-First
- Augmenter la conversion blog → panier grâce au CTA enrichi et au maillage interne

## Méthodologie de déploiement à grande échelle

Cette approche peut être généralisée à l'ensemble du blog Quitoque (1000+ articles) via :
1. Un template GEO appliqué aux articles existants
2. Un audit de cannibalisation pour fusionner les doublons sémantiques
3. L'enrichissement saisonnier des contenus (Noël, Saint-Valentin, BBQ été, etc.)
4. L'intégration systématique d'une FAQ et d'un encart Answer-First sur chaque template article

---

POC réalisé par datashake dans le cadre de l'audit SEO + GEO Quitoque.
