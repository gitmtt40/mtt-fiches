# MTT Fiches HTML Interactives

Hébergement des fiches pédagogiques interactives Move to Top 4.0 pour intégration dans LearnWorlds via External Link.

---

## Structure du repo

```
mtt-fiches/
├── README.md
├── c01a/                        # Cours C01-A (Démarrer sans conflit)
│   ├── fiche_c01a_section02_v3_external.html
│   ├── fiche_c01a_section03_v1.html
│   └── fiche_c01a_section04_v1.html
├── c01b/                        # Cours C01-B
├── c02/                         # Cours C02
├── m1/                          # Module M1
└── assets/                      # Assets partagés (si besoin)
    ├── logos/
    └── styles/
```

---

## URLs des fiches

Format : `https://[USERNAME].github.io/mtt-fiches/[COURS]/[FICHIER].html`

Exemple : `https://movetotop.github.io/mtt-fiches/c01a/fiche_c01a_section02_v3_external.html`

---

## Intégration dans LearnWorlds

### Étape 1 — Ajouter l'activité External Link

1. Course outline → Section → **Add activity**
2. Catégorie **Embed** → **External link**
3. Titre : `J'identifie mes blocages personnels: Fiche à compléter`
4. Page URL : coller l'URL GitHub de la fiche
5. **Save**

### Étape 2 — Configuration de la complétion

- Par défaut : **When visited** (immédiat)
- Recommandé MTT : **Time-Based** → 60 secondes minimum
- L'élève doit rester sur la fiche au moins 1 minute avant validation

### Étape 3 — Configuration visuelle (optionnel)

- Course settings → Course player
- Skin : **Minimal & Dark**
- Hide left path player : **ON**
- Résultat : fiche en plein écran, zéro distraction

---

## Convention de nommage

```
fiche_[code-cours]_section[N]_v[version].html

Exemples :
fiche_c01a_section02_v3_external.html
fiche_c01a_section03_v1.html
fiche_c02b_section04_v1.html
fiche_m1_section01_v1.html
```

---

## Workflow de mise à jour

### Méthode 1 — GitHub Desktop (recommandée)

1. Ouvrir GitHub Desktop
2. Modifier le fichier HTML localement
3. Commit → "Mise à jour fiche C01-A Section 02"
4. Push origin
5. **La fiche est en ligne en 30 secondes**

### Méthode 2 — GitHub Web

1. Aller sur github.com/[USERNAME]/mtt-fiches
2. Naviguer vers le fichier
3. Cliquer **Edit** (icône crayon)
4. Modifier le code
5. Commit changes
6. **La fiche est en ligne immédiatement**

---

## Standards techniques (tous les fichiers)

### BLOC 1 — localStorage unique
```javascript
const ID="mtt-c01a-s02-fiche"; // Clé unique par fiche
```

### BLOC 2 — Auto-sauvegarde
Toutes les interactions sont sauvegardées en temps réel dans le navigateur de l'élève.

### BLOC 3 — Impression PDF
Bouton en bas de page — génère un PDF propre sans barre de navigation.

### BLOC 4 — Responsive mobile
Toutes les fiches s'adaptent automatiquement aux téléphones.

---

## Maintenance

### Vérifier qu'une fiche est bien en ligne
URL de test : `https://[USERNAME].github.io/mtt-fiches/[COURS]/[FICHIER].html`

Si erreur 404 :
1. Vérifier que le fichier existe dans le repo
2. Vérifier que GitHub Pages est activé (Settings → Pages → Source: main branch)
3. Attendre 1-2 minutes après le push

### Rollback (revenir en arrière)
GitHub garde l'historique de tous les changements. Pour revenir à une version précédente :
1. Aller dans l'onglet Commits
2. Cliquer sur le commit voulu
3. View file → Copy raw contents
4. Remplacer le contenu actuel → Commit

---

## Limites techniques

| Critère | Limite GitHub Pages |
|---------|---------------------|
| Taille repo total | 1 Go |
| Taille par fichier | 100 Mo (largement suffisant pour HTML) |
| Bande passante | 100 Go/mois |
| Visites/mois | ~1 000 000 (avec fiches 100 Ko) |

**Pour MTT :** Même avec 500 fiches de 100 Ko chacune = 50 Mo total = **2% de la limite**. Aucun risque de dépassement.

---

## Support

- Documentation GitHub Pages : https://docs.github.com/pages
- Standards MTT : voir `STANDARDS_FICHES_HTML_MTT_V1.md` dans le projet principal
- Contact : [email support MTT]

---

*Repo créé par Poaty + Claude (Anthropic) — MTT 4.0 — Avril 2026*
