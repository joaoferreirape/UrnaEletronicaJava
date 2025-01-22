# UrnaEletronicaJava

Este é um projeto acadêmico que objetiva exercitar os conceitos da **Programação Orientada a Objetos - POO** através da codificação de uma **Urna Eletrônica** na linaguagem **Java**.

Elaborado como proposta educacional para alunos dos cursos de computação.

## Requisitos

### Funcionais

1. Candidatos Pré-Configurados: A urna deve conter 5 candidatos fictícios, com nome e número pré-definidos. Sugestão de candidatos (inspirados em figuras da ciência e música):
    * 01 - Ada Lovelace
    * 02 - Alan Turing
    * 03 - Marie Curie
    * 04 - Albert Einstein
    * 05 - Ludwig van Beethoven
1. Entrada de Votos: O programa deve solicitar ao usuário a entrada de 10 votos, um por vez, pelo console. O usuário deve digitar o número do candidato.
1. Validação de Votos: O programa deve validar se o número digitado corresponde a um candidato válido (entre 01 e 05). Caso o número seja inválido, o programa deve exibir uma mensagem de erro e solicitar a entrada de um novo voto. Votos nulos (qualquer entrada que não seja um número entre 01 e 05) devem ser contabilizados separadamente.
1. Apuração dos Votos: O programa deve contabilizar os votos de cada candidato e os votos nulos.
1. Exibição dos Resultados: Ao final da votação (após receber 10 votos válidos), o programa deve exibir:
    * O número de votos recebidos por cada candidato.
    * O percentual de votos de cada candidato em relação ao total de votos válidos.
    * O número de votos nulos.
    * O nome do candidato vencedor (aquele com o maior número de votos válidos). Em caso de empate, informar que houve empate.

### Não-funcionais

1. Repositório git com o nome UrnaEletronicaJava
1. O repostiório deverá ser público
1. O repositório deverá conter um README.md
1. O repositório deverá conter o LICENSE, padrão Creative Commons provido pelo próprio GitHub
1. Projeto desenvolvido utilizando o Visual Studio Code ou qualquer outro editor de texto simples, não utilizar nenhuma IDE Java
1. O projeto deverá conter um arquivo/classe UrnaEletronicaJava contendo o método main() que chamará todo o restante do código.
1. Sugestão de Estrutura de Classes:
    * Candidato:
        * Atributos: nome (String), numero (int), votos (int).
        * Construtor: Recebe nome e número.
        * Métodos: getNome(), getNumero(), getVotos(), incrementarVotos().
    * UrnaEletronicaJava:
        * Atributos: candidatos (um array ou ArrayList de objetos Candidato), votosNulos (int).
        * Construtor: Inicializa os candidatos pré-configurados.
        * Métodos: receberVoto(int numero), apurarResultados(), exibirResultados().
        * Método main() para executar a simulação.

### Exemplo de interação com o usuário

```bash
Bem-vindo à Urna Eletrônica!

Candidatos:
01 - Ada Lovelace
02 - Alan Turing
03 - Marie Curie
04 - Albert Einstein
05 - Ludwig van Beethoven

Digite o número do seu candidato: 02
Digite o número do seu candidato: 01
Digite o número do seu candidato: 06
Digite o número do seu candidato: 03
... (continua até 10 votos válidos)

Resultado da Votação:

Ada Lovelace: 3 votos (30.0%)
Alan Turing: 2 votos (20.0%)
Marie Curie: 4 votos (40.0%)
Albert Einstein: 0 votos (0.0%)
Ludwig van Beethoven: 1 voto (10.0%)
Votos Nulos: 0

Vencedor: Marie Curie
```

## Pré-requisitos de infraestrutura

A fim de suportar o desenvolvimento do projeto utilizando Microsoft Windows, recomendo utilizar a infraestrutura básica descrita a seguir.

*Observação*: Há um conjunto de variáveis de ambiente necessárias ao bom funcionamento do ambiente de desenvolvimento. Adapte-as conforme necessário e de acordo com o seu sistema.

*Observação*: Atente para atualizar nos exemplos a seguir os números de versão e caminho das ferramentas que forem instaladas.

* Client git (git-scm): [https://git-scm.com/downloads](https://git-scm.com/downloads)
    * git config --global user.name "Seu nome, pode espaços e acentos"
    * git config --global user.email "email@que.faz.login.no.git"
    * git config --global credential.helper store
    * git config --global init.defaultbranch main
    * git config --list
* Oracle Java 17: [https://www.oracle.com/br/java/technologies/downloads/#java17](https://www.oracle.com/br/java/technologies/downloads/#java17)
    * Nome da variável    _JAVA_OPTIONS
        * Valor da variável   -Dswing.aatext=true -Dawt.useSystemAAFontSettings=on
    * Nome da variável    JAVA_OPTIONS
        * Valor da variável   -Dswing.aatext=true -Dawt.useSystemAAFontSettings=on
    * Nome da variável    JAVA_EXE
        * Valor da variável   C:\Work\Apps\Oracle\Java\jdk-17\bin\java.exe
    * Nome da variável    JAVA_HOME
        * Valor da variável   C:\Work\Apps\Oracle\Java\jdk-17
    * Nome da variável    JDK_HOME
        * Valor da variável   C:\Work\Apps\Oracle\Java\jdk-17
    * Nome da variável    JRE
        * Valor da variável   C:\Work\Apps\Oracle\Java\jdk-17
    * Nome da variável    JRE_HOME
        * Valor da variável   C:\Work\Apps\Oracle\Java\jdk-17
    * Adicione uma entrada no PATH do Windows.
        * Ainda em VARIÁVEIS DO SISTEMA, dê dois cliquem em PATH, e depois clique em novo e adicione a entrada:
        * C:\Work\Apps\Oracle\Java\jdk-17\bin
        * Clique em MOVER PARA CIMA e deixe este caminho acima em primeiro na lista.
* Apache Maven:
    * Nome da variável    MAVEN_HOME
        * Valor da variável   C:\Work\Apps\Apache\Maven\apache-maven-3.9.9
    * Nome da variável    M2
        * Valor da variável   C:\Work\Apps\Apache\Maven\apache-maven-3.9.9\bin
    * Nome da variável    MAVEN_OPTS
        * Valor da variável   -Xms256m -Xmx512m
    * Adicione uma entrada no PATH do Windows.
        * Em VARIÁVEIS DE AMBIENTE, dê dois cliquem em PATH, e depois clique em novo e adicione a entrada:
        * C:\Work\Apps\Apache\Maven\apache-maven-3.9.9\bin
* Gradle:
    * Nome da variável    GRADLE_HOME
        * Valor da variável   C:\Work\Apps\Gradle\gradle-8.12
    * Adicione uma entrada no PATH do Windows.
        * Em VARIÁVEIS DE AMBIENTE, dê dois cliquem em PATH, e depois clique em novo e adicione a entrada:
        * C:\Work\Apps\Gradle\gradle-8.12\bin
* Microsoft Visual Studio Code: [https://code.visualstudio.com/Download](https://code.visualstudio.com/Download)
    * Defina nas configurações do VSCode para que utilize o *Command Prompt* ou *cmd* como padrão para o terminal no Windows. Evite o *Powrshell* ou qualquer outro que tenha instalado.
    * Extension Pack for Java: [https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack)

Após instalar as ferramentas e definir as variáveis de ambiente, reinicie seu computador.

Para testar tudo que fora instalado e configurado, abra o command prompt e digite cada um dos comandos a seguir:

* java -version
* javac -version
* mvn --version
* gradle --version

## Edição local

Clone o repositório em sua máquina e edite o código com seu editor LaTeX de preferência:

```bash
git clone https://github.com/joaoferreirape/UrnaEletronicaJava.git
```

## Contribuindo

Por favor leia [CONTRIBUTING.md](https://github.com/joaoferreirape/UrnaEletronicaJava/blob/main/CONTRIBUTING.md) para detalhes sobre os processos de submissão das suas contribuições via pull request.

## Autores

* **João Ferreira** - [https://github.com/joaoferreirape](https://github.com/joaoferreirape)

Veja a lista de pessoas que eventualmente tenha contribuído com este projeto: https://github.com/joaoferreirape/UrnaEletronicaJava/graphs/contributors

## Licença

Este projeto está sob a licença [CC0 1.0 Universal - Creative Commons License ](https://github.com/joaoferreirape/UrnaEletronicaJava/blob/main/LICENSE) - veja o arquivo [LICENSE](https://github.com/joaoferreirape/UrnaEletronicaJava/blob/main/LICENSE) para detalhes.
