# Meu Portfólio | Bernardo Diniz

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?logo=javascript&logoColor=black)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Publicado-222222?logo=github&logoColor=white)

Portfólio pessoal de Bernardo Diniz, desenvolvido como uma landing page para
apresentar perfil profissional, formação, experiências, habilidades técnicas e
canais de contato.

## Demonstração

- **Site publicado:**
  [bernardodiniz-1898.github.io/Meu-Portifolio](https://bernardodiniz-1898.github.io/Meu-Portifolio/)
- **Código-fonte:**
  [github.com/BernardoDiniz-1898/Meu-Portifolio](https://github.com/BernardoDiniz-1898/Meu-Portifolio)

## Objetivo

O projeto funciona como um currículo digital de página única. O conteúdo foi
organizado para permitir que recrutadores, empresas e parceiros conheçam a
trajetória profissional do autor e encontrem rapidamente seus meios de contato.

## Funcionalidades

- Navegação por âncoras entre as seções da página.
- Navbar fixa com mudança visual durante a rolagem.
- Menu lateral adaptado para dispositivos móveis.
- Hero com apresentação profissional e chamadas para ação.
- Seção de perfil, formação e objetivos.
- Timeline de experiências profissionais.
- Cards de habilidades com barras animadas.
- Animações de entrada baseadas em `IntersectionObserver`.
- Links diretos para e-mail, WhatsApp e GitHub.
- Layout responsivo para desktop, tablet e celular.
- Rolagem suave com compensação para a navbar fixa.
- Foco visível para navegação por teclado.

## Seções

| Seção | Conteúdo |
|---|---|
| Início | Apresentação, título profissional e chamadas para ação |
| Sobre | Perfil, formação, localização e objetivos |
| Experiência | Histórico profissional em formato de timeline |
| Habilidades | Tecnologias e conhecimentos declarados pelo autor |
| Contato | E-mail, WhatsApp, localização e GitHub |

## Tecnologias utilizadas

### Implementação

- HTML5
- CSS3
- JavaScript Vanilla
- CSS Grid e Flexbox
- CSS Custom Properties
- Media queries
- Intersection Observer API
- GitHub Pages

### Recursos externos

- [Google Fonts](https://fonts.google.com/) para as fontes Inter e Fira Code.
- [Font Awesome](https://fontawesome.com/) para os ícones da interface.
- [cdnjs](https://cdnjs.com/) para entrega do Font Awesome.

> [!NOTE]
> Python, PHP, Laravel, Linux e Java aparecem como habilidades no conteúdo do
> portfólio, mas não são tecnologias utilizadas na implementação deste site.

## Arquitetura

O projeto não possui backend, banco de dados ou etapa de compilação. Todo o
conteúdo é servido diretamente pelo GitHub Pages.

```text
Navegador
   |
   |-- index.html
   |      |-- estrutura e conteúdo
   |      |-- metadados e dependências externas
   |      `-- JavaScript da interface
   |
   `-- style.css
          |-- tokens visuais
          |-- componentes e animações
          `-- responsividade
```

## Estrutura

```text
Meu-Portifolio/
├── index.html   # Conteúdo, estrutura e comportamento
├── style.css    # Tema, layout, animações e responsividade
└── README.md    # Documentação do projeto
```

## Como executar

Não é necessário instalar dependências.

Clone o repositório:

```bash
git clone https://github.com/BernardoDiniz-1898/Meu-Portifolio.git
cd Meu-Portifolio
```

### Abrir diretamente

Abra `index.html` em um navegador moderno.

### Servidor HTTP local

Usar um servidor local reproduz melhor o comportamento da publicação.

Com Python:

```bash
python -m http.server 8000
```

No Windows, também é possível usar:

```bash
py -m http.server 8000
```

Acesse `http://localhost:8000`.

## Responsividade

O layout utiliza dois breakpoints principais:

| Largura | Comportamento |
|---|---|
| Acima de 900 px | Hero em duas colunas e habilidades em três colunas |
| Até 900 px | Hero vertical e habilidades em duas colunas |
| Até 600 px | Menu lateral e grids em uma única coluna |

No mobile, o bloco decorativo de código é ocultado para priorizar o conteúdo e
reduzir a densidade visual.

## Interatividade

### Menu móvel

O botão hambúrguer alterna a classe `active` na navegação. Selecionar um link
fecha o painel automaticamente.

### Animações de entrada

Os cards de informações, experiências, habilidades e contatos são observados
com `IntersectionObserver`. Quando entram na viewport, recebem a classe
`visible` e executam suas transições.

### Barras de habilidades

Cada habilidade possui um valor em `data-level`. O JavaScript converte esse
valor em largura percentual quando a barra entra na área visível.

### Navbar

Após 50 pixels de rolagem, a navbar recebe fundo semitransparente, blur e borda
inferior.

## Publicação

O site está hospedado no GitHub Pages a partir da branch `main`:

```text
https://bernardodiniz-1898.github.io/Meu-Portifolio/
```

Não existe workflow próprio no repositório. A publicação utiliza o processo de
deploy configurado pelo GitHub Pages.

## Dependências de rede

O HTML e o CSS local continuam disponíveis sem internet, mas a apresentação
completa depende de serviços externos:

- Google Fonts para as fontes personalizadas.
- cdnjs para o Font Awesome.

Se esses serviços estiverem indisponíveis, o navegador usará fontes de sistema
e os ícones poderão não aparecer.

## Acessibilidade

O projeto já possui idioma `pt-BR`, hierarquia de títulos, links semânticos e
estados de foco visíveis. Ainda existem melhorias importantes:

- Informar o estado do menu com `aria-expanded` e `aria-controls`.
- Permitir fechamento do menu com a tecla `Escape`.
- Adicionar um elemento `<main>` e um link para pular ao conteúdo.
- Adicionar semântica de progresso às barras de habilidades.
- Respeitar a preferência `prefers-reduced-motion`.
- Manter o conteúdo visível quando o JavaScript estiver indisponível.

## Limitações conhecidas

- Não existe uma seção de projetos ou estudos de caso nesta versão.
- Não existe formulário de contato ou backend para envio de mensagens.
- O link de GitHub presente na página aponta para a página inicial do serviço,
  não diretamente para o perfil do autor.
- Informações como idade, cargo atual e ano do rodapé exigem atualização manual.
- Parte do conteúdo começa invisível e depende de JavaScript para aparecer.
- Ícones e fontes dependem de CDNs externos.
- Não há testes automatizados, linter ou validação de links configurados.
- Metadados de compartilhamento social ainda não foram adicionados.

## Próximos passos

- Adicionar uma seção com projetos reais e links para código e demonstração.
- Corrigir o link do perfil no GitHub e adicionar LinkedIn.
- Adicionar currículo para download.
- Melhorar a navegação móvel e a acessibilidade por teclado.
- Aplicar animações como melhoria progressiva, com conteúdo visível por padrão.
- Extrair o JavaScript para um arquivo separado.
- Adicionar Open Graph, URL canônica e dados estruturados.
- Criar verificações automatizadas de HTML, CSS, acessibilidade e links.
- Adicionar screenshots da versão desktop e mobile ao repositório.

## Autor

Desenvolvido por [Bernardo Diniz](https://github.com/BernardoDiniz-1898).

## Licença

Este repositório ainda não possui uma licença definida. Consulte o autor antes
de reutilizar ou redistribuir o código.
