# Site para profissional de Psicologia

Primeiro projeto de site comercial finalizado! Como estou iniciante ainda, quase tudo é muito novo para mim, escolhi desenvolver um site estilo para uma profissional da área de psicologia com o objetivo de praticar os conceitos recentemente aprendidos nos módulos de HTML e CSS. Em vários pontos acabei empacando, mas com algumas horas de pesquisa, e outras de retorno aos estudos, consegui resolver os problemas que tive aos poucos, até finalizar totalmente o projeto. Em breve implementarei as novas tecnologias conforme for aprendendo e estou empolgado para os próximos níveis!

## Visão geral

### ⚔️ O desafio

- Construir um site landing page para uma profissional de psicologia.

### 🖼️ Aparência

  <img src="./src/design/site-psicologa-overview-1.gif" width="900"><img src="./src/design/site-psicologa-overview-2.gif" width="568">
  <img src="./src/design/site-psicologa-overview-3.gif" width="200">

### 🖇️ Links

- Acesso ao site: [https://trincode.github.io/site-huddle-one-page](https://trincode.github.io/site-huddle-one-page/)
- Repositório github: [https://github.com/trincode/site-huddle-one-page](https://github.com/trincode/site-huddle-one-page)

## Meu processo

### Tecnologias

- HTML
- CSS

### Desafios e Conceitos aplicados

- Responsive Design
- CSS Flexbox
- CSS Grid

### O que aprendi

Para facilitar possíveis alterações de cores e definir a largura máxima da tela criei as seguintes variáveis globais:

```css
:root {
    --cor-fundo: #fdecfd;
    --cor-principal: #5e376d;
    --cor-acessoria1: #ee82ee;
    --cor-acessoria2: #d5b7e6;
    --cor-alternativa1: #f8c0c8;
    --cor-alternativa2: #efe7d3;
    
    --largura-max: 1280px;
}
```

Para criar o menu responsivo em CSS precisei da seguinte estrutura:

```html
<input type="checkbox" name="menu-responsivo" id="menu-responsivo" class="menu-responsivo">

<label for="menu-responsivo">
    <div class="menu">
        <span class="responsivo"></span>
    </div>
</label>
```
```css
.menu-responsivo:checked ~ ul {
    display: flex;
    flex-flow: column wrap;
    text-align: center;
    background-color: var(--cor-fundo);
    transform: translateY(75%);
    position: absolute;
    right: 0;
    width: 153.27px;
    z-index: 2;
}
    
.menu-responsivo:checked ~ ul .item {
    display: inline-block;
}
    
.cabecalho .navegacao .item {
    color: var(--cor-principal);
    border-radius: 10px;
    transition: 0.2s ease-in;
    width: 100%;
}
    
.cabecalho .navegacao .item:hover {
    background-color: var(--cor-acessoria1);
    color: #fdecfd;
}
```

Para adicionar a seta indicando rolagem para baixo usei um pseudoelemento na seção principal do site:

```css
.principal::after {
    content: url('../imagens/icones/arrow-down-48.png');
    position: absolute;
    bottom: 0px;
    animation: arrowdown 0.8s infinite alternate;
}

@-webkit-keyframes arrowdown {
    0% {
        -webkit-transform: translateY(0);
        -webkit-transition: ease-in-out;
        opacity: 0.8;
    }
    100% {
        -webkit-transform: translateY(-70px);
        opacity: 0;
    }
}

@keyframes arrowdown {
    0% {
        -webkit-transform: translateY(0);
        -webkit-transition: ease-in-out;
        opacity: 0.8;
    }
    100% {
        -webkit-transform: translateY(-70px);
        opacity: 0;
    }
}
```

### Desenvolvimento contínuo

Pretendo adicionar um formulário para registrar dados de contato de possíveis clientes.

### Recursos úteis

- [Ionicons - Biblioteca de ícones](https://ionic.io/ionicons/v4) - Me ajudou a aplicar os ícones relacionados a redes sociais de forma mais facilitada;
- [Icons8 - Biblioteca de ícones e imagens](https://icons8.com/) - Consegui gerar as imagens dos ícones (png) da seção tratamentos e a setinha indicadora de rolagem na seção principal;

## Autor

- LinkedIn - [Clayton Trindade](https://www.linkedin.com/in/clayton-trindade-93b925329/)

- Instagram - [@trincode - Clayton Trindade](https://www.instagram.com/trincode/)

## Agradecimentos

Meus agradecimentos aos [@roberto-hofstetter](https://github.com/roberto-hofstetter) e [@cadudias](https://github.com/cadudias), criadores do DevQuest, curso no qual aprendi a maioria dos conhecimentos utilizados aqui nesse projeto!

