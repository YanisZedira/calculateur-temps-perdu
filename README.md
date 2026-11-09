# Calculateur du temps perdu

Un calculateur en une seule page HTML, sans dépendance, pour estimer ce que les tâches répétitives coûtent chaque année à une petite entreprise : devis, relances, ressaisie, prise de rendez-vous.

**Essayer : [yaniszedira.github.io/calculateur-temps-perdu](https://yaniszedira.github.io/calculateur-temps-perdu/)**

Le calcul se fait dans le navigateur. Aucune donnée n'est envoyée, aucun cookie n'est posé.

## Ce qu'il calcule

| Résultat | Formule |
|---|---|
| Heures par an | minutes par tâche × fois par semaine × semaines travaillées ÷ 60 |
| Jours par an | heures par an ÷ 7 |
| Coût par an | heures par an × coût horaire chargé |

Par défaut : 47 semaines travaillées (52 moins les congés payés) et 35 euros de coût horaire chargé. Les six tâches de départ sont des exemples à remplacer.

Le résultat est un ordre de grandeur. Toutes les heures comptées ne se récupèrent pas : une automatisation en reprend une partie, et il reste un temps de contrôle.

## L'utiliser sur votre site

**En cadre intégré**, le plus simple :

```html
<iframe src="https://yaniszedira.github.io/calculateur-temps-perdu/"
        title="Calculateur du temps perdu" loading="lazy"
        style="width:100%;height:900px;border:0"></iframe>
```

**En copie**, pour l'adapter : téléchargez `docs/index.html`, qui contient le style et le script. Les tâches de départ sont dans le tableau `DEFAULTS` en bas du fichier :

```js
var DEFAULTS = [
  ['Rédiger et envoyer des devis', 20, 5], // libellé, minutes, fois par semaine
];
```

Les couleurs sont des variables CSS en tête de fichier, avec une version sombre automatique.

## Pourquoi ce calcul

Avant d'automatiser, il faut savoir ce qui coûte. Dans une petite structure, les tâches les plus chères sont rarement les plus pénibles : ce sont celles qui reviennent dix fois par semaine. Ce calculateur sert à les classer, pas à promettre un gain.

- La version d'origine, avec la méthode détaillée : [calculateur sur yz-automation.fr](https://yz-automation.fr/calculateur-temps-perdu).
- Ce qu'une automatisation coûte réellement : [prix d'une automatisation en entreprise](https://yz-automation.fr/ressources/blog/prix-automatisation-entreprise-2026).
- [Checklist SEO local](https://github.com/YanisZedira/checklist-seo-local) : 40 points pour une entreprise locale.
- [llms-txt-generator](https://github.com/YanisZedira/llms-txt-generator) : générer un fichier llms.txt à partir d'un sitemap.

## Licence

MIT. Écrit par Yanis Zedira, fondateur de [YZ Automation](https://yz-automation.fr), qui conçoit des sites, des agents IA et des automatisations pour les PME.
