Documentation -- Déploiement Cockpit & Nextcloud
Services installés
Ce serveur a été configuré avec deux services principaux : - Cockpit : Interface web d'administration du serveur. - Nextcloud : Plateforme de gestion et partage de fichiers, déployée via Docker.

1. Cockpit
Description
Cockpit est une interface web permettant de superviser et administrer le serveur : - Monitoring système (CPU, RAM, stockage...) - Gestion des services - Logs - Mise à jour du système - Gestion des sessions et utilisateurs

Déploiement effectué
Installation du paquet cockpit
Démarrage du service
Activation automatique au démarrage
Ouverture du port 9090
Accès
"http:10.0.108.86:9090"
2. Nextcloud (avec MariaDB)
Description
Nextcloud est une plateforme cloud auto‑hébergée pour stocker, synchroniser et partager des fichiers.

Déploiement via Docker Compose "docker-compose.yml"
L'installation inclut : - Un conteneur MariaDB (base de données) - Un conteneur Nextcloud - Deux volumes persistants :\

db_data → données MariaDB\
nextcloud_data → fichiers Nextcloud
Accès
"http:10.0.108.86:8080"
Résumé
Service Type Port Statut

Cockpit Admin Web 9090 Actif Nextcloud Cloud Web 8080 Actif MariaDB Base SQL --- Actif

Auteur
OMAR TALIBI.
