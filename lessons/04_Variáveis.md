# Variáveis

## Introdução

Variáveis em Python são como contêineres que armazenam valores. Podemos imaginá-las como caixas que guardam informações, e sempre podemos recuperar o que foi armazenado. Nesta analogia, cada caixa é uma variável.

<p align="center">
	<img src="https://www.make.com/en/help/image/uuid-0e2736c7-2a14-1c95-9cba-ffb6ad68b32d.png" alt="Caixas como representação para variáveis" style="width: 80%; max-width: 320px;">
</p>

Para identificar de qual caixa queremos pegar o objeto armazenado, basta etiquetar a caixa com um nome que faz referência ao que está guardado. Assim são as variáveis em Python; cada uma tem um nome e um valor associado.

## Declarando Variáveis em Python

Em Python, você pode declarar uma variável da seguinte forma:

```python
nome = "Adaías Magdiel"
```

Aqui, criamos uma variável chamada `nome` e utilizamos o sinal de `=` para atribuir o valor `"Adaías Magdiel"`, que é uma string (um valor de texto). Esta é a sintaxe padrão para criar variáveis em Python: você escolhe um nome significativo que segue algumas regras (veremos mais sobre isso adiante) e utiliza o sinal de atribuição `=` para associar um valor a essa variável.

A seguir, alguns exemplos de variáveis em Python:

```python
idade = 21
solteiro = True
altura_em_metros = 1.71
```

## Exibindo Variáveis

Para exibir os valores armazenados nas variáveis, utilizamos a função `print`, que já conhecemos da aula anterior:

```python
print(nome)
print(idade)
print(solteiro)
print(altura_em_metros)
```

Ao contrário das strings, não é necessário colocar o nome das variáveis entre aspas ao utilizar a função `print`. Isso ocorre porque, ao usar variáveis, você faz referência a algo já declarado, e o interpretador entende e sabe encontrar essas referências.

Caso você decidisse colocar o nome da variável entre aspas, imprimiria literalmente o nome definido, em vez do valor atribuído.

## Tipos Primitivos em Python

O termo "tipo primitivo" refere-se a dados básicos facilmente manipuláveis, independentes de outros tipos. Em Python, temos os seguintes tipos primitivos:

- **Inteiros (`int`):** Representam números inteiros, tanto negativos quanto positivos.
- **Ponto Flutuante (`float`):** Representam números decimais, utilizando o ponto (`.`) para separar as casas decimais.
- **Booleanos (`bool`):** Representam valores verdadeiros (`True`) ou falsos (`False`).
- **Strings (`str`):** Representam valores de texto e sempre estão entre aspas.

## Regras Para a Nomeação de Variáveis

Ao criar variáveis em Python, é essencial seguir algumas regras para garantir a clareza e consistência no seu código. Essas regras ajudam a manter um estilo padronizado e facilitam a leitura do seu código por outros desenvolvedores. Aqui estão algumas diretrizes simples:

### Boas Práticas e Padronização de Código

1. **Comece com uma letra ou sublinhado (_):**
   - **Aceitável:** `idade`, `_nome`, `_valor_total`
   - **Não Aceitável:** `123abc`, `@nome`, `&total_valor`

   Variáveis devem começar com uma letra (maiúscula ou minúscula) ou um sublinhado (\_). Não é permitido iniciar com números ou caracteres especiais, exceto o sublinhado.

2. **Evite caracteres especiais:** 
   - **Aceitável:** `preco_total`, `numero_itens`
   - **Não Aceitável:** `preço_total`, `número_itens`

   Use apenas letras, números e sublinhados em nomes de variáveis. Evite caracteres especiais, como acentos ou espaços. Apesar de Python suportar acentos no nome de variáveis é uma boa prática evitar sempre que possível.

3. **Use nomes descritivos:**
   - **Aceitável:** `idade_usuario`, `nome_completo`
   - **Não Aceitável:** `a`, `x1`

   Escolha nomes que descrevam claramente o propósito da variável. Nomes descritivos tornam o código mais legível.

4. **Evite palavras reservadas:** 
   - **Aceitável:** `total_itens`, `nome_cliente`
   - **Não Aceitável:** `print`, `for`, `if`

   Não use palavras reservadas da linguagem Python como nomes de variáveis, pois isso pode causar conflitos e erros.

### Padrões da linguagem Python

Em Python, é comum seguir o padrão de nomenclatura chamado de `snake_case` para nomear variáveis. O `snake_case` é uma convenção que utiliza letras minúsculas para as palavras e separa-as por sublinhados. Por exemplo: `nome_variavel`, `idade_usuario`, `total_itens`.

Este padrão é amplamente adotado na comunidade Python por suas vantagens em termos de legibilidade e simplicidade. Ao utilizar `snake_case`, torna-se mais fácil distinguir as palavras em um nome de variável, especialmente quando comparado com outros padrões de nomenclatura. Além do `snake_case`, também temos:

1. **CamelCase:**
   - Exemplo: `nomeVariavel`, `idadeUsuario`, `totalItens`
   - Neste padrão, cada palavra, exceto a primeira, começa com uma letra maiúscula. Embora seja comumente utilizado em outras linguagens, como Java e JavaScript, não é tão prevalente na comunidade Python.

2. **PascalCase:**
   - Exemplo: `NomeVariavel`, `IdadeUsuario`, `TotalItens`
   - Semelhante ao CamelCase, mas com a primeira letra também em maiúscula. Este padrão é utilizado principalmente para nomear classes em Python, não sendo tão comum para variáveis.

3. **Kebab Case ou Hyphen Case:**
   - Exemplo: `nome-variavel`, `idade-usuario`, `total-itens`
   - Usa hifens para separar palavras. Embora seja amplamente utilizado em URLs e na definição de nomes de arquivos em alguns contextos, não é convencional para nomear variáveis em Python.

---

Essa foi uma abordagem inicial e introdutória sobre variáveis, espero que o conceito e o uso tenha sido bem explicado. Nas próximas aulas veremos mais sobre variáveis e começaremos a utilizá-las nos nossos programas.

> Até a próxima e obrigado pelos peixes!
