# PO - Clone da Landing Page HBO MAX

Como Product Owner sênior, vou orientar sua equipe de 5 desenvolvedores iniciantes para criar um clone fiel da landing page HBO MAX, considerando a stack HTML + CSS e o prazo de 10 dias.

![Referência HBO MAX](https://github.com/user-attachments/assets/1a135c56-8bc6-4dce-940f-b1143a404e14)

## 1. Análise Inicial

### Mapeamento Detalhado da Página

Analisando a landing page HBO MAX, identifiquei os seguintes elementos principais:

**Estrutura da Página:**
- **Header/Navegação:** Logo HBO MAX, menu de navegação (INÍCIO, SÉRIES TV, FILMES, etc.), botão "ASSINE AGORA"
- **Hero Section:** Grid de thumbnails dos conteúdos com overlay do logo HBO MAX centralizado e call-to-action "Planos a partir de R$18,90/mês"
- **Seção de Planos:** Cards comparativos dos três planos (Básico com Anúncios, Standard, Platinum) com preços e funcionalidades
- **Seção de Conteúdos Destacados:** Carrossel horizontal com diferentes categorias de conteúdo (dramas, comédias, etc.)
- **Seção "Estreias que vão dar o que falar":** Grid de 6 thumbnails de novos lançamentos
- **Seção "Descubra o melhor de":** Carrossel de categorias (Realidades, Ação, Comédia) com conteúdos específicos
- **Footer:** Links organizados por categorias, informações legais, redes sociais

### Identificação de Desafios Técnicos

**Principais desafios considerando HTML + CSS e nível iniciante:**
1. **Grid Layout Complexo:** A página usa grids tanto para o hero section quanto para as seções de conteúdo, exigindo domínio de CSS Grid
2. **Responsividade Avançada:** Diferentes layouts para mobile/desktop com reorganização de elementos
3. **Carrosseis Horizontais:** Implementar scroll horizontal suave apenas com CSS
4. **Sobreposição de Elementos:** Logo centralizado sobre o grid de thumbnails com background semi-transparente
5. **Sistema de Cards:** Cards de planos com diferentes estados e comparações visuais

### Avaliação de Complexidade

**Complexidade Geral: 7/10**

**Justificativa:**
- Layout complexo com múltiplas seções e tipos de grid
- Necessidade de criar carrosseis apenas com CSS
- Responsividade em vários breakpoints
- Fidelidade visual alta exigida
- Sobreposições e efeitos visuais avançados para nível iniciante

### Sugestão de Componentização

```
hbo-max-clone/
├── index.html
├── css/
│   ├── styles.css (main stylesheet)
│   ├── header.css
│   ├── hero.css
│   ├── plans.css
│   ├── content-sections.css
│   ├── footer.css
│   └── responsive.css
├── images/
│   ├── thumbnails/
│   ├── logos/
│   └── icons/
└── assets/
    └── fonts/
```

### Observações UX/UI

- **Responsividade:** Mobile-first approach com breakpoints em 768px e 1024px
- **Acessibilidade:** Alt texts para todas as imagens, navegação por teclado, contraste adequado
- **Performance:** Otimização de imagens, CSS minificado
- **Fidelidade visual:** Cores HBO (#000000, #9D2EFF), tipografia, espaçamentos exatos

## 2. Planejamento de Sprints

### Sprint 1 - Setup e Estrutura Base
**Objetivo:** Configurar ambiente, estrutura base do projeto e implementar header responsivo
**Duração:** 1 semana

#### Desenvolvedor #1
- [ ] **#001 - Setup do Projeto e Estrutura HTML Base**
  - **Descrição:** Criar a estrutura inicial do projeto com arquivos HTML e CSS organizados. Definir a estrutura semântica básica da página (header, main, sections, footer) e configurar o arquivo CSS principal com reset e variáveis CSS para cores e fontes da HBO MAX.
  - **Critérios de aceite:** 
    - Estrutura de pastas criada conforme componentização
    - index.html com estrutura semântica completa
    - CSS reset aplicado
    - Variáveis CSS definidas para cores e fontes
    - Arquivo funciona sem erros no navegador
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** HTML5, CSS3
  - **Sugestão de recursos/técnicas:** Semantic HTML, CSS Custom Properties, CSS Reset
  - **Foco de treinamento:** Estruturação semântica e organização de arquivos
  - **Dependências:** Nenhuma
  - **Labels:** frontend, setup

#### Desenvolvedor #2
- [ ] **#002 - Implementação do Header e Navegação**
  - **Descrição:** Criar o header da página com logo HBO MAX, menu de navegação horizontal e botão "ASSINE AGORA". Usar Flexbox para organizar elementos e garantir que fique responsivo. Implementar states do menu (hover) e posicionamento correto dos elementos.
  - **Critérios de aceite:**
    - Header fixo no topo da página
    - Logo HBO MAX posicionado à esquerda
    - Menu navegação centralizado com links funcionais
    - Botão "ASSINE AGORA" destacado à direita
    - Hover states implementados
    - Responsivo em mobile (menu hambúrguer opcional)
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 10 horas
  - **Tecnologias:** HTML5, CSS3, Flexbox
  - **Sugestão de recursos/técnicas:** Flexbox justify-content, align-items, hover pseudo-classes
  - **Foco de treinamento:** Flexbox Layout e estados CSS
  - **Dependências:** #001
  - **Labels:** frontend, design

#### Desenvolvedor #3
- [ ] **#003 - Coleta e Otimização de Assets**
  - **Descrição:** Pesquisar e coletar todas as imagens necessárias (thumbnails, logos, ícones) para replicar a página HBO MAX. Organizar assets em pastas apropriadas, otimizar tamanhos para web e criar estrutura de nomenclatura padronizada. Documentar origem e uso de cada asset.
  - **Critérios de aceite:**
    - Todas as imagens da referência coletadas
    - Assets organizados em pastas por categoria
    - Imagens otimizadas para web (formato adequado, compressão)
    - Nomenclatura padronizada e documentada
    - Lista de assets criada para referência da equipe
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** Ferramentas de otimização de imagem
  - **Sugestão de recursos/técnicas:** Compressão de imagens, formatos webp/jpg, nomenclatura semântica
  - **Foco de treinamento:** Organização de assets e otimização
  - **Dependências:** #001
  - **Labels:** design, frontend

#### Desenvolvedor #4
- [ ] **#004 - Configuração CSS Base e Tipografia**
  - **Descrição:** Definir toda a base tipográfica do projeto seguindo o design HBO MAX. Configurar fonts families, tamanhos, pesos e line-heights. Criar classes utilitárias para textos e estabelecer hierarquia visual. Implementar sistema de cores usando variáveis CSS.
  - **Critérios de aceite:**
    - Fontes HBO MAX implementadas (ou similares)
    - Sistema de classes tipográficas criado
    - Variáveis CSS para cores definidas
    - Hierarquia visual estabelecida (h1, h2, h3, p, etc.)
    - Classes utilitárias funcionais
    - Teste em diferentes tamanhos de tela
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** CSS3, Google Fonts
  - **Sugestão de recursos/técnicas:** CSS Custom Properties, @import para fonts, rem units
  - **Foco de treinamento:** Sistema de design e variáveis CSS
  - **Dependências:** #001
  - **Labels:** frontend, design

#### Desenvolvedor #5
- [ ] **#005 - Documentação Initial e Tutorial Git/GitHub**
  - **Descrição:** Criar documentação inicial do projeto incluindo README detalhado, guia de instalação e configuração do ambiente, e tutorial prático de Git/GitHub para a equipe. Estabelecer padrões de commit, branching e code review. Criar templates para issues e pull requests.
  - **Critérios de aceite:**
    - README.md completo com instruções de setup
    - Tutorial Git/GitHub específico para o projeto
    - Padrões de commit definidos e documentados
    - Templates de issue e PR criados
    - Guia de contribuição estabelecido
    - Estrutura do projeto documentada
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** Markdown, Git, GitHub
  - **Sugestão de recursos/técnicas:** Markdown syntax, Git workflow, GitHub features
  - **Foco de treinamento:** Documentação técnica e versionamento
  - **Dependências:** #001
  - **Labels:** documentação

### Sprint 2 - Hero Section e Grid Principal
**Objetivo:** Implementar a seção hero com grid de thumbnails e overlay do logo HBO MAX
**Duração:** 1 semana

#### Desenvolvedor #1
- [ ] **#006 - Estrutura HTML do Hero Section**
  - **Descrição:** Criar a estrutura HTML semântica para a seção hero principal, incluindo container para o grid de thumbnails, área de overlay para logo e call-to-action. Definir containers e elementos necessários para posterior estilização com CSS Grid.
  - **Critérios de aceite:**
    - Estrutura HTML semântica do hero implementada
    - Containers apropriados para grid e overlay
    - Elementos de texto e CTA estruturados
    - Acessibilidade básica implementada (alt texts, roles)
    - HTML válido e sem erros
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 6 horas
  - **Tecnologias:** HTML5
  - **Sugestão de recursos/técnicas:** Semantic HTML, accessibility attributes
  - **Foco de treinamento:** Estruturação semântica avançada
  - **Dependências:** #001, #003
  - **Labels:** frontend

#### Desenvolvedor #2
- [ ] **#007 - CSS Grid Layout do Hero**
  - **Descrição:** Implementar CSS Grid para organizar os thumbnails na seção hero, criando layout responsivo que se adapta a diferentes tamanhos de tela. Usar grid-template-areas e auto-fit para responsividade. Garantir que thumbnails mantenham proporção adequada.
  - **Critérios de aceite:**
    - Grid responsivo funcionando em desktop e mobile
    - Thumbnails mantém proporção correta
    - Layout se adapta a diferentes quantidades de itens
    - Espaçamento adequado entre elementos
    - Performance otimizada
  - **Dificuldade:** ⭐⭐⭐⭐
  - **Estimativa:** 12 horas
  - **Tecnologias:** CSS3, CSS Grid
  - **Sugestão de recursos/técnicas:** CSS Grid, grid-template-columns, auto-fit, aspect-ratio
  - **Foco de treinamento:** CSS Grid Layout avançado
  - **Dependências:** #006
  - **Labels:** frontend, design

#### Desenvolvedor #3
- [ ] **#008 - Overlay e Posicionamento do Logo Central**
  - **Descrição:** Criar overlay semi-transparente sobre o grid de thumbnails e posicionar logo HBO MAX no centro com call-to-action. Usar position absolute/relative e z-index para sobreposição correta. Implementar backdrop-filter ou background rgba para efeito visual.
  - **Critérios de aceite:**
    - Overlay semi-transparente funcionando
    - Logo HBO MAX centralizado perfeitamente
    - Call-to-action visível e destacado
    - Efeito visual similar à referência
    - Funcionamento em diferentes resoluções
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 10 horas
  - **Tecnologias:** CSS3, Position, Z-index
  - **Sugestão de recursos/técnicas:** CSS positioning, backdrop-filter, transform centering
  - **Foco de treinamento:** Posicionamento CSS e camadas
  - **Dependências:** #007
  - **Labels:** frontend, design

#### Desenvolvedor #4
- [ ] **#009 - Responsividade do Hero Section**
  - **Descrição:** Implementar responsividade completa do hero section, adaptando grid, overlay e elementos para mobile, tablet e desktop. Criar breakpoints apropriados e testar em diferentes dispositivos. Ajustar tamanhos de fonte e espaçamentos proporcionalmente.
  - **Critérios de aceite:**
    - Hero responsivo em todos os breakpoints
    - Grid se reorganiza adequadamente no mobile
    - Textos legíveis em qualquer tamanho
    - Performance mantida em dispositivos móveis
    - Testes realizados em diferentes navegadores
  - **Dificuldade:** ⭐⭐⭐⭐
  - **Estimativa:** 12 horas
  - **Tecnologias:** CSS3, Media Queries
  - **Sugestão de recursos/técnicas:** Media queries, mobile-first approach, flexible units
  - **Foco de treinamento:** Design responsivo avançado
  - **Dependências:** #008
  - **Labels:** frontend, responsive

#### Desenvolvedor #5
- [ ] **#010 - Testes e Validação do Hero Section**
  - **Descrição:** Realizar testes abrangentes do hero section em diferentes navegadores e dispositivos. Validar HTML e CSS, verificar acessibilidade, performance e fidelidade visual com a referência. Documentar bugs encontrados e implementar correções.
  - **Critérios de aceite:**
    - Testes realizados em Chrome, Firefox, Safari, Edge
    - Validação HTML e CSS sem erros
    - Acessibilidade verificada (navegação por teclado, contraste)
    - Performance aceitável (LCP < 2.5s)
    - Fidelidade visual > 90% comparada à referência
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** DevTools, Validators
  - **Sugestão de recursos/técnicas:** Browser DevTools, W3C Validators, accessibility tools
  - **Foco de treinamento:** Testing e debugging
  - **Dependências:** #009
  - **Labels:** testing, quality-assurance

### Sprint 3 - Seção de Planos
**Objetivo:** Implementar seção de comparação de planos com cards responsivos
**Duração:** 1 semana

#### Desenvolvedor #1
- [ ] **#011 - Estrutura HTML da Seção de Planos**
  - **Descrição:** Criar estrutura HTML semântica para a seção de planos, incluindo título, descrição e containers para os três cards de planos (Básico, Standard, Platinum). Organizar informações de cada plano de forma hierárquica e acessível.
  - **Critérios de aceite:**
    - HTML semântico para seção de planos
    - Estrutura de cards bem definida
    - Informações organizadas hierarquicamente
    - Acessibilidade implementada
    - HTML válido
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 6 horas
  - **Tecnologias:** HTML5
  - **Sugestão de recursos/técnicas:** Semantic HTML, card patterns, accessibility
  - **Foco de treinamento:** Estruturação de componentes
  - **Dependências:** #001
  - **Labels:** frontend

#### Desenvolvedor #2
- [ ] **#012 - Estilização dos Cards de Planos**
  - **Descrição:** Estilizar os cards de planos usando Flexbox, criando layout visual atrativo com destaque para diferentes planos. Implementar hierarquia visual, cores adequadas e espaçamentos consistentes. Criar hover effects e estados visuais.
  - **Critérios de aceite:**
    - Cards visualmente atraentes e consistentes
    - Hierarquia visual clara (preços destacados)
    - Hover effects implementados
    - Cores e tipografia da marca HBO MAX
    - Layout equilibrado entre os três cards
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 10 horas
  - **Tecnologias:** CSS3, Flexbox
  - **Sugestão de recursos/técnicas:** Flexbox layout, CSS transitions, card design patterns
  - **Foco de treinamento:** Flexbox e design de componentes
  - **Dependências:** #011
  - **Labels:** frontend, design

#### Desenvolvedor #3
- [ ] **#013 - Grid Layout para Organização dos Cards**
  - **Descrição:** Usar CSS Grid para organizar os três cards de planos horizontalmente no desktop e adaptá-los para layout vertical no mobile. Garantir espaçamento adequado e alinhamento perfeito entre os cards.
  - **Critérios de aceite:**
    - Layout em grid funcionando para os cards
    - Alinhamento perfeito entre elementos
    - Espaçamento consistente
    - Adaptação adequada para mobile
    - Cards mantém altura similar
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** CSS3, CSS Grid
  - **Sugestão de recursos/técnicas:** CSS Grid, grid-template-columns, gap property
  - **Foco de treinamento:** CSS Grid para componentes
  - **Dependências:** #012
  - **Labels:** frontend, design

#### Desenvolvedor #4
- [ ] **#014 - Botões e CTAs dos Planos**
  - **Descrição:** Criar e estilizar botões de call-to-action para cada plano, implementando diferentes estados (normal, hover, active) e garantindo acessibilidade. Botões devem ser visualmente distintos mas consistentes com o design system.
  - **Critérios de aceite:**
    - Botões estilizados conforme design HBO MAX
    - Estados visuais implementados (hover, active, focus)
    - Acessibilidade de teclado funcionando
    - Consistência visual entre todos os botões
    - Responsividade adequada
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** CSS3
  - **Sugestão de recursos/técnicas:** CSS pseudo-classes, button accessibility, transitions
  - **Foco de treinamento:** Estados CSS e acessibilidade
  - **Dependências:** #013
  - **Labels:** frontend, accessibility

#### Desenvolvedor #5
- [ ] **#015 - Responsividade da Seção de Planos**
  - **Descrição:** Implementar responsividade completa da seção de planos, adaptando layout de grid para mobile (empilhamento vertical), ajustando tamanhos de fonte, espaçamentos e garantindo usabilidade em todos os dispositivos.
  - **Critérios de aceite:**
    - Layout responsivo funcionando em todos os breakpoints
    - Cards empilham verticalmente no mobile
    - Textos e botões permanecem legíveis
    - Espaçamentos proporcionais
    - Usabilidade mantida em touch devices
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 10 horas
  - **Tecnologias:** CSS3, Media Queries
  - **Sugestão de recursos/técnicas:** Responsive design, mobile-first, flexible layouts
  - **Foco de treinamento:** Design responsivo para componentes
  - **Dependências:** #014
  - **Labels:** frontend, responsive

### Sprint 4 - Seções de Conteúdo e Carrosseis
**Objetivo:** Implementar seções de conteúdo com carrosseis horizontais
**Duração:** 1 semana

#### Desenvolvedor #1
- [ ] **#016 - Estrutura HTML das Seções de Conteúdo**
  - **Descrição:** Criar estrutura HTML para as seções "As grandes histórias..." e "Estreias que vão dar o que falar", incluindo títulos, containers para carrosseis e grids de thumbnails. Organizar elementos para posterior implementação de scroll horizontal.
  - **Critérios de aceite:**
    - HTML semântico para todas as seções de conteúdo
    - Containers apropriados para carrosseis
    - Estrutura preparada para scroll horizontal
    - Acessibilidade básica implementada
    - HTML válido
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** HTML5
  - **Sugestão de recursos/técnicas:** Semantic HTML, carousel patterns
  - **Foco de treinamento:** Estruturação de componentes complexos
  - **Dependências:** #003
  - **Labels:** frontend

#### Desenvolvedor #2
- [ ] **#017 - Carrossel CSS Horizontal**
  - **Descrição:** Implementar carrossel horizontal usando apenas CSS com scroll suave. Criar layout que permite scroll horizontal de thumbnails mantendo responsividade. Usar overflow-x e scroll-behavior para navegação suave.
  - **Critérios de aceite:**
    - Carrossel horizontal funcionando
    - Scroll suave implementado
    - Thumbnails mantém proporção
    - Funciona em diferentes dispositivos
    - Performance otimizada
  - **Dificuldade:** ⭐⭐⭐⭐
  - **Estimativa:** 14 horas
  - **Tecnologias:** CSS3, Flexbox
  - **Sugestão de recursos/técnicas:** overflow-x: scroll, scroll-behavior: smooth, flexbox
  - **Foco de treinamento:** CSS scroll e carrosseis
  - **Dependências:** #016
  - **Labels:** frontend, advanced

#### Desenvolvedor #3
- [ ] **#018 - Grid de Estreias**
  - **Descrição:** Implementar grid de 6 thumbnails para seção "Estreias que vão dar o que falar" usando CSS Grid. Criar layout responsivo que se adapta de 3x2 no desktop para 2x3 no mobile, mantendo proporções adequadas.
  - **Critérios de aceite:**
    - Grid 3x2 funcionando no desktop
    - Adaptação para 2x3 no mobile
    - Proporções mantidas
    - Espaçamento adequado
    - Responsividade suave
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 10 horas
  - **Tecnologias:** CSS3, CSS Grid
  - **Sugestão de recursos/técnicas:** CSS Grid, grid-template-columns, responsive grid
  - **Foco de treinamento:** CSS Grid responsivo
  - **Dependências:** #016
  - **Labels:** frontend, design

#### Desenvolvedor #4
- [ ] **#019 - Seção "Descubra o melhor de"**
  - **Descrição:** Implementar seção de categorias com carrossel e navegação por tabs (Realidades, Ação, Comédia). Criar sistema de tabs funcionais apenas com CSS usando radio buttons ou similar, mantendo acessibilidade.
  - **Critérios de aceite:**
    - Sistema de tabs funcionando
    - Carrossel específico para cada categoria
    - Navegação acessível por teclado
    - Visual consistente com referência
    - Performance adequada
  - **Dificuldade:** ⭐⭐⭐⭐
  - **Estimativa:** 14 horas
  - **Tecnologias:** CSS3
  - **Sugestão de recursos/técnicas:** CSS-only tabs, radio buttons, pseudo-classes
  - **Foco de treinamento:** CSS interativo avançado
  - **Dependências:** #017
  - **Labels:** frontend, advanced

#### Desenvolvedor #5
- [ ] **#020 - Responsividade das Seções de Conteúdo**
  - **Descrição:** Garantir responsividade completa de todas as seções de conteúdo, adaptando carrosseis, grids e sistemas de navegação para mobile. Testar usabilidade touch e ajustar espaçamentos e tamanhos proporcionalmente.
  - **Critérios de aceite:**
    - Todas as seções responsivas
    - Carrosseis funcionam em touch devices
    - Grids se adaptam adequadamente
    - Navegação por tabs acessível no mobile
    - Performance mantida
  - **Dificuldade:** ⭐⭐⭐⭐
  - **Estimativa:** 12 horas
  - **Tecnologias:** CSS3, Media Queries
  - **Sugestão de recursos/técnicas:** Touch-friendly design, responsive carousels
  - **Foco de treinamento:** Responsividade avançada
  - **Dependências:** #019
  - **Labels:** frontend, responsive

### Sprint 5 - Footer e Finalização
**Objetivo:** Implementar footer, FAQ section e finalizar o projeto
**Duração:** 1 semana

#### Desenvolvedor #1
- [ ] **#021 - Estrutura HTML do Footer**
  - **Descrição:** Criar estrutura HTML completa do footer incluindo links organizados por categorias, informações legais, redes sociais e seção de FAQ. Organizar elementos de forma semântica e acessível.
  - **Critérios de aceite:**
    - Footer estruturado semanticamente
    - Links organizados por categorias
    - Seção de FAQ estruturada
    - Informações legais incluídas
    - Acessibilidade implementada
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** HTML5
  - **Sugestão de recursos/técnicas:** Semantic HTML, footer patterns, accessibility
  - **Foco de treinamento:** Estruturação completa de páginas
  - **Dependências:** #001
  - **Labels:** frontend

#### Desenvolvedor #2
- [ ] **#022 - Estilização do Footer**
  - **Descrição:** Estilizar footer usando Flexbox e Grid para organizar links em colunas, implementar hierarquia visual e garantir consistência com o design HBO MAX. Criar hover effects e estados visuais apropriados.
  - **Critérios de aceite:**
    - Footer estilizado conforme referência
    - Links organizados em colunas
    - Hierarquia visual clara
    - Hover effects implementados
    - Consistência com design system
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 10 horas
  - **Tecnologias:** CSS3, Flexbox, Grid
  - **Sugestão de recursos/técnicas:** CSS Grid para layout, Flexbox para alinhamento
  - **Foco de treinamento:** Combinação Grid + Flexbox
  - **Dependências:** #021
  - **Labels:** frontend, design

#### Desenvolvedor #3
- [ ] **#023 - Seção FAQ com Acordeão**
  - **Descrição:** Implementar seção de FAQ com funcionalidade de acordeão usando apenas CSS. Usar técnicas como checkbox hack ou details/summary para criar expand/collapse functionality mantendo acessibilidade.
  - **Critérios de aceite:**
    - FAQ accordion funcionando apenas com CSS
    - Animações suaves de abertura/fechamento
    - Acessibilidade de teclado mantida
    - Visual consistente com referência
    - Performance otimizada
  - **Dificuldade:** ⭐⭐⭐⭐
  - **Estimativa:** 12 horas
  - **Tecnologias:** CSS3, HTML5
  - **Sugestão de recursos/técnicas:** CSS accordion, details/summary, transitions
  - **Foco de treinamento:** CSS interativo avançado
  - **Dependências:** #021
  - **Labels:** frontend, advanced

#### Desenvolvedor #4
- [ ] **#024 - Otimização Final e Performance**
  - **Descrição:** Otimizar CSS final, remover código desnecessário, minificar arquivos, otimizar imagens e implementar melhorias de performance. Verificar carregamento de recursos e ajustar para melhor experiência do usuário.
  - **Critérios de aceite:**
    - CSS otimizado e minificado
    - Imagens otimizadas para web
    - Tempo de carregamento < 3s
    - Sem código CSS não utilizado
    - Performance testada e documentada
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 10 horas
  - **Tecnologias:** CSS3, Performance Tools
  - **Sugestão de recursos/técnicas:** CSS optimization, image compression, performance testing
  - **Foco de treinamento:** Otimização e performance
  - **Dependências:** #023
  - **Labels:** performance, optimization

#### Desenvolvedor #5
- [ ] **#025 - Testes Finais e Deploy**
  - **Descrição:** Realizar testes finais abrangentes em todos os navegadores e dispositivos, criar documentação de entrega, implementar deploy no GitHub Pages e criar apresentação final com comparativo visual original vs clone.
  - **Critérios de aceite:**
    - Testes completos em todos os navegadores principais
    - Deploy funcional no GitHub Pages
    - Documentação de entrega completa
    - Vídeo demo criado
    - Comparativo visual documentado
    - README atualizado com instruções finais
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 12 horas
  - **Tecnologias:** GitHub Pages, Testing Tools
  - **Sugestão de recursos/técnicas:** Cross-browser testing, deployment, documentation
  - **Foco de treinamento:** Deploy e documentação
  - **Dependências:** #024
  - **Labels:** testing, deployment, documentation

## 3. Tutorial Git/GitHub para Desenvolvedores Iniciantes

### 3.1 O que é Git e GitHub?

- **Git**: Sistema de controle de versão que permite rastrear mudanças no código e colaborar com outros desenvolvedores.
- **GitHub**: Plataforma online que hospeda repositórios Git e oferece ferramentas de colaboração.

### 3.2 Configuração Inicial

#### No VSCode (Primeira vez)
```bash
# Configurar nome e email (necessário apenas uma vez)
git config --global user.name "Seu Nome"
git config --global user.email "seu.email@exemplo.com"
```

#### No GitHub (GUI)
1. Criar conta no GitHub.com
2. Fazer login na plataforma
3. Criar um novo repositório para o projeto: "hbo-max-clone"

### 3.3 Comandos Essenciais do Git no VSCode

#### Comandos Básicos no Terminal do VSCode:

```bash
# Verificar o status dos arquivos
git status

# Adicionar arquivos específicos para commit
git add nome-do-arquivo.html
git add .  # adiciona todos os arquivos modificados

# Fazer commit (salvar uma versão)
git commit -m "Mensagem descritiva do que foi feito"

# Ver histórico de commits
git log --oneline

# Enviar mudanças para o GitHub
git push origin main

# Baixar mudanças do GitHub
git pull origin main

# Criar uma nova branch (ramificação)
git checkout -b nome-da-nova-branch

# Mudar para uma branch existente
git checkout nome-da-branch

# Ver todas as branches
git branch

# Mergear (juntar) uma branch na main
git checkout main
git merge nome-da-branch
```

### 3.4 Usando Git através da Interface do VSCode

#### Painel Source Control (Ctrl+Shift+G):
1. **Mudanças não commitadas** aparecem na seção "Changes"
2. **Adicionar ao Stage**: Clique no "+" ao lado do arquivo
3. **Fazer Commit**: Digite a mensagem na caixa de texto e clique em "✓ Commit"
4. **Push**: Clique nos três pontos (...) → "Push"
5. **Pull**: Clique nos três pontos (...) → "Pull"

#### Branches no VSCode:
1. **Criar branch**: Clique no nome da branch atual (canto inferior esquerdo) → "Create new branch"
2. **Trocar branch**: Clique no nome da branch atual → Selecione a branch desejada

### 3.5 Usando a Interface Web do GitHub

#### Visualizando o Código:
1. Acesse seu repositório no GitHub.com
2. Navegue pelos arquivos clicando neles
3. Use o botão "Code" para ver opções de download

#### Fazendo Mudanças Direto no GitHub:
1. **Editar arquivo**: Clique no arquivo → Clique no ícone de lápis (Edit)
2. **Fazer commit**: Após editar, role para baixo → Escreva mensagem do commit → "Commit changes"
3. **Criar arquivo**: Botão "Add file" → "Create new file"

#### Pull Requests (PRs):
1. **Criar PR**: Vá para "Pull requests" → "New pull request"
2. **Selecionar branches**: Escolha a branch de origem e destino
3. **Revisar**: Adicione título, descrição e revisar as mudanças
4. **Merge**: Após aprovação, clique em "Merge pull request"

### 3.6 Fluxo de Trabalho Recomendado para o Projeto

#### Para cada nova funcionalidade:
```bash
# 1. Sempre comece com a branch main atualizada
git checkout main
git pull origin main

# 2. Crie uma nova branch para sua task
git checkout -b feature/task-001-setup-projeto

# 3. Trabalhe normalmente, fazendo commits pequenos e frequentes
git add .
git commit -m "Adicionar estrutura HTML base"

# 4. Quando terminar, envie sua branch
git push origin feature/task-001-setup-projeto

# 5. Abra um Pull Request no GitHub para revisão
# 6. Após aprovação, faça merge e delete a branch
```

### 3.7 Situações Comuns e Soluções

#### Erro "Please commit your changes":
```bash
# Salve suas mudanças antes de trocar de branch
git add .
git commit -m "WIP: Salvando progresso"
git checkout outra-branch
```

#### Desfazer o último commit (sem perder mudanças):
```bash
git reset --soft HEAD~1
```

#### Ver diferenças antes de fazer commit:
```bash
git diff  # no terminal
# ou use a aba "Source Control" no VSCode
```

#### Resolver conflitos de merge:
1. O VSCode destacará os conflitos
2. Escolha qual versão manter ou combine ambas
3. Remova as marcações de conflito (`<<<<<<<`, `=======`, `>>>>>>>`)
4. Faça commit das correções

### 3.8 Boas Práticas para o Projeto

#### Mensagens de Commit:
- Use presente do indicativo: "Adiciona" ao invés de "Adicionei"
- Seja específico: "Implementa header responsivo com navegação"
- Evite mensagens vagas: "Update", "Fix", "Changes"

#### Estrutura de Branches:
- `main`: Código principal e estável
- `feature/task-XXX-nome`: Novas funcionalidades
- `fix/task-XXX-nome`: Correções de bugs
- `docs/task-XXX-nome`: Atualizações de documentação

#### Commits Frequentes:
- Faça commits pequenos e frequentes
- Cada commit deve representar uma mudança lógica
- Teste antes de fazer commit

### 3.9 Checklist de Git/GitHub para Desenvolvedores

**Antes de começar uma task:**
- [ ] Branch main está atualizada (`git pull origin main`)
- [ ] Nova branch criada com nome descritivo
- [ ] Ambiente de desenvolvimento funcionando

**Durante o desenvolvimento:**
- [ ] Commits frequentes com mensagens claras
- [ ] Código testado antes de cada commit
- [ ] Arquivos desnecessários não commitados

**Ao finalizar uma task:**
- [ ] Branch enviada para GitHub (`git push`)
- [ ] Pull Request criado com descrição detalhada
- [ ] Código revisado por outro membro da equipe
- [ ] Merge aprovado e branch deletada

### 3.10 Links Úteis

- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [GitHub Desktop](https://desktop.github.com/) - Interface gráfica alternativa
- [Visualizing Git](https://git-school.github.io/visualizing-git/) - Ferramenta para entender branches
- [Oh My Git!](https://ohmygit.org/) - Jogo para aprender Git

## 4. Recomendações Finais

### Ferramenta de Gestão Recomendada

**GitHub Projects** - Por integrar nativamente com o repositório e ser gratuito, ideal para iniciantes.

### Estratégia de Versionamento e Colaboração

- **Branches obrigatórias** para cada task (`feature/task-XXX-nome`)
- **Pull Requests** para todas as mudanças na main
- **Code Review** obrigatório entre pares (mínimo 1 aprovação)
- **Deploy** apenas da branch `main`
- **Commits semânticos** seguindo padrão estabelecido

### Estratégia de Testes

- **Testes manuais por checklist** após cada task
- **Revisão de layout** comparando lado a lado com referência
- **Teste funcional** de cada componente em diferentes dispositivos
- **Cross-browser testing**: Chrome, Firefox, Safari, Edge
- **Teste entre pares**: um colega revisa o trabalho do outro

### Principais Riscos e Pontos de Atenção

- **Limitações de prazo**: Manter escopo enxuto, evitar funcionalidades extras
- **Gargalos técnicos**: Grid e Flexbox podem ser desafiadores - documentar dúvidas
- **Conflitos de merge**: Comunicar sempre quando trabalhar no mesmo arquivo
- **Integração**: Testes constantes de integração entre seções
- **Qualidade**: Manter foco na fidelidade visual sem comprometer cronograma

### Checkpoints Intermediários

- **Daily stand-ups**: 15min diários para alinhamento
- **Review semanal**: 1h para apresentação dos resultados da sprint
- **Dúvidas técnicas**: Canal dedicado para suporte entre pares
- **Demo incremental**: Apresentação do progresso a cada sprint

## 5. Checklist de Entrega Final

- [ ] Código revisado, limpo e comentado
- [ ] README/documentação básica com instruções de instalação
- [ ] Tutorial Git/GitHub incluído na documentação
- [ ] Histórico de commits organizado e com mensagens claras
- [ ] Deploy disponível (GitHub Pages) com URL funcional
- [ ] Screenshots comparativos (original vs clone)
- [ ] Vídeo demo da página funcionando (2-3 minutos)
- [ ] Todos os critérios de sucesso validados
- [ ] Feedback dos pares incorporado
- [ ] Repositório organizado com estrutura de pastas clara
- [ ] Acessibilidade básica implementada
- [ ] Responsividade testada em múltiplos dispositivos
- [ ] Performance otimizada (imagens, CSS)

## 6. Critérios de Sucesso (Definição de Pronto)

- [ ] O visual é idêntico ou muito próximo ao da referência
- [ ] Todas as funcionalidades presentes na referência estão implementadas
- [ ] O site é responsivo (funciona bem em mobile e desktop)
- [ ] O site atende ao mínimo de acessibilidade (ex.: nível AA)
- [ ] Passa por todos os testes e revisões definidos
- [ ] Possui documentação básica (README) e instruções para rodar localmente
- [ ] Entrega inclui prints ou vídeo demonstrativo do resultado
- [ ] **Todos os desenvolvedores dominam Git/GitHub** e seguem o fluxo de trabalho definido

## 7. Cronograma Resumido

| Sprint | Período | Foco Principal | Entregáveis |
|--------|---------|----------------|-------------|
| 1 | Dias 1-2 | Setup e Header | Estrutura base + Header responsivo |
| 2 | Dias 3-4 | Hero Section | Grid principal + Overlay |
| 3 | Dias 5-6 | Seção de Planos | Cards comparativos responsivos |
| 4 | Dias 7-8 | Conteúdos | Carrosseis + Grids de conteúdo |
| 5 | Dias 9-10 | Footer + Entrega | Footer + FAQ + Deploy final |

**Data de entrega:** 10 dias
**Total de horas por pessoa:** 50 horas (10h/semana x 1 semana)
**Total de horas da equipe:** 250 horas

## 8. Observações UX/UI Detalhadas

### Design System HBO MAX

**Cores principais:**
- Preto: #000000
- Roxo HBO: #9D2EFF
- Branco: #FFFFFF
- Cinza escuro: #1C1C1C
- Cinza claro: #8E8E93

**Tipografia:**
- Font principal: Helvetica Neue, Arial, sans-serif
- Títulos: Bold, 2.5rem - 1.5rem
- Corpo: Regular, 1rem - 0.875rem
- Botões: Medium, 1rem

**Espaçamentos:**
- Container max-width: 1200px
- Padding lateral: 20px (Mobile), 40px (Desktop)
- Grid gap: 16px (Mobile), 24px (Desktop)
- Section spacing: 60px (Mobile), 100px (Desktop)

**Breakpoints:**
- Mobile: 320px - 767px
- Tablet: 768px - 1023px
- Desktop: 1024px+

### Acessibilidade Requirements

**WCAG AA Compliance:**
- Contraste mínimo 4.5:1 para texto normal
- Contraste mínimo 3:1 para texto grande
- Navegação completa por teclado
- Alt texts descritivos para todas as imagens
- Focus indicators visíveis
- Headings hierárquicos (h1, h2, h3...)
- ARIA labels quando necessário

## 9. Governança e Comunicação

### Rituais Recomendados

**Daily Standup (15min - Segunda a Sexta)**
- O que fiz ontem?
- O que vou fazer hoje?
- Tenho algum bloqueio?

**Sprint Review (1h - A cada 2 dias)**
- Demo do que foi desenvolvido
- Feedback do time
- Retrospectiva rápida
- Planejamento da próxima sprint

**Code Review (Assíncrono)**
- Todo PR deve ser revisado por pelo menos 1 pessoa
- Feedback construtivo e didático
- Aprovação obrigatória antes do merge

### Canais de Comunicação

**GitHub Issues**: Para bugs e melhorias
**GitHub Discussions**: Para dúvidas técnicas
**Pull Request Reviews**: Para feedback de código
**README do projeto**: Para documentação central

## 10. Templates de Documentação

### Template de Pull Request
```
## Descrição
Implementação do [componente/funcionalidade]

## Task relacionada
- Resolve #XXX

## Screenshots
[Adicionar screenshots antes/depois]

## Checklist
- [ ] Código testado em Chrome e Firefox
- [ ] Responsivo em mobile e desktop
- [ ] Sem erros no console
- [ ] Código comentado quando necessário
- [ ] Fidelidade visual mantida
```

### Template de Issue
```
## Descrição
Descrição clara do problema ou funcionalidade

## Critérios de aceite
- [ ] Critério 1
- [ ] Critério 2

## Informações adicionais
Screenshots, links, referências
```

## 11. Informações do Projeto

### Dados Gerais
- **Página de referência:** HBO MAX Landing Page
- **Nível técnico da equipe:** Iniciante
- **Tamanho da equipe:** 5 desenvolvedores
- **Disponibilidade:** 10 horas/semana por pessoa
- **Stack tecnológica:** HTML + CSS
- **Prazo desejado:** 10 dias
- **Foco de treinamento:** Grid Layout e Flexbox no CSS
- **Observações UX/UI:** Site responsivo, dark mode opcional, acessibilidade AA

### Entregáveis Principais
1. **Análise Inicial:** ✅ Completa
2. **Planejamento de Sprints:** ✅ 5 sprints com 25 tasks distribuídas
3. **Tutorial Git/GitHub:** ✅ Completo e didático
4. **Recomendações Finais:** ✅ Estratégias e ferramentas definidas

## 12. Restrições e Diretrizes

- **Não** utilizar JavaScript ou bibliotecas externas
- **Não** adicionar funcionalidades não presentes na referência
- **Sempre** considerar nível iniciante ao propor tasks
- **Priorizar** Grid Layout e Flexbox para treinamento
- **Manter** fidelidade visual alta
- **Documentar** todas as decisões técnicas
- **Usar Git/GitHub** obrigatoriamente

---

**Próximos Passos:**
1. Revisar este planejamento com toda a equipe
2. Configurar o repositório GitHub "hbo-max-clone"
3. Distribuir as tasks da Sprint 1
4. Estabelecer rituais de comunicação
5. Iniciar o desenvolvimento!

**Contato do PO:** Product Owner HBO MAX Clone Project
**Data de criação:** 2025-06-06
**Última atualização:** 2025-06-06

Estou disponível para esclarecimentos e ajustes no planejamento. Vamos criar um clone incrível da HBO MAX! 🚀
