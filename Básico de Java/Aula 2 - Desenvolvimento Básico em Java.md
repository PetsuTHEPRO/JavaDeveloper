# Tipo Primitivos

Como tipos primitivos entendemos aquelas tipos de informação mais usuais e básicos. São os habituais de outras linguagens de programação. Descreveremos algum dado para ter em conta em cada tipo.

- **Boolean**: Não é um valor numérico, só admite os valores true ou false.

- **Char**: Usa o código UNICODE e ocupa cada caractere 16 bits.

- **Inteiros**: Diferem nas precisões e podem ser positivos ou negativos.

    - Byte: 1 byte.
    - Short: 2 bytes.
    - Int: 4 bytes.
    - Long: 8 bytes.

- **Float**: Igual que os inteiros também diferem nas precisões e podem ser positivos ou negativos.
    - Float: 4 bytes.
    - Double: 8 bytes.

# Wrappers

 Tipo          | Tipo Primitivo | Classe Wrapper | Subclasse |
 --------------|----------------|----------------|-----------|
 Lógico        | Boolean        | Boolean        | Object    |
 Caractere     | Char           | Caracter       | Object    |
 Integral      | byte           | Byte           | Number    |
 Integral      | short          | Short          | Number    |
 Integral      | int            | Integer        | Number    |
 Integral      | long           | Long           | Number    |
 Ponto Fluante | float          | Float          | Number    |
 Ponto Fluante | Double         | Double         | Number    |

- São os Objetos que representam os primitivos.
- Auto-Boxing e Unboxing.

Após o Java 5 surgiu a funcionalidade do Autoboxing onde o próprio Java já converte o tipo primitivo em Wrapper se este achar que é necessário.

**AutoBoxing** 

```
HashMap hashMap = new HashMap();
hashMap.put(10, “Carlos”);
hashMap.put(11, “Jose”);
hashMap.put(12, “Pedro”);
```

> Exemplo: Integer integer = 9;

**Boxing Conversion**

O Boxing é a conversão de tipos primitivos em seu respectivo Wrapper correspondente.

```
Boolean meuBoolean = true;
//a conversão é feita de forma automática para o boolean
Integer meuInteger = 1203;
Double meuDouble = 10.20;
```

Obs: É claro que se você tentar realizar um Boxing Conversion de um tipo primitivo para um Wrapper errado você terá um errode compilação.

**Unboxing Conversion**

É o processo inverso do autoboxing, convertendo um objeto proveniente de uma classe que acondiciona um tipo primitivo para um valor primitivo. Para exemplificar o emprego de unboxing, basta fazer o oposto dos exemplos de autoboxing.

> Exemplo:
> int in = 0;
> in = new Integer(9);

Leitura importante parte 1: https://www.devmedia.com.br/autoboxing-e-unboxing-em-java/28620
Leitura importante parte 2: https://www.devmedia.com.br/conhecendo-as-classes-wrappers-autoboxing-e-auto-unboxing/7384

> Importante ressaltar que o operador "==" tem que ser usado apenas quando for comparar variáveis de tipo primitivos, então para comparar Wrapper utilizamos **equals**, pois por causa do padrão de projeto Flyweigth