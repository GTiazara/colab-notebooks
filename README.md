# Colab Notebooks

Collection de notebooks Python exécutables localement avec JupyterLab ou dans Google Colab.

## Lancer le projet en local avec JupyterLab

Depuis la racine du dépôt, créez un environnement virtuel (une seule fois) :

```bash
python3 -m venv venv
```

Activez-le et installez JupyterLab, son kernel Python et les bibliothèques utilisées par le notebook :

```bash
source venv/bin/activate
python -m pip install --upgrade pip
python -m pip install jupyterlab ipykernel gdown pandas pyarrow matplotlib seaborn scipy statsmodels
python -m ipykernel install --sys-prefix --name colab-notebooks --display-name "Python (colab-notebooks)"
```

À chaque nouvelle session de travail, placez-vous à la racine du dépôt, activez le venv et lancez JupyterLab en lui donnant ce dossier comme racine :

```bash
cd /chemin/vers/colab-notebooks
source venv/bin/activate
jupyter lab --notebook-dir="$PWD"
```

Dans JupyterLab, ouvrez `IA_ING_ML0_data_analysis.ipynb` et sélectionnez le kernel **Python (colab-notebooks)** si nécessaire. Exécutez les cellules dans l’ordre. Le notebook télécharge les données dans `donnees_drive/`; le dossier Google Drive source doit être accessible par lien.

## Utiliser le notebook dans Google Colab

Ouvrez le notebook depuis le dépôt GitHub avec ce lien :

[Ouvrir IA_ING_ML0_data_analysis.ipynb dans Google Colab](https://colab.research.google.com/github/GTiazara/colab-notebooks/blob/main/IA_ING_ML0_data_analysis.ipynb)

Dans Colab, choisissez **Connecter**, puis **Exécution > Tout exécuter**. Colab utilise son propre environnement Python : le venv local n’est pas nécessaire. Les cellules d’installation du notebook installent les bibliothèques requises. Le téléchargement des données fonctionne si le dossier Drive partagé est accessible par lien; les fichiers présents sur la machine locale ne sont pas automatiquement disponibles dans Colab.
