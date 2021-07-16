# Instalação

**Ferramentas**

- Gradle
- Maven
- IntelliJ

Link do Site: https://start.spring.io

1- Instalar o Maven e Gradle.

2- Configurar variaveis de ambiente.

3- Depois abrir o site anterior e baixar um projeto.

4- Importar um projeto no IntelliJ.

# O que precisamos saber sobre Java

- O que é Java?
Java é uma linguagem de programaçãoe plataforma computacional lançada em 1995 pela **Sun Microsystems**, por um time comandado por **James Gosling**. Anos depois foi adquirida pela **Oracle**.

Diferente de outras linguagens de programação, que são **compiladas** para **código nativo**, o Java é compilado para um **bytecode** que é interpretado por uma **máquina virtual**.

- O que é compilador?
Um **compilador** é um **programa** que, a partir de um **código fonte**, cria um programa semanticamente equivalente, porém escrito em outra linguagem, **código objeto**. Um compilador traduz um programa de uma linguagem textual para uma linguagem de máquina, específica para um processador e sistema operacional.

O nome compilador é usado principalmente para os programas que traduzem o **código fonte** de uma **linguagem de programação de alto nível** para uma **linguagem de programação de baixo nível**(pro exemplo, **Assembly** ou **Código de Máquina**).

- O que é bytecode?
É o **Código originado** da compilação de programa Java.

O bytecodeé o programa interpretado e executado pela Máquina Virtual Java, JVM.

- O que é JVM?
Antes de explicar o que é uma JVM, vamos entender o que é uma VM!

Uma VM é uma Máquina Virtual, ou Virtual Machine, é um software que simula uma máquina física e consegue executar vários programas, gerenciar processos, memória e arquivos. Tudo isso faz parte de uma plataforma com memória, processador e outros recursos totalmente virtuais, sem dependência de hardware.

Então, uma JVM é uma máquina virtual que executa programas Java, executando os bytecodes em linguagem de máquina para cada sistema operacional.

| Código Java (.java) | -- (Compilador **javac**) --- > | bytecode (.class) | ----[ JVM ]---- > Linux, Windows, MacOS  

- O que é JRE?
JRE significa Java runtime Environment, ou Ambiente de Execução do Java, é composto pela Java Virtual Machine(JVM), bibliotecas e APISs da linguagem Java e outros componentes para suporte da plataforma Java.

Ele representa a parte responsável pela execução do software Java.

- O que é JDK?

Java Development Kit(JDK), Kit de Desenvolvimento Java, é um conjunto de utilitários que permitem criar software para a **plataforma Java**. É composto pelo **compilador Java, bibliotecas** da linguagem, ferramentas e a JRE.

- O que é Java SE?

Java Standard Edition(SE), é a distrivbuição mínima da plataforma de desenvolvimento de aplicações Java.

OpenJDK é a implementação de referência opensource da Plataforma Java, Java Se, que ainda é mantida pela Oracle.

- O que é Java EE?

Java **Enterprise Edition**, é uma extensão da Java SE que possui suporte a desenvolvimento de sistema corporativos.

Além do mínimo da plataforma, o Java EE possui diversas especificações de partes da infraestrutura de aplicações, como acesso a banco de dados, mensageria, serviços web, parser de arquivos e outras.

Ex: JBoss (RedHat), Weblogic (oracle), WebSphere(IBM).

- O que é Jakarta EE?

Com a falta de investimento da Oracle no Java, ela cedeu todo o código, implementações e especificações do Java EE para a Eclipse Foundation, mas como o nome Java EE é uma marca registrada, foi escolhido o nome Jakarta EE.

Agora a evolução da especificações e padrões do Java será feito sob o nome Jakarta EE, com compatibilidade com o Java EE.