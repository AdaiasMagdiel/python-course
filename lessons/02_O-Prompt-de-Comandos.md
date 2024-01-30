# O Prompt de Comandos

Nesta lição, aprenderemos o básico do prompt de comandos do Windows para manipular e executar nossos scripts em Python.

## Introdução

Você pode abrir o prompt de comandos de algumas maneiras:

- Uma delas é pesquisando por CMD na busca do Windows.
- A outra é através do Executar, pressionando as teclas <kbd>Win</kbd> + <kbd>R</kbd>, digitando `CMD` na tela que aparecerá e pressionando <kbd>Enter</kbd>.

## Verificando o Python

Para verificar se o Python foi instalado, digite o seguinte comando no prompt de comandos:

```cmd
C:\Users\Usuário>python --version
```

Se a saída for semelhante a isso, significa que o Python foi instalado corretamente.

```cmd
C:\Users\Usuário>python --version
Python 3.x.x
```

Se esse comando retornar algum erro, recomendo reler o [capítulo anterior](01_Introduction.md).

## Comandos básicos

Para utilizar o prompt de comandos com mais eficiência, é preciso primeiro aprender alguns comandos básicos, como manipulação de arquivos e diretórios.
Ao abrir o CMD, você começa na pasta raiz do seu usuário, geralmente em `C:\Users\Seu Nome`.

### dir

Para ver os arquivos na sua pasta atual, você pode utilizar o comando `dir` (do inglês *directory*, diretório), como pode ser visto abaixo:

```cmd
C:\Users\Usuário>dir
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

### del

O comando `del` é utilizado para remover arquivos e se aplica exclusivamente a arquivos. Assim como o comando `cd`, ele aceita argumentos, que, neste caso, são um ou mais arquivos a serem excluídos.

```cmd
C:\Users\Usuário>del arquivo.txt
```

Se o comando for bem-sucedido, nenhuma mensagem será retornada.

Se você fornecer um arquivo inexistente como argumento para o comando, uma mensagem será exibida, indicando que não foi possível localizar o arquivo informado:

```cmd
C:\Users\Usuário>del nao-existe.txt
Não foi possível encontrar C:\Users\Usuário\nao-existe.txt
```

Ao informar uma pasta como argumento para o comando, será solicitada uma confirmação, e todos os arquivos da pasta serão apagados (exceto os arquivos dentro de subpastas presentes no diretório informado).

```cmd
C:\Users\Usuário>del pasta
C:\Users\Usuário\pasta\*, Tem certeza (S/N)? 
```

Existem algumas opções úteis para este comando:

- **/S**: Exclui arquivos especificados de todos os subdiretórios.
- **/Q**: Modo silencioso, sem solicitar confirmação para a exclusão.

Você pode utilizá-las da seguinte forma:

```cmd
C:\Users\Usuário>del pasta /q
```

Ou

```cmd
C:\Users\Usuário>del pasta /s
```

Ou até mesmo

```cmd
C:\Users\Usuário>del pasta /s /q
```

> Tome cuidado ao utilizar a opção `/s` em conjunto com a opção `/q`, pois isso permite que o comando exclua todos os itens da pasta e das subpastas sem solicitar confirmação.

### rd

Do inglês "remove directory", o comando `rd`, como o próprio nome sugere, é utilizado para excluir diretórios através do CMD.

Assim como o comando `del`, seu uso é bastante simples; basta digitar o comando e informar a pasta (ou pastas) a ser excluída.

```cmd
C:\Users\Usuário>rd pasta
```

Da mesma forma que o comando `del`, se o comando `rd` não retornar nada, significa que a exclusão foi bem-sucedida.

No entanto, há um detalhe: o comando `rd` exclui apenas pastas vazias. Se você tentar apagar uma pasta que contenha arquivos, será exibida a seguinte mensagem de erro:

```cmd
C:\Users\Usuário>rd pasta
A pasta não está vazia.
```

Então, como podemos apagar uma pasta que não está vazia? A resposta é simples: utilizando o comando `rd` com as mesmas opções que vimos no comando `del`, ou seja, `/s` e `/q` em conjunto, da seguinte forma:

```cmd
C:\Users\Usuário>rd pasta /s /q
A pasta não está vazia.
```

A opção `/s` indica ao comando que você realmente deseja apagar os itens internos, e a opção `/q` indica que não é necessário confirmar a ação.

Se você utilizar apenas a opção `/s`, a ação será concluída da mesma forma, mas será solicitada confirmação para a exclusão.

### mkdir

O comando `mkdir` (do inglês *make directory*, criar diretório) é utilizado para criar novos diretórios no CMD. Essa é uma operação fundamental quando você precisa organizar e estruturar seus arquivos no sistema.

Ao utilizar o `mkdir`, você pode criar um novo diretório especificando seu nome como argumento, da seguinte forma:

```cmd
C:\Users\Usuário>mkdir NovoDiretorio
```

É importante observar algumas coisas ao utilizar este comando:

1. Evite espaços em branco ou caracteres especiais nos nomes dos diretórios para garantir compatibilidade com diferentes sistemas operacionais. Caso você queira nomear uma pasta com um nome contendo espaços você deve colocar o nome dentro de aspas: ```mkdir "nome com espaços"``` mas essa não é uma prática recomendada.

2. Se o diretório que você está criando já existir, o comando retornará uma mensagem informando que o diretório não pode ser criado.

```cmd
C:\Users\Usuário>mkdir Downloads
Já existe uma subpasta ou arquivo com esse nome.
```

### type

O comando `type` no CMD do Windows é utilizado para exibir o conteúdo de arquivos de texto diretamente no prompt de comando.

```cmd
C:\Users\Usuário>type arquivo.txt
```

Isso exibirá o conteúdo do arquivo "arquivo.txt" diretamente na tela do CMD.

#### Criando um Arquivo em Branco

Uma aplicação interessante do type é criar arquivos em branco usando o dispositivo especial `NUL`.

Para criar um arquivo em branco, você pode usar o seguinte comando:

```cmd
C:\Users\Usuário>type NUL > arquivo.txt
```

Neste exemplo, `NUL` é um dispositivo especial do Windows que representa uma porta nula. Ao redirecionar a saída do `type NUL` para um arquivo (`> arquivo.txt`), você cria um arquivo vazio chamado "arquivo.txt". O simbolo `>` nesse contexto indica que você está enviando algo para algum lugar, no caso está enviando o conteúdo de NUL para o arquivo arquivo.txt (que será criado nessa ação).

#### O que é NUL?

Em sistemas Windows, `NUL` é um dispositivo que aceita dados, mas os descarta, efetivamente criando uma saída nula. Portanto, quando você redireciona `type NUL` para um arquivo, você está essencialmente direcionando nada para o arquivo, resultando em um arquivo vazio.

É preciso observar que o uso do dispositivo `NUL` para criar arquivos em branco é específico do ambiente CMD do Windows e pode não ser aplicável em outros sistemas operacionais.

### copy

O comando `copy` no CMD do Windows é usado para copiar arquivos de um local para outro. É uma ferramenta útil para duplicar ou fazer backups de arquivos de maneira rápida e eficiente.

Para realizar uma cópia simples de um arquivo, você pode usar o seguinte formato:

```cmd
C:\Users\Usuário>copy arquivo_origem.txt destino\
```

Este comando copiará o arquivo "arquivo_origem.txt" para o diretório de destino especificado.

Observações Importantes

1. Se um arquivo com o mesmo nome já existir no destino, o comando `copy` solicitará uma confirmação antes de substituí-lo. Você pode optar por confirmar digitando `S` para sim ou `N` para não.

2. Utilize as opções apropriadas, como `/Y`, para suprimir mensagens de confirmação ao substituir automaticamente arquivos existentes.

```cmd
C:\Users\Usuário>copy /Y arquivo.txt D:\Destino\
```

Este comando copiará o arquivo "arquivo.txt" para o destino especificado, substituindo automaticamente qualquer arquivo com o mesmo nome sem solicitar confirmação.


### move

O comando `move` no CMD do Windows é utilizado para mover arquivos ou renomeá-los.

Para mover um arquivo de um local para outro, você pode usar o seguinte formato:

```cmd
C:\Users\Usuário>move arquivo.txt novo_destino\
```

Este comando move o arquivo "arquivo.txt" para o novo destino especificado.

#### Exemplo de Renomeação de Arquivo

Além de mover arquivos, o comando `move` também pode ser usado para renomear arquivos:

```cmd
C:\Users\Usuário>move arquivo_antigo.txt novo_nome.txt
```

Este comando renomeia o arquivo "arquivo_antigo.txt" para "novo_nome.txt".

Observações Importantes

1. Se um arquivo com o mesmo nome já existir no destino, o comando `move` solicitará uma confirmação antes de substituí-lo. Você pode optar por confirmar digitando `S` para sim ou `N` para não.

2. Utilize as opções apropriadas, como `/Y`, para suprimir mensagens de confirmação ao substituir automaticamente arquivos existentes.

#### Exemplo com Opção /Y

```cmd
C:\Users\Usuário>move /Y arquivo.txt D:\Destino\
```

Este comando move o arquivo "arquivo.txt" para o destino especificado, substituindo automaticamente qualquer arquivo com o mesmo nome sem solicitar confirmação.

### cls

O comando `cls` no CMD do Windows é utilizado para limpar a tela do prompt de comando, proporcionando uma visualização mais limpa e organizada.

Para limpar a tela, basta digitar o seguinte comando:

```cmd
C:\Users\Usuário>cls
```

Este comando remove todas as informações e comandos anteriores da tela. O `cls` é especialmente útil quando a tela do prompt de comando fica cheia de saídas de comandos anteriores, tornando difícil acompanhar ou visualizar novas informações.

### ren

O comando `ren` no CMD do Windows é utilizado para renomear arquivos ou grupos de arquivos. Ele oferece uma maneira simples de alterar o nome de um arquivo sem mover seu local no sistema de arquivos.

Para renomear um arquivo, você pode usar o seguinte formato:

```cmd
C:\Users\Usuário>ren arquivo_antigo.txt novo_nome.txt
```

Este comando renomeia o arquivo "arquivo_antigo.txt" para "novo_nome.txt".

#### Diferença entre `ren` e `move`

Embora tanto `ren` quanto `move` possam ser usados para renomear arquivos, a principal diferença está no escopo de sua funcionalidade:

- **`ren` (rename):** Como o próprio nome sugere, o `ren` é usado exclusivamente para renomear arquivos. Ele não altera a localização física do arquivo no sistema de arquivos.

- **`move`:** O `move`, além de mover arquivos para diferentes diretórios, também pode ser usado para renomear arquivos. Isso significa que, ao utilizar o `move` para renomear um arquivo, você pode, ao mesmo tempo, alterar seu local no sistema de arquivos.

Observações Importantes

1. Se um arquivo com o mesmo nome já existir no diretório, o comando `ren` solicitará uma confirmação antes de substituí-lo. Você pode optar por confirmar digitando `S` para sim ou `N` para não.

2. Utilize as opções apropriadas, como `/Y`, para suprimir mensagens de confirmação ao substituir automaticamente arquivos existentes.

---

Esta foi uma breve introdução aos comandos fundamentais do CMD no Windows, focando na manipulação de arquivos e diretórios. Embora tenhamos abordado comandos como `cd`, `dir`, `del`, `rd`, `mkdir`, `type`, `copy`, `move`, `cls`, e `ren`, é importante destacar que há muitos outros comandos disponíveis para uma variedade de tarefas e você pode consultar todos usando o comando `help` e lendo a seção de ajuda no próprio CMD.

> Até a próxima e obrigado pelos peixes!
