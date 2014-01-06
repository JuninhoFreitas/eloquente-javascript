# Eloquente JavaScript

### 2ª edição

Uma moderna introdução ao JavaScript, programação e maravilhas digitais.

[[nova capa aqui]]

### Escrito por **Marijn Haverbeke**

#### Traduzido por **[Eric Oliveira](https://github.com/eoop/eo_op)**

Licensiado sobre licença [Creative Commons attribution-noncommercial.](http://creativecommons.org/licenses/by-nc/3.0/) Todo código neste livro também pode ser considerado sobre [licença MIT](http://opensource.org/licenses/MIT).

Ilustrações por vários artistas: *Sea of bits* (capítulo 1) e *weresquirrel* (capítulo 4) por Margarita Martínez e José Menor. Mysterious computer (introdução) por Philip Tyrer.

## Conteúdo

* [Introdução](https://github.com/eoop/eloquente-javascript#introdu%C3%A7%C3%A3o)
1. [Valores, Tipos e Operadores]()
2. [Estrutura do Programa]()
3. [Funções]()
4. [Estrutura de Dados: Objeto e Array]()
5. [Funções de Ordem Superior]()
6. [A Vida Secreta dos Objetos]()
7. [Prática: Vida Eletrônica]()
8. [Erros e Manipulação de Erros]()


---

# Introdução

Este livro é sobre conversar com computadores. Computadores se tornaram uma das ferramentas fundamentais do nosso tempo. Ser capaz de controlá-los efetivamente é uma habilidade extremamente útil. Com a mentalidade certa, também pode ser muito divertido!

Há uma lacuna entre nós, organismos biológicos models com um talento para o raciocínio espacial e social, e o computador, um simples manipulador de dados insignificantes, sem nossos preconceitos e instintos. Felizmente, tivemos um grande progresso em preencher essa lacuna nos últimos sessenta anos.

A história da interação humano-computador tem se afastado da ideia fria e reducionista do mundo sobre o computador, apresentando camadas mais amigáveis em cima disso. As duas ideias mais importantes neste processo tem sido o uso de linguagens de computador, que mapeiam bem para o nosso cérebro por se parecer com as linguagens que usamos para conversas uns com os outros, e interfaces gráficas apontar e clicar (ou toque), que nós facilmente por causa de imitar o mundo tangível fora da máquina.

![Mysterios Computar](http://eloquentjavascript.net/2nd_edition/preview/img/mysterious-computer.jpg)

Interfaces gráficas tendem a ser mais fáceis descobrir que linguagens - detectar um botão é mais rápido do que aprender uma gramática. Por essa razão, eles se tornaram a forma dominante de interagir com sistemas orientados ao consumidor. Compare com os telefones atuais, onde você pode realizar todo tipo de tarefa tocando e passando os elementos que aparecem na tela, com o *Commodore 64* de 1982, o aparelho que me introduziu a computação, onde tudo que você recebia era um cursor piscando, e você conseguia isto digitando comandos.

Obviamente, o telefone *touchscreen* é mais acessível, e é inteiramente apropriado que esses dispositivos utilizem uma interface gráfica. Mas as interfaces baseadas em linguagens têm outra vantagem - uma vez que você aprenda esta linguagem, ela tende a ser mais expressiva, tornando mais fácil compor a funcionalidade fornecida pelo sistema de novas maneiras, e até mesmo criando seus próprios blocos de construção.

Com o *Commodore 64*, quase todas as tarefas no sistema eram realizadas dando comandos embutidos na linguagem da máquina (um dialeto da linguagem de programação BASIC). Isto permitia aos usuários gradualmente progredir de simplesmente usar o computador (carregando programas) para de fato programá-los. Você estava *dentro* de um ambiente de programação desde o início, em vez de ter que procurar ativamente por um.

Isto foi perdido pela mudança para as interfaces gráficas de usuário. Mas as interfaces baseadas em linguagem, na forma de linguagens de programação, continuam aqui, em cada máquina, em grande parte escondida do usuário comum. Uma tal linguagem, JavaScript, está disponível em quase todos os dispositivos de consumidores como parte de um navegador web.

Este livro pretende torná-lo familiar com esta linguagem o suficiente para que você seja capaz de fazer com o computador o que você quiser.

# Na Programação

> Eu não esclareço os que não estão prontos para aprender, nem desperto aqueles que não estão ansiosos para dar uma explicação a si próprios. Se eu apresentei um canto da praça, e eles não podem voltar para mim com os outros três, eu não deveria passar por estes pontos novamentes. **Confúcio**

Antes de explicar JavaScript, eu também quero introduzir os princípios básicos de programação. Programação, ao que parece, é difícil. As regras fundamentais são claras e simples. Mas programas, criados em cima destas regras básicas, tendem a tornar-se complexos o suficiente para introduzir suas próprias regras e complexidades. Você está construindo seu próprio labirinto, e pode simplesmente perder-se nele.

Para tirar algum proveito deste livro, mais do que apenas uma leitura passiva é necessário. Trate de ficar atento, faça um esforço para entender o exemplo de código, e somente continue quando você estiver razoavelmente seguro que você entendeu o material que veio antes.

> O programador de computadores é um criador de universos no qual ele é o único responsável. Universos de complexidade virtualmente ilimitada podem ser criados sob a forma de programas de computador. **Joseph Weizenbaum, Computer Power and Human Reason**

Um programa é muitas coisas. É um pedaço de texto digitado por um programador, que é a força direta que faz que o computador faça o que faz, são dados na memória do computador, mas ele controla as ações realizadas nesta mesma memória. Analogias que tentam comparar programas com objetos que somos familiares tendem a ser insuficientes. Uma conexão superficial é a com uma máquina - muitas partes separadas tendem a ser envolvidas, e para fazer o conjunto todo precisamos considerar as maneiras que estas partes se interconectam e contribuam para a operação do todo.

Um computador é uma máquina feita para atuar como um hospedeiro para estas máquinas imateriais. Computadores por si próprios podem somente fazer coisas estúpidas e simples. A razão deles serem tão úteis que eles fazem coisas em uma velocidade incrível. Um programa pode ingenuamente combinar enormes números de simples ações ao invés de fazer coisas complicadas.

Para muitos de nós, escrever programas de computador é um fascinante jogo. Um programa é uma construção do pensamento. Não tem custos de construção, é leve e cresce facilmente ante nossas digitações.

Se não formos cuidadosos, seu tamanho e complexidade vão aumentar fora de controle, confundindo até a pessoa que o criou. Este é o principal problema da programação: manter os programas sobre controle. Quando um programa funciona, ele é lindo. A arte de programar é a habilidade de controlar a complexidade. Um grande programa é suave, é simples em sua complexidade.

Alguns programadores acreditam que esta complexidade é melhor gerenciada usando somente um pequeno conjunto de técnicas bem entendidas em seus programas. Eles compõe regras rígidas (*"boas práticas"*) prescrevendo a forma que programas devem ter, e os mais zelosos sobre isso vão considerar aqueles que saem desta pequena zona de segurança *maus programadores*.

Quanta hostilidade perante a riqueza da programação - tentar reduzir a algo simples e previsível, colocando um tabu em todos os lindos e misteriosos programas! A paisagem das técnicas de programação é enorme, fascinante em sua diversidade, e permanece largamente inexplorada. É sem dúvida perigoso ir neste caminho, atraindo o programador inexperiente em todo tipo de confusão, mas isso só significa que você deve proceder com cautela e manter o juízo. Conforme você aprende, sempre haverá novos desafios e novos territórios a ser explorados. Programadores que recusam de manter-se explorando vão estagnar, esquecer sua alegria, e ficar entediado com seu trabalho.

# Porque linguagens importam?

No começo, no nascimento da programação, não havia linguagens de programação. Programas pareciam algo desta forma:

00110001 00000000 00000000
00110001 00000001 00000001
00110011 00000001 00000010
01010001 00001011 00000010
00100010 00000010 00001000
01000011 00000001 00000000
01000001 00000001 00000001
00010000 00000010 00000000
01100010 00000000 00000000

Este é um programa que soma os números do 1 ao 10 e imprimi o resultado (1 + 2 + ... 10 = 55). Isso pode rodar em uma muito simples, uma máquina hipotética. Para programar os primeiros computadores, era necessário configurar grandes arrays de chaves na posição certa, ou fazer furos em cartões e alimentá-los no computador. Você pode imaginar como isso era tedioso, e um procedimento propenso ao erro. Mesmo escrever simples programas requeriam muita habilidade e disciplina. Os complexos eram quase inconcebíveis.

Claro, inserindo manualmente estes padrões misteriosos de bits (1 e 0) fez que o programador tivesse uma profunda sensação de ser um poderoso feiticeiro. E isto tem que valer alguma coisa em termos de satisfação no trabalho.

Cada linha do programa contém uma simples instrução. Isto pode ser escrito assim:

1. Guarde o número 0 na posição da memória 0.
2. Guarde o número 1 na posição da memória 1.
3. Guarde o valor da posição da memória 1 na posição da memória 2.
4. Subtraia o número 11 do valor na posição da memória 2.
5. Se o valor na posição da memória 2 é o número 0, continue com a instrução 9.
6. Adicione o valor da posição da memória 1 para posição de memória 0.
7. Adicione o número 1 ao valor da posição de memória 1.
8. Continue com a instrução 3.
9. Retorne o valor da posição da memória 0.

marcador : http://eloquentjavascript.net/2nd_edition/preview/00_intro.html#p_M+oRlzgd8m
