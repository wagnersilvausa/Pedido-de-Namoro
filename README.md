# Uma pergunta importante 💗

<p align="center">
  <strong>Uma experiência web romântica, interativa e personalizada para transformar um pedido especial em uma pequena história.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=111" alt="JavaScript" />
  <img src="https://img.shields.io/badge/sem_depend%C3%AAncias-2A101D?style=for-the-badge" alt="Sem dependências" />
</p>

## Sobre o projeto

Este projeto é uma página estática que conduz a pessoa por uma sequência de momentos antes da pergunta final. A experiência combina suspense, música, fotos, animações e uma declaração personalizada em um único arquivo HTML, sem frameworks ou etapa de compilação.

O site foi desenvolvido com foco em:

- experiência emocional progressiva;
- funcionamento em computador e celular;
- fotos exibidas sem cortes;
- transições que não revelam a pergunta antes da hora;
- carregamento antecipado da trilha sonora;
- navegação simples e acessível por teclado.

## Fluxo da experiência

1. Abertura com uma mensagem de suspense.
2. Transição opaca em formato de coração.
3. Barra interativa preenchida com sete toques.
4. Sequência `Amor é...` com três fotos formando a frase `Você me completa`.
5. Frase de ligação e acesso à declaração.
6. Carta personalizada com rolagem responsiva.
7. Pedido final acompanhado das fotos do casal.
8. Confirmação com animação de celebração.

## Principais recursos

- layout totalmente responsivo;
- animações e transições feitas somente com CSS e JavaScript;
- galeria com proporções naturais e `object-fit: contain`;
- reprodução de áudio local com `preload="auto"`;
- botão de resposta negativa com comportamento evasivo;
- suporte a `prefers-reduced-motion`;
- elementos semânticos e mensagens com atributos ARIA;
- nenhuma dependência externa para executar o site.

## Tecnologias

- **HTML5** para a estrutura e semântica;
- **CSS3** para layout, responsividade e animações;
- **JavaScript** para interações, estados, áudio e confetes;
- **arquivos locais** para fotos e música.

## Estrutura principal

```text
mozao/
├── index.html          # Página completa, estilos e interações
├── img/                # Fotografias utilizadas na experiência
│   └── *.jpg
└── music/              # Trilha sonora ativa
    └── *.mp3
```

## Executando localmente

O projeto não exige instalação de pacotes. Depois de baixar ou clonar o repositório, inicie um servidor estático na pasta raiz.

### Com Python

```bash
python -m http.server 5500
```

No Windows, também é possível usar:

```powershell
py -m http.server 5500
```

Depois, acesse:

```text
http://localhost:5500
```

> Usar um servidor local evita limitações do navegador ao abrir áudio e outros arquivos diretamente pelo protocolo `file://`.

## Personalização

As principais alterações podem ser feitas diretamente no [`index.html`](./index.html):

- **nome e textos:** procure pelos títulos e parágrafos da introdução, carta e pergunta final;
- **fotos:** substitua os arquivos em `img/` e atualize os respectivos caminhos no HTML;
- **música:** substitua o MP3 em `music/` e atualize o atributo `src` do elemento `<audio>`;
- **volume:** altere o valor de `loveSong.volume` no JavaScript;
- **ritmo das animações:** ajuste o objeto `timing` dentro de `startLoveSequence()`;
- **cores:** edite as variáveis declaradas em `:root` no início do CSS.

Ao substituir imagens, mantenha nomes de arquivo simples e confira a apresentação em telas pequenas.

## Música e autoplay

A trilha começa a ser pré-carregada assim que a página abre. Navegadores modernos podem impedir a reprodução automática antes da primeira interação. Por isso, o site tenta iniciar o áudio novamente no primeiro toque, clique ou pressionamento de tecla.

## Publicação

Por ser um site estático, o projeto pode ser hospedado diretamente em serviços como:

- GitHub Pages;
- Vercel;
- Netlify;
- qualquer servidor capaz de entregar arquivos HTML e mídia estática.

Publique o conteúdo da pasta raiz e preserve a estrutura relativa de `img/` e `music/`.

## Privacidade e direitos de uso

Este projeto contém fotografias, uma mensagem pessoal e uma música hospedada localmente. Antes de tornar o repositório público:

- confirme a autorização das pessoas presentes nas fotos;
- revise se a mensagem pode ficar visível publicamente;
- confirme que você possui permissão para hospedar e distribuir a música;
- lembre-se de que arquivos de um repositório público podem ser baixados por qualquer pessoa.

## Licença

Este repositório não inclui uma licença de código aberto. O conteúdo pessoal, as fotografias e os arquivos de áudio não devem ser reutilizados sem autorização.

