# Configuração do Linux Mint

## Terminator

```sudo apt install terminator```

## Insomnia 

```https://insomnia.rest/download```

## Meld

```sudo apt install meld```

## Ohmyzsh

1. ```sudo apt install zsh```
2. Acessar o site ```https://ohmyz.sh/```

## Git

```sudo apt-get install git```

### Última Versão

1. ```add-apt-repository ppa:git-core/ppa```
2. ```apt update```
3. ```apt upgrade``` ou ```apt install git```

## Java

```sudo apt-get install openjdk-8-jdk``` ou ```sudo apt-get install openjdk-17-jdk```

### Trocar versão

1. ```sudo update-alternatives --config java```
2. ```sudo update-alternatives --config javac```

## Maven

```sudo apt install maven```

Obs: Na pasta .m2 tem que configurar settings.xml, se necessário.

## Dbeaver

```https://dbeaver.io/```

## VPN

1. ```sudo apt install network-manager-vpnc```
2. ```sudo apt install network-manager-vpnc-gnome```
3. ```sudo apt install network-manager-openconnect-gnome```

## NVM(Node)

```https://github.com/nvm-sh/nvm```

### Comandos

1. ```nvm list-remote```
2. ```nvm install xxx```
3. ```nvm alias default xxx```

## Docker

```$ sudo apt update```

```
$ sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```

```
$ sudo mkdir -p /etc/apt/keyrings
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

```
$ echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

```$ sudo apt update```

```$ sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin```

```$ sudo usermod -aG docker $USER```

**Obs:** Reiniciar o computador

## Docker Composer

Verificar versão ```docker compose version```
