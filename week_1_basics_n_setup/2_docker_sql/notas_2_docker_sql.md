
# Eejecutar el contenedor con postgress

```
docker run -it \
  -e POSTGRES_USER="root" \
  -e POSTGRES_PASSWORD="root" \
  -e POSTGRES_DB="ny_taxi" \
  -v "$(pwd)/ny-taxi-volume:/var/lib/postgresql/data" \
  -p 5432:5432 \
  postgres:13
```

# probar conexión a postgress con la librería pgcli de python

pip install pgcli

pgcli -h localhost -p 5432 -u root -d ny_taxi

# nueva ubicación del backup con los datos de taxis

https://github.com/DataTalksClub/nyc-tlc-data

# descargar dataset

wget https://github.com/DataTalksClub/nyc-tlc-data/releases/download/yellow/yellow_tripdata_2021-01.csv.gz

# Docker compose

docker-compose up

# Docker compose -data

docker-compose up -d
docker-compose down

# ingreso a pgadmin
usuario: admin@admin.com
clave: root

# datos bd
host: pgdatabase
user: root
pass: root

#

# Crear llave

```
ssh-keygen -t rsa -f gcp -C anderson -b 2048
```

# Crear archivo config de ssh

```
vi ~/.ssh/config
```

```
Host de-zoomcamp
    Hostname <gcp-ip-instance>
    User anderson
    IdentityFile ~/.ssh/gcp
```

# Instalar docker

```
sudo apt-get update
sudo apt-get install docker.io
```

# Docker sin sudo

##### 1. Add the `docker` group if it doesn't already exist

```console
$ sudo groupadd docker
```

##### 2. Add the connected user `$USER` to the docker group

Optionally change the username to match your preferred user.

```console
$ sudo gpasswd -a $USER docker
```

**IMPORTANT**: Log out and log back in so that your group membership is re-evaluated.

##### 3. Restart the `docker` daemon

```console
$ sudo service docker restart
```

If you are on Ubuntu 14.04-15.10, use `docker.io` instead:

```console
$ sudo service docker.io restart
```

# Instalar docker compose

```
mkdir ~/bin

wget https://github.com/docker/compose/releases/download/v2.15.1/docker-compose-linux-x86_64 -O ~/bin/docker-compose

chmod +x ~/bin/docker-compose

echo "export PATH=$HOME/bin:$PATH" >> ~/.bashrc
```

