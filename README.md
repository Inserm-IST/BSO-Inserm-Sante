# Baromètre Santé Inserm de la Science Ouverte

## Présentation

Dans une démarche similaire à celle du [Baromètre de la Science Ouverte des publications de l'Inserm](https://github.com/Inserm-IST/BSO-Inserm) et du [Baromètre santé de la Science Ouverte](https://barometredelascienceouverte.esr.gouv.fr/sante) publié par le ministère de l'Enseignement supérieur et de la Recherche, l'Inserm souhaite évaluer le nombre de publications résultant des essais cliniques et des études observationnelles dont il est le promoteur.


En particulier, L'Inserm a pour objectifs :

- **Repérer les études sans publication :** Identifier les études qui n'ont donné lieu à aucune publication et tenter d'en comprendre les raisons.
- **Encourager la publication des résultats négatifs :** Promouvoir la publication des résultats d'études négatives ou peu concluantes, qui sont souvent sous-valorisés.
- **Analyser le statut d'accès des publications :** Évaluer si ces publications sont en accès ouvert ou fermé, afin de promouvoir une plus grande transparence et accessibilité.

## Organisation

Ce dépôt est structuré en plusieurs [notebooks Jupyter](https://jupyter.org/), chacun dédié à une étape spécifique du processus :

- **`01_extraction_donnees_sante.ipynb`**  
Contient le code pour l'extraction automatique des données des études, en utilisant différentes API telles que [ClinicalTrials](https://clinicaltrials.gov/), [PubMed](https://pubmed.ncbi.nlm.nih.gov/), [Unpaywall](https://unpaywall.org/products/api), et [OpenAlex](https://openalex.org/).

- **`02_traitement_donnees_sante.ipynb`**  
Permet d'analyser et d'interpréter les données des études extraites dans le notebook précédent, notamment en générant des visualisations.

- **`03_traitement_manuel_donnees_sante.ipynb`**  
Intègre les données nécessitant un traitement manuel avec celles récupérées automatiquement dans les notebooks précédents.  
À partir de cet ensemble de données, génère des statistiques et des visualisations, qui peuvent ensuite être exportées sous forme d'iframes pour une intégration dans une page web HTML.

## Installation

### Cloner le repository localement :

```bash
git clone https://github.com/Inserm-IST/BSO-Inserm-Sante.git
```

Se déplacer dans le répertoire nouvellement créé :

``` bash
cd BSO-Inserm-Sante/
```

### Créer un environnement virtuel :

**Pour plus de détails, voir [Create and Use Virtual Environments](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/)**

Créer un environnement virtuel `.venv` :

```bash
python -m venv .venv
```

Activer l'environnement virtuel :  

```bash
# Unix/macOS
source .venv/bin/activate

# Windows
.venv\Scripts\activate
```

Installer les bibliothèques dans l'environnement virtuel :

```bash
python -m pip install -r requirements.txt
```

### Lancer le notebook :

```bash
jupyter notebook
```
