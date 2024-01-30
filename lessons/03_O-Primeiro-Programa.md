# A Linguagem de Programação Python

A Wikipédia traz a seguinte definição da linguagem Python: "Uma linguagem de programação de alto nível, interpretada, imperativa, orientada a objetos, funcional, de tipagem dinâmica e forte."

Eu sei, são muitos termos e a maioria parece ser composta por palavras que não fazem muito sentido juntas, mas vamos analisar parte por parte e tentar entender o que isso significa.

**Uma linguagem de programação de alto nível**

Quando falamos de linguagens de programação, é comum usarmos as seguintes definições: "alto nível" e "baixo nível". Estas configuram um espectro onde uma linguagem de baixo nível está mais próxima da linguagem de máquina do que da linguagem humana, enquanto as linguagens de alto nível são projetadas para parecerem mais próximas da linguagem humana, permitindo uma compreensão mais fácil do que está sendo escrito.

**Interpretada**

Novamente estamos diante de definições para linguagens de programação, onde temos linguagens interpretadas e linguagens compiladas. Basicamente, uma linguagem é compilada quando o seu código passa por um processo para se tornar o mais próximo possível do código de máquina. Já uma linguagem interpretada não sofre esse processo e é executada linha a linha em tempo de execução, como é o caso do Python.

**Imperativa, orientada a objetos e funcional**

Esses termos referem-se a paradigmas de linguagem. Paradigma é uma palavra que significa "exemplo" ou "padrão". Basicamente, no contexto de linguagens, paradigma indica como aquela linguagem recebe e interpreta instruções. Algumas linguagens implementam apenas um tipo de paradigma e executam o código de uma única maneira. Outras, como o Python, recebem e executam as instruções de várias maneiras possíveis. Comumente, chamamos essas linguagens de multiparadigmas, pois aceitam vários modelos de instruções.

**Tipagem dinâmica e forte**

Python é uma linguagem de tipagem dinâmica e forte. Isso significa que você não precisa declarar explicitamente o tipo de uma variável, e a linguagem verifica de forma rigorosa a compatibilidade de tipos durante a execução. Essas características tornam o Python flexível e robusto, facilitando a escrita de código conciso e expressivo.

A tipagem dinâmica em Python permite uma maior flexibilidade na manipulação de variáveis, enquanto a tipagem forte ajuda a evitar erros relacionados à incompatibilidade de tipos, contribuindo para a segurança do código. Isso torna o Python uma linguagem poderosa e acessível para programadores de diferentes níveis de experiência.

Pode ser que, à primeira vista, alguns desses conceitos sejam complicados de entender, mas veremos ao decorrer do curso mais e mais sobre cada um desses pontos.

Aqui está o texto com algumas modificações sugeridas:

## Olá, Mundo!

No mundo da programação, existe uma tradição que perdura há algum tempo quando estamos prestes a escrever nosso primeiro programa, independentemente da linguagem escolhida.

Trata-se do "Olá, Mundo!" Essa frase é usada na criação do primeiro programa e serve como uma suave introdução ao ambiente de desenvolvimento da linguagem.

Então, vamos lá.

### Exibindo uma mensagem na tela

Em Python, para exibir uma mensagem na tela, usamos a função `print`. Traduzindo para o português, ela se chamaria "imprimir". Isso é possivelmente uma alusão aos primeiros computadores que, para exibir informações, literalmente as imprimiam.

Para criar nosso primeiro programa e exibir a mensagem "Olá, Mundo!", crie um arquivo chamado `ola_mundo.py`. É importante que a extensão do arquivo seja `.py`, pois essa é a extensão comum de um arquivo escrito em Python e que será usado pelo interpretador para executar.

Nesse arquivo, digite o seguinte e salve:

```python
print("Olá, Mundo!")
```

No prompt de comandos, navegue até a pasta onde se localiza o arquivo e digite:

```cmd
C:\Users\Usuário\Python\Aulas>python ola_mundo.py
```

Nesse comando, você chama o interpretador do Python e passa o nome do arquivo como argumento. Você deve receber uma saída parecida com essa:

```cmd
C:\Users\Usuário\Python\Aulas>python ola_mundo.py
Olá, Mundo!
```

Parabéns! Você criou seu primeiro programa e o seu primeiro "Olá, Mundo!".

#### Entendendo o código

Para exibir a mensagem na tela, usamos a função `print` da linguagem, mas o que é uma função?

No contexto da programação, uma função é um bloco de código que realiza uma tarefa específica e pode ser chamado (ou invocado) de outros lugares do programa. Ela é uma maneira de organizar e reutilizar código, permitindo que você divida um programa em partes menores e mais gerenciáveis.

A princípio, você não precisa entender exatamente o que é uma função. Teremos uma aula específica onde aprofundaremos nesse assunto. No entanto, você precisa entender como uma função é chamada e como ela normalmente se comporta.

Uma função geralmente tem um nome e é chamada da seguinte forma: `nome` `(` `argumentos` `)`.

Você invoca a função pelo nome, e entre parênteses, você passa os argumentos para a função. Dependendo da função, ela pode receber um ou mais argumentos. No caso da função `print`, ela recebe o que você deseja exibir na tela e pode passar uma ou mais informações.

Para passar mais de uma informação para uma função, você separa os argumentos usando vírgulas, assim: `nome` `(` `argumento1`, `argumento2`,... `)`.

No nosso exemplo, passamos um texto para a função (formalmente chamado de `string`). Mais adiante, estudaremos sobre as `strings`, mas por enquanto, você precisa saber que todo texto literal precisa estar entre aspas, sejam elas simples ' ou duplas ".

Vamos passar mais de um argumento para a função `print` e ver como ela se comporta. Crie um novo arquivo chamado `exemplo_02.py` com o seguinte conteúdo:

```python
print("Olá", "mundo", "!")
```

Perceba que colocamos cada palavra como um argumento distinto para a função. Ao executar, temos a seguinte saída:

```cmd
C:\Users\Usuário\Python\Aulas>python exemplo_02.py
Olá Mundo !
```

Repare que, apesar de não termos colocado espaços entre as palavras em cada argumento, o Python retornou o texto com espaços. Esse é o comportamento padrão da função: ao receber mais de um argumento, ela exibe na tela, separando os argumentos com espaços.

Experimente brincar com o código, trocando os textos, passando mais textos e sinta como a linguagem se comporta com as suas alterações.
