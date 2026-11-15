# Portfólio Pessoal

**Aluno:** Matheus Hernandes
**Curso:** Técnico em Desenvolvimento de Sistemas

**Site publicado:** https://github.com/matheusdechernandes/portifolio

## Descrição

Este é o meu portfólio pessoal. Ele foi feito a partir da atividade da agenda 15 da disciplina de Desenvolvimento de Sistemas I e depois eu fiz algumas melhorias para deixar o site com a minha cara.

No site eu apresento quem eu sou, minha formação, alguns projetos que já fiz e as formas de entrar em contato comigo.

## Tecnologias utilizadas

- HTML5
- CSS3
- Bootstrap 5
- Devicon (ícones das tecnologias)
- Git e GitHub
- GitHub Pages (publicação)

## Como o projeto funciona

O site tem uma página só (`index.html`), dividida em partes. O menu no topo leva para cada parte usando links com `#`, por exemplo `href="#projetos"` leva até a seção que tem `id="projetos"`.

- **Menu:** feito com a navbar do Bootstrap. Fica fixo no topo (`sticky-top`) e no celular vira um botão.
- **Carousel:** mostra três slides que trocam sozinhos, com efeito de fade (`carousel-fade`).
- **Perfil:** foto, nome, uma descrição sobre mim, cards com informações e as tecnologias que estou estudando.
- **Formação:** seção nova (ver abaixo).
- **Projetos:** seis cards com os programas e páginas que fiz no curso. Cada card tem uma imagem do programa funcionando, uma descrição e um botão que abre o código no meu repositório [projetos](https://github.com/matheusdechernandes/projetos).
- **Contato:** botões para GitHub e LinkedIn.
- **Rodapé:** ano e tecnologias usadas.

Os estilos que eu criei ficam no arquivo `estilo.css`, que está ligado ao HTML pela tag `<link>` dentro do `<head>`.

## Recursos novos

### 1. Animação ao passar o mouse nos cards

Quando o mouse passa em cima de um card de projeto ou de formação, o card sobe um pouco e a sombra fica mais forte.

**Como fiz:** criei as classes `card-projeto` e `card-formacao` e coloquei nos cards. No `estilo.css` usei:

```css
.card-projeto,
.card-formacao {
  transition: 0.3s;
}

.card-projeto:hover,
.card-formacao:hover {
  transform: translateY(-10px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2) !important;
}
```

- `:hover` aplica o estilo só quando o mouse está em cima.
- `transform: translateY(-10px)` move o card 10 pixels para cima.
- `transition: 0.3s` faz o movimento acontecer devagar, em 0,3 segundos, em vez de pular.
- Usei `!important` na sombra porque o Bootstrap já coloca uma sombra no card (`shadow-sm`) e precisei que a minha tivesse prioridade.

### 2. Nova seção: Formação

Criei uma seção nova entre o Perfil e os Projetos, com três cards: o curso técnico, a faculdade de Administração e o meu trabalho na Prefeitura de Barueri. Cada card tem um `badge` do Bootstrap mostrando a situação (Cursando, Concluído, Experiência).

**Como fiz:** copiei a estrutura de cards da seção Projetos, troquei a imagem por um `badge` e usei `col-md-4` para ficarem três cards lado a lado. No CSS coloquei uma borda azul em cima de cada card (`border-top`). Também adicionei o link "Formação" no menu.

### 3. Textos no carousel

No projeto da aula o carousel só tinha imagens. Eu coloquei em cada slide um título, uma frase e um botão que leva para uma seção do site.

**Como fiz:** usei a classe `carousel-caption` do Bootstrap dentro de cada `carousel-item`. No CSS escureci um pouco a imagem com `filter: brightness(70%)` para o texto branco ficar fácil de ler, e mudei a posição do texto com `bottom: 35%` para ele ficar mais no meio do slide.

## Estrutura de pastas

```
portfolio/
├── index.html
├── estilo.css
├── README.md
└── imagens/
    ├── slide1.png, slide2.png, slide3.png
    ├── perfil.png
    └── p1.png a p6.png
    └── logo.png
```
