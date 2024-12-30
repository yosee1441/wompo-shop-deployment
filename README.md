# wompo-shop-deployment
Guia rapida para instalación de Docker y Docker Compose en la VM

## Instala Docker
```bash
sudo apt update
sudo apt install -y docker.io
sudo systemctl start docker
sudo systemctl enable docker
```

## Instala Docker Compose
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/v2.21.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

## Verifica la instalación
```bash
docker --version
docker-compose --version
```

## Clonar el Repositorio
```bash
git https://github.com/yosee1441/wompo-shop-deployment.git
cd wompo-shop-deployment
```

## Configurar Variables de Entorno
```bash
# BACK
BACK_PORT=

# WOMPO
BACK_URL_BASE=
BACK_API_KEY_PUB_WOMPO=
BACK_API_KEY_PRV_WOMPO=
BACK_API_KEY_EVENTS_WOMPO=
BACK_API_KEY_INTEGRITY_WOMPO=

# DATABASE
BACK_POSTGRES_DB=
BACK_POSTGRES_USER=
BACK_POSTGRES_PASSWORD=

# FRONT
FRONT_PORT=
```

## Construir y Levantar los Contenedores
```bash
sudo docker-compose up -d --build
```
