# Instalação do Linux Mint

Baixar a imagem no site ```https://www.linuxmint.com/download.php```

Utilizar o programa para gerar o pendriver bootável ```https://www.balena.io/etcher/```

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

**Obs:** Agora só ir em configurações de rede (próximo ao relogio) é adicionar a VPN

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

## Portainer - Gerenciador Docker

```docker volume create portainer_data```

```
docker run -d -p 9002:9000 --name portainer \
    --restart=always \
    -v /var/run/docker.sock:/var/run/docker.sock \
    -v portainer_data:/data \
    portainer/portainer-ce:latest
```

## SafeNet

1. Baixar e instalar a versao: safenetauthenticationclient_10.7.77_amd64.deb ```https://certificados.serpro.gov.br/arserpro/pages/information/drivers_token_download.jsf```

2. Instalar as dependências do Assinador SafeNet
- opensc 
- openssl 
- libengine-pkcs11-openssl 
- libccid 
- pcscd 
- pcsc-tools 
- pkcs11-data

Erro no log pjeoffice: CRYPTO/Crypto.c:258: init_openssl_crypto: Assertion `lib' failed
A versão 10.0.37 do driver SafeNet exige uma versão da libssl dentro do intervalo fixo >=0.9.8 || <=1.0.1. Porém, no Ubuntu >=20.04, a libssl está na versão 1.1. Neste caso específico, a compatibilidade não foi comprometida e é preciso "enganar" o driver para que ele encontre a biblioteca correta. Para isso, crie um link apontando para a libssl do Ubuntu:

```sudo ln -s /usr/lib/x86_64-linux-gnu/libcrypto.so.3 /usr/lib/x86_64-linux-gnu/libcrypto.so``` 

ou 

```sudo ln -s /usr/lib/x86_64-linux-gnu/libcrypto.so.1.1 /usr/lib/x86_64-linux-gnu/libcrypto.so```

## Microsoft Teams

Baixar ```https://www.microsoft.com/pt-br/microsoft-teams/download-app```

## VSCode

Baixar ```https://code.visualstudio.com/```

## Extensões

- Angular Language Service
- Color Highlight
- DotENV
- Dracula Official
- EditorConfig for VS Code
- GitLens — Git supercharged
- Git History
- JavaScript (ES6) code snippets
- Jest
- Path Intellisense
- Prettier - Code formatter
- REST Client
- Todo Tree
- TypeScript Importer
- vscode-icons
- CodeSnap
- SonarLint
- Version Lens
- Extension Pack for Java
- Spring Boot Extension Pack

## Eclipse IDE

Baixar ```https://www.eclipse.org/downloads/packages/``` 

**Obs:** Verificar a versão conforme a sua necessidade.

## PHP

1. ```sudo apt install software-properties-common```
2. ```sudo add-apt-repository ppa:ondrej/php```
3. ```sudo apt install php8.1 php8.1-bcmath php8.1-curl php8.1-gd php8.1-intl php8.1-mysql```  

## Python

```https://www.python.org/```
