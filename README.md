**$${\textsf{\color{red}Version [bêta]: Travail en cours, sujet à modification}}$$**

# Presentation :

Dans une démarche similaire au [Baromètre de la Science Ouverte des publications Inserm](https://github.com/Inserm-IST/BSO-Inserm) et au [Baromètre français de la Science Ouverte](https://barometredelascienceouverte.esr.gouv.fr/), on souhaite évaluer le nombre de publications qui sont le résultat d'essais cliniques ou d'études observationnelles  dont l'INSERM est le promoteur.

En particulier, on souhaite :
- Repérer les études qui ne donnent lieu à aucune publication et essayer de comprendre les raisons de cette absence de publication.
- Identifier et encourager la publication de résultats d'études négatives
- Analyser le statut d'accès (ouvert ou fermé) de ces publications

# Organisation :

Ce dépôt est divisé en plusieurs [notebooks Jupyter](https://jupyter.org/) :

- `01_extraction_donnees_sante.ipynb`  
Contient le code pour l'extraction automatique les données des études, en utilisant différentes API.

- `02_traitement_donnees_sante.ipynb`  
Comprendre et interpréter les données des études extraites dans le notebook précédent, notamment en générant des visualisations.

- `03_traitement_manuel_donnees_sante.ipynb`  
Intégrer les données qui ont dû faire l'objet d'un traitement manuel.

# Installation :

## Cloner le repository localement :

```bash
git clone https://github.com/Inserm-IST/BSO-Inserm-Sante.git
```

Ce déplacer dans le répertoire nouvellement créer :

``` bash
cd BSO-Inserm-Sante/
```

## Créer un environnement virtuel :

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
## Lancer le notebook :

```bash
jupyter notebook
```