# Baromètre de la Science Ouverte des études affiliées Inserm

**$${\textsf{\color{red}Version [bêta]: Travail en cours, sujet à modification}}$$**

## Presentation

Dans une démarche similaire à celle du [Baromètre de la Science Ouverte des publications de l'Inserm](https://github.com/Inserm-IST/BSO-Inserm) et du [Baromètre français de la Science Ouverte](https://barometredelascienceouverte.esr.gouv.fr/), nous souhaitons évaluer le nombre de publications résultant des essais cliniques ou des études observationnelles dont l'INSERM est le promoteur.

En particulier, nous avons pour objectifs :

- Repérer les études qui ne donnent lieu à aucune publication et tenter de comprendre les raisons de cette absence de publication.
- Identifier et encourager la publication des résultats d'études négatives.
- Analyser le statut d'accès (ouvert ou fermé) de ces publications.

## Organisation

Ce dépôt est divisé en plusieurs [notebooks Jupyter](https://jupyter.org/) :

- `01_extraction_donnees_sante.ipynb`  
Contient le code pour l'extraction automatique les données des études, en utilisant différentes API ([ClinicalTrials](https://clinicaltrials.gov/), [PubMed](https://pubmed.ncbi.nlm.nih.gov/), [Unpaywall](https://unpaywall.org/products/api) et [OpenAlex](https://openalex.org/)).

- `02_traitement_donnees_sante.ipynb`  
Permet de comprendre et interpréter les données des études extraites dans le notebook précédent, notamment en générant des visualisations.

- `03_traitement_manuel_donnees_sante.ipynb`  
Intègre les données qui ont dû faire l'objet d'un traitement manuel avec les données récupérées automatiquement dans les notebooks précédents.  
À partir de cet ensemble de données, génère des statistiques et des visualisations.

## Installation

### Cloner le repository localement :

```bash
git clone https://github.com/Inserm-IST/BSO-Inserm-Sante.git
```

Se déplacer dans le répertoire nouvellement crée :

``` bash
cd BSO-Inserm-Sante/
```

### Créer un environnement virtuel :

**Pour plus de détails, voir [Create and Use Virtual Environments.](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/)**

Créer un environnement virtuel '.venv' :

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

Installer les librairies dans l'environnement virtuel :

```bash
python -m pip install -r requirements.txt
```

### Lancer le notebook :

```bash
jupyter notebook
```
