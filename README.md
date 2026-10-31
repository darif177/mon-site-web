# FD TECH — Site vitrine + veille technologique

Site web statique (HTML / CSS / JS, sans dépendance ni build) pour un studio
d'IA, avec une section **Veille technologique** qui regroupe des liens vers
88 sites de référence (IA, développement, cybersécurité, actualités,
constructeurs tech, open source).

## Lancer le site

Double-clique simplement sur `index.html`, ou ouvre-le dans ton navigateur :

```
C:\Users\AbdelkarimDarif\Desktop\nexa-ai\index.html
```

Aucune installation, aucun serveur nécessaire.

## Structure

```
nexa-ai/
├── index.html            # Tout le contenu (hero, services, veille, contact…)
└── assets/
    ├── css/style.css     # Design, thèmes clair/sombre, responsive
    └── js/main.js        # Menu, animations, filtres, formulaire
```

## Fonctionnalités

- Design sombre / clair (bouton en haut à droite, choix mémorisé)
- Menu mobile, navigation active au scroll, barre de progression
- Animations d'apparition, compteurs animés
- Section **Veille** : filtres par catégorie + recherche instantanée
- FAQ dépliante
- Formulaire de contact avec validation en français
- 100 % responsive, accessible au clavier, respect de `prefers-reduced-motion`

## Ajouter un site à la veille

Dans `index.html`, duplique une carte `<a class="link-card">` et modifie :

```html
<a class="link-card"
   data-cat="dev"                              <!-- ia | dev | cyber | actu | tech | open -->
   data-search="mots clés pour la recherche"   <!-- mots-clés cachés -->
   href="https://exemple.com"
   target="_blank" rel="noopener noreferrer">

  <span class="link-card__logo" style="--lg1:#8b5cf6;--lg2:#5b21b6">EX</span>
  <span class="link-card__body">
    <span class="link-card__top">
      <strong>Nom du site</strong>
      <span class="link-card__cat">Dev</span>
    </span>
    <span class="link-card__desc">Courte description du site.</span>
    <span class="link-card__url">exemple.com</span>
  </span>
  <svg class="link-card__arrow" viewBox="0 0 24 24"><path d="M7 17 17 7M8 7h9v9"/></svg>
</a>
```

Les compteurs des filtres se mettent à jour automatiquement : rien d'autre à faire.

## Personnaliser

- **Nom / logo** : remplace `FD TECH` dans `index.html` (header + footer).
- **Couleurs** : variables `--accent`, `--accent-2`, `--accent-3` et `--grad`
  en haut de `assets/css/style.css`.
- **Textes** : tout est directement dans `index.html`.
- **Formulaire** : l'envoi est simulé dans `assets/js/main.js`
  (cherche `Simulation d'envoi`). Branche un service comme Formspree, Netlify
  Forms ou ton API pour recevoir les messages.
- **Coordonnées** : email, téléphone et adresse dans la section `#contact`.

## Mettre en ligne

Le site étant statique, tu peux le déposer tel quel sur :

- **Netlify / Vercel** : glisser-déposer le dossier `nexa-ai`
- **GitHub Pages** : pousser le dossier dans un dépôt puis activer Pages
- **N'importe quel hébergement** (OVH, Hostinger…) : envoyer les fichiers par FTP

Pense à remplacer le domaine `WEBMASTER@HIGHTECH.EDU` et les liens sociaux
(`#` dans le footer) par tes vraies informations avant la mise en ligne.
