# Tipo Primitivos

Como tipos primitivos entendemos aqueles tipos de informação mais usuais e básicos. São os habituais de outras linguagens de programação. Descreveremos algum dado para ter em conta em cada tipo.

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

Wrapper vem do verbo inglês "wrap" que significa envolver. Eles são um nome adicional ao padrão de projeto Decorator. Tem como principal função "envolver coisas" adicionando funcionalidade à elas.

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
- O java conta com 8 wrappers para tipos primitivos.
- E existe dezenas wrappers: Para tratar o fluxo de conexões como orientado a objetos(ObjectInputStream), fluxos de audio(AudioInputStream), baseados em tipos primitivos(DataInputStream), ou adicionar buffers(BufferedInputStream) a eles.
- Apesar de temos Wrappers, ainda usamos tipos primitivos, em alguns casos, por serem mais rápidos e consomem menos memória.

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

## Modificadores de Acesso

public: Pode ser acessada de qualquer lugar por qualquer entidade que possa visualizar a classe a que ela pertence.

private: Os métodos e atributos da classe definidos como privados não podem ser acessados ou usados por nenhuma outra classe. Esses atributos e métodos também não podem ser visualizados pelas classes herdadas.

protected: Pode ser acessada apenas por quem está no mesmo pacote.

Modificadores podem ser aplicados pelos atributos e métodos, uma vez que não faz muito sentido criar deixar uma classe privada.

### Abstract

abstract:Esse modificador não é aplicado nas variáveis,

- Uma classe abstracta é apenas uma ideia de uma classe, ela não vai virar um objeto.
- Lembrando que os metódos abstratos não tem corpo.
- Se um classe tiver um metódo abstrato a classe tem que ser abstrata!

### Static

É usado para a criação de uma variável que poderá ser acessada por todas as instâncias de objetos desta classe como uma variável comum, ou seja, a variável criada será a mesma em todas as intâncias e quando seu conteúdo é modificado numa das instâncias, a modificação ocorre em todas as demais. E nas declarações de métodos ajudam no acesso direto à classe, portanto não é necessários instanciar um objeto para acesar o método.

### Final

Quando aplicado na classe, não permite estender, nos métodos impede que o mesmo seja sobrescrito(overriding) na subclasse, e nos valores de variáveis não pode ser alterado depois que já tenha sido atribuído um valor.

### Interfaces

Métodos abstratos
    Devem ser implementados por todos;
    Novos métodos quebram as implementações;
Métodos default
    São herdados a todos que implementam;
    Novos métodos não quebram as implementações;

### Enums

- Basicamente é dicionários de dados imutável;
- Não é permitido criar novas intâncias;
- O construtor é sempre declarado como private;
- Por convenção, por serem objetos constantes e imutáveis(static final), os nomes são em MAIÚSCULOS.
