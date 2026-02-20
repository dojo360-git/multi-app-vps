# Lancement des stacks Docker

# 1) Creer le reseau + reverse proxy (ports 80 et 81)
docker compose -f docker-compose.network.yml up -d

# 2) Demarrer le site accueil (www)
docker compose -f docker-compose.web_accueil.yml up -d

# 3) Demarrer le site information (info)
docker compose -f docker-compose.web_info.yml up -d

# Verification
# www.app-dojo360.ovh  -> IP:80  -> accueil/index.html
# info.app-dojo360.ovh -> IP:81  -> information/index.html
# autre sous-domaine sur IP:80 -> accueil/404.html