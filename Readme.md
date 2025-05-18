# Analyse des facteurs influençant la réussite étudiante en L1

## Objectif du projet

Ce projet explore les facteurs ayant une influence sur la réussite des étudiants en première année de licence (L1), en se basant sur un échantillon d'étudiants issus des universités du Sud-Ouest de la France.  
L’objectif est d'aider les rectorats à **mieux orienter les futurs étudiants** selon leur profil en s’appuyant sur des données historiques.

---

## Description des données

- **Taille de l’échantillon** : données sur 6400 étudiants
- **Variables qualitatives** :
  - Sexe
  - Profession des parents
  - Série du BAC
  - Type de BAC
  - Mention au BAC
  - Obtention du BAC
  - Réussite en L1
- **Variable quantitative** :
  - Note en Mathématiques au BAC

---

## Analyses réalisées

### Analyse univariée
- Répartition par sexe : 39% femmes, 60% hommes
- Professions parentales majoritairement « très favorables » (40%)
- Taux de redoublement : 58% non redoublants
- Série du BAC : 70% ES, 24% S
- Type de BAC : 96% général
- Obtention du BAC : 81%
- Mention au BAC : 34% avec mention
- Notes en mathématiques : moyenne de 9,83 (écart-type : 3,96)

---

### Analyse bivariée de la réussite en L1 selon :

| Variable                          | Dépendance ? | V de Cramer | Conclusion                              |
|----------------------------------|--------------|-------------|-----------------------------------------|
| **Sexe**                         |  Oui        | 0,216       | Les femmes réussissent significativement mieux |
| **Profession des parents**       |  Non        | 0,058       | Influence négligeable                   |
| **Redoublement**                 |  Oui        | 0,265       | Les non-redoublants réussissent mieux   |
| **Série du BAC**                 |  Oui        | 0,280       | S et STT plus performants               |
| **Type de BAC**                  |  Oui        | 0,190       | Le BAC général favorise la réussite     |
| **Mention (qualité)**            |  Oui        | 0,500       | Influence forte                         |
| **Mention (obtention)**          |  Oui        | 0,490       | Influence moyenne à forte               |
| **Note en mathématiques**        |  Oui        | 0,500       | Corrélation positive                    |

Tous les tests statistiques montrent des **p-values < 2,2e-16**, sauf pour la profession des parents (p = 0,07).

---

## Visualisations & outils

- Diagrammes en barres
- Boxplots
- Tableaux croisés
- Tests : Khi², V de Cramer, test d’égalité des proportions, test de Student, test de Wilcoxon, test de Kruskal-Wallis

---

## Environnement technique

- **Langage** : R
- **IDE** : RStudio
- **Packages utilisés** : `ggplot2`, `dplyr`, `rstatix`, `vcd`, `readr`, `tidyverse`

---

## Conclusion

- **Variables significativement liées à la réussite** :
  - Sexe, type et série de BAC, redoublement, mention, notes en math
- **Variable non significative** :
  - Profession des parents (p-value = 0,07)

Les résultats mettent en évidence que certains profils (bons résultats en mathématiques, mentions au BAC, non-redoublement) **ont des chances plus élevées de réussir leur L1**. Ces analyses peuvent aider à construire des outils d’orientation plus adaptés et objectifs.

---

## Auteur

Projet réalisé par **Abderrahmane Boufares**  
boufares11@gmail.com

---

## Utilisation

```R
# Pour lancer le projet
openProject("reussite_etudiante_L1.Rproj")

# Pour installer les packages nécessaires
install.packages(c("dplyr", "ggplot2", "rstatix", "vcd", "readr", "tidyverse"))
