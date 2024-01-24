# O Prompt de Comandos

Nesta lição, aprenderemos o básico do prompt de comandos do Windows para manipular e executar nossos scripts em Python.

## Introdução

Você pode abrir o prompt de comandos de algumas maneiras:

- Uma delas é pesquisando por CMD na busca do Windows.
- A outra é através do Executar, pressionando as teclas <kbd>Win</kbd> + <kbd>R</kbd>, digitando `CMD` na tela que aparecerá e pressionando <kbd>Enter</kbd>.

## Verificando o Python

Para verificar se o Python foi instalado, digite o seguinte comando no prompt de comandos:

```cmd
C:\Users\Usuário> python --version
```

Se a saída for semelhante a isso, significa que o Python foi instalado corretamente.

```cmd
C:\Users\Usuário> python --version
Python 3.x.x
```

Se esse comando retornar algum erro, recomendo reler o [capítulo anterior](01_Introduction.md).

## Comandos básicos

Para utilizar o prompt de comandos com mais eficiência, é preciso primeiro aprender alguns comandos básicos, como manipulação de arquivos e diretórios.
Ao abrir o CMD, você começa na pasta raiz do seu usuário, geralmente em `C:\Users\Seu Nome`.

### dir

Para ver os arquivos na sua pasta atual, você pode utilizar o comando `dir` (do inglês *directory*, diretório), como pode ser visto abaixo:

```cmd
C:\Users\Usuário> dir
```

Que gera a seguinte saída:

```cmd
C:\Users\Usuário>dir
 O volume na unidade C não tem nome.
 O Número de Série do Volume é ...

 Pasta de C:\Users\Usuário

23/01/2024  19:55    <DIR>          .
23/01/2024  19:55    <DIR>          ..
16/09/2023  19:50                94 .gitconfig
...
18/11/2023  07:49    <DIR>          Desktop
24/01/2024  09:20    <DIR>          Documents
24/01/2024  18:32    <DIR>          Downloads
24/03/2021  10:41    <DIR>          Favorites
...
```

Esta saída mostra os itens dentro do diretório "C:\Users\Usuário".

- **Data e Hora:** Indica a data e a hora da última modificação ou criação do arquivo ou diretório.

- **\<DIR\>:** Indica que o item listado é um diretório (pasta).

- **.:** Refere-se ao diretório atual.

- **..:** Refere-se ao diretório pai (um nível acima).

- **Nome do Diretório/Arquivo:** Indica o nome do diretório ou arquivo.

- **Tamanho do Arquivo:** Indica o tamanho do arquivo em bytes. Se for um diretório, o campo será `<DIR>`.

Neste exemplo:

- O primeiro item (.) representa o diretório atual.
- O segundo item (..) representa o diretório pai.
- Os itens seguintes são diretórios e arquivos no diretório "C:\Users\Usuário".

Caso você queira obter apenas os nomes dos arquivos e pastas sem maiores detalhes, você pode utilizar o comando `dir` com a opção `/b` (do inglês *bare*, simples). A saída será a seguinte:

```cmd
C:\Users\RECEPCAO>dir /b
.gitconfig
...
Desktop
Documents
Downloads
Favorites
...
```

### cd

O comando `cd` (do inglês *change directory*, mudar diretório) é um dos mais importantes. Junto com o comando `dir`, permite que você navegue entre pastas de maneira eficiente e rápida.

Você pode transitar entre pastas da seguinte maneira:

```cmd
C:\Users\Usuário>cd Downloads

C:\Users\Usuário\Downloads>
```

Basta inserir o comando `cd` e, em seguida, o nome da pasta para a qual você deseja ir. Caso precise ver as pastas disponíveis na sua pasta atual, basta utilizar o, já conhecido, comando `dir` (ou `dir /b`, se preferir).

Caso precise voltar para a pasta que você estava, basta utilizar `..` como argumento para o comando. É comum, nos sistemas de arquivos de terminais, utilizar `.` para se referir à pasta atual e `..` para a pasta anterior, como no exemplo abaixo:

```cmd
C:\Users\Usuário\Downloads>cd ..

C:\Users\Usuário>
```

[Continua]
