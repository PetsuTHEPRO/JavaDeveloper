## Tomadas de Decisão

"Quando escrevemos programas, geralmente ocorre a necessidade de decidir o que fazer depedendo de alguma condição encontrada durante a execução"

## Concatenação

Concatenação é um termo usado em computação para designar a operação de unir o conteúdo de duas string.

string é uma sequência de caracteres.

**Definição**: Agrupamento de duas ou mais células que, incluindo fórmulas, textos ou outras informações contida no seu interior, dá origem a um único resultado.

## Estrutura de Repetição

**Definição**: Dentro da lógica de programação é uma estrutura que permite executar mais de uma vez o mesmo comando ou conjunto de comandos, de acordo com uma condição ou com um contador.

Quando uma condição no laço de repetição não é cumprida, o laço entra em loop e nunca acaba.

**Definição de Linguagem de Programação**: Linguagem de Programação é uma linguagem escrita e formal que especifica um conjunto de instruções e regras usadas para gerar programas(software). Um software pode ser desenvolvido para rodar em um computador, dispositivo móvel ou em qualquer equipamento que permita sua execução.

**Alto Nível**: Essas são aquelas cuja sintaxe se aproxima mais da nossa linguagem e se distanciam mais da linguagem de máquina.

**Baixo Nível**: É aquela que se aproxima mais da linguagem de máquina. Essas são as que você precisa ter o conhecimento direto da arquitetura do computador para fazer alguma coisa.

**Compiladas**: É uma linguagem de programação em que o código fonte, é executado diretamente pelo sistema operacional ou pelo processador, após ser traduzido por meio de um processo chamado compilação.

**Interpretadas**: É uma linguagem de programação em que o código fonte é executado por um programa de computador chamado interpretador, que em seguida é executado pelo sistema operacional ou processador.

Link da IDE do Portugol: https://github.com/UNIVALI-LITE/Portugol-Studio/releases/

## Desvio Condicional

- Se: É utilizada a palavra reservada **se**, a condição a ser testada entre parenteses e as instruções que devem ser executadas entre chaves caso o desvio seja **verdadeiro**.


Exemplo de Programa usando o **se**:

```
se(media>=7){
    escreva("Parabéns! Você foi aprovado.")
}
senao{
    escreva("Infelizmente, você foi reprovado.")
}
```

Exemplo de Programa: Menu

```
    escreva("1- Abrir Netflix 2- Abrir Amazon Prime 3- Abrir HBO GO 4- Sair")
    inteiro menu = 0
    escreva("Sua opção:")
    leia(menu)

    se(menu==1){
        escreva("OK!! Abrir Netflix!!")
    }
    
    se(menu==2){
        escreva("OK!! Abrir Amazon Prime!!")
    }
    se(menu==3){
        escreva("OK!! Abrir Abrir HBO GO!!")
    }
    se(menu==4){
        escreva("Saindo...")
    }
```

## Laço de Repetição

Dentro da lógica de programação é uma estrutura que permite executar mais de uma vez o mesmo comando ou conjunto de comandos, de acordo com uma condição ou com um **contador**.

```
funcao inicio(){

    inteiro contador, limite, resultado
    contador = 0
    limite = 10
    faca{
        resultado = 9 * contador
        escreva("9 X " + contador + "=" + resultado + "\n")
        contador++ 
    }enquanto(contador <= limite)
}
```

## Matriz e Vetores

Uma matriz é uma coleção de variáveis de mesmo tipo, acessíveis com um único nome e armazenados contiguamente na memória.

A individualização de cada variável de um vetor é feita através do uso de índices.

Os vetores são matrizes de uma só dimensão.

**Exercício final**

inteiro dadosCliente[][] = {{"João", "São Paulo", "(11) 9999-5241"}, {"Maria", "Ribeirão Preto", "(16) 9999-8596"}, {"Ana","Manaus","(92) 9999-8574"}}