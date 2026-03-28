+-----------------------------------------------------------------------+
| **ENCG SETTAT --- UNIVERSITÉ HASSAN 1ER**                             |
|                                                                       |
| *École Nationale de Commerce et de Gestion*                           |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| **COMPTE RENDU**                                                      |
|                                                                       |
| **Analyse de la Détection de Fraude Télécom**                         |
|                                                                       |
| *Étude des CDR (Call Detail Records) --- Dataset Temps Réel*          |
+-----------------------------------------------------------------------+

  ----------------- --------------------------------- --------------------- -----------------
  **Date**          **Source**                        **Enregistrements**   **Période**

  Mai 2025          realtime_cdr_fraud_dataset.xlsx   **24 543**            Temps réel ---
                                                                            2025
  ----------------- --------------------------------- --------------------- -----------------

  -----------------------------------------------------------------------
  **ALERTE CRITIQUE : Taux de fraude de 50,2% --- Surveillance immédiate
  requise**

  -----------------------------------------------------------------------

**📋 1. CONTEXTE ET OBJECTIFS DE L\'ANALYSE**

**1.1 Contexte général**

La fraude téléphonique représente une menace croissante pour les
opérateurs de télécommunications en Afrique et dans le monde. Le présent
compte rendu documente l\'analyse approfondie d\'un jeu de données CDR
(Call Detail Records) en temps réel, portant sur 24 543 appels collectés
en mai 2025 dans sept pays africains. L\'objectif principal est
d\'identifier les patterns de fraude, de quantifier leur ampleur et de
proposer des recommandations opérationnelles.

**1.2 Périmètre de l\'étude**

-   Source de données : fichier realtime_cdr_fraud_dataset.xlsx (feuille
    principale)

-   Période d\'analyse : Mai 2025 --- données collectées en temps réel

-   Zone géographique : 7 pays africains (UG, EG, KE, ET, NG, GH, ZA)

-   Variables analysées : 14 colonnes --- identifiants, durée, type
    d\'appel, localisation, statut, type de fraude

-   Outils utilisés : Python (pandas), Excel (openpyxl), Dashboard HTML
    interactif (Chart.js)

**1.3 Questions directrices**

-   Quelle est l\'ampleur réelle de la fraude dans le dataset CDR ?

-   Quels types de fraude sont les plus fréquents et les plus dangereux
    ?

-   Existe-t-il des patterns géographiques ou temporels spécifiques ?

-   Le type d\'appel (local vs international) influence-t-il le taux de
    fraude ?

-   Quelles mesures préventives peuvent être mises en place ?

**📊 2. INDICATEURS CLÉS DE PERFORMANCE (KPIs)**

Le tableau ci-dessous synthétise les indicateurs clés extraits du
dataset CDR :

  ------------------------- --------------- ------------------------------
  **Indicateur**            **Valeur**      **Interprétation**

  Total appels analysés     **24 543**      Volume complet du dataset CDR
                                            temps réel

  Appels frauduleux         **12 320**      Dépasse les appels légitimes
                                            --- situation critique

  Appels légitimes          **12 223**      Seulement 49,8% du trafic est
                                            authentique

  Taux de fraude global     **50,2%**       **Seuil critique (norme
                                            industrie \< 5%)**

  Durée moyenne d\'appel    **163 sec**     2 min 43 sec en moyenne ---
                                            durées très variables (10s à
                                            1840s)

  Fraudes internationales   **5 807**       61% des appels internationaux
                                            sont frauduleux

  Fraudes locales           **6 513**       43% des appels locaux sont
                                            frauduleux
  ------------------------- --------------- ------------------------------

**🔍 3. ANALYSE DES TYPES DE FRAUDE**

**3.1 Répartition des types de fraude détectés**

L\'analyse du dataset révèle quatre catégories distinctes de fraude
téléphonique, réparties de manière quasi-uniforme, ce qui suggère une
diversification délibérée des techniques frauduleuses par les acteurs
malveillants.

  ---------------------- ------------ ------------ ------------ --------------
  **Type de Fraude**     **Cas        **% des      **% total    **Niveau
                         détectés**   fraudes**    CDR**        risque**

  **SIM Box Fraud**      3 096        25,1%        12,6%        **CRITIQUE**

  **Subscription Fraud** 3 089        25,1%        12,6%        **CRITIQUE**

  **Random Fraud**       3 083        25,0%        12,6%        **ÉLEVÉ**

  **Call Masking**       3 052        24,8%        12,4%        **ÉLEVÉ**

  **TOTAL FRAUDES**      **12 320**   **100%**     **50,2%**    ---
  ---------------------- ------------ ------------ ------------ --------------

**3.2 Description des types de fraude**

**SIM Box Fraud (3 096 cas) :** Technique consistant à utiliser des
passerelles SIM illégales pour router des appels internationaux comme
des appels locaux, permettant d\'éviter les frais d\'interconnexion.
C\'est le type de fraude le plus répandu dans le dataset.

**Subscription Fraud (3 089 cas) :** Utilisation d\'identités fausses ou
volées pour souscrire à des services téléphoniques. Les fraudeurs
accumulent des dettes de services sans intention de payer, causant des
pertes directes pour les opérateurs.

**Random Fraud (3 083 cas) :** Transactions frauduleuses générées de
manière aléatoire ou opportuniste, souvent liées à des tentatives de
test de cartes SIM compromises ou d\'exploitation de failles temporaires
dans les systèmes.

**Call Masking (3 052 cas) :** Manipulation de l\'identité de
l\'appelant (CLI spoofing) pour dissimuler l\'origine réelle de
l\'appel. Utilisé pour des escroqueries téléphoniques, du phishing vocal
(vishing) ou pour contourner les listes noires.

**🌍 4. ANALYSE GÉOGRAPHIQUE**

**4.1 Taux de fraude par pays d\'origine**

L\'analyse géographique révèle une distribution quasi-uniforme de la
fraude entre les 7 pays couverts, suggérant une présence systémique et
organisée plutôt qu\'une concentration géographique isolée.

  -------------------- ------------ ---------------- --------------- ------------
  **Pays**             **Total      **Frauduleux**   **Légitimes**   **Taux
                       Appels**                                      Fraude**

  🇿🇦 ZA --- Afrique du 3 452        1 770            1 682           **51,3%**
  Sud                                                                

  🇰🇪 KE --- Kenya      3 549        1 800            1 749           **50,7%**

  🇺🇬 UG --- Ouganda    3 596        1 814            1 782           **50,4%**

  🇪🇬 EG --- Égypte     3 557        1 786            1 771           **50,2%**

  🇳🇬 NG --- Nigeria    3 455        1 732            1 723           **50,1%**

  🇪🇹 ET --- Éthiopie   3 480        1 718            1 762           **49,4%**

  🇬🇭 GH --- Ghana      3 454        1 700            1 754           **49,2%**

  **TOTAL**            **24 543**   **12 320**       **12 223**      **50,2%**
  -------------------- ------------ ---------------- --------------- ------------

**4.2 Observation clé --- Uniformité géographique**

Fait marquant : les taux de fraude varient très peu entre les pays
(49,2% à 51,3%), avec un écart maximal de seulement 2,1 points de
pourcentage. Cette uniformité géographique remarquable suggère fortement
:

-   Une organisation criminelle transnationale coordonnée opérant
    simultanément dans plusieurs pays

-   L\'utilisation de techniques automatisées (bots, scripts) générant
    des CDR frauduleux de manière systématique

-   Une possible caractéristique intrinsèque du dataset de simulation
    utilisé pour la recherche

**📞 5. ANALYSE PAR TYPE D\'APPEL ET DURÉE**

**5.1 Local vs International**

  ------------------ -------------- ---------------- --------------- -----------
  **Type d\'Appel**  **Total**      **Frauduleux**   **Légitimes**   **Taux
                                                                     Fraude**

  🌐 International   9 510          **5 807**        3 703           **61,1%**

  📍 Local           15 033         6 513            8 520           **43,3%**
  ------------------ -------------- ---------------- --------------- -----------

Les appels internationaux présentent un taux de fraude de 61,1%,
significativement supérieur aux appels locaux (43,3%). Cet écart de 17,8
points confirme que le réseau international est davantage ciblé par les
fraudes de type SIM Box, dont le mécanisme consiste précisément à router
des appels internationaux de manière illicite.

**5.2 Distribution par durée d\'appel**

  ----------------- ---------------- --------------- -------------- -----------
  **Tranche de      **Frauduleux**   **Légitimes**   **Total**      **%
  Durée**                                                           Fraude**

  \< 30 secondes    3 022            1 897           4 919          **61,4%**

  30 -- 60 sec      2 688            1 548           4 236          **63,5%**

  1 -- 2 min        1 886            2 402           4 288          **44,0%**

  2 -- 5 min        2 991            4 021           7 012          **42,7%**

  5 -- 10 min       1 402            1 883           3 285          **42,7%**

  \> 10 min         331              472             803            **41,2%**
  ----------------- ---------------- --------------- -------------- -----------

Observation critique : les appels très courts (\< 60 secondes)
concentrent les taux de fraude les plus élevés (61--64%). Ce pattern est
caractéristique des fraudes automatisées (SIM Box, CLI spoofing) qui
génèrent de nombreux appels brefs pour tester la connectivité ou initier
des escroqueries. Les appels plus longs (\> 1 min) présentent des taux
de fraude plus modérés mais toujours préoccupants.

**✅ 6. CONCLUSIONS ET RECOMMANDATIONS**

**6.1 Conclusions principales**

-   Le taux de fraude global de 50,2% est 10x supérieur aux seuils
    d\'alerte habituels du secteur télécom

-   Les 4 types de fraude sont quasi-équitablement répartis, indiquant
    une diversification stratégique des attaques

-   L\'uniformité géographique (49-51% dans tous les pays) suggère une
    organisation criminelle transnationale coordonnée

-   Les appels internationaux sont proportionnellement plus frauduleux
    (61%) que les appels locaux (43%)

-   Les appels très courts (\< 60 sec) sont significativement plus
    frauduleux --- signature typique des attaques automatisées

**6.2 Recommandations opérationnelles**

**Court terme (0--3 mois) :**

-   Déployer immédiatement des filtres automatiques sur les appels
    internationaux de moins de 60 secondes

-   Implémenter un système de scoring en temps réel basé sur les
    patterns identifiés (durée, pays, heure)

-   Renforcer la vérification KYC (Know Your Customer) pour lutter
    contre la Subscription Fraud

**Moyen terme (3--12 mois) :**

-   Déployer un modèle de Machine Learning supervisé (Random Forest,
    XGBoost) entraîné sur ce dataset

-   Établir une coopération inter-opérateurs dans les 7 pays pour
    partager les listes noires de CDR

-   Mettre en place un système de détection des SIM Box via analyse des
    patterns de signalisation

**Long terme (\> 12 mois) :**

-   Adopter une architecture de détection de fraude basée sur l\'IA avec
    apprentissage continu

-   Standardiser les protocoles d\'échange de données CDR au niveau
    régional africain

-   Mettre en place un observatoire de la fraude télécom commun aux
    opérateurs partenaires

**6.3 Limites de l\'étude**

-   Le dataset couvre une période très courte (quelques secondes de
    collecte temps réel), limitant l\'analyse temporelle

-   L\'uniformité parfaite des taux par pays (49-51%) suggère que le
    dataset pourrait être simulé/synthétique

-   L\'absence de dimension temporelle étendue empêche l\'identification
    de tendances saisonnières

-   Les données d\'identité (caller_id, receiver_id) sont probablement
    anonymisées pour des raisons de conformité RGPD

+-----------------------------------------------------------------------+
| **Document produit par ENCG Settat --- Université Hassan 1er**        |
|                                                                       |
| *Analyse Fraude Télécom \| Dataset : realtime_cdr_fraud_dataset.xlsx  |
| \| Mai 2025*                                                          |
+-----------------------------------------------------------------------+
