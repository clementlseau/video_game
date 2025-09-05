# Video Game / Wikipedia Analyzer

Projet pour analyser un fichier `wikipedia.json`.

## Installation

1. Cloner le projet

2. 
- Aller au root et ajouter le .env contenant la clé OPENAI.
- Aller au root/data et ajouter le fichier wikipedia.json

Depuis le root :

3. Installer [Poetry](https://python-poetry.org/docs/).

4. Run sur linux ou wsl de preference (sinon changer la 2eme ligne "source..." pour l'equivalent windows afin d'activer l'environement)
```bash
poetry install --no-root
source $(poetry env info --path)/bin/activate
poetry run python -m ipykernel install --user --name=video-game-env --display-name "video-game-env"
```

5. Lancer docker desktop on your computer (fonctionne pour windows et linux via wsl)

6. Run :
```bash
docker run -d   --name elasticsearch_video_game   -p 9200:9200   -e "discovery.type=single-node"   -e "xpack.securit
y.enabled=false"   docker.elastic.co/elasticsearch/elasticsearch:8.19.0
```

7. Ouvrir le notebook et choisir le kernel video-game dans le notebook

8. Run le notebook..