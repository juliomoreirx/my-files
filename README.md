# PO - Clone da Landing Page HBO Max

Como Product Owner sênior, vou orientar sua equipe de 5 desenvolvedores iniciantes para criar um clone fiel da landing page da HBO Max, considerando a stack HTML+CSS e o prazo até 17/06/2025.

![Referência HBO Max](https://github.com/user-attachments/assets/1a135c56-8bc6-4dce-940f-b1143a404e14)


## 1. Análise Inicial

### Mapeamento Detalhado da Página

Analisando a landing page da HBO Max, identifiquei os seguintes elementos principais:

**Estrutura da Página:**
- **Header/Navegação:** Logo HBO Max, menu de navegação horizontal, botão de login
- **Hero Section:** Banner principal com conteúdo em destaque e call-to-action
- **Carrossel de Conteúdo:** Grid responsivo com posters de filmes/séries
- **Seção de Planos:** Cards com opções de assinatura (Básico, Standard, Platinum)
- **Seção de Categorias:** Grid com diferentes gêneros (Ação, Comédia, Drama, etc.)
- **Seção "Estreias":** Destaque para novos lançamentos
- **Seção de Gêneros:** Carrossel horizontal com conteúdo por categoria
- **FAQ Section:** Perguntas frequentes com accordion
- **Footer:** Links institucionais, redes sociais, informações legais

### Identificação de Desafios Técnicos

**Principais desafios considerando HTML+CSS e nível iniciante:**
1. **Responsividade complexa:** Layout que funciona em mobile e desktop
2. **Grid layouts:** Organização de múltiplos cards de conteúdo
3. **Carrosseis/Sliders:** Movimento horizontal de conteúdo (usando CSS puro)
4. **Accordion FAQ:** Funcionalidade expand/collapse
5. **Hover effects:** Interações visuais nos cards
6. **Tipografia e cores:** Fidelidade ao design original

### Avaliação de Complexidade

**Complexidade Geral: 7/10**

**Justificativa:**
- Layout complexo com múltiplas seções
- Responsividade avançada necessária
- Limitação do CSS puro para interações
- Grande quantidade de elementos visuais
- Necessidade de organização de assets (imagens)

### Sugestão de Componentização

```
src/
├── index.html
├── css/
│   ├── styles.css (arquivo principal)
│   ├── header.css
│   ├── hero.css
│   ├── content-grid.css
│   ├── pricing.css
│   ├── categories.css
│   ├── faq.css
│   ├── footer.css
│   └── responsive.css
├── images/
│   ├── logo/
│   ├── posters/
│   ├── backgrounds/
│   └── icons/
└── assets/
    └── fonts/
```

### Observações UX/UI

- **Responsividade:** Mobile-first approach obrigatório
- **Acessibilidade:** Contraste adequado, navegação por teclado, alt texts
- **Performance:** Otimização de imagens, CSS organizado
- **Fidelidade visual:** Cores, fontes e espaçamentos fiéis ao original

## 2. Planejamento de Sprints

### Sprint 1 - Estrutura Base e Header
**Objetivo:** Criar a estrutura HTML básica e implementar o header responsivo
**Duração:** 1 semana

#### Desenvolvedor #1
- [ ] **#001 - Estrutura HTML Base**
  - **Descrição:** Criar a estrutura semântica completa do HTML da landing page. Isso inclui definir todas as seções principais (header, main, footer) com as tags semânticas apropriadas (nav, section, article, etc.). Esta tarefa é fundamental pois servirá como base para todo o projeto.
  - **Critérios de aceite:** HTML validado, estrutura semântica correta, comentários organizacionais, arquivo index.html funcional
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** HTML5
  - **Sugestão de recursos/técnicas:** Semantic HTML, HTML5 tags (nav, main, section, article, aside)
  - **Foco de treinamento:** HTML semântico e boas práticas
  - **Dependências:** Nenhuma
  - **Labels:** frontend, documentação

#### Desenvolvedor #2
- [ ] **#002 - Header Responsivo**
  - **Descrição:** Implementar o header da HBO Max com logo, menu de navegação e botão de login. O header deve ser fixo no topo e responsivo, colapsando em menu hambúrguer no mobile. Use Flexbox para organizar os elementos horizontalmente.
  - **Critérios de aceite:** Header fixo, logo posicionado, menu responsivo, botão de login estilizado, funciona em mobile e desktop
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 10 horas
  - **Tecnologias:** HTML, CSS
  - **Sugestão de recursos/técnicas:** Flexbox, Position fixed, Media Queries, CSS pseudo-classes
  - **Foco de treinamento:** Flexbox e responsividade
  - **Dependências:** #001
  - **Labels:** frontend, design

#### Desenvolvedor #3
- [ ] **#003 - Reset CSS e Variáveis**
  - **Descrição:** Criar um CSS reset personalizado e definir todas as variáveis CSS (cores, fontes, espaçamentos) baseadas no design da HBO Max. Isso garantirá consistência visual em todo o projeto e facilitará manutenções futuras.
  - **Critérios de aceite:** CSS reset aplicado, variáveis definidas, documentação das cores e fontes, estilos base criados
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 6 horas
  - **Tecnologias:** CSS
  - **Sugestão de recursos/técnicas:** CSS Variables (Custom Properties), CSS Reset, Typography
  - **Foco de treinamento:** CSS avançado e organização
  - **Dependências:** #001
  - **Labels:** frontend, design

#### Desenvolvedor #4
- [ ] **#004 - Setup do Projeto e Git**
  - **Descrição:** Configurar a estrutura de pastas do projeto, criar o README inicial com instruções de setup, configurar o repositório Git e criar os primeiros commits. Documentar o processo de desenvolvimento local.
  - **Critérios de aceite:** Estrutura de pastas organizada, README completo, repositório configurado, .gitignore criado
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 4 horas
  - **Tecnologias:** Git, GitHub
  - **Sugestão de recursos/técnicas:** Git commands, Markdown, File organization
  - **Foco de treinamento:** Git/GitHub e documentação
  - **Dependências:** Nenhuma
  - **Labels:** documentação

#### Desenvolvedor #5
- [ ] **#005 - Coleta e Organização de Assets**
  - **Descrição:** Coletar todas as imagens necessárias (logo, posters, backgrounds), otimizá-las para web e organizá-las na estrutura de pastas. Criar um inventário dos assets com suas respectivas utilizações.
  - **Critérios de aceite:** Todas as imagens coletadas e otimizadas, pastas organizadas, inventário de assets criado, imagens com nomes descritivos
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** HTML
  - **Sugestão de recursos/técnicas:** Image optimization, File naming conventions, Asset organization
  - **Foco de treinamento:** Organização de projeto e otimização
  - **Dependências:** #004
  - **Labels:** design, frontend

### Sprint 2 - Hero Section e Layout Principal
**Objetivo:** Implementar a seção hero com background e call-to-action principal
**Duração:** 1 semana

#### Desenvolvedor #1
- [ ] **#006 - Hero Section Layout**
  - **Descrição:** Criar a seção principal (hero) com background em vídeo ou imagem, título principal, subtítulo e botão de call-to-action. Esta seção deve ocupar toda a altura da viewport e ser o ponto focal da página.
  - **Critérios de aceite:** Hero section com altura 100vh, background implementado, textos sobrepostos, botão funcional
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 10 horas
  - **Tecnologias:** HTML, CSS
  - **Sugestão de recursos/técnicas:** CSS Background, Flexbox, Viewport units (vh, vw), Text overlay
  - **Foco de treinamento:** Layout avançado e posicionamento
  - **Dependências:** #001, #003
  - **Labels:** frontend, design

#### Desenvolvedor #2
- [ ] **#007 - Responsividade do Hero**
  - **Descrição:** Adaptar a seção hero para diferentes tamanhos de tela, ajustando tipografia, espaçamentos e posicionamento dos elementos. Garantir que funcione bem em mobile, tablet e desktop.
  - **Critérios de aceite:** Hero responsivo em todos os breakpoints, textos legíveis, botão acessível em mobile
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** CSS
  - **Sugestão de recursos/técnicas:** Media Queries, Responsive Typography, Mobile-first design
  - **Foco de treinamento:** Design responsivo avançado
  - **Dependências:** #006
  - **Labels:** frontend, design

#### Desenvolvedor #3
- [ ] **#008 - Grid de Conteúdo Base**
  - **Descrição:** Criar a estrutura CSS Grid para exibir os cards de filmes/séries em layout responsivo. Esta será a base para todas as seções de conteúdo da página.
  - **Critérios de aceite:** Grid responsivo criado, cards se adaptam a diferentes telas, espaçamento consistente
  - **Dificuldade:** ⭐⭐⭐⭐
  - **Estimativa:** 12 horas
  - **Tecnologias:** CSS
  - **Sugestão de recursos/técnicas:** CSS Grid, Grid Template Areas, Responsive Grid
  - **Foco de treinamento:** CSS Grid avançado
  - **Dependências:** #003
  - **Labels:** frontend

#### Desenvolvedor #4
- [ ] **#009 - Cards de Conteúdo**
  - **Descrição:** Desenvolver os componentes de card individuais para filmes/séries, incluindo poster, hover effects e informações básicas. Cada card deve ter interação visual quando o usuário passa o mouse.
  - **Critérios de aceite:** Cards estilizados, hover effects funcionais, imagens otimizadas, layout consistente
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 10 horas
  - **Tecnologias:** HTML, CSS
  - **Sugestão de recursos/técnicas:** CSS Hover effects, Transitions, Transform
  - **Foco de treinamento:** Interações CSS e animações
  - **Dependências:** #008
  - **Labels:** frontend, design

#### Desenvolvedor #5
- [ ] **#010 - Integração e Testes**
  - **Descrição:** Integrar todos os componentes desenvolvidos até agora, realizar testes de compatibilidade entre browsers e dispositivos, e documentar os resultados dos testes.
  - **Critérios de aceite:** Todas as seções integradas, testes realizados em Chrome/Firefox/Safari, documentação de bugs/issues
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 6 horas
  - **Tecnologias:** HTML, CSS
  - **Sugestão de recursos/técnicas:** Cross-browser testing, Developer tools, Bug documentation
  - **Foco de treinamento:** Testing e debugging
  - **Dependências:** #006, #007, #008, #009
  - **Labels:** testing

### Sprint 3 - Seção de Planos e Carrossel
**Objetivo:** Implementar a seção de planos de assinatura e carrossel de conteúdo
**Duração:** 1 semana

#### Desenvolvedor #1
- [ ] **#011 - Seção de Planos Layout**
  - **Descrição:** Criar a seção "Escolha o melhor plano para você" com três cards de preços (Básico, Standard, Platinum). Cada card deve ter lista de benefícios, preço e botão de ação.
  - **Critérios de aceite:** Três cards de planos criados, layout em grid, informações completas, preços destacados
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 10 horas
  - **Tecnologias:** HTML, CSS
  - **Sugestão de recursos/técnicas:** CSS Grid, Card layouts, Typography hierarchy
  - **Foco de treinamento:** Layout de cards e hierarquia visual
  - **Dependências:** #008
  - **Labels:** frontend, design

#### Desenvolvedor #2
- [ ] **#012 - Estilização dos Cards de Planos**
  - **Descrição:** Aplicar estilos visuais aos cards de planos, incluindo cores, sombras, hover effects e destacar o plano recomendado. O plano do meio deve ter destaque visual especial.
  - **Critérios de aceite:** Cards estilizados, plano central destacado, hover effects, cores da marca aplicadas
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** CSS
  - **Sugestão de recursos/técnicas:** Box-shadow, CSS Gradients, Hover states, Visual hierarchy
  - **Foco de treinamento:** Design visual e efeitos CSS
  - **Dependências:** #011
  - **Labels:** frontend, design

#### Desenvolvedor #3
- [ ] **#013 - Carrossel Horizontal CSS**
  - **Descrição:** Implementar carrossel horizontal para navegação de conteúdo usando apenas CSS (sem JavaScript). Criar scroll horizontal suave com snap points.
  - **Critérios de aceite:** Carrossel funcional, scroll horizontal, snap behavior, navegação suave
  - **Dificuldade:** ⭐⭐⭐⭐⭐
  - **Estimativa:** 14 horas
  - **Tecnologias:** CSS
  - **Sugestão de recursos/técnicas:** CSS Overflow, Scroll-snap, Flexbox horizontal
  - **Foco de treinamento:** CSS avançado para interações
  - **Dependências:** #009
  - **Labels:** frontend

#### Desenvolvedor #4
- [ ] **#014 - Seção de Categorias**
  - **Descrição:** Criar a seção que exibe diferentes categorias de conteúdo (Crianças e Família, Reality, Novelas, etc.) com imagens representativas e labels.
  - **Critérios de aceite:** Grid de categorias criado, imagens e labels posicionados, hover effects aplicados
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 10 horas
  - **Tecnologias:** HTML, CSS
  - **Sugestão de recursos/técnicas:** CSS Grid, Image overlays, Text positioning
  - **Foco de treinamento:** Sobreposição de elementos e posicionamento
  - **Dependências:** #008
  - **Labels:** frontend, design

#### Desenvolvedor #5
- [ ] **#015 - Responsividade das Seções**
  - **Descrição:** Adaptar todas as seções criadas nesta sprint para serem totalmente responsivas, testando em diferentes dispositivos e orientações.
  - **Critérios de aceite:** Todas as seções responsivas, breakpoints definidos, teste em dispositivos móveis
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** CSS
  - **Sugestão de recursos/técnicas:** Media Queries, Responsive design patterns, Mobile testing
  - **Foco de treinamento:** Design responsivo completo
  - **Dependências:** #011, #012, #013, #014
  - **Labels:** frontend, testing

### Sprint 4 - FAQ e Footer
**Objetivo:** Implementar a seção de perguntas frequentes e footer institucional
**Duração:** 1 semana

#### Desenvolvedor #1
- [ ] **#016 - Estrutura FAQ Accordion**
  - **Descrição:** Criar a estrutura HTML e CSS para a seção de FAQ com efeito accordion (expand/collapse) usando apenas CSS com checkbox hack ou details/summary.
  - **Critérios de aceite:** FAQ funcional, expand/collapse suave, perguntas organizadas, acessível por teclado
  - **Dificuldade:** ⭐⭐⭐⭐
  - **Estimativa:** 12 horas
  - **Tecnologias:** HTML, CSS
  - **Sugestão de recursos/técnicas:** Details/Summary elements, CSS Transitions, Checkbox hack
  - **Foco de treinamento:** Interações CSS avançadas
  - **Dependências:** #003
  - **Labels:** frontend

#### Desenvolvedor #2
- [ ] **#017 - Estilização do FAQ**
  - **Descrição:** Aplicar estilos visuais ao FAQ, incluindo ícones de expand/collapse, tipografia adequada, espaçamentos e efeitos de transição suaves.
  - **Critérios de aceite:** FAQ estilizado, ícones funcionais, transições suaves, tipografia legível
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** CSS
  - **Sugestão de recursos/técnicas:** CSS Icons, Transitions, Typography, Pseudo-elements
  - **Foco de treinamento:** Estilização de componentes interativos
  - **Dependências:** #016
  - **Labels:** frontend, design

#### Desenvolvedor #3
- [ ] **#018 - Footer Institucional**
  - **Descrição:** Criar o footer completo com logo, links institucionais organizados em colunas, redes sociais e informações legais. O footer deve ser bem estruturado e responsivo.
  - **Critérios de aceite:** Footer completo, links organizados, logo posicionado, redes sociais incluídas
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** HTML, CSS
  - **Sugestão de recursos/técnicas:** CSS Grid, Flexbox, Link styling
  - **Foco de treinamento:** Layouts de footer e organização de conteúdo
  - **Dependências:** #003
  - **Labels:** frontend

#### Desenvolvedor #4
- [ ] **#019 - Seção "Estreias"**
  - **Descrição:** Implementar a seção que destaca os novos lançamentos com layout especial, usando cards maiores e posicionamento estratégico para dar destaque ao conteúdo.
  - **Critérios de aceite:** Seção de estreias criada, cards destacados, layout diferenciado, imagens otimizadas
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 10 horas
  - **Tecnologias:** HTML, CSS
  - **Sugestão de recursos/técnicas:** CSS Grid, Card variations, Image optimization
  - **Foco de treinamento:** Variações de layout e destaque visual
  - **Dependências:** #009
  - **Labels:** frontend, design

#### Desenvolvedor #5
- [ ] **#020 - Navegação e Links**
  - **Descrição:** Implementar toda a navegação interna da página, criar smooth scroll entre seções, configurar todos os links e testar a navegabilidade completa.
  - **Critérios de aceite:** Navegação funcional, smooth scroll implementado, todos os links testados, navegação acessível
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 6 horas
  - **Tecnologias:** HTML, CSS
  - **Sugestão de recursos/técnicas:** CSS Smooth scroll, Anchor links, Keyboard navigation
  - **Foco de treinamento:** Navegação e acessibilidade
  - **Dependências:** #002, #018
  - **Labels:** frontend, testing

### Sprint 5 - Acessibilidade e Polimento Final
**Objetivo:** Implementar acessibilidade, otimizações e realizar testes finais
**Duração:** 1 semana

#### Desenvolvedor #1
- [ ] **#021 - Acessibilidade WCAG**
  - **Descrição:** Implementar recursos de acessibilidade seguindo padrões WCAG AA: alt texts, roles ARIA, navegação por teclado, contraste de cores e suporte a screen readers.
  - **Critérios de aceite:** Alt texts completos, navegação por teclado funcional, contraste adequado, roles ARIA implementados
  - **Dificuldade:** ⭐⭐⭐⭐
  - **Estimativa:** 12 horas
  - **Tecnologias:** HTML, CSS
  - **Sugestão de recursos/técnicas:** ARIA attributes, Semantic HTML, Color contrast, Keyboard navigation
  - **Foco de treinamento:** Acessibilidade web
  - **Dependências:** Todas as seções principais
  - **Labels:** frontend, testing

#### Desenvolvedor #2
- [ ] **#022 - Otimização e Performance**
  - **Descrição:** Otimizar CSS (minificação, organização), otimizar imagens, implementar lazy loading para imagens e melhorar a performance geral da página.
  - **Critérios de aceite:** CSS otimizado, imagens comprimidas, lazy loading implementado, page speed melhorado
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 10 horas
  - **Tecnologias:** CSS, HTML
  - **Sugestão de recursos/técnicas:** CSS optimization, Image compression, Lazy loading, Performance testing
  - **Foco de treinamento:** Otimização web
  - **Dependências:** Todas as seções
  - **Labels:** frontend

#### Desenvolvedor #3
- [ ] **#023 - Testes Cross-browser**
  - **Descrição:** Realizar testes extensivos em diferentes navegadores (Chrome, Firefox, Safari, Edge) e dispositivos, documentar incompatibilidades e criar fixes necessários.
  - **Critérios de aceite:** Testes realizados em 4+ browsers, issues documentados, fixes implementados, relatório de compatibilidade
  - **Dificuldade:** ⭐⭐⭐
  - **Estimativa:** 10 horas
  - **Tecnologias:** CSS, HTML
  - **Sugestão de recursos/técnicas:** Browser testing, Developer tools, Cross-browser CSS
  - **Foco de treinamento:** Testing e debugging
  - **Dependências:** Projeto quase completo
  - **Labels:** testing

#### Desenvolvedor #4
- [ ] **#024 - Documentação Final**
  - **Descrição:** Criar documentação completa do projeto incluindo README detalhado, comentários no código, guia de instalação, estrutura do projeto e tutorial de manutenção.
  - **Critérios de aceite:** README completo, código comentado, guia de instalação, documentação de estrutura
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 8 horas
  - **Tecnologias:** Markdown
  - **Sugestão de recursos/técnicas:** Documentation writing, Markdown, Code comments
  - **Foco de treinamento:** Documentação técnica
  - **Dependências:** Projeto completo
  - **Labels:** documentação

#### Desenvolvedor #5
- [ ] **#025 - Deploy e Entrega**
  - **Descrição:** Preparar o projeto para deploy, criar versão de produção, realizar deploy (GitHub Pages ou similar), criar demo video/screenshots e preparar apresentação final.
  - **Critérios de aceite:** Projeto deployado, demo funcionando, screenshots/video criados, link de acesso disponível
  - **Dificuldade:** ⭐⭐
  - **Estimativa:** 6 horas
  - **Tecnologias:** Git, GitHub Pages
  - **Sugestão de recursos/técnicas:** GitHub Pages, Static site deployment, Demo creation
  - **Foco de treinamento:** Deploy e apresentação
  - **Dependências:** Projeto completo
  - **Labels:** frontend, documentação

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
3. Criar um novo repositório para o projeto

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
git checkout -b feature/nome-da-funcionalidade

# 3. Trabalhe normalmente, fazendo commits pequenos e frequentes
git add .
git commit -m "Adicionar header responsivo"

# 4. Quando terminar, envie sua branch
git push origin feature/nome-da-funcionalidade

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
- Seja específico: "Corrige responsividade do menu mobile"
- Evite mensagens vagas: "Update", "Fix", "Changes"

#### Estrutura de Branches:
- `main`: Código principal e estável
- `feature/nome-funcionalidade`: Novas funcionalidades
- `fix/nome-problema`: Correções de bugs
- `docs/nome-documentacao`: Atualizações de documentação

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

**Alternativa:** Notion - Para times que preferem interface mais visual e documetação integrada.

### Estratégia de Versionamento e Colaboração

- **Branches obrigatórias** para cada funcionalidade
- **Pull Requests** para todas as mudanças na main
- **Code Review** obrigatório entre pares (mínimo 1 aprovação)
- **Deploy** apenas da branch `main`
- **Commits semânticos** seguindo padrão estabelecido

### Estratégia de Testes

- **Testes manuais por checklist** após cada task
- **Revisão de layout** comparando lado a lado com referência
- **Teste funcional** de cada componente em diferentes dispositivos
- **Teste entre pares**: um colega revisa o trabalho do outro
- **Cross-browser testing** nas últimas sprints

### Principais Riscos e Pontos de Atenção

- **Limitações de prazo**: Manter escopo enxuto, evitar funcionalidades extras
- **Gargalos técnicos**: Documentar dúvidas e buscar ajuda quando necessário
- **Conflitos de merge**: Comunicar sempre quando trabalhar no mesmo arquivo
- **Integração**: Testes constantes de integração entre componentes
- **Qualidade**: Manter foco na fidelidade visual sem comprometer cronograma

### Checkpoints Intermediários

- **Daily stand-ups**: 15min diários (async via chat se necessário)
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
| 1 | Semana 1 | Estrutura base e header | HTML base, header responsivo, setup Git |
| 2 | Semana 2 | Hero section e grid | Hero completo, grid de conteúdo, cards básicos |
| 3 | Semana 3 | Planos e carrossel | Seção de planos, carrossel CSS, categorias |
| 4 | Semana 4 | FAQ e footer | FAQ accordion, footer, seção estreias |
| 5 | Semana 5 | Polimento final | Acessibilidade, testes, deploy, documentação |

**Data de entrega:** 17/06/2025
**Total de horas por pessoa:** 50 horas (10h/semana x 5 semanas)
**Total de horas da equipe:** 250 horas

## 8. Observações UX/UI Detalhadas

### Design System HBO Max

**Cores principais:**
- Roxo HBO: #7B2CBF
- Azul escuro: #1A1A2E
- Preto: #000000
- Branco: #FFFFFF
- Cinza: #8E8E93

**Tipografia:**
- Font principal: "HBO Sans" ou "Arial", sans-serif
- Títulos: Bold, tamanhos variados (24px-48px)
- Corpo: Regular, 16px-18px
- Botões: Semi-bold, 14px-16px

**Espaçamentos:**
- Container max-width: 1200px
- Padding lateral: 20px (mobile), 40px (desktop)
- Grid gap: 16px (mobile), 24px (desktop)
- Section spacing: 60px (mobile), 100px (desktop)

**Breakpoints:**
- Mobile: 320px - 768px
- Tablet: 768px - 1024px
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

**Sprint Review (1h - Toda Sexta)**
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
Breve descrição do que foi implementado

## Tasks relacionadas
- Resolve #001

## Screenshots
[Adicionar screenshots antes/depois]

## Checklist
- [ ] Código testado em Chrome e Firefox
- [ ] Responsivo em mobile e desktop
- [ ] Sem erros no console
- [ ] Código comentado quando necessário
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

## 11. Sprint 0 - Preparação e Onboarding (Opcional)

### Objetivos da Sprint 0:
- [ ] Todos os desenvolvedores têm Git instalado e configurado
- [ ] Todos têm contas no GitHub e acesso ao repositório
- [ ] Todos conseguem fazer clone, commit, push e pull
- [ ] Todos sabem usar branches e Pull Requests
- [ ] Estrutura inicial do projeto criada
- [ ] Documentação básica (README) no lugar

### Tasks típicas da Sprint 0:
- Setup do ambiente de desenvolvimento
- Tutorial prático de Git/GitHub
- Criação da estrutura de pastas do projeto
- Configuração de ferramentas (linters, formatadores)
- Primeira contribuição de cada desenvolvedor (ex: adicionar nome no README)

## 12. Informações do Projeto

### Dados Gerais
- **Página de referência:** HBO Max Landing Page (conforme imagem fornecida)
- **Nível técnico da equipe:** Iniciante
- **Tamanho da equipe:** 5 desenvolvedores
- **Disponibilidade:** 10 horas/semana por pessoa
- **Stack tecnológica:** HTML + CSS
- **Prazo desejado:** 17/06/2025
- **Observações UX/UI:** Site responsivo para mobile e desktop, dark mode opcional, acessibilidade mínima AA, seguir o layout o mais fiel possível

### Entregáveis Principais
1. **Análise Inicial:** ✅ Completa
2. **Planejamento de Sprints:** ✅ Completo com 25 tasks distribuídas
3. **Tutorial Git/GitHub:** ✅ Completo e didático
4. **Recomendações Finais:** ✅ Estratégias e ferramentas definidas

## 13. Restrições e Diretrizes

- **Não** utilizar tecnologias, bibliotecas ou dependências externas fora da stack definida
- **Não** adicionar etapas desnecessárias ou tarefas que fujam do escopo da referência
- **Sempre** considerar o real nível técnico da equipe ao propor tasks e estimativas
- **Priorizar** entregas funcionais e incrementais a cada sprint
- **Manter** tasks com escopos bem definidos, objetivos claros e mensuráveis
- **Padronizar** o código usando convenções definidas
- **Documentar** cada decisão técnica e eventuais dúvidas/enfrentamentos durante o processo
- **Fomentar** a comunicação, revisão entre pares e dúvidas constantes
- **Usar Git/GitHub** obrigatoriamente para todo o versionamento e colaboração

## 14. Padronização de Código e Dependências

### Padrão mínimo de código:
- Seguir convenções de nomeação de arquivos, funções e variáveis
- Usar identação consistente (2 espaços)
- Comentários curtos sempre que houver lógica não trivial
- Estrutura de CSS organizada por seções

### Bibliotecas permitidas:
- Apenas HTML5 e CSS3 puros
- Fontes do Google Fonts (se necessário)
- Qualquer exceção deve ser previamente aprovada

### Padrão Git:
- Branches nomeadas seguindo: `feature/`, `fix/`, `docs/`
- Commits em português, tempo presente
- Pull Requests obrigatórios para merge na main

---

**Próximos Passos:**
1. Revisar este planejamento com toda a equipe
2. Configurar o repositório GitHub
3. Distribuir as tasks da Sprint 1
4. Estabelecer rituais de comunicação
5. Iniciar o desenvolvimento!

**Contato do PO:** juliomoreirx
**Data de criação:** 05/06/2025
**Última atualização:** 05/06/2025

Estou disponível para esclarecimentos e ajustes no planejamento. Vamos criar um clone incrível da HBO Max! 🚀
