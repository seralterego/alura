# IMERSÃO DEV | AULA 5: REFATORANDO O ALURAFLIX COM FUNÇÕES

fonte: <https://imersao.dev/aulas/aula05-aluraflix-interacoes-funcoes>
PDF para organizar texto: [aqui](../assets/PDFs/aula05.pdf)

---

## REFATORANDO O ALURAFLIX COM FUNÇÕES
> Na maior parte das vezes, queremos que as partes do nosso código não saiam executando a qualquer hora, mas somente no momento em que queremos que isso aconteça. Por exemplo, se um trecho do programa depende de alguma informação que venha do usuário - uma seleção feita na tela ou um texto em um formulário -, temos que deixar claro no código que "este trecho tem que ser executado na hora certa". Para isso, entre outras coisas, utilizamos uma ferramenta super comum em programação, a função.
>
> Link do template:
> <https://codepen.io/imersao-dev/pen/XWpWrod>
>
> Durante a aula de hoje, vamos refatorar o projeto do AluraFlix da aula anterior para continuar integrando o HTML e o JavaScript, também fazendo com que as partes certas do programa funcionem exatamente no momento certo.
>
> Além do código executar somente quando queremos, também vamos ver formas diferentes de usar o JavaScript para acessar o HTML e deixar a visualização mais legal.
>
>
### Conteúdo detalhado dessa aula
> - Sintaxe e criação de funções no JavaScript;
> - Integrando funções criadas no JavaScript com o HTML que está sendo exibido na tela;
> - Condicionando a execução (ou "chamada") de uma função a um clique em um botão na tela;
> - Usando o JavaScript para acessar o que está sendo exibido na tela e pegar valores digitados pelo usuário com querySelector() e .value;
> - Passar informações que as funções precisam para funcionar, através dos parâmetros;
> - Utilizar o .endsWith() para verificar se um texto termina com determinados caracteres;
> - Ver mais um exemplo de reatribuição de variável para "limpar" o texto do campo com "".
>
### Desafios dessa aula!
> - Substituir o pôster de cada filme pelo trailer. Dica: pesquisem pela opção embed no menu de compartilhamento do YouTube;
> - Estudar o innerHTML e a função que está criando a lista de pôsters. Como o código funciona para adicionar filmes sem utilizar array?
> - Criar a função validaFilme() que faça somente a verificação que está sendo feita no if.
>
### Links importantes para você acompanhar a aula
> - [Repositório do código final da aula 4](https://codepen.io/imersao-dev/pen/BapaBPO)
>
### Conteúdo extra:
> - Iterações são parte importante do estudo de lógica de programação e nem sempre a gente pega de primeira. Por isso, produzimos um [vídeo extra](./assets/livesEextras/videos/extra01) para você dar um gás nesse tema e tirar suas dúvidas. Ou ter dúvidas novas, o que também é bom!
> - [Refazendo a aula 1 com outra linguagem de programação](./assets/livesEextras/videos/extra02)
> - [Como abrir um programa do CodePen no VSCode](./assets/livesEextras/videos/extra03)

### Links citados nessa aula:
> - [Documentação da MDN sobre arrays](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array)

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
