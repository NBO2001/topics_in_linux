# Topics in linux

Um curso de linux oferecido como disciplina pelo IComp em dezembro de 2023.

## Exercício 1

### 1. **Escolha de Programa no Linux** *(2,0 pontos)*

   Para este exercício, o programa escolhido foi o **more**. 

a. **Propósito:**

Ler arquivos de textos gigantescos. Pelo menos eu uso para isso 😅.


b. **Sintaxe:**

```bash
more [options] file ...
```

c. **Seção (número e categoria):**

-- Procurar o que é


d. **Opção e sua descrição:**

More é um filtro para paginar através de texto uma tela por vez. Esta versão é especialmente primitiva. Os usuários devem estar cientes de que o less(1) fornece emulação do more(1) com melhorias extensivas.

**Algumas da opções:**

```Bash
-d, --silent
    Prompt with "[Press space to continue, 'q' to quit.]", and display
    "[Press 'h' for instructions.]" instead of ringing the bell when an
    illegal key is pressed.
-f, --no-pause
    Count logical lines, rather than screen lines (i.e., long lines are
    not folded).
-p, --print-over
    Do not scroll. Instead, clear the whole screen and then display the
    text. Notice that this option is switched on automatically if the
    executable is named page.
-c, --clean-print
    Do not scroll. Instead, paint each screen from the top, clearing
    the remainder of each line as it is displayed.

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

### **3. Ao usar o sistema, um usuário se deparou com um arquivo com uma extensão diferente: aiff. No momento, ele estava sem internet para consultar o tipo de arquivo. Como ele estava usando Linux, ele poderia consultar no próprio sistema mais informações sobre o propósito desse tipo de arquivo com essa extensão. Para auxiliar nessa questão, procure um arquivo com essa extensão usando o seguinte comando:**

```bash
$ find / -type f -name '*.aiff' 2>/dev/null
/System/Library/Sounds/Ping.aiff
```

**Caso seu sistema não possua um arquivo com tal extensão, você pode usar o arquivo contido no colabweb. Com base nisso, responda:**  *(2,0 pontos)*

*a. Qual comando pode ser usado para consultar informações sobre o tipo desse arquivo?*

```bash
file [-bcdEhiklLNnprsSvzZ0] [--apple] [--exclude-quiet] [--extension] [--mime-encoding] [--mime-type] [-e testname] [-F separator] [-f namefile] [-m magicfiles] [-P name=value] file ...
```
*b. Descreva para que serve essa extensão (aiff).*

A extensão de arquivo AIFF (Audio Interchange File Format) é comumente usada para armazenar dados de áudio digital. O formato AIFF é não comprimido e é frequentemente utilizado para armazenar áudio de alta qualidade e sem perdas.


### **4. Ao listar um arquivo com informações detalhadas, um usuário possui apenas informações sobre a última modificação. Por exemplo:**

```bash
$ ls -l /etc/passwd
-rw-r--r-- 1 root root 2311 Mar 16 17:26 /etc/passwd
```

**Porém, um usuário gostaria de saber mais informações sobre o arquivo, como o último acesso a ele. Qual comando pode ser usado para isso?** *(2,0 pontos)*

```bash
$ ls -lu /etc/passwd
-rw-r--r-- 1 root root 3042 dez 13 19:38 /etc/passwd
```

### **5. Um usuário acabou de dar um comando complexo na shell, ocupando três linhas do terminal. Ele gostaria de repetir esse comando, mas por algum motivo, a tecla seta para cima para recuperar o último comando não está funcionando. Com base nisso responda:** *(2,0 pontos)*

*a. Qual comando pode ser usado para consultar os últimos comandos no sistema?*

```bash
$ history
```

*b. Como ele pode repetir esse comando complexo sem ter que digitá-lo novamente no
terminal.*

```bash
$ !!
```