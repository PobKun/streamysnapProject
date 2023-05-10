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