# Connection au VPS en SSH

ssh user@x.x.x.x


cd multi-app-vps


git pull 


docker compose -f docker-compose.network.yml up -d --force-recreate

docker compose -f docker-compose.web_accueil.yml up -d --force-recreate

docker compose -f docker-compose.web_info.yml up -d --force-recreate