NAME = backend
PORT = 8080

# Cible par défaut
ALL: RUN

# Construire l'image Docker
init:
	docker build --tag $(NAME) .

# Rebuild forcé (sans cache)
rebuild:
	docker build --no-cache --tag $(NAME) .

# Lancer le conteneur
run:
	docker run -p $(PORT):8080 $(NAME)

# Nettoyer : supprimer les conteneurs et images associées
clean:
	-docker rm -f $(shell docker ps -aq --filter "ancestor=$(NAME)") 2>/dev/null || true
	-docker rmi -f $(NAME) 2>/dev/null || true
