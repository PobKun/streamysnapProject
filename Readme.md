<b><h1>Streamysnap Service</h1></b>
sudo docker network create auth_streamysnap_network <br />
<hr />

<b><h1>DATABASE SERVICE</h1></b>
cd database <br />
sudo chmod a+rwx ./mariadb  (For Ubuntu) <br />
sudo chmod 0777 ./mariadb/data (For Ubuntu) <br />
sudo docker compose --env-file ../config/.env up -d <br />
<hr />

<b><h1>AUTH SERVICE</h1></b>
cd auth <br />
sudo docker compose --env-file ../config/.env up -d <br />
<hr />

<b><h1>FRONTEND SERVICE</h1></b>
cd frontend <br />
sudo docker compose --env-file ../config/.env up -d <br />
<hr />

<b><h4>CODE</h4></b>
golang : https://github.com/parinyapt/StreamySnap_AuthService (API Auth) <br />
docker images: https://hub.docker.com/r/pobkun/streamysnap-authservice <br />
nextjs : ... (Frontend) <br />
docker images: https://hub.docker.com/r/pobkun/streamysnap-nextservice <br />
