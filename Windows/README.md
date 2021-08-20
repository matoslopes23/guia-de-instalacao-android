# Instalação das ferramentas no Windows

## Feramentas que você deve instalar no seu computador:
- Node.js 14 (LTS);
- Yarn 1;
- JDK 11 (LTS);
- Android Studio e dependências.

## Instalando dependências
Você precisará do Node, da interface de linha de comando React Native, de um JDK e do Android Studio.

Embora você possa usar qualquer editor de sua escolha para desenvolver seu aplicativo, você precisará instalar o Android Studio para configurar as ferramentas necessárias para construir seu aplicativo React Native para Android, porém você também pode utilizar o Expo para executar seu app e emular diretamente no celular, esta opção serve para quem tem um computador inferior.

### Node, JDK
Instale o Node via [Chocolatey](https://chocolatey.org/), um gerenciador de pacotes popular para Windows.

- Get Started
![Capturar](https://user-images.githubusercontent.com/82974806/130160616-6e1e9b63-2ae5-402c-98e0-a903929f062f.PNG)

![Capturar1](https://user-images.githubusercontent.com/82974806/130160710-be44cc5e-7c94-49e5-882c-84d14692e8f0.PNG)

Abra o Windows PowerShell em modo administrador!
![power](https://user-images.githubusercontent.com/82974806/130160979-64b2ebba-da11-4519-88d1-587c0b2eb5c9.PNG)

Agora execute o seguinte comando:
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
![Capturar](https://user-images.githubusercontent.com/82974806/130161190-9b54fd9c-17ea-48c1-a261-616bf26a6f29.PNG)
Obs: Aguarde alguns segundos para que o comando seja concluído.

Se você não encontrar nenhum erro, está pronto para usar o Chocolatey! Digite chocoou choco -?
```
choco
choco -?
```

Se você deseja alternar entre as diferentes versões do Node, pode instalar o Node por meio do nvm-windows , um gerenciador de versões do Node para Windows.

O React Native também requer o [Java SE Development Kit (JDK)](https://openjdk.java.net/projects/jdk8/), que também pode ser instalado usando o Chocolatey.

Abra um Prompt de Comando do Administrador (clique com o botão direito em Prompt de Comando e selecione "Executar como Administrador") e execute o seguinte comando:
```
choco install -y nodejs.install openjdk8
```
![Capturar3 (2)](https://user-images.githubusercontent.com/82974806/130161427-32a4b8ce-aad0-4e1d-af40-f5886b29b16e.PNG)
![Capturar4 (2)](https://user-images.githubusercontent.com/82974806/130161491-53978ff8-e2ee-42c5-9219-a61d6a9158a3.PNG)

Verifique se o Node e o NPM foram instalados com o comando:
```
none --version
npm --version
```
![Capturar5 (2)](https://user-images.githubusercontent.com/82974806/130161590-1091d486-47d1-438c-a82d-421dd67593da.PNG)

Instale o Yarn com o comando:
```
npm install -g yarn
```
![Capturar6 (2)](https://user-images.githubusercontent.com/82974806/130161701-e786c6ff-680b-41bf-b6c8-1e61918ee8ec.PNG)

Verifique se o yarn foi instalado corretamente com o comando:
```
yarn -v
```
![Capturar7 (2)](https://user-images.githubusercontent.com/82974806/130161793-d2ae8173-7422-4610-a7a5-12759e53e8b3.PNG)

## Instalando Android Studio

Acesse a página do [Android Studio](https://developer.android.com/studio?hl=pt&gclid=CjwKCAjwgviIBhBkEiwA10D2j9kYr5C2YCESgaRcB2h1dC4t6_kX4wN6l10M4ps80fCFbrrs0FM4dhoC4AYQAvD_BwE&gclsrc=aw.ds) e clique no botão Download Android Studio.
![Capturar8](https://user-images.githubusercontent.com/82974806/130161937-6c9b155b-7dd3-42ff-a025-eb16931bb6ac.PNG)

Aceite os termos:
![Capturar9](https://user-images.githubusercontent.com/82974806/130161996-c3c93c00-4e40-4d27-a4b4-18c96f658232.PNG)
Obs:
- Só assim irá iniciar o download do arquivo
- Vá até a pasta de download e abra o arquivo exe
- Esse arquivo possui uma pasta android-studio dentro. Extraia essa pasta em um local de preferência (Ex.: ~/).
![Capturar10 (2)](https://user-images.githubusercontent.com/82974806/130162161-7385f35c-6d70-4b08-9101-253f4f373538.PNG)

Dê um duplo clique no arquivo de instalação

- Vai aparecer essa tela:
- Next






![Capturar11](https://user-images.githubusercontent.com/82974806/130162253-5f964bbd-eae1-4ccc-8b6d-0a5ebb52b650.PNG)

- Next






![Capturar12](https://user-images.githubusercontent.com/82974806/130162340-f123152d-8586-452a-b3d4-40f952e897ec.PNG)

- Next






![Capturar13](https://user-images.githubusercontent.com/82974806/130162343-5a360020-2eab-4e5b-90ed-f89bd8bf49b7.PNG)

- Install






![Capturar14](https://user-images.githubusercontent.com/82974806/130162345-01cc051b-d726-4738-a60e-84b34620f8d6.PNG)

- Next






![Capturar15](https://user-images.githubusercontent.com/82974806/130162347-5998abf8-82b8-48b0-b44e-808da5ab845e.PNG)

- Finish






![Capturar16](https://user-images.githubusercontent.com/82974806/130162348-36eaba32-13bc-427c-bcdf-7663baba4de7.PNG)

- Next
![Capturar17](https://user-images.githubusercontent.com/82974806/130162350-4a8d3c17-3d07-468f-929b-01127d6d2095.PNG)

- Next
![Capturar18](https://user-images.githubusercontent.com/82974806/130162353-54551455-939c-447d-8f3a-2f4be539ac0c.PNG)

- Next
![Capturar19](https://user-images.githubusercontent.com/82974806/130162354-42572813-54c8-42bf-912a-b2eb7b7a95c1.PNG)

- Finish
![Capturar20](https://user-images.githubusercontent.com/82974806/130162355-e3dc047d-cc70-47ea-882e-60ec179f83e9.PNG)

#### Welcome to Android Studio
Configuração SDK Manager
- Passo 1: Clique no botão "More Actions"
- Passo 2: SDK Manager
![Capturar21](https://user-images.githubusercontent.com/82974806/130162946-57cbb4c3-8b2f-4478-8383-ef0cd6e01ca4.PNG)


- Passo 1: Android SDK
- Passo 2: SDK Platforms
![Capturar22](https://user-images.githubusercontent.com/82974806/130163022-89b94214-4ced-4eb2-9292-c794c692dad2.PNG)

- Passo 1: Marque a opção "Show Package Details
- Passo 2: Android 10.0(Q)
- Passo 3: Marque as opções que você vê na imagem
- Passo 4: Apply
![Capturar23](https://user-images.githubusercontent.com/82974806/130163084-205814a0-7326-4910-85b5-f43f6513e8c6.PNG)

- oK




![Capturar24](https://user-images.githubusercontent.com/82974806/130163164-1a05c4d7-b8e0-4b1b-a6c8-7df6344cc057.PNG)

- Aceite os termos
- Next
![Capturar25](https://user-images.githubusercontent.com/82974806/130163169-253e8244-35b4-4866-8484-5f818c6fe3b2.PNG)

- Apply
- Ok





![Capturar27](https://user-images.githubusercontent.com/82974806/130163171-21b5cac2-efec-45bb-a140-8edc497c28fd.PNG)

- Finish
![Capturar28](https://user-images.githubusercontent.com/82974806/130163173-d4fabb95-39cd-43e2-898a-3f524072a59d.PNG)

Configuração AVD Manager
- Passo 1: Clique no botão "More Actions"
- Passo 2: AVD Manager
![Capturar21](https://user-images.githubusercontent.com/82974806/130162946-57cbb4c3-8b2f-4478-8383-ef0cd6e01ca4.PNG)

- Create Virtual Device...
![Capturar29](https://user-images.githubusercontent.com/82974806/130163995-bcfb7051-f582-4ee9-8d98-309ba42f7e34.PNG)

- Phone
- Picel 2
- Next
![Capturar30](https://user-images.githubusercontent.com/82974806/130163999-1facef21-fab7-4933-aef9-938f92824e98.PNG)


- Q
- Next
![Capturar31](https://user-images.githubusercontent.com/82974806/130164001-345dad82-edff-4683-9b8d-72d63f8b37c4.PNG)

- AVD Name
- Next
![Capturar32](https://user-images.githubusercontent.com/82974806/130164003-f540e681-b2f0-4958-8ab9-db98092b5518.PNG)

- Máquina Virtual Criada
- Pode fechar
![Capturar33](https://user-images.githubusercontent.com/82974806/130164004-44f41118-78c2-42a6-bb5a-0d908a91a9fc.PNG)

### Configurando Variável de Ambiente
Caminho para achar a Sdk

- Abra o seu dispositivo de unidade





![Capturar34](https://user-images.githubusercontent.com/82974806/130164461-39e634ed-133b-4981-8383-65dc750b24f5.PNG)

- Entre na unidade C
![Capturar35](https://user-images.githubusercontent.com/82974806/130164530-78539a36-bd6a-4f37-8a10-bd0a56689ae1.PNG)

- Entre em usuários
![Capturar36](https://user-images.githubusercontent.com/82974806/130164624-2b086084-ae29-4fc8-a311-93e5ab899b05.PNG)

- Entre em seu perfil de usuário
![Capturar36](https://user-images.githubusercontent.com/82974806/130164738-3b40bf04-3bf8-4976-9290-748a05cc06db.PNG)

- Entre na pasta AppData
![Capturar37](https://user-images.githubusercontent.com/82974806/130164794-51d727ed-8b19-49a9-bfd9-77088f6c2e15.PNG)

- Entre em Local
![Capturar38](https://user-images.githubusercontent.com/82974806/130164871-6207930a-13e3-4763-846c-8b642f1bceac.PNG)

- Entre em Android








![Capturar39](https://user-images.githubusercontent.com/82974806/130164953-4e19e7f4-4f83-47e5-a8ce-fcb1ad69254b.PNG)

obs: Lá você encontrará uma pasta chamada SDK
![Capturar40](https://user-images.githubusercontent.com/82974806/130165174-3a397f1e-33ac-4412-a371-2b345ff4fb30.PNG)
- Entre na pasta Sdk 
![sdk](https://user-images.githubusercontent.com/82974806/130165477-ceec422b-747c-47eb-8a9a-5e87e21847ca.PNG)

- e copie o caminho dela na barra de endereços, por exemplo:
```
C:\Users\tavar\AppData\Local\Android\Sdk
```


Com o caminho da SDK copiado
Agora aperte o botão Menu iniciar do Windows e procure por:
```
Editar as variáveis de ambiente do sistema
```
Aparecerá essa tela:
- Clique em Variáveis de Ambiente





![variaves](https://user-images.githubusercontent.com/82974806/130166248-eb84dc48-1958-4773-8363-275873860c76.PNG)

- Clique em Novo
- obs: Em variáveis de usuário






![cap2](https://user-images.githubusercontent.com/82974806/130166490-a8e8db6e-a084-4a6c-a54b-b8410e5736e4.PNG)

- Acrescente o nome da Variável:
```
ANDROID_HOME
```
- Cole o caminho da Sdk
- obs: Lembrando que tem que ser o seu caminho, da sua máquina, isso aqui é só um exemplo
```
C:\Users\tavar\AppData\Local\Android\Sdk
```
- ok





![Capturar42](https://user-images.githubusercontent.com/82974806/130166667-1665225c-c43f-4b05-881b-56952f5e6995.PNG)

Ainda em Variáveis de usuário, clique em Path e em seguida editar
![Capturar43](https://user-images.githubusercontent.com/82974806/130167322-c8756917-ca8b-4bd4-82fd-153d3ed04402.PNG)

Em seguida, clique em novo e adicione o caminho padrão:
```
%LOCALAPPDATA%\Android\Sdk
```
![Capturar44](https://user-images.githubusercontent.com/82974806/130167464-c8238f2e-c23d-4505-b79e-959680a85378.PNG)

- Clique em ok e pronto!

Para finalizar, abra o seu terminal em modo adminitrador e instale o Expo-cli com o comando:
```
npm install -g expo-cli
```
![Capturar45](https://user-images.githubusercontent.com/82974806/130167827-cfa95a38-6c40-4377-9df6-909a72abbdf5.PNG)

![Capturar46](https://user-images.githubusercontent.com/82974806/130167863-a50312b8-08a8-4e84-8425-c1f8a067f569.PNG)

# Instalação e Configuração finalizada com sucesso!

