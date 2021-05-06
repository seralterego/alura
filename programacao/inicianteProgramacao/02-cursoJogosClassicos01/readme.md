p# Curso de Jogos clássicos parte 1: Iniciando no JavaScript com Pong

<!-- LEGENDAS para ÍCONES:
  - :link:               = Links da web
  - :running::dash:      = Fazendo
  - :books:              = Conteúdo
  - :memo:               = Exercícios
  - :white_check_mark:   = Feito
  - :dart:               = Módulo Concluído
  - :trophy:             = Medalhas
  - :information_source: = Informação importante
  - :name_badge:         = Certificado
  - :warning:            = Prioridades
  - :page_facing_up:     = para Artigos
  - :tada:               = para Eventos
  - :notebook:           = Conteúdo extra com Livro
  - :blue_book:          = Conteúdo extra da Alura+
  - :headphones:         = Conteúdo em áudio
  - :tv:                 = Conteúdo em vídeo
-->

:link: <https://cursos.alura.com.br/course/pong-javascript>

> **Faça esse curso de Lógica de promgração e:**
> - Desenvolva um jogo do zero em duas linguagens de promgração diferentes
> - Dê seus primeiros passos no mundo do JavaScript
> - Aprenda a trabalhar com variáveis e funções
> - Crie um jogo completo, com animações, controles, sons e placar
> - Saiba como utlizar em seus projetos um código compartilhado no Github.

---

## AULAS

### Pong no Scratch

#### **Introdução**
>
> (...) e neste curso iremos desenvolver o primeiro jogo lucrativo da história, um jogo de esporte conhecido por Pong, que simula um tênis de mesa. (...)
>
> Inicialmente, vamos desenvolvê-lo utilizando a linguagem Scratch. (...) Em seguida, após aperfeiçoarmos nossa lógica de programação, desenvolveremos o mesmo jogo utilizando outra linguagem, o JavaScript.

#### **Preparando o ambiente**
>
> Olá, neste curso vamos criar um jogo do zero, utilizando duas linguagens de programação diferentes: [Scratch](https://scratch.mit.edu/) e [Javascript](https://www.caelum.com.br/apostila-html-css-javascript/38CA-eventos-com-javascript#caracteristicas-da-linguagem) dentro do [P5](https://editor.p5js.org/).
> <hr>
> Neste treinamento, não usaremos uma IDE como VSCode, pois para executar a biblioteca precisaríamos subir um servidor e esse não é o objetivo do curso. Vamos dedicar toda atenção apenas no JavaScript.
> <hr>
>
> Vamos desenvolver o jogo do [Pong](https://pt.wikipedia.org/wiki/Pong), que é um jogo eletrônico de esporte que simula uma partida de tênis de mesa.
>
> Você precisa de um cadastro para salvar e compartilhar seus projetos dentro do Scratch.

Feito isso, podemos começar.

#### **Bolinha e minha raquete**
>
> Vamos começar a criar nosso jogo de Pong com o Scratch, para fortalecermos nossa lógica de programação! Relembrando que a bolinha atuará em posições aleatórias, e temos que acertá-la, colidindo com ela por meio das raquetes. Acessaremos o [site do Scratch](http://scratch.mit.edu/) — caso não esteja logado em sua conta, na etapa anterior há uma explicação de preparação do ambiente, com um passo a passo do que é necessário para criá-la.
>
> Clicaremos em "Criar", no menu superior, e para configurarmos a língua utilizada, poderemos clicar no ícone de globo localizado no menu do topo, e selecionar "Português Brasileiro". No Pong, temos um fundo preto, e a bolinha e as raquetes na cor branca. Vamos deletar o gatinho clicando no "x" do painel inferior direito, ou clicando com o lado direito do mouse e selecionando "Apagar".
>
> Feito isso, clicaremos no painel "Palco", no canto inferior direito, na aba "Cenários" no painel principal, e trocaremos a cor de preenchimento para preto, que será a mesma cor do contorno. Selecionaremos a ferramenta de quadrado e criaremos um que ocupe todo o espaço disponível.
>
> Para criarmos a bolinha, clicaremos no ícone com a face de um gato no canto inferior direito da tela para selecionarmos um **ator**, que pode ser algum próprio da galeria do Scratch. No caso, queremos personalizá-lo, portanto clicaremos na opção "Pintar", o que abrirá um editor bem similar ao que utilizamos para pintar o cenário. Desta vez, tanto a cor quanto o contorno serão em branco. Com a ferramenta de círculo, desenharemos uma bolinha. Alinhe o centro do círculo desenhado à tela do painel, pois a discrepância entre esses pontos pode gerar bugs no jogo como a bolinha pular de posição ou mesmo rebater várias vezes na raquete.
>
> Sobre o painel localizado à direita, para testarmos, clicaremos no ícone de bandeira verde, porém nada acontece. Geralmente, quando jogamos algo, os personagens não ficam posicionados aleatoriamente, tampouco na última posição em que estiveram. Isto é, eles possuem uma posição inicial, e neste jogo não será diferente.
>
> Selecionaremos uma posição inicial para a nossa bolinha clicando em "Eventos", e em "quando [ícone de bandeira verde] for clicado", que arrastaremos ao painel principal. Depois, clicaremos em "Movimento" e em "vá para x: 182 y: -135", que também arrastaremos ao painel principal, encaixando na primeira "peça". Clicaremos nestes valores para os alterarmos para `0` e `0`.
>
> Assim, ao clicarmos no ícone de bandeira verde, teremos que a bolinha começa no centro do jogo. Agora, precisaremos movimentá-la! Clicaremos e arrastaremos "mova 10 passos" para o painel principal, encaixando-a na peça anterior. Clicando no ícone de bandeira verde, a bolinha se locomove um pouco para a direita, mas se clicarmos novamente, nada acontece.
>
> Acontece que, quando nosso jogo se inicia, ele faz o que está definido na segunda peça e logo muda para a terceira, entretanto, isto ocorre apenas uma vez, quando na verdade queremos que a bolinha siga se movimentando. Para isso, clicaremos e arrastaremos outro evento "quando [ícone de bandeira verde] for clicado" para cima de "mova 10 passos", formando um segundo conjunto. E então clicaremos em "Controle" e em "sempre", que arrastaremos ao segundo conjunto, englobando o "mova 10 passos".
>
> Assim, o movimento acontecerá sempre, ou seja, os 10 passos serão adicionados continuamente. Ao testarmos, a bolinha começará no centro e terminará no canto direito da tela, visível pela metade. Para um movimento de vai e volta, existe um código em "Movimento" que verifica essa colisão com as bordas da nossa tela, denominada "se tocar na borda, volte", o qual posicionaremos dentro de "sempre", abaixo de "mova 10 passos".
>
> Aumentaremos a velocidade da bolinha aumentando o número de passos para `12`. Entretanto, deste modo o movimento se dará apenas horizontalmente, então, poderemos indicar uma direção para ela, acrescentando "aponte para a direção 90" logo abaixo de "vá para x: 0 y: 0". Reparem que, ao clicarmos no valor, é demonstrado um círculo para demonstrar que o movimento se inicia em 90º. Vamos alterá-lo para `45`.
>
> Desta vez, a nossa bolinha se movimenta em vários sentidos, de acordo com essa angulação. E como é que iremos interagir com este jogo? Teremos raquetes, atores que criaremos a seguir!

#### Bolinha e minha raquete parte 2
>
> Renomearemos o novo ator para "bolinha", e pintaremos outro ator, denominado "minha raquete", um retângulo de preenchimento e contorno brancos, para simular uma das raquetes. Na aba "Código", uma vez que queremos que ele comece do lado esquerdo da tela, enquanto a bolinha está no centro, definiremos que quando a bandeira verde for pressionada, queremos que a raquete vá para X `-220` e Y `0`.
>
> Isso, porém, ainda não fará com que a raquete se movimente, pois não programamos nosso jogo para fazer isso. Queremos utilizar nosso teclado para que a raquete se mova verticalmente, e para fazermos isto de forma organizada, arrastaremos outro "quando [ícone de bandeira verde] for clicado" e encaixaremos abaixo dele "se [hexágono] então", existente em "Controle".
>
> De "Sensores", clicaremos e arrastaremos "tecla espaço pressionada?" no espaço onde havia o símbolo de hexágono, e modificaremos "espaço" para "seta para cima". Assim, se a seta para cima for pressionada, a bolinha irá para cima. Sempre que tivermos dúvidas em relação a X e Y, no canto inferior esquerdo do programa podemos clicar em "Selecionar Cenário" e em "Xy-grid", que utilizaremos como gabarito. O X corresponde ao eixo horizontal, enquanto o Y corresponde ao eixo vertical.
>
> Então, assim que a seta para cima for pressionada, queremos que a raquete vá para cima também. Ou seja, adicionaremos um valor para Y, e para tal clicaremos e arrastaremos "adicione 10 a y" dentro de "se [hexágono] então". Ao testarmos, porém, a raquete não se movimenta, já que o código é executado assim que o jogo é ligado, momento em que ainda não estamos com a tecla da seta para cima pressionada, e esta verificação é feita apenas uma vez.
>
> Para resolvermos isso, envolveremos todo o segundo bloco abaixo de "quando [ícone de bandeira verde] for clicado" em outro, "sempre". No entanto, isso fará com que consigamos mover a raquete apenas para cima, portanto duplicaremos o bloco envolvido por "sempre" — clicando com o lado direito do mouse e em "Duplicar" — e substituiremos "seta para cima" por "seta para baixo", e o valor `10` por `-10`.
>
> A bolinha ainda não está colidindo com a raquete, ultrapassando-a e tocando a lateral da tela. Podemos, inclusive, visualizar isto melhor diminuindo a velocidade da bolinha, que queremos que mude de direção assim que tocar na raquete. Podemos criar um bloco para verificar se estamos tocando na borda.
>
> <p style="background-color: #333; padding: 10px; color: white">
> Para deixar o código organizado, é possível clicar com o lado direito do mouse no painel principal e em "Limpar Blocos".
> </p>
>
> Continuando, criaremos mais um bloco de código para quando o jogo for iniciado, para verificarmos se a bolinha está tocando a raquete. Teremos, então, "quando [ícone de bandeira verde] for clicado", e logo abaixo, "se [hexágono] então", cujo hexágono será preenchido por "tocando em minha raquete?".
>
> Para invertermos a rota da bolinha, reconhecendo a colisão com a raquete e alterar a direção, inverteremos o valor multiplicando-o por `-1`. De "Movimento", clicaremos e arrastaremos "aponte para a direção 90" para dentro de "se 'tocando em minha raquete?' então". Substituiremos o valor `90` pela opção "direção".
>
> De "Operadores" selecionaremos o bloco verde com `"[] * []"`, e para o primeiro espaço arrastaremos o "direção" que tínhamos movimentado anteriormente, o qual multiplicaremos por -1, valor que digitaremos no segundo espaço do bloco. Daí, sim, encaixaremos o bloco final para onde "direção" estava antes, de modo a ficar "aponte para a direção 'direção * -1'".
>
> Porém, mais uma vez, o código só foi executado uma vez, quando o jogo se iniciou. Envolveremos todo o bloco do "se..." em outro, "sempre". Agora, sim, temos o comportamento esperado!

#### Oponente e placar
>
> A colisão da bolinha com a raquete está funcionando bem, porém a bolinha está se movimentando muito devagar e, além disso, nosso oponente é a parede. Vamos corrigir estes pontos alterando o bloco de código referente ao movimento da bolinha para "mova 12 passos" e duplicando a raquete que criamos clicando com o lado direito do mouse sobre o ator "minha raquete" e depois em "Duplicar".
>
> Por ser uma cópia, a segunda raquete fará exatamente os mesmos movimentos da primeira, portanto não iremos enxergá-la. Em relação ao bloco de código da segunda raquete, então, substituiremos o bloco "vá para x: -220 y: 0" por "vá para x: 239 y: 9". Vamos ajustar o eixo Y da segunda raquete para que fique alinhada à primeira, mudando seu valor de `9` para `0`.
>
> Com isso, se testarmos o jogo, as duas raquetes se movimentam de forma similar, sincronizadas, cada uma de um lado da tela. Assim, iremos remover os blocos "se..." da primeira raquete, responsáveis pelos seus movimentos. Queremos que a raquete do oponente se movimente para colidir com a bolinha, assim que ela voltar da colisão com a primeira raquete.
>
> Poderíamos passar a posição da bolinha para a raquete do oponente, porém, para cada ator no Scratch existem códigos em "Movimento" denominados "posição x", "posição y". Todavia, não queremos saber se a bolinha estará mais para a direita ou para a esquerda, pois o movimento da raquete do oponente também será na vertical. Isto é, precisaremos passar a posição Y da bolinha.
>
> Sendo assim, criaremos uma variável para guardar este valor, de modo a conseguirmos compartilhá-lo com outros atores. Acessaremos a opção "Variáveis" e clicaremos em "Criar uma Variável"; ela se chamará "posição y da bolinha". Sempre que a bolinha se movimentar, o valor desta variável será alterada, e para isso acrescentaremos "mude 'minha variável' para 0" entre "mova 12 passos" e "se tocar na borda, volte". Alteraremos "minha variável" para "posição y da bolinha", e encaixaremos "posição y" no lugar de "0".
>
> Reparem que, ao criarmos uma variável, existem as opções de visibilidade "Para todos os atores" e "Apenas para este ator"; no caso, escolhemos a primeira. Agora, para que a raquete do oponente se mova verticalmente, incluiremos "deslize por 1 segs. até x: 236 y: 56" dentro de "sempre", sendo que a posição X será a mesma do início, 239, enquanto a Y será substituída por "posição y da bolinha".
>
> Ao testarmos, teremos que a raquete não está seguindo a bolinha. Isto acontece pois deixamos o deslize durante `1` segundo, então o alteraremos para `0`, para que ele ocorra no mesmo momento que a bolinha. A posição Y da bolinha está aparecendo na tela — será que a pessoa que for jogar precisará desta informação?
>
> Vamos esconder esta variável selecionando o ator bolinha e incluindo, no primeiro bloco de código, "esconda a variável 'posição y da bolinha'", logo após o "aponte para a direção 45". Nosso jogo está cada vez melhor, mas será que a raquete do oponente realmente está tocando na bolinha, isto é, existe a colisão?
>
> Para enxergarmos isto, vamos diminuir novamente a velocidade da bolinha, de `12` para `2`, e clicar no ícone da bandeira verde. A bolinha está tocando na borda da tela, ultrapassando a segunda raquete! Para o código correspondente a esta ação feito para a primeira raquete, iremos a "Operadores", clicaremos e arrastaremos o losango composto por "[hexágono] ou [hexágono]" para o painel principal, dentro do bloco "se...".
>
> <p style="background-color: #333; padding: 10px; color: white">
> Neste momento, a segunda raquete estava nomeada como "minha raquete2" por *default*, por ser uma cópia, lembram? Basta renomeá-la para darmos uma sentido para ela, como para "raquete do oponente".
> </p>
>
> Isso quer dizer que se a bolinha estiver tocando na "minha raquete" ou em "raquete do oponente", esperamos que a direção seja alterada, resultando na efetiva colisão. Entretanto, teremos um problema: o oponente sempre irá seguir a posição da bolinha, ou seja, ele nunca irá errar. Consequentemente, nossas chances de ganharmos o jogo será mínima. Precisaremos pensar em alguma maneira de aumentá-las!

#### Oponente e placar parte 2
>
> Estamos passando à raquete do oponente a posição Y da bolinha... E se manipulássemos este valor, incluindo uma margem de erro? Então, em vez de passarmos a posição exata da bolinha em "mude 'posição y da bolinha' para 0", incluiremos no lugar de 0 um bloco de operação "[] - []", que terá no primeiro espaço "posição y", e no segundo, 50. Além disso, voltaremos a aumentar a velocidade da bolinha para 12.
>
> Ao testarmos, em dado momento a bolinha toca a lateral da tela, e não a raquete do oponente, o que significaria o ganho de um ponto para nós. Mas como é que iremos saber disso? De que forma contabilizaremos isso? Seria interessante se estas pontuações ficassem visíveis de alguma forma.
>
> Já sabemos que armazenamos valores na memória do nosso computador por meio de variáveis. Por conta disso, criaremos duas variáveis, disponíveis para todos os atores — uma para armazenamento dos nossos pontos, denominada "meus pontos", e outra para os pontos do oponente, "pontos do oponente". Deixar da maneira padrão não é tão interessante visualmente, então clicaremos sobre elas com o lado direito do mouse para verificarmos as opções de exibição das variáveis; neste caso, escolheremos "letras grandes".
>
> <p style="background-color: #333; padding: 10px; color: white">
> Também é possível clicar duas vezes sobre a exibição das variáveis para alterá-las!
> </p>
>
> Apesar de termos incluído esta exibição de pontuação, os pontos não estão sendo marcados ainda. Isso porque ainda não programamos desta forma. Precisaremos indicar que, assim que a bolinha tocar na lateral da tela (e não nas raquetes), queremos que um ponto seja marcado para o adversário. O valor do X identifica este momento, então, se X for menor que `229`, queremos acrescentar um ponto para o oponente.
>
> Para fazermos esta verificação, manteremos o ator "bolinha" selecionado e criaremos o código correspondente: "quando [ícone de bandeira verde] for clicado", seguido por "se [hexágono] então", cujo hexágono ficará com "'posição x' < -229", e dentro do qual teremos "adicione 1 a 'pontos do oponente'". Todo código inserido em uma repetição, isto é, que acontece mais de uma vez, tem uma borda dourada.
>
> Da maneira em que está, este último bloco de código possui esta borda assim que clicamos no ícone de bandeira verde, mas ela não se mantém. É necessário envolvermos o bloco contendo "se..." em outro, "sempre". Além disso, queremos poder criar nossos próprios pontos, então dentro de "sempre" acrescentaremos outro bloco "se...", que ficará "se 'posição x' > 229 então" acompanhado por "adicione 1 a 'meus pontos'".
>
>

#### Sons e compartilhando o jogo

#### Faça como eu fiz na aula

#### Jogo mais difícil

#### O que aprendemos?

---

### Iniciando no JavaScript

#### Cenário e bolinha

#### Colisão com as bordas

#### Raio e diâmetro

#### Refatoração e funções

#### Faça como eu fiz na aula

#### Função na programação

#### O que aprendemos?

---

### Criando minha raquete no jogo

#### Criando minha raquete

#### Movimento minha raquete

#### Colisão com a raquete

#### Importando outra biblioteca

#### Faça como eu fiz na aula

#### Outras bibliotecas no GitHub

#### O que aprendemos?

---

### Criando a raquete do oponente

#### Raquete do oponente

#### Colisão com o oponente

#### Placar do jogo

#### Faça como eu fiz na aula

#### Marcando pontos

#### O que aprendemos?

---

### Editando placar e adicionando sons

#### Editando o placar do jogo

#### Preparando o ambiente

#### Adicionando sons

#### Faça como eu fiz na aula

#### Sons no P5 JS

#### Para saber mais

#### O que aprendemos?

#### Conclusão

#### Parabéns