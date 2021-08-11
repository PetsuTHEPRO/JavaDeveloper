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

