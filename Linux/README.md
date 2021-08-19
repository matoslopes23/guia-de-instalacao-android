#  Guia de Instalação no Linux
## Dependências
### Para configurar o ambiente Android no Linux, iremos realizar 4 instalações principais:

- Node.js 14 (LTS);
- Yarn 1;
- JDK 11 (LTS);
- Android Studio e dependências

## Ubuntu
Certifique-se que você tenha o cURL instalado executando o seguinte comando no terminal:
```
sudo apt-get install curl
```
![1](https://user-images.githubusercontent.com/82974806/130141905-e81068a4-7c97-4af4-b357-f0f9d57272f3.png)

### Instalando Node.js 14 (LTS)
Nesse tutorial, iremos ensinar como instalar o Node.js 14 (LTS) diretamente utilizando o cURL. Caso queira usar um package manager, você poder utilizar o nvm.

#### Agora com o cURL instalado, vamos instalar o Node.js 14 (LTS) utilizando os seguintes comandos:
OBS: Se você já tiver o Node.js instalado em sua máquina, certifique-se que sua versão é a 12 ou mais recente.

```
curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
sudo apt-get install -y nodejs
```
![2](https://user-images.githubusercontent.com/82974806/130142122-ecce66b9-060c-4229-a0a0-1b740a835155.png)

![3](https://user-images.githubusercontent.com/82974806/130142197-1640a150-8d56-434f-a2bb-6d3dffe89bb1.png)

Após a instalação, verifique se ela foi realizada com sucesso com os comandos (execute um de cada vez):
```
node -v
npm -v
```
![4](https://user-images.githubusercontent.com/82974806/130142293-b94e9297-648a-44d2-9690-cc5da8c323ec.png)

### Instalando Yarn 1
Execute o comando para instalar o Yarn:
```
sudo npm install --global yarn
```

```
yarn -v
```

![yarn](https://user-images.githubusercontent.com/82974806/130142880-9ab4c563-e7c0-4a45-8562-e2b337b3d244.png)

### Instalando JDK 11 (Java Development Kit)
#### Agora precisamos instalar a JDK (Java Development Kit) na versão 11 (LTS mais recente) com o seguinte comando:
OBS: Se você já tiver o JDK instalado em sua máquina, certifique-se que sua versão seja a 8 ou mais recente.
```
sudo add-apt-repository ppa:openjdk-r/ppa
sudo apt-get update
sudo apt-get install openjdk-11-jdk
```
![6](https://user-images.githubusercontent.com/82974806/130143114-c07cfdad-8148-4c79-a1ff-e8d320e01050.png)

Podemos testar a instalação do JDK com o seguinte comando:
```
java -version
```
![7](https://user-images.githubusercontent.com/82974806/130143169-b455e110-c1e8-4124-a703-c87098d0d6f8.png)

OBS: Caso possua outras versões do java, pode selecionar a versão 11 como padrão usando o comando:
```
sudo update-alternatives --config java
```

## Preparativos para usar o Android Studio

### Crie uma pasta em um local desejado para instalação da SDK. Ex: ~/Android/Sdk
Obs:Anote esse caminho para ser utilizado posteriormente

#### Obs: Anote também o endereço de instalação do JDK 11. Exemplo:
```
/usr/lib/jvm/java-11-openjdk-amd64
```

#### Verificar caminho Java:
Obs: Caso você não saiba!
```
sudo update-alternatives --config java
```
![caminhojava](https://user-images.githubusercontent.com/82974806/130145008-442e3e3a-12f4-4f64-b18c-62657b09ea77.png)

- Copie o caminho do Java
- Edite o arquivo .bashrc:
```
sudo gedit ~/.bashrc
```
![bashrc](https://user-images.githubusercontent.com/82974806/130145504-04753697-2a78-4459-8b91-982ef47859ce.png)

### Obs: Esse comando irá fazer com que abra um editor de texto. Não mude nada!
### Apenas acrescente essas novas variáveis de ambiente no final do arquivo que irá abrir!

```
export JAVA_HOME=CAMINHO_ANOTADO_COM_SUA_VERSÃO
export ANDROID_HOME=~/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
```
![variaveis](https://user-images.githubusercontent.com/82974806/130145699-28b54e9f-2940-464f-a988-21f5538a78d4.png)

### Obs: Não esqueça de substituir o valor na linha JAVA_HOME pelo caminho que você anotou anteriormente. Além disso, caso esteja utilizando uma pasta diferente para a SDK do Android, altere acima.

## Instalando Android Studio

Acesse a página do [Android Studio](https://developer.android.com/studio?hl=pt&gclid=CjwKCAjwgviIBhBkEiwA10D2j9kYr5C2YCESgaRcB2h1dC4t6_kX4wN6l10M4ps80fCFbrrs0FM4dhoC4AYQAvD_BwE&gclsrc=aw.ds) e clique no botão Download Android Studio.

![8](https://user-images.githubusercontent.com/82974806/130147400-cc3a67f6-1e61-484e-8e70-6e41c963d93f.png)

#### Aceite os termos:
![9](https://user-images.githubusercontent.com/82974806/130147554-c0e752a0-0a1f-4564-9a93-3822650109e0.png)
### Obs: Só assim irá iniciar o download do arquivo
#### Vá até a pasta de download e abra o arquivo tar.gz.
#### Esse arquivo possui uma pasta android-studio dentro. Extraia essa pasta em um local de preferência (Ex.: ~/).

### Após a extração, adicione a seguinte variável ambiente no seu sistema:
```
export PATH=$PATH:~/android-studio/bin
```
#### Obs: Edite o arquivo .bashrc novamente
A adição desse caminho possibilita a execução do Android Studio diretamente pelo terminal com o comando studio.sh. Caso tenha extraído em uma pasta diferente ou alterado o nome da pasta, ajuste o path acima para o que você utilizou.

#### Agora, abra o terminal (reinicie se já estiver aberto) e execute o seguinte comando:
```
studio.sh
```
### Caso não funcione, abra o Android Studio seguindo os seguintes passos:
- Abra um terminal na pasta bin
#### obs: No meu caso, o meu caminho ficou assim: ~/Apps/android-studio-2020.3.1.23-linux/android-studio/bin

- Pasta bin:
Entre nela
![1](https://user-images.githubusercontent.com/82974806/130149020-95205ea6-8dd0-4383-819d-4d3b65861e30.png)

- Dentro da pasta bin, abra um terminal
![2](https://user-images.githubusercontent.com/82974806/130149129-23fd9df7-03f6-47a1-a094-0bda857ee32b.png)

- Terminal pasta bin:
![bin](https://user-images.githubusercontent.com/82974806/130149338-e97b8ced-2a53-40ee-a4e6-57e3ad32fe94.png)

#### Liste todos arquivos que existem na pasta bin com o comando:
```
ls -la
```
![ls-la](https://user-images.githubusercontent.com/82974806/130149814-163a6c6d-a591-407f-961b-99a8957c0c59.png)

#### Execute o Android Studio com o comando:
```
./studio.sh
```
![sh](https://user-images.githubusercontent.com/82974806/130150079-7ed2fd96-71a2-4b52-ae61-48bf0709f655.png)

### Configurando o Android Studio
- Segue os prints

- Send usage statistics to Google
![3](https://user-images.githubusercontent.com/82974806/130150993-4c9f8c9b-3cc6-43af-820d-dd971da9c262.png)

- Next
![4](https://user-images.githubusercontent.com/82974806/130150985-46e91605-4e12-4f0e-ac9d-999e08691e29.png)

- Next
![5](https://user-images.githubusercontent.com/82974806/130150987-5db1a34e-c627-4390-a400-5b9620cd2cdc.png)

- Next
![6](https://user-images.githubusercontent.com/82974806/130150995-fac79b18-749f-4edc-96ed-e6486bd9abf8.png)

- Next
![8](https://user-images.githubusercontent.com/82974806/130150990-c1a43f1e-4796-4af6-bde2-8d66b6fbbe52.png)

- Next
![9](https://user-images.githubusercontent.com/82974806/130151467-874e6a1e-16ed-4a2a-9dce-8c8b6ec669bd.png)

- Finish
![7](https://user-images.githubusercontent.com/82974806/130151000-66c1c5af-f105-4720-a7f8-61c894eb7787.png)

#### Welcome to Android Studio
![studio](https://user-images.githubusercontent.com/82974806/130151690-37116563-4fcd-4cef-9e3b-bd163c0667b1.png)

#### Configuração SDK Manager
- Passo 1: Clique no botão "More Actions"
- Passo 2: SDK Manager

- Passo 1: Android SDK
- Passo 2: SDK Platforms
![10](https://user-images.githubusercontent.com/82974806/130152263-551fe35e-11eb-41d0-b5e5-bf679ea2bb64.png)

- Passo 1: Marque a opção "Show Package Details
- Passo 2: Android 10.0(Q)
- Passo 3: Marque as opções que você vê na imagem
- Passo 4: Apply
![11](https://user-images.githubusercontent.com/82974806/130152272-b2c5668b-00f5-4597-aabc-fea10bbe1b57.png)

- Ok





![12](https://user-images.githubusercontent.com/82974806/130152292-e3fa62a9-a0db-406e-98b6-21101d8ebb48.png)

- Aceite os termos
- Next
![13](https://user-images.githubusercontent.com/82974806/130152303-784c8694-5a2b-4da7-830d-1119a6dc8b01.png)

- Finish
![14](https://user-images.githubusercontent.com/82974806/130152314-b1812c2c-5d29-476c-9692-246dfc9a613c.png)

- SDK Tools
- Marque a opção 29.0.2
![15](https://user-images.githubusercontent.com/82974806/130152333-d4de94da-81a3-4910-9a5b-79410108876b.png)

- Ok





![16](https://user-images.githubusercontent.com/82974806/130152356-522b1e1b-3176-4dd0-a435-faddcae3cebd.png)

- Finish
![17](https://user-images.githubusercontent.com/82974806/130152367-83a27d2d-c4f9-40bb-aa95-d79a68a8a71a.png)

- Apply
- Ok
![18](https://user-images.githubusercontent.com/82974806/130152384-c94ef62a-5723-4907-89bd-91467063e458.png)

#### Welcome to Android Studio
![studio](https://user-images.githubusercontent.com/82974806/130151690-37116563-4fcd-4cef-9e3b-bd163c0667b1.png)

#### Configuração AVD Manager
- Passo 1: Clique no botão "More Actions"
- Passo 2: AVD Manager

- Create Virtual Device...
![19](https://user-images.githubusercontent.com/82974806/130153517-49190fcb-ef90-4ed6-ac52-a444ded8a168.png)

- Phone
- Picel 2
- Next
![20](https://user-images.githubusercontent.com/82974806/130153532-fea1d6f6-8719-4384-ac89-dca0e621bf81.png)

- Q
- Next
![21](https://user-images.githubusercontent.com/82974806/130153540-66849983-7f8c-4ff7-8ab2-86765f63c61d.png)

- AVD Name
- Next
![22](https://user-images.githubusercontent.com/82974806/130153548-eb8a53c9-bee2-4784-9066-53caf1b45ab4.png)

- Máquina Virtual Criada
- Pode fechar
![23](https://user-images.githubusercontent.com/82974806/130153557-804e10a7-02eb-4580-9a3b-9a6b44aa86f1.png)

# Instalação e Configuração finalizada com sucesso!!
