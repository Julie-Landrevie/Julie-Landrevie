# Julie Landrevie
### Football Data & Video Analyst

*Turning football data into tactical and performance decisions.*

[![Portfolio](https://img.shields.io/badge/Portfolio-Notion-black?style=flat-square&logo=notion)](https://notion.so/julie-landrevie)
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

[![Tableau de bord](https://img.shields.io/badge/▶_Tableau_de_bord-GitHub_Pages-2a78d6?style=flat-square&logo=github)](https://julie-landrevie.github.io/womens-football-load-monitoring/)
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

## 🗂️ Tous les projets

| Projet | Description | Stack | App |
|--------|-------------|-------|-----|
| ⚖️ **Suivi de charge — football féminin** | Charge interne et externe, GPS, alertes, retour au jeu, seuils féminins — SoccerMon | R · arrow · Plotly | [Tableau de bord ↗](https://julie-landrevie.github.io/womens-football-load-monitoring/) |
| 🤖 **Assistant IA — Lois du Jeu** | RAG sur le livret IFAB 2026/27 et grille d'évaluation : 22 % → 0 % de réponses fausses avec le texte officiel | Python · BM25 · API Mistral | [Code ↗](https://github.com/Julie-Landrevie/lois-du-jeu-ia) |
| 🔍 **ScoutPro** | Scouting interactif — 6 343 joueurs sur 43 compétitions, Scout Report, percentiles | Python · StatsBomb · Streamlit | [Live ↗](https://scoutpro-football.streamlit.app) |
| 🏃 **Physical Intensity & Tracking** | Kilométrage, vitesse max, zones d'intensité — SkillCorner + Metrica Sports | Python · pandas · Plotly | [Live ↗](https://physical-tracking.streamlit.app) |
| 📊 **Tactical Dashboard** | Réseaux de passes, xG, pressing, heatmaps — StatsBomb Open Data | Python · mplsoccer · Plotly | [Live ↗](https://tactical-dashboard-football.streamlit.app) |
| 🕸️ **Pass Network & Team Structure** | Réseaux de passes, joueurs pivots par centralité | Python · NetworkX · mplsoccer | [Live ↗](https://pass-network.streamlit.app) |
| 🎯 **xG & Shooting Profile** | Qualité des tirs, shot maps, profils de finisseurs | Python · StatsBomb · mplsoccer | [Live ↗](https://xg-shooting-analysis.streamlit.app) |
| 🏆 **World Cup 2026 Predictor** | Modèle de Poisson + Monte Carlo (2 000 simulations) | Python · SciPy · Streamlit | [Live ↗](https://worldcup-2026-predictor.streamlit.app) |
| ⚽ **MPG Optimizer** | Fantasy football — programmation linéaire sous contraintes (PuLP), API MPG × FBref | Python · PuLP · Streamlit | [Live ↗](https://mpg-optimizer.streamlit.app) |

---

## 📹 Analyse Vidéo

Les projets data ne racontent qu'une partie de l'histoire.

Exemple sur **Dartfish** : codage de la finale de la Supercoupe d'Espagne (Real Madrid 2-5 FC Barcelone), positionnement du gardien sur les frappes croisées, et plan d'entraînement en 4 blocs (technique, physique, tactique, mental).

[![Vidéo](https://img.shields.io/badge/▶_Voir_l'analyse-YouTube-FF0000?style=flat-square&logo=youtube)](https://youtu.be/QwjbEjAHlig)
[![Portfolio](https://img.shields.io/badge/Détails-Portfolio_Notion-black?style=flat-square&logo=notion)](https://notion.so/julie-landrevie)

---

## 🛠️ Stack technique

```
Analyse vidéo    │ Dartfish · Once Sport · Nacsport
Programmation    │ Python · pandas · mplsoccer · Plotly · Streamlit
                 │ R · tidyverse · ggplot2 · R Markdown
IA générative    │ RAG (recherche BM25) · API Mistral · évaluation (juge automatique + relecture)
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

**[julie.landrevie@free.fr](mailto:julie.landrevie@free.fr)** · **[Portfolio complet](https://notion.so/julie-landrevie)** · **[LinkedIn](https://linkedin.com/in/julie-landrevie)**

---

<div align="center">
<sub>⚽ "Data without context is just noise. Context without data is just opinion."</sub>
</div>
