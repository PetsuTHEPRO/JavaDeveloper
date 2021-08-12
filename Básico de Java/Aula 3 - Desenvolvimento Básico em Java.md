### String 

```
public class TestAutoBoxingWrapper {
    public static void main(String[] args){

        var nome = "André";
        var sobreNome = "Gomes";
        final var nomeCompleto = nome + sobreNome;

        System.out.println("nome do cliente:" + nome + sobreNome);
        var string = new String("Minha String");

        // Aula sobre String | Método charAt()
        // Retorna o caractere na posição indicada!!
        System.out.println("Caractere na posição: " + string.charAt(5));

        // Aula sobre String | Método length()
        // Retorna o tamanho da String!!
        System.out.println("Quantidade= " + string.length());

        // Aula sobre String | Método trim()
        // Remove a parte branca antes de depois!!
        System.out.println("Sem trim [" + string + "]");
        System.out.println("Com trim [" + string.trim() + "]");

        // Aula sobre String | Método toLowerCase()
        // Retorna a string em LowerCase!!
        System.out.println("Lower: " + string.toLowerCase());

        // Aula sobre String | Método toUpperCase()
        // Retorna a string em UpperCase!!
        System.out.println("Upper: " + string.toUpperCase());

        // Aula sobre String | Método contains()
        // Retorna se contém o char!!
        System.out.println("Contém M?" + string.contains("M"));
        System.out.println("Contém X?" + string.contains("X"));

        // Aula sobre String | Método replace()
        // Retorna a String trocando um char por outro!!
        System.out.println("Replace/troca " + string.replace("n","$"));

        // Aula sobre String | Método equals()
        // Retorna true ou false, quando a string é igual!!
        System.out.println("Equals " + string.equals(" Minha String "));

        // Aula sobre String | Método equalsIgnoreCase()
        // Retorna true ou false, mas não verifica se é LowerCase ou UpperCase!!
        System.out.println("EqualsIgnoreCase?" + string.equalsIgnoreCase(" MiNhA StRiNG "));

        // Aula sobre String | Método substring()
        // Retorna o uma string nas posições iniciais até finais!!
        System.out.println("Substring(1,6)=" + string.substring(1,6));

        // Exercícios
        System.out.println("A B C D E F G".toCharArray());
        System.out.println("Aula de Java".split(" "));
        System.out.println("Aula".concat("de Java"));
        System.out.println("1234 asda qw".replaceAll("[0-9]","#"));

        // Aula sobre String | Método format
        final var mensagem = string.format("O cliente %s possui um sobrenome %s", nome, sobreNome);
        System.out.println(mensagem);

        System.out.println(String.format("Número %.2", 1.222d));
    }
}
```

**Regexp: Use [^A-Za-z0-9]**

# Java Data

Para importa as bibliotecas de datas:
import java.util.Date;

Essa biblioteca tem dois construtores que podemos utilizar, **Date() and Date(long date)**

**Date ()**

Este construtor vai alocar um objeto da classe Date e o inicializará com o milissegundo mais próximo do período da sua execução.

**Date(long date)**

Diferente do construtor anterior, esse construtor espera que você passe os milissegundos com base padrão de tempo(epoch) que usa como referência **1 de janeiro de 1970 00:00:00**.

>Uma pequena pausa... O que é o Epoch?
>"O epoch timestamp é um padrão largamente aceito para representar uma data como um inteiro 32-bits a partir do início do Unix Epoch..."

# Métodos Uteis para Trabalhar com Datas

**After and Before**:
```
Date dataAtual = new Date();
Date dataPassado = new Date(161312480761L);

boolean isAfter = dataAtual.after(dataPassado);
boolean isBefore = dataAtual.before(dataPassado);
// O primeiro método retorna true, se a data atual for posterior a data passado;
// O segundo método retorna true, se a data atual for anterior a data passado;

```

**compareTo and equals**:
```
Date dataNoPassado = new Date(1513124807691L);
Date dataNoFuturo = new Date(1613124807691L);
Date mesmaDataNoFuturo = new Date(1613124807691L);

boolean isEquals = dataNoFuturo.equals(mesmaDataNoFuturo);
//Retorna true se as datas são as mesmas.
//Retorna false se as datas forem diferentes.

int case1 = dataNoPassado.compareTo(dataNoFuturo); // Retorna -1, porque a data verificada é anterior.

int case2 = dataNoFuturo.compareTo(dataNoPassado); // Retorna 1, porque a data verificada é posterior.

int case3 = dataNoFuturo.compareTo(mesmaDataNoFuturo); // Retorna 0, porque a data verificada é a mesma.

```

**from e toInstant**

## Classe Instant

- Surgiu 1na JDK 1.8;
- Imutável e Thread safe;
- Modela um ponto instantâneo de uma linha do tempo;
- Indicado para gravar marcações temporais em eventos da sua aplicação;


## Calendar

Para importar e utilizar o calendar: **java.util.Calendar;**

**Calendar**: é uma classe abstrata que provê métodos para converter data entre um instante específico.

O Calendar possui alguns campos específicos para manipulação como MONTH, YEAR, HOUR etc.

Para pegar data atual você usar os métodos:

```
Calendar agora = Calendar.getInstance();

System.out.println(agora);

```

**Método .add(.MONTH or .DATE or .YEAR, 15 or -15);** 
// Esse método adiciona um valor na data instanciada;

Imprimindo datas e horas(Formatação): 

- System.out.println("%tc", agora); // Dom jul 14 20:58:11 BRT 2019
- System.out.println("%tF", agora); // 2019-07-14
- System.out.println("%tD", agora); // 07/14/19
- System.out.println("%tr", agora); // 08:58:11 PM
- System.out.println("%tT", agora); // 20:58:11