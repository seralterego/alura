# IMERSÃO DEV | AULA 8: TRUNFO, IMAGENS, MANIPULAÇÃO DO HTML E CSS

fonte: <https://imersao.dev/aulas/aula08-supertrunfo-sistema>
PDF para organizar texto: [aqui](../assets/PDFs/aula08.pdf)

---

## TRUNFO, IMAGENS, MANIPULAÇÃO DO HTML E CSS
> Nesta oitava aula da Imersão Dev, vamos evoluir ainda mais nosso Trunfo, focando em exibir as cartas na tela! O código da aula para você acompanhar está aqui: <https://codepen.io/imersao-dev/pen/JjEjjZv>
>
> Neste programa, vamos descobrir que podemos alterar não só o conteúdo do HTML com Javascript. Vamos aprender como manipular o CSS e exibir nossas cartas no tela. Além disso, vamos usar o código abaixo no decorrer desta aula:
>
~~~javascript
var moldura = '<img src="https://www.alura.com.br/assets/img/imersoes/dev-2021/card-super-trunfo-transparent.png" style=" width: inherit; height: inherit; position: absolute;">';
~~~
>
### Conteúdo detalhado dessa aula
> - Adicionando o campo imagem nos objetos com o caminho da imagem;
> - Criar uma função que exibe a carta do jogador após o sorteio das cartas;
> - Adicionar a moldura da carta;
> - Escrever o resultado na tela após o duelo das cartas informando se o jogador venceu ou perdeu;
> - Criar uma função que exibe a carta da máquina;
> - Exibir os atributos e pontos da carta da máquina.
>
### Desafios dessa aula!
> - Criar novas cartas com imagens e atributos diferentes.
>
### Links importantes para você acompanhar a aula
> - [Codepen - editor de código online](https://codepen.io/)
> - [HTML, CSS e JavaScript, quais as diferenças](https://www.alura.com.br/artigos/html-css-e-js-definicoes)
> - [Usando o VSCode](extra03)
> - [Primeira aula da imersão com Python](extra02)
> - [Repositório do código final da aula 8](https://codepen.io/imersao-dev/pen/LYxYYzm)
>
### Links citados nessa aula
> - [Mais sobre variáveis](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Grammar_and_types#vari%C3%A1veis)
> - [Mais sobre a função parseFloat](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/parseFloat)
>
### Conteúdo extra:
> Manipular o CSS pelo JS não é tarefa fácil. Pensando nisso, vamos disponibiliar o código da função exibiCartaJogador():
>
~~~javascript
function exibeCartaJogador() {
    var divCartaJogador = document.getElementById("carta-jogador")
    var moldura = '<img src="https://www.alura.com.br/assets/img/imersoes/dev-2021/card-super-trunfo-transparent.png" style=" width: inherit; height: inherit; position: absolute;">';
    divCartaJogador.style.backgroundImage = `url(${cartaJogador.imagem})`
    var nome = `<p class="carta-subtitle">${cartaJogador.nome}</p>`
    var opcoesTexto = ""

    for (var atributo in cartaJogador.atributos) {
        opcoesTexto += "<input type='radio' name='atributo' value='" + atributo + "'>" + atributo + " " + cartaJogador.atributos[atributo] + "<br>"
    }

    var html = "<div id='opcoes' class='carta-status'>"

    divCartaJogador.innerHTML = moldura + nome + html + opcoesTexto + '</div>'
}
~~~
>
### Como compartilhar seu CodePen:
> - Clique na opção Settings no canto superior direito;
> - Selecione a opção Pen Details (Detalhes);
> - No campo Pen Title você pode dar o nome do seu projeto;
> - No campo Pen Description, você pode dar detalhes sobre o projeto (o que ele faz, qual objetivo do projeto);
> - Para compartilhar seu projeto, no campo Tags, você pode adicionar #imersaodev,#alura
> - Agora só salvar seu projeto e compartilhar o link marcando a Alura nas redes sociais!

### QUEM SÃO OS MERGULHADORES?
> - Paulo Silveira | Co-fundador e CEO da Alura
> - Rafaella Ballerini | Instrutora de Front-end na Alura, criadora de conteúdo
> - Guilherme Lima | Desenvolvedor e Instrutor na Alura
