# Raio-X Estratégico — 2º dia do ENEM

Plataforma interativa de apoio ao estudo de **Ciências da Natureza** para o ENEM, com foco em repertório estratégico, visualização de dados e revisão de prova.

[![HTML5](https://img.shields.io/badge/HTML5-100%25-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-v3-06B6D4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Chart.js](https://img.shields.io/badge/Chart.js-4.4.1-FF6384?logo=chart.js&logoColor=white)](https://www.chartjs.org/)

## 🚀 Acesso rápido

| Recurso | Link |
|---------|------|
| **Aplicação principal** | [Abrir `index.html`](index.html) |
| **Checklist para impressão** | [Abrir `checklist.html`](checklist.html) |
| **Repositório GitHub** | [Bio-Tech-Edu/repcn](https://github.com/Bio-Tech-Edu/repcn) |

> A aplicação carrega recursos via CDN. Recomenda-se acesso com conexão à internet.

---

## 📋 O que é este projeto

Este repositório contém uma aplicação web estática, sem backend, projetada para apoiar aulas, revisões e simulados de preparação para o ENEM. Foca especialmente no segundo dia da prova — Ciências da Natureza e suas Tecnologias — e é ideal para uso em:

- Sala de aula com projetor
- Grupos de estudo presenciais ou remotos
- Revisão individual antes da prova
- Eventos preparatórios e aulões

## 🎯 Principais recursos

### Painel analítico
- Distribuição das 45 questões de Ciências da Natureza (Biologia, Química, Física)
- Análise de frequência de temas e competências BNCC
- **Mapa de calor** com 23 subtemas e suas taxas de cobrança (2014–2024)
- Filtros por disciplina e modal com detalhes de competências

### Estudo de caso integrado
Usa a **Estação de Tratamento de Água** como situação-problema para integrar:
- **Química:** coagulação, floculação, tratamento de misturas
- **Física:** decantação, gravidade, empuxo, densidade
- **Biologia:** desinfecção, cloração, saneamento, eutrofização

### Simulação e prática
- **Think-Pair-Share:** dinâmica colaborativa com cronômetro
- Questões comentadas com gabarito e análise de distratores
- Protocolo prático para gestão de tempo na prova
- Guia de eliminação de distratores (3 perfis identificáveis)

### Material de revisão
- **Checklist de conteúdos** prioritários por componente
- Versão otimizada para **impressão/PDF**
- Símbolos visuais e códigos de competência BNCC/ENEM

---

## 📁 Estrutura do repositório

```
repcn/
├── index.html              # Aplicação principal (dashboard + módulos pedagógicos)
├── checklist.html          # Guia de revisão para impressão/PDF
├── mapa_calor.csv          # Base de dados: 23 temas × frequência × competências
├── assets/
│   ├── galeria/            # Fotos do evento (com instruções de uso)
│   ├── HQ_TRI.png          # Infográfico sobre Teoria de Resposta ao Item
│   ├── pamella_avatar.png  # Avatar da professora
│   ├── pre_enem_avatar.png # Logo do projeto
│   └── ...
├── docs/
│   └── Plano de Aula Executivo.docx    # Estrutura pedagógica da aula
├── SPRINTS.md              # Histórico de desenvolvimento e backlog
├── .gitignore              # Configuração de arquivos ignorados
└── README.md               # Este arquivo
```

---

## ⚙️ Como usar localmente

### Opção 1: abrir direto no navegador

```bash
git clone https://github.com/Bio-Tech-Edu/repcn.git
cd repcn
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows
```

### Opção 2: com servidor local

```bash
cd repcn
python3 -m http.server 8000
# Acesse: http://localhost:8000
```

---

## 🌐 Publicação no GitHub Pages

1. Abra o repositório no GitHub
2. Vá em **Settings → Pages**
3. Em **Build and deployment**, selecione:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/ (root)`
4. Salve as configurações

A página ficará disponível em:
```
https://bio-tech-edu.github.io/repcn/
```

---

## 📸 Como adicionar fotos à galeria

1. Salve as imagens em `assets/galeria/` (`.jpg` ou `.png`)
2. Abra `index.html` e localize `GALERIA_FOTOS`
3. Adicione cada foto com `src` e `alt` descritivos:

```javascript
const GALERIA_FOTOS = [
  {
    src: 'assets/galeria/foto1.jpg',
    alt: 'Estudantes participando do aulão em Juscimeira-MT'
  },
  {
    src: 'assets/galeria/foto2.jpg',
    alt: 'Professora apresentando o dashboard do Raio-X'
  }
];
```

4. Salve o arquivo e publique

> Consulte [`assets/galeria/README.md`](assets/galeria/README.md) para instruções detalhadas.

---

## 👥 Contexto pedagógico

| Aspecto | Descrição |
|---------|-----------|
| **Público-alvo** | Estudantes do Ensino Médio (2º e 3º anos) |
| **Componente curricular** | Ciências da Natureza e suas Tecnologias |
| **Duração sugerida** | 50 minutos (aula ou revisão) |
| **Metodologia** | Estudo de Caso Integrado + Think-Pair-Share |
| **Competências trabalhadas** | Competências específicas 1 e 3 de Ciências da Natureza (BNCC) |
| **Projeto associado** | Pré-ENEM Digit@l MT / SEDUC-MT |

---

## 🔧 Desenvolvimento e manutenção

A aplicação é intencionalmente simples e estática. Para editar conteúdo ou fazer melhorias:

### Arquivos principais
- `index.html` — interface, estilos (Tailwind), dados e interações
- `checklist.html` — material de impressão
- `mapa_calor.csv` — frequência e competências dos temas
- `SPRINTS.md` — decisões técnicas e backlog de melhorias

### Checklist pré-publicação
- [ ] Gráficos carregam corretamente (rosca + barras TRI)
- [ ] Mapa de calor responde aos filtros por disciplina
- [ ] Cronômetro Think-Pair-Share funciona
- [ ] Tema claro/escuro alternancia corretamente
- [ ] Checklist imprime bem em PDF
- [ ] Imagens da galeria carregam
- [ ] Navegação por teclado (abas, botões)
- [ ] Textos alternativos em imagens estão presentes

---

## 📚 Dados e conteúdo

O arquivo [`mapa_calor.csv`](mapa_calor.csv) organiza 23 subtemas de Ciências da Natureza com:
- Disciplina (Biologia, Química, Física)
- Tema principal e subtema
- Frequência relativa (%)
- Nível de calor (muito alta, alta, média, baixa)
- Competências BNCC/ENEM associadas
- Descrição sintética da competência

Os dados são incorporados ao `index.html` e renderizados interativamente via Chart.js e lógica JavaScript.

---

## ✨ Recursos técnicos

- **100% HTML/CSS/JavaScript** — sem framework backend
- **Responsivo** — funciona em desktop, tablet e mobile
- **Acessível** — navegação por teclado, ARIA labels, contraste revisado
- **Tema claro/escuro** — detecta preferência do SO e permite alternância manual
- **Offline-ready** — uma vez carregado, funciona sem conexão (exceto gráficos dinâmicos)

---

## 📖 Histórico e evolução

O projeto passou por 4 sprints de desenvolvimento:
- **Sprint 0:** Auditoria do código legado e correção de sintaxe
- **Sprint 1:** Restauração funcional completa
- **Sprint 2:** Redesign visual (sistema de design raio-x/diagnóstico)
- **Sprint 3:** Acessibilidade e interações
- **Sprint 4:** QA e documentação

Consulte [`SPRINTS.md`](SPRINTS.md) para detalhes técnicos, decisões de design e backlog futuro.

---

## 🤝 Créditos

Desenvolvido por **[Bio+Tech EduDesign](https://github.com/bio-tech-edu)**

**Apoio institucional:**
- Governo do Estado de Mato Grosso
- Secretaria de Estado de Educação (SEDUC-MT)
- Pré-ENEM Digit@l MT

**Professora responsável:** Pâmella Araújo Balcaçar
- 🎓 Licenciada em Ciências Biológicas (UFMT)
- 💻 Tecnóloga em Informática
- 🏫 Mais de 14 anos de docência

---

## 📜 Licença
MIT — livre para uso pedagógico em escolas públicas e privadas. Veja [LICENÇA](LICENSE) .

---

## 🎯 Status

Projeto educacional ativo em evolução. Sugestões de melhorias são bem-vindas via issues no repositório.

**Última atualização:** 2026-09-29

--- 

🇧🇷 Feito com ❤️ para estudantes brasileiros do ENEM 🇧🇷
