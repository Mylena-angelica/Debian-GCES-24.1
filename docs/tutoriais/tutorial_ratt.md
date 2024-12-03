
# Guia para Executar o `ratt` no Ubuntu e Debian

Este guia descreve o processo passo a passo para configurar e executar o `ratt` no Ubuntu e Debian, utilizando os repositórios do Debian Sid apenas para fontes específicas de pacotes.

## Etapa 1: Adicionar o Debian Sid ao `/etc/apt/sources.list`

Os repositórios do Debian Sid contêm as versões mais recentes de pacotes que podem ser necessárias em situações específicas. Para habilitá-los:

1. Abra o arquivo `/etc/apt/sources.list` no seu editor preferido (ex.: `nano`):

    ```bash
    sudo nano /etc/apt/sources.list
    ```

2. Adicione as seguintes linhas ao final do arquivo, ajustando a arquitetura conforme necessário (por exemplo, `amd64`, `arm64`):

    ```plaintext
    deb [arch=ARCH] http://deb.debian.org/debian sid main
    deb-src [arch=ARCH] http://deb.debian.org/debian sid main
    ```

    Substitua `ARCH` pela arquitetura apropriada para os pacotes que você deseja instalar.

3. Salve o arquivo e saia do editor.

---

## Etapa 2: Configurar Preferências do Apt (Pinning)

Para evitar atualizações acidentais do sistema para o Debian Sid, configure as preferências do `apt`:



1. Execute o comando `apt policy` para verificar a prioridade dos seus repositórios de download de pacotes.

O repositório do Debian deve parecer com isso:

```bash
   $ apt policy | grep debian

  500 http://deb.debian.org/debian sid/main amd64 Packages
     origin deb.debian.org

```

Obs: Talvez apareçam outros repositórios Debian, principalmente se sua distro for baseada no debian, tome cuidado para não confundí-las com a Debian Sid recém adicionada

2.  Crie um novo arquivo em `/etc/apt/preferences.d/debian-sid`:

    ```bash
    sudo nano /etc/apt/preferences.d/debian-sid
    ```

3. Adicione o seguinte conteúdo:

    ```plaintext
    Package: *
    Pin: origin deb.debian.org
    Pin-Priority: 50
    ```
  ⚠️ Note que a origin aqui é a mesma apontada pelo `apt policy`.
   Isso garante que os pacotes do Sid só sejam instalados quando especificados explicitamente.

4. Salve o arquivo e saia do editor.


5. Atualize seus pacotes e execute novamente o comando apt policy para checar se o pin funcionou

```bash
sudo apt update
apt policy | grep debian

# Dessa vez o output esperado seria esse
50 http://deb.debian.org/debian sid/main amd64 Packages
     origin deb.debian.org
```


---

## Etapa 3: Atualizar as Listas de Pacotes

Execute o comando abaixo para atualizar as listas de pacotes:

```bash
sudo apt update
```

Se encontrar erros relacionados a chaves GPG, siga a próxima etapa para resolvê-los.

---

## Etapa 4: Adicionar Chaves GPG Ausentes

Os repositórios do Debian Sid podem exigir chaves GPG específicas para verificação. Caso o comando `sudo apt update` relate chaves ausentes (por exemplo, `0E98404D386FA1D9` e `6ED0E7B82643E131`), adicione-as manualmente:

1. Usando `apt-key`:

    ```bash
    sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 0E98404D386FA1D9 6ED0E7B82643E131
    ```

2. Alternativamente, usando `wget`:

    ```bash
    # Adicionar a primeira chave
    wget -qO - https://ftp-master.debian.org/keys/archive-key-12.asc | sudo tee /etc/apt/trusted.gpg.d/debian-archive-key-12.asc
    
    # Adicionar a segunda chave
    wget -qO - https://ftp-master.debian.org/keys/archive-key-13.asc | sudo tee /etc/apt/trusted.gpg.d/debian-archive-key-13.asc
    ```

3. Atualize novamente as listas de pacotes:

    ```bash
    sudo apt update
    ```

   Certifique-se de que não haja erros e que o repositório do Sid esteja disponível para as fontes necessárias.

---

## Etapa 5: Instalar e Executar o `ratt`

Instale o `ratt` 

```bash
sudo apt install ratt
```


Execute o `ratt` conforme necessário para seu caso de uso. Normalmente ele será com o arquivo `.changes` que possui a arquitetura do seu pacote, por exemplo:

```bash
ratt <nome_do_pacote>_<versao>_<arquitetura>.changes
```

exemplo de arquivo:

```bash
ratt golang-k8s-apimachinery_0.31.3-1_amd64.changes
```
---


Seguindo estas etapas, você poderá configurar e executar o `ratt` de maneira segura no Ubuntu e Debian.
