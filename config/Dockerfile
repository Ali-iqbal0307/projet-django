# Utiliser l'image officielle de Python
FROM python:3.10


# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier requirements.txt séparément (Optimisation Docker)
COPY requirements.txt .

# Installer les dépendances
RUN pip install --no-cache-dir -r requirements.txt

# Copier tous les fichiers du projet dans le conteneur
COPY . .

# Exposer le port 8000 (Django)
EXPOSE 8000

# Commande pour démarrer le serveur Django
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
