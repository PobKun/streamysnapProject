### AUTH SERVICE ####
sudo docker network create auth_streamysnap_network
sudo docker compose --env-file ./config/.env up
