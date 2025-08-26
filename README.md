# Vitrine Boutique
Catalogue statique (Arma 3 RP) — vitrine avec photos, prix, quantités.

## 🚗 Présentation

Un site vitrine statique pour afficher les véhicules ou autres biens disponibles dans le jeu (Arma 3 RP).
Il montre **photos**, **prix**, **quantités**, et des **pastilles** (Neuf, Occasion, Promo).
Il se met à jour simplement en modifiant un fichier : **`data.json`**.

---

## 📂 Structure du projet

```
Motorsport/
│
├── index.html      ← Le site (⚠️ à ne pas modifier sans connaissances HTML)
├── data.json       ← Les données (catégories, véhicules, réglages)
└── images/         ← Toutes les images
    ├── logo/       ← Logo du site
    ├── tags/       ← Icônes pour Neuf, Occasion, Promo
    ├── sport/      ← Images des véhicules de la catégorie Sport
    ├── suv/        ← Images des SUV
    └── moto/       ← Images des motos
```

---

## ✏️ Modifier le contenu

### 1️⃣ Changer le logo

* Remplacer `images/logo/logo.png` par votre image (même nom et extension).
* PNG, JPG, WEBP… sont acceptés.

### 2️⃣ Modifier les tags (icônes Neuf, Occasion, Promo)

* Les fichiers sont dans `images/tags/`.
* Changez-les si vous voulez un autre style (même nom et extension).

### 3️⃣ Modifier les objets

* Ouvrez `data.json` → section `"vehicles"`.
* Chaque véhicule suit ce format :

```json
{
  "id": "spr-01",
  "name": "Nom du véhicule",
  "category": "sport",
  "price": 55000,
  "quantity": 5,
  "image": "images/sport/mon-vehicule.webp",
  "tags": ["Neuf"]
}
```

* **`tags`** peut être vide `[]` ou contenir `"Neuf"`, `"Occasion"`, `"Promo"` (ou plusieurs).
* **`category`** doit correspondre à l’une des catégories dans `"categories"`.

### 4️⃣ Modifier les catégories

* Dans `"categories"` de `data.json` :

```json
{ "id": "sport", "name": "Sport" }
```

* **`id`** = identifiant interne (en minuscules, sans espace).
* **`name`** = nom affiché sur le site.

---

## 🌐 Mettre à jour le site

### Si vous êtes **collaborateur** sur ce dépôt :

1. Ouvrez `data.json` dans GitHub.
2. Cliquez sur **✏️ Edit**.
3. Modifiez, puis **Commit changes**.
4. Le site se met à jour automatiquement.

### Si vous voulez **votre propre version** (fork) :

1. Cliquez sur **Fork** en haut à droite sur GitHub.
2. Activez **Settings → Pages → Deploy from a branch → main / root**.
3. Modifiez `data.json` quand vous voulez → commit → votre site est à jour.

---

## 💡 Astuces

* Les images doivent avoir des noms **sans espaces** et respecter la **casse** (majuscules/minuscules).
* Utilisez un format web optimisé (WEBP ou JPG compressé) pour accélérer le chargement.
* `lowStockThreshold` dans `settings` détermine quand un stock est affiché comme **faible**.

---

## ⚠️ À ne pas toucher

* **`index.html`** : c’est le moteur du site.
* Modifiez-le uniquement si vous savez ce que vous faites (HTML/CSS/JS).

---

## 🛠️ Technologies utilisées

* [Pico.css](https://picocss.com/) pour le style.
* [Alpine.js](https://alpinejs.dev/) pour la réactivité.
* GitHub Pages pour l’hébergement.

---

## 📜 Licence

* **Code** : libre d’utilisation personnelle (pas de licence officielle définie).
* **Images et contenus** : tous droits réservés à leurs auteurs.

