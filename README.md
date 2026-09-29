# Raio-X Estratégico — 2º dia do ENEM

> Plataforma educacional interativa para revisar Ciências da Natureza — Biologia, Química e Física — com foco em repertório, leitura estratégica de questões e Teoria de Resposta ao Item (TRI).

[![HTML5](https://img.shields.io/badge/HTML5-100%25-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-CDN-06B6D4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Chart.js](https://img.shields.io/badge/Chart.js-4.4.1-FF6384?logo=chart.js&logoColor=white)](https://www.chartjs.org/)
[![Licença](https://img.shields.io/badge/licença-a%20definir-lightgrey)](LICENSE)

O projeto foi desenvolvido para o aulão **“Raio-X Estratégico — Decodificando o 2º Dia do ENEM”**, realizado no contexto do **Pré-ENEM Digit@l MT**, em Juscimeira-MT. A aplicação é estática, funciona diretamente no navegador e não possui backend.

## Acesse

- **Aplicação principal:** [abrir `index.html`](index.html)
- **Checklist imprimível:** [abrir `checklist.html`](checklist.html)
- **Repositório:** [Bio-Tech-Edu/repcn](https://github.com/Bio-Tech-Edu/repcn)

> Os gráficos, ícones, fontes e estilos principais são carregados por CDN. Para visualizar todos os recursos, é necessária uma conexão com a internet.

## O que a aplicação oferece

### Painel interativo

- Panorama das 45 questões de Ciências da Natureza, distribuídas entre Biologia, Química e Física.
- Gráfico de distribuição estimada por nível de dificuldade e relação com a TRI.
- Mapa de calor com **23 subtemas** e suas frequências relativas.
- Filtros por disciplina e modal com competências BNCC/ENEM associadas.

### Estudo de caso integrado

A Estação de Tratamento de Água é usada como situação-problema para conectar as três áreas:

- **Química:** coagulação, floculação e tratamento de misturas.
- **Física:** decantação, gravidade, empuxo e densidade.
- **Biologia:** desinfecção, cloração, saneamento e eutrofização.

### Prática e revisão

- Dinâmica **Think-Pair-Share** com cronômetro para as etapas Think, Pair e Share.
- Questões comentadas com gabarito e análise dos distratores.
- Guia de identificação de três perfis de distrator:
  - falsa verdade ou extrapolação;
  - inversão de causa e efeito;
  - generalização absoluta.
- Protocolo prático para organização do tempo no segundo dia do ENEM.
- Checklist de conteúdos prioritários pronto para impressão ou exportação em PDF.

### Recursos de interface

- Navegação por abas com suporte a teclado e atributos ARIA.
- Tema claro/escuro com persistência em `localStorage`.
- Link para pular diretamente ao conteúdo principal.
- Foco visível e respeito a `prefers-reduced-motion`.
- Descrições alternativas para imagens e gráficos.
- Galeria de fotos com carrossel acessível, preparada para os registros do evento.

## Estrutura do repositório

```text
.
├── index.html                 # Aplicação principal: painel e módulos pedagógicos
├── checklist.html             # Guia de revisão otimizado para impressão/PDF
├── mapa_calor.csv             # Dados dos 23 subtemas e competências associadas
├── assets/
│   ├── galeria/               # Fotos do evento e instruções de publicação
│   └── *.png                  # Identidade visual, avatares e ilustrações
├── docs/
│   └── *.docx                 # Plano executivo da aula
├── SPRINTS.md                 # Histórico técnico, decisões e backlog
├── .gitignore                 # Arquivos e diretórios locais ignorados pelo Git
└── README.md                  # Documentação do projeto
```

## Como executar localmente

Não há etapa de instalação ou compilação. Depois de clonar o repositório, abra `index.html` em um navegador moderno:

```bash
git clone https://github.com/Bio-Tech-Edu/repcn.git
cd repcn

# macOS
open index.html

# Linux
xdg-open index.html

# Windows PowerShell
Start-Process .\index.html
```

Também é possível abrir os arquivos diretamente pelo gerenciador de arquivos. Para uma experiência mais próxima de um ambiente publicado, use um servidor estático local:

```bash
python3 -m http.server 8000
```

Em seguida, acesse <http://localhost:8000>.

## Publicação no GitHub Pages

1. No GitHub, abra **Settings → Pages**.
2. Em **Build and deployment**, selecione **Deploy from a branch**.
3. Escolha a branch `main` e a pasta `/ (root)`.
4. Salve e aguarde a publicação.

A URL normalmente será:

```text
https://bio-tech-edu.github.io/repcn/
```

## Dados e fontes do conteúdo

O arquivo [`mapa_calor.csv`](mapa_calor.csv) organiza a frequência relativa dos temas por disciplina, subtema, nível de calor e competências BNCC/ENEM. O array `HEAT` em [`index.html`](index.html) é usado pela interface para renderizar o mapa de calor no navegador.

O material pedagógico está relacionado ao plano executivo disponível em [`docs/`](docs/) e ao histórico de desenvolvimento documentado em [`SPRINTS.md`](SPRINTS.md).

## Adicionando fotos à galeria

1. Salve as imagens em [`assets/galeria/`](assets/galeria/), preferencialmente em `.jpg` ou `.png`.
2. Em `index.html`, localize `GALERIA_FOTOS`.
3. Adicione cada foto com um texto alternativo descritivo:

```js
const GALERIA_FOTOS = [
  {
    src: 'assets/galeria/foto1.jpg',
    alt: 'Estudantes participando do aulão em Juscimeira-MT'
  }
];
```

4. Salve e publique. O carrossel será montado automaticamente.

Consulte também [`assets/galeria/README.md`](assets/galeria/README.md) para as instruções específicas da galeria.

## Desenvolvimento e manutenção

O projeto é intencionalmente simples: a interface, os estilos e a lógica da aplicação estão concentrados em arquivos HTML, sem dependências instaladas localmente. Para alterar o conteúdo principal, os pontos de entrada mais importantes são:

- `index.html`: layout, estilos, dados pedagógicos e interações;
- `checklist.html`: versão para impressão;
- `mapa_calor.csv`: fonte tabular do mapa temático;
- `SPRINTS.md`: decisões técnicas, auditoria e backlog.

Antes de publicar uma alteração, verifique manualmente:

- carregamento dos gráficos e do mapa de calor;
- filtros de disciplina e de distratores;
- cronômetro Think-Pair-Share;
- alternância de tema;
- funcionamento do checklist para impressão;
- existência das imagens referenciadas na galeria;
- navegação por teclado e textos alternativos.

## Contexto pedagógico

- **Público:** estudantes do Ensino Médio, especialmente 2º e 3º anos.
- **Área:** Ciências da Natureza e suas Tecnologias.
- **Duração planejada:** 50 minutos.
- **Metodologia:** Estudo de Caso Integrado + Think-Pair-Share.
- **Competências:** competências específicas 1 e 3 de Ciências da Natureza.
- **Projeto:** Pré-ENEM Digit@l MT / SEDUC-MT.

## Créditos

Desenvolvido por [Bio+Tech EduDesign](https://github.com/bio-tech-edu), com apoio institucional do Governo do Estado de Mato Grosso e do projeto Pré-ENEM Digit@l MT.

## Status

Projeto educacional estático em evolução. O histórico das sprints, a auditoria do código legado e o backlog de melhorias estão registrados em [`SPRINTS.md`](SPRINTS.md).

## Licença

Ainda não há um arquivo `LICENSE` no repositório. Defina e adicione uma licença antes de distribuir o código ou os materiais para reutilização pública.
