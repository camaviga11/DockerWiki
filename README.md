# DockerWiki
Configuaracion de Docker para el desarrollo de software.

## Instalacion Docker-ce

## Linux - KDE Neon -Comm

Desinstalar versiones anteriores de Docker
```shell
sudo apt-get remove docker docker-engine docker.io containerd runc
```

Actualizar los repositorios KDE Neon
```shell
sudo pkcon update
```

Actualizar los repositorios Ubuntu
```shell
sudo apt-get update
```

Instalacion de paquetes necesarios
```shell
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```

Instalar una GPG-key
```shell
sudo mkdir -m 0755 -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

Configurar el repositorio
```shell
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

Actualizar los repositorios KDE Neon
```shell
sudo pkcon update
```

Actualizar los repositorios Ubuntu
```shell
sudo apt-get update
```

Instalar Docker
```shell
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

Referencias
[Guia de instalacion de oficial de docker en Ubuntu](https://docs.docker.com/engine/install/ubuntu/)

Referencias generales
[Git Flow](https://danielkummer.github.io/git-flow-cheatsheet/index.es_ES.html)
