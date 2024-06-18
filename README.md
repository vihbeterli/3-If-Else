# Estruturas Condicionais

Nesta etapa introduziremos o conteúdo de ESTRUTURAS CONDICINAIS, junto dos TIPOS DE ENTRADAS DE DADOS.

De forma simples, uma estrutura de condição é um molde que nos permite escolher mais de um caminho diante de um impasse, semelhante às bifurcações nas ruas e rodovias.

Existem três moldes/estruturas de condição no JavaScript/ECMA Script, são elas:

- If Else (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else)
- Switch Case (https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/switch)
- Operador Ternário (https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Conditional_operator)

Nós vamos estudá-los exatamente nesta ordem, assim àqueles que quiserem avançar mais rápido, pode seguir nesta ordem.

# If... Else (Se... Senão)

A estrutura de condição If Else é a mais clássica, sua estrutura básica pode ser representada por:

```
if (condicao){
    resultado 1 para a condição
}else{
    resultado 2 para a condição
}
```

Com base neste modelo podemos montar o exemplo a seguir:

```
if ( 2+2 == 4 ){
    document.write("A soma é verdadeira");
}else{
    document.write("A soma é falsa");
}
```

Destrinchando o exemplo acima temos,

- Na linha 1 a abertura da estrutura de condição seguido da expressão ```2+2 == 4```, essa expressão está verificando se a soma de 2+2 é igual ao valor 4.
- Caso seja verdadeira, a condição entra na linha 2, onde imprime em tela o texto "A soma é verdadeira".
- Caso o resultado da expressão na linha 1 seja falsa, a condição passa direto para a linha 4 e imprime em tela o texto "A soma é falsa".

## E se existir duas ou mais condições aninhadas/seguintes?


É relativamente normal lidar com mais de uma condição na programação, principalmente se uma delas exigir novas condições. Ex.: verifique se um número é ímpar e positivo.

Esta condição pode ser resolvida verificando se o número é ímpar, caso verdadeiro, verificar se ele também é positivo; através do código:

```
let numeroImparPositivo = 5;

if (numeroImparPositivo % 2 != 0){

    if (numeroImparPositivo >= 0){
        document.write(`O número ${numeroImparPositivo} é ímpar e positivo`);
    
    }else{
        document.write(`O número ${numeroImparPositivo} não é positivo`);
    }

}else{
    document.write(`O número ${numeroImparPositivo} não é ímpar`);
}
```
Destrinchando o exemplo acima temos,

- Na linha 1, a criação da variável ```numeroImparPositivo``` e a atribuição do valor 5.
- Na linha 3, a verificação se o valor da variável é ímpar, por meio da expressão ```numeroImparPositivo % 2 != 0```, onde o valor 5 está sendo dividido por 2 até retornar o menor resto possível, ou seja, 5/2 = 3 -> 3/2 = 1. Em seguida verifica se o resto, 1, é diferente de 0 - ```1 != 0``` - o operador ````!=``` representa diferença. Caso a condição seja verdadeira, entra na linha 4 em diante. Caso contrário, entra na linha 13.
-- Na linha 5, é verificado se o numeroImparPositivo é positivo, por meio da expressão ```numeroImparPositivo >= 0```, onde vê se o valor 5 é maior que 0. 
    --> Caso a condição seja verdadeira, entra na linha 6 e imprime o texto "O número ${numeroImparPositivo} é ímpar e positivo".
    --> Caso contrário, entra na linha 9 e imprime o texto "O número ${numeroImparPositivo} não é positivo".
- Na linha 13, caso nenhuma condição seja verdadeira, imprime o texto "O número ${numeroImparPositivo} não é ímpar".

Com If Else é sempre bom cuidar da abertura e fechamento das chaves ```{}```, dito isso, existe uma forma tão eficiente quanto esta, porém menor.


# Entrada de Dados


O input (entrada de dados) pode ocorrer de diversas formas no ambiente da programação, tudo irá depender da linguagem e biblioteca. Neste início começaremos utilizando a função  ```prompt()```, esta recebe um TEXTO como entrada e esse texto podemos receber em uma variável, assim:

```
let texto = prompt("Digite seu texto aqui");
```

Para enteder melhor podemos separar em duas partes ```let texto``` e ```prompt("Digite seu texto aqui")```, na primeira parte temos:

- A criação da variável texto, do tipo ```let```, ou seja, que pode receber outro valor posteriormente.

Na segunda parte temos:

- A chamada da função ```prompt()``` - por padrão toda função possui ```()``` ao final do nome - onde recebe um texto como parâmetro ```"Digite seu texto aqu"```. As áspas dão sentido a essa frase como um texto. Por fim a função pede ao usuário que digite um texto, por meio de uma entrada visual em tela.

Então, juntando tudo temos:

-> A chamada da função ```prompt()``` recebe como entrada de dados do usuário um texto que é atribuído a variável ```texto``` do tipo ```let```.


## Entrada de Dados Numérica

Para entradas de dados do tipo numérica nós podemos utilizar uma função de conversão, ou seja, que converterá o conteúdo de texto para número. Tal função é o ```parseInt()``` e pode ser utilizado da seguinte forma:

```
const texto = prompt("Digite seu texto aqui");

let numero = parseInt(texto);
```

Observando o trecho temos,

- Na linha 1 o recebimento de um texto e o armazenamento na variável ```texto```.
- Na linha 3, a chamada da função ```parseInt()```, enviando a variável ```texto``` como parâmetro, e atribuido o resultado dessa chamada à variável ```numero```.

Esse trecho pode ser simplificado da seguinte forma:

```
let numero = parseInt(prompt("Digite seu texto"));
```

Dessa forma enviamos direto a função ```prompt()``` como parâmetro da função ```parseInt()```, sem a criação de variáveis extras.


### Erros

Durante a programação é normal testarmos para verificar se tudo está correndo bem, dito isso, é natural que alguns erros ocorram por tentar receber um valor do tipo errado, por exemplo:

- Tentar receber um texto em uma entrada numérica.

Mais adiante no conteúdo lidaremos melhor com tratamento de dados, mas no momento vocês conseguem lidar com o conteúdo atual.

