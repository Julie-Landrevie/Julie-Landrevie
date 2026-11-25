# Julie Landrevie
### Football Data & Video Analyst

*Turning football data into tactical and performance decisions.*

[![Site](https://img.shields.io/badge/Portfolio-julie--landrevie.github.io-0d8f84?style=flat-square)](https://julie-landrevie.github.io/)
[![Notion](https://img.shields.io/badge/Détails-Notion-black?style=flat-square&logo=notion)](https://notion.so/julie-landrevie)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Julie_Landrevie-0A66C2?style=flat-square&logo=linkedin)](https://linkedin.com/in/julie-landrevie)
[![Email](https://img.shields.io/badge/Email-julie.landrevie%40free.fr-EA4335?style=flat-square&logo=gmail)](mailto:julie.landrevie@free.fr)

---

## Qui je suis

Après plus de 4 ans en cabinet de conseil, dont une mission pour les **Jeux Olympiques Paris 2024**, je me reconvertis vers l'analyse data, vidéo et performance dans le football.

Ce n'est pas un virage à 180°. C'est la même logique : **comprendre des systèmes complexes, extraire ce qui compte, et le rendre actionnable**. Sauf qu'aujourd'hui, le terrain de jeu c'est un rectangle vert et les 22 joueurs et joueuses qui s'y déplacent.

Certifiée en **Sports Analytics** (Université du Michigan) et **Analyse Vidéo & Data dans le Sport** (Université de Lorraine), je travaille à la fois le code (Python, R, StatsBomb, SkillCorner, GPS) et la vidéo (Dartfish et Once Sport certifiée ; Nacsport en cours).

> Ce qui me distingue : je fais les deux. Data **et** vidéo. Chiffres **et** images. C'est rare — et c'est délibéré.

---

## ⭐ Projet phare — Suivi de charge en football féminin d'élite

> **Le travail quotidien d'un sport scientist, de la donnée brute au tableau de bord du staff.**

Pipeline R complet de monitoring de la charge interne et externe sur deux saisons de deux équipes féminines de première division norvégienne (données ouvertes **SoccerMon** : 50 joueuses, questionnaires quotidiens et 10 075 fichiers GPS à 10 Hz, ~99 Go).

- **Contrôle qualité d'abord** : un jour sans déclaration y vaut 0 (repos et oubli indiscernables) → aucune alerte sous 70 % de jours documentés
- **Alertes utilisables par un staff** : de ~1 jour sur 5 en alerte à 13–16 épisodes par joueuse et par an
- **Ratio et valeurs absolues** : pour un même ACWR de 0,8, la charge aiguë varie de 189 à 379 UA/jour ; dans 94 % des pics de course à haute intensité, l'ACWR sRPE reste sous le seuil
- **Retour au jeu** : reprise progressive après une absence individuelle (59 % → 76 % → 100 % en 3 semaines), 148 % de la charge d'avant dès la 1re semaine après une coupure collective, profil accélération-vitesse en séance (Morin et al.)
- **Seuils féminins** (SkillCorner) : 67 % des journées avec du sprint au-dessus de 23 km/h, contre 44 % avec le seuil masculin de 25 km/h

**Stack :** R · tidyverse · ggplot2 · arrow · R Markdown · JavaScript · Plotly · GitHub Pages

[![Tableau de bord](https://img.shields.io/badge/▶_Tableau_de_bord-GitHub_Pages-0d8f84?style=flat-square&logo=github)](https://julie-landrevie.github.io/womens-football-load-monitoring/)
[![Code](https://img.shields.io/badge/Code-GitHub-181717?style=flat-square&logo=github)](https://github.com/Julie-Landrevie/womens-football-load-monitoring)

---

## 🤖 Projet IA — Assistant sur les Lois du Jeu, avec évaluation

> **Un modèle de langage répond-il mieux avec le texte officiel ? Et comment le mesurer ?**

Assistant de questions-réponses sur le livret **IFAB 2026/27** (276 pages) : découpage du PDF par loi avec contrôle qualité, recherche documentaire (RAG, BM25 codé à la main), génération via l'API Mistral avec citation obligatoire de la loi. Surtout, une **grille d'évaluation sur 40 questions** : exactitude, bonne loi citée, refus justifiés, rappel de la recherche, relecture humaine des cas contestés.

- **Sans le livret** : 22 % de réponses fausses, alors que le modèle cite une loi dans 97 % des cas (exemple : l'ancienne règle des 6 secondes pour le gardien)
- **Avec le livret** : aucune réponse fausse ; nouveautés 2026/27 traitées 3 fois sur 3 (0 sur 3 sans)
- **v1 → v2** : l'analyse des erreurs désigne la recherche comme maillon faible ; une fois corrigée, 94 % de réponses exactes (81 % en v1) et 3 % de refus (19 % en v1)
- **Juge automatique contrôlé** : les 3 verdicts « faux » étaient démentis à la relecture dans le texte officiel

**Stack :** Python · pypdf · BM25 · API Mistral · unittest (17 tests)

[![Code](https://img.shields.io/badge/Code_et_résultats-GitHub-181717?style=flat-square&logo=github)](https://github.com/Julie-Landrevie/lois-du-jeu-ia)

---

## 📏 Vestiaire — seuils féminins et outil de suivi pour les staffs

> **Les seuils de sprint masculins cachent-ils des joueuses ?**

Les seuils de vitesse publiés par **SkillCorner** (sprint > 23 km/h, accélération > 2,7 m/s² chez les femmes ; 25 km/h et 3 m/s² chez les hommes) appliqués aux GPS de SoccerMon. Les seuils sont ceux de SkillCorner ; les calculs sur SoccerMon sont les miens.

- **43 % → 15 %** des séances de match sans aucun sprint, seuils masculins puis féminins
- **16 → 69 m** de sprint par match (médiane)
- **0,96** de corrélation de rang entre les deux classements : le gain est individuel, l'ordre des joueuses change peu
- Prototype d'outil de suivi pensé pour un staff

**Stack :** Python · pandas · unittest

[![Code](https://img.shields.io/badge/Code_et_résultats-GitHub-181717?style=flat-square&logo=github)](https://github.com/Julie-Landrevie/vestiaire-metrics)

---

## ⚖️ Comparer les joueuses à opportunités égales

> **Le classement d'une joueuse change-t-il quand on tient compte de son temps de jeu, de la possession de son équipe et de ses adversaires ?**

634 matchs de quatre championnats féminins 2023/24 (WSL, Frauen-Bundesliga, Liga F, Serie A — StatsBomb Open Data).

- **×1,33** de pressions par minute pour une remplaçante, comparée à elle-même titulaire sur la même fenêtre de match (200 joueuses)
- **34 %** des joueuses changent nettement de rang en pressions quand on passe du « par 90 » au « par possession adverse »
- Application pour comparer deux joueuses selon la normalisation choisie

**Stack :** Python · pandas · bootstrap · Streamlit · Altair · pytest

[![App](https://img.shields.io/badge/▶_Application-Streamlit-0d8f84?style=flat-square&logo=streamlit)](https://womens-football-opportunity.streamlit.app)
[![Code](https://img.shields.io/badge/Code-GitHub-181717?style=flat-square&logo=github)](https://github.com/Julie-Landrevie/womens-football-opportunity)

---

## 🔬 Trois études courtes sur le football féminin

Trois questions, un même dépôt, des intervalles de confiance à chaque fois (StatsBomb Open Data).

| Étude | Question | Résultat clé |
|-------|----------|--------------|
| **Phases arrêtées** | Le football féminin dépend-il davantage des coups de pied arrêtés ? | Non : 39,8 % du xG hors penalty des deux côtés (écart 0,0 point, IC 95 % −1,3 à +1,3). La définition retenue pèse plus que le genre (17 % → 50 %) |
| **Penalties** | Où tirent les joueuses, avec quelle réussite ? | 45 % visent le bas à droite de la gardienne ; 60,9 % de réussite en séance de tirs au but contre 76,2 % en match |
| **Fiabilité des statistiques** | Combien de minutes avant qu'une statistique par 90 soit fiable ? | 22 statistiques sur 24 fiables sur une saison de WSL ; les contres demandent 2 026 minutes. Aussi fiables que chez les hommes à minutes égales |

**Stack :** Python · pandas · bootstrap · intervalles de Wilson · Spearman-Brown · pytest

[![Code](https://img.shields.io/badge/Code_et_résultats-GitHub-181717?style=flat-square&logo=github)](https://github.com/Julie-Landrevie/etudes-football-feminin)

---

## 🗂️ Tous les projets

| Projet | Description | Stack | App |
|--------|-------------|-------|-----|
| ⚖️ **Suivi de charge — football féminin** | Charge interne et externe, GPS, alertes, retour au jeu, seuils féminins — SoccerMon | R · arrow · Plotly | [Tableau de bord ↗](https://julie-landrevie.github.io/womens-football-load-monitoring/) |
| 📏 **Vestiaire** | Seuils de sprint féminins (SkillCorner) sur les GPS SoccerMon : 43 % → 15 % de matchs sans sprint | Python · pandas | [Code ↗](https://github.com/Julie-Landrevie/vestiaire-metrics) |
| ⚖️ **Opportunités égales** | Classer les joueuses par minute, par possession, par fenêtre de match — 4 championnats féminins | Python · Streamlit · Altair | [Live ↗](https://womens-football-opportunity.streamlit.app) |
| 🔬 **Trois études courtes** | Phases arrêtées, penalties, fiabilité des statistiques en football féminin | Python · bootstrap · pytest | [Code ↗](https://github.com/Julie-Landrevie/etudes-football-feminin) |
| 🤖 **Assistant IA — Lois du Jeu** | RAG sur le livret IFAB 2026/27 et grille d'évaluation : 22 % → 0 % de réponses fausses avec le texte officiel | Python · BM25 · API Mistral | [Code ↗](https://github.com/Julie-Landrevie/lois-du-jeu-ia) |
| 🔍 **ScoutPro** | Scouting interactif — 6 343 joueurs (compétitions masculines), percentiles par groupe de postes, Scout Report | Python · StatsBomb · Streamlit | [Live ↗](https://scoutpro-football.streamlit.app) |
| 🏃 **Physical Intensity & Tracking** | Kilométrage, vitesse max, zones d'intensité — SkillCorner + Metrica Sports | Python · pandas · Plotly | [Live ↗](https://physical-tracking.streamlit.app) |
| 📊 **Tactical Dashboard** | Réseaux de passes, xG, pressing, heatmaps — StatsBomb Open Data | Python · mplsoccer · Plotly | [Live ↗](https://tactical-dashboard-football.streamlit.app) |
| 🕸️ **Pass Network & Team Structure** | Réseaux de passes, joueurs pivots par centralité | Python · NetworkX · mplsoccer | [Live ↗](https://pass-network.streamlit.app) |
| 🎯 **xG & Shooting Profile** | Qualité des tirs, shot maps, profils de finisseurs | Python · StatsBomb · mplsoccer | [Live ↗](https://xg-shooting-analysis.streamlit.app) |
| 🏆 **World Cup 2026 Predictor** | Modèle de Poisson + Monte Carlo (2 000 simulations) | Python · SciPy · Streamlit | [Live ↗](https://worldcup-2026-predictor.streamlit.app) |
| ⚽ **MPG Optimizer** | Fantasy football — programmation linéaire sous contraintes (PuLP), API MPG × FBref | Python · PuLP · Streamlit | [Live ↗](https://mpg-optimizer.streamlit.app) |

---

## 📹 Analyse Vidéo

Les projets data ne racontent qu'une partie de l'histoire.

**Once Sport** : 96 actions codées sur le résumé de Manchester City – PSG, avec mon propre panneau de codage (40 types d'actions, 9 zones).

**Tennis de table** : finale des Championnats de France 2025 codée point par point dans Dartfish (151 points) — 62 % des points du vainqueur gagnés en coup droit, 91 % au 7e set.

**Dartfish** : codage de la finale de la Supercoupe d'Espagne (Real Madrid 2-5 FC Barcelone), positionnement du gardien sur les frappes croisées, et plan d'entraînement en 4 blocs (technique, physique, tactique, mental).

[![Vidéo](https://img.shields.io/badge/▶_Voir_l'analyse-YouTube-FF0000?style=flat-square&logo=youtube)](https://youtu.be/QwjbEjAHlig)
[![Portfolio](https://img.shields.io/badge/Détails-Portfolio-0d8f84?style=flat-square)](https://julie-landrevie.github.io/)

---

## 🛠️ Stack technique

```
Analyse vidéo    │ Dartfish · Once Sport · Nacsport
Programmation    │ Python · pandas · mplsoccer · Plotly · Streamlit
                 │ R · tidyverse · ggplot2 · R Markdown
IA générative    │ RAG (recherche BM25) · API Mistral · évaluation (juge automatique + relecture)
Statistiques     │ bootstrap · intervalles de Wilson · Spearman-Brown · Poisson · Monte Carlo
Sources data     │ StatsBomb · SkillCorner · Metrica Sports · SoccerMon (GPS) · FBref
Environnement    │ Jupyter · Git · VS Code · GitHub Pages
```

---

## 🎓 Certifications

- 🎓 **Sports Analytics** — University of Michigan (Coursera)
- 🎓 **Analyse Vidéo & Data dans le Sport** — Université de Lorraine
- ✅ **Dartfish Certified Analyst**
- ✅ **Once Sport Certified** 
- 🔨 **Nacsport Certified** *(en cours)*

---

## 📬 Me contacter

Je suis ouverte à toute opportunité en **data analyst**, **data / IA appliquée au sport**, **analyste vidéo**, **sport science** ou **scout data** — club, agence, éditeur de données ou fédération.

**[julie.landrevie@free.fr](mailto:julie.landrevie@free.fr)** · **[Portfolio](https://julie-landrevie.github.io/)** · **[Notion](https://notion.so/julie-landrevie)** · **[LinkedIn](https://linkedin.com/in/julie-landrevie)**

---

<div align="center">
<sub>⚽ "Data without context is just noise. Context without data is just opinion."</sub>
</div>
