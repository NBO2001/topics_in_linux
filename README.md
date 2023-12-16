# Topics in linux

Um curso de linux oferecido como disciplina pelo IComp em dezembro de 2023.

**Nome: Natanael B.**

**Matrícula: _________**

## Exercício 1

### 1. **Escolha de Programa no Linux** *(2,0 pontos)*

   Para este exercício, o programa escolhido foi o **docker**. 

a. **Propósito:**

O Docker é uma ferramenta amplamente empregada para gerenciar, criar e remover contêineres e imagens.

b. **Sintaxe:**

```bash
docker [OPTIONS] COMMAND [ARG...]
```

c. **Seção (número e categoria):**

```bash
DOCKER(1)
```


d. **Opção e sua descrição:**

**Algumas da opções:**

```Bash
OPTIONS
       --help
         Print usage statement

       --config=""
         Specifies  the location of the Docker client configuration files. The
       default is '~/.docker'.

       -D, --debug=true|false
         Enable debug mode. Default is false.

       -H, --host=[unix:///var/run/docker.sock]: tcp://[host]:[port][path]  to
       bind or unix://[/path/to/socket] to use.
         The socket(s) to bind to in daemon mode specified using one or more
         tcp://host:port/path,  unix:///path/to/socket,  fd://*  or fd://sock‐
       etfd.
         If the tcp port is not specified, then it will default to either 2375
       when
         --tls is off, or 2376 when --tls is on, or --tlsverify is specified.

       -l, --log-level="debug|info|warn|error|fatal"
         Set the logging level. Default is info.

       --tls=true|false
         Use TLS; implied by --tlsverify. Default is false.

       --tlscacert=~/.docker/ca.pem
         Trust certs signed only by this CA.

       --tlscert=~/.docker/cert.pem
         Path to TLS certificate file.

       --tlskey=~/.docker/key.pem
         Path to TLS key file.

       --tlsverify=true|false
         Use  TLS and verify the remote (daemon: verify client, client: verify
       daemon).
         Default is false.

       -v, --version=true|false
         Print version information and quit. Default is false.
```

### **2. Em ambientes Linux é muito comum que arquivos de configuração do usuário fiquem no seu diretório pessoal (/home/nome\_do\_usuario). Contudo, o usuário está com problemas para encontrar esses arquivos. Ao listar o conteúdo do diretório, esses arquivos não são exibidos.** *(2,0 pontos)*

* a. Qual comando pode ser usado para mostrar todos os arquivos, incluindo os arquivos
ocultos?

```bash
ls -a
```

* b. Liste o nome de pelo menos três arquivos ocultos encontrados nessa listagem executada no seu diretório home.
```bash
natanael@natanael:~$ ls -a
.bash_history
.bash_logout
.bashrc 
.gitconfig
```

### **3. Ao listar um arquivo com informações detalhadas, um usuário possui apenas informações sobre a última modificação. Por exemplo:**

```bash
$ ls -l /etc/passwd
-rw-r--r-- 1 root root 2311 Mar 16 17:26 /etc/passwd
```

**Porém, um usuário gostaria de saber mais informações sobre o arquivo, como o último acesso a ele. Qual comando pode ser usado para isso?** *(2,0 pontos)*

```bash
$ ls -lu /etc/passwd
-rw-r--r-- 1 root root 3042 dez 13 19:38 /etc/passwd
```

### **4. Um usuário acabou de dar um comando complexo na shell, ocupando três linhas do terminal. Ele gostaria de repetir esse comando, mas por algum motivo, a tecla seta para cima para recuperar o último comando não está funcionando. Com base nisso responda:** *(2,0 pontos)*

*a. Qual comando pode ser usado para consultar os últimos comandos no sistema?*

```bash
$ history
```

*b. Como ele pode repetir esse comando complexo sem ter que digitá-lo novamente no
terminal.*

```bash
$ !!
```

### **5. No diretório pessoal do seu usuário, execute os comandos (um de cada vez)** *(2,0 pontos)*
```bash
$ cat /etc/*
$ cat /etc/* | more
$ cat /etc/* | less
$ more /etc/*
$ less /etc/*
```

**Crie os arquivos CatSemPipe, CatMore, CatLess, MoreSemPipe e LessSemPipe. Escreva o que cada comando faz dentro de seus respectivos arquivos.**

Ex:

```bash
$ echo "O comando cat /etc/* faz blablabla ..." > CatSemPipe
```

Resposta:

```bash
$ echo "O comando cat /etc/* ele contatena o conteúdo de todos os arquivos da pasta etc" > CatSemPipe
$ echo "O comando cat /etc/* | more ele contatena o conteúdo de todos os arquivos da pasta etc e a saida vai para o programa more, em que é mostrado no terminal de forma controlada" > CatMore
$ echo "O comando cat /etc/* | less ele contatena o conteúdo de todos os arquivos da pasta etc e a saida vai para o programa more, em que é mostrado no terminal de forma controlada, mas aqui pode navegar para cima e para baixo" > CatLess
$ echo "O comando more /etc/*  É mostrado no terminal de forma controlada" > MoreSemPipe
$ echo "O comando less /etc/* | less É mostrado no terminal de forma controlada, mas aqui pode navegar para cima e para baixo" > LessSemPipe
```