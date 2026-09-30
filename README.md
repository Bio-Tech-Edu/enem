# Raio-X do ENEM — Aulão em Juscimeira

Plataforma estática de apoio pedagógico para o ENEM, com foco em Ciências da Natureza, análise de repertório e revisão estratégica do 2º dia da prova. O projeto reúne dashboards interativos, materiais de aula, checklist de revisão e recursos visuais para uso em sala de aula, estudo individual e preparação para simulados.

[![HTML5](https://img.shields.io/badge/HTML5-100%25-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-v3-06B6D4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Chart.js](https://img.shields.io/badge/Chart.js-4.4.1-FF6384?logo=chart.js&logoColor=white)](https://www.chartjs.org/)

## Visão geral

Este repositório contém uma aplicação web estática, sem backend, projetada para apoiar aulas, revisões e simulados do ENEM. A proposta central é transformar a análise de tendências e competências em uma experiência visual e acessível para estudantes e professores.

A estrutura do projeto inclui:

- dashboard principal em `index.html`
- painel do 1º dia em `primeiro-dia.html`
- painel do 2º dia em `segundo-dia.html`
- checklist imprimível em `checklist.html`
- materiais pedagógicos e dados em `docs/`
- ativos visuais em `assets/`

## Objetivos do projeto

- facilitar a revisão de conteúdos de Ciências da Natureza
- apresentar padrões históricos do ENEM por disciplina e tema
- conectar teoria, competências e aplicação prática
- apoiar aulas em grupo, revisão individual e estudos em contexto escolar

## Recursos principais

### Painel analítico
- análise de frequência de temas e competências
- visualização por disciplina: Biologia, Química e Física
- mapas de calor e indicadores didáticos
- apresentação de tendências históricas com foco no ENEM

### Material didático
- estudo de caso integrado com contexto real
- abordagem de repertório estratégico e de análise de distratores
- checklist para revisão rápida e impressão
- suporte visual para sala de aula e para estudo autônomo

### Experiência de uso
- responsividade para desktop, tablet e mobile
- tema claro/escuro
- navegação simples e focada em acesso educacional
- layout visual com linguagem pedagógica e institucional

## Estrutura do repositório

```text
repcn/
├── index.html                   # Página principal do projeto
├── primeiro-dia.html            # Painel do 1º dia do ENEM
├── segundo-dia.html             # Painel do 2º dia do ENEM
├── checklist.html               # Material de revisão para impressão
├── LICENSE                      # Licença MIT
├── README.md                    # Documentação do projeto
├── SPRINTS.md                   # Histórico de desenvolvimento
├── assets/
│   ├── biotech_edudesign.png   # Logo institucional
│   ├── gov_mato_grosso.png     # Marca do governo estadual
│   ├── HQ_TRI.png              # Infográfico de TRI
│   ├── pamella_avatar.png       # Avatar do professor
│   ├── pre_enem.png            # Logotipo do projeto
│   ├── pre_enem_avatar.png     # Avatar do projeto
│   └── galeria/                # Pasta para fotos do evento
├── docs/
│   ├── mapa_calor.csv          # Base de dados de temas e frequência
│   ├── mapeamento_temas_redacao_enem.csv
│   └── Plano de Aula Executivo ... .docx
└── .gitignore
```

## Como executar localmente

### Opção 1: abrir diretamente no navegador

```bash
git clone https://github.com/Bio-Tech-Edu/repcn.git
cd repcn
# macOS
open index.html
# Linux
xdg-open index.html
# Windows
start index.html
```

### Opção 2: usar um servidor local

```bash
cd repcn
python3 -m http.server 8000
```

Depois, acesse:

```text
http://localhost:8000
```

> Como a aplicação depende de bibliotecas externas via CDN, a conexão com a internet é recomendada na primeira carga.

## Publicação no GitHub Pages

1. Acesse o repositório no GitHub.
2. Vá em `Settings` → `Pages`.
3. Em `Build and deployment`, selecione:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/ (root)`
4. Salve as configurações.

A página ficará disponível em:

```text
https://bio-tech-edu.github.io/repcn/
```

## Melhorias de qualidade e boas práticas para este tipo de projeto

A implementação atual mostra um bom alinhamento pedagógico e visual com o público-alvo. Para projetos estáticos de apresentação e ensino, as práticas mais importantes são:

### 1) Separar conteúdo, apresentação e comportamento
- manter HTML para estrutura semântica
- usar CSS para estilos e design sistemático
- manter lógica em JavaScript sem misturar regras de negócio com marcação
- evitar duplicação de trechos repetidos

### 2) Priorizar acessibilidade
- usar linguagem semântica (`header`, `main`, `section`, `article`, `nav`)
- garantir contraste adequado entre texto e fundo
- incluir textos alternativos em imagens e ícones informativos
- oferecer navegação por teclado e foco visível
- respeitar `prefers-reduced-motion` quando houver animações

### 3) Otimizar performance e carga
- reduzir arquivos pesados e imagens desnecessárias
- usar dimensões adequadas de imagem antes de publicar
- preferir carregamento otimizado para recursos externos
- manter a interface responsiva e leve para mobile

### 4) Manter dados e conteúdo organizados
- armazenar bases e listas em arquivos estruturados (`CSV`, JSON, ou módulos JS)
- separar conteúdos pedagógicos de código visual
- documentar como dados foram gerados, atualizados e mantidos

### 5) Garantir manutenção e escalabilidade
- documentar a arquitetura do projeto e a estrutura de pastas
- nomear arquivos de forma consistente
- manter a documentação de uso, revisão e publicação atualizada
- registrar decisões de design e evolução em `SPRINTS.md`

### 6) Validar em diferentes ambientes
- verificar renderização em navegadores modernos
- testar no mobile e em telas menores
- validar links internos, imagens e recursos externos
- confirmar funcionamento de interações e temas claro/escuro

### 7) Usar padrões de engenharia leves, mas consistentes
- definir convenções para nomes de arquivos, classes e scripts
- evitar código inline excessivo em páginas grandes
- manter a estrutura simples, rastreável e fácil de evoluir

## Checklist de qualidade recomendada

- [ ] HTML válido e semântica correta
- [ ] Contraste visual adequado em todas as telas
- [ ] Imagens com `alt` descritivo
- [ ] Navegação por teclado funcionando
- [ ] Responsividade em celulares e tablets
- [ ] Gráficos e interações carregando corretamente
- [ ] Links internos e externos funcionando
- [ ] Layout consistente com a identidade do projeto
- [ ] Documentação atualizada e fácil de seguir

## Desenvolvimento e manutenção

### Arquivos principais
- `index.html`: dashboard principal e estrutura geral
- `primeiro-dia.html`: conteúdo do primeiro dia do ENEM
- `segundo-dia.html`: conteúdo do segundo dia do ENEM
- `checklist.html`: material de revisão otimizado para impressão
- `docs/mapa_calor.csv`: dados estruturados de frequências e temas
- `SPRINTS.md`: histórico de evolução e backlog do projeto

### Recomendação para evoluir o código

Para uma próxima etapa de refinamento, vale considerar:

- quebrar a lógica em arquivos JS dedicados
- separar o CSS em folhas específicas, caso o projeto cresça
- padronizar dados em módulos reutilizáveis
- incluir validação HTML/CSS e testes básicos de navegação
- documentar cada página e seu objetivo didático

## Créditos

Desenvolvido por [Bio+Tech EduDesign](https://github.com/bio-tech-edu).

Apoio institucional:
- Governo do Estado de Mato Grosso
- Secretaria de Estado de Educação (SEDUC-MT)
- Projeto Pré-ENEM Digit@l MT

Professora responsável: Pâmella Araújo Balcaçar

## Licença

Este projeto está licenciado sob a MIT License. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

## Status

Projeto educacional ativo, com foco em material pedagógico e apresentação visual para preparação do ENEM.

---

Feito com propósito pedagógico para fortalecer a aprendizagem e a tomada de decisão em revisão de conteúdos do ENEM.
