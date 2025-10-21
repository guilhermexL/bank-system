# 🏦 BankSystem

Sistema bancário moderno e responsivo desenvolvido para demonstração de conceitos de gestão de configuração de software e interface de usuário.

## Descrição

Este projeto apresenta uma interface web completa de um sistema bancário fictício, incluindo tela de login com autenticação para testes e um painel de usuário com funcionalidades essenciais de operações bancárias. O sistema foi desenvolvido seguindo as melhores práticas de gestão de configuração de software.

## Funcionalidades

### Tela de Login
- Autenticação de usuários
- Login para ambiente de testes
- Design moderno com gradiente
- Validação de campos
- Feedback visual de erros

### Painel do Usuário
- **Dashboard** com visão geral da conta
- **Saldo** em tempo real
- **Extrato** de movimentações recentes
- **Transferências** entre contas
- **Depósitos** 
- **Saques**
- Ações rápidas para operações frequentes

## Design e Interface

- Interface moderna e limpa
- Esquema de cores: azul e branco com gradientes
- Ícones minimalistas
- Cards com sombras e bordas arredondadas
- Animações suaves e efeitos hover
- Totalmente responsivo

## Responsividade

O sistema foi desenvolvido com abordagem **mobile-first** e é totalmente responsivo:

### Mobile (320px - 480px)
- Menu hambúrguer
- Sidebar deslizante com overlay
- Cards em coluna única
- Botões otimizados para toque (44px mínimo)
- Espaçamentos e fontes ajustados

### Tablet (481px - 768px)
- Sidebar colapsável
- Layout de 2 colunas
- Espaçamentos médios
- Sidebar visível por padrão

### Desktop (769px+)
- Sidebar fixa sempre visível
- Layout multi-colunas (2-3 colunas)
- Espaçamentos completos
- Efeitos hover aprimorados

## Tecnologias Utilizadas

- **HTML5**: Estrutura semântica
- **CSS3**: Estilização moderna com Flexbox e Grid
- **JavaScript**: Lógica de navegação e interações
- **Responsive Design**: Media queries para adaptação a diferentes dispositivos

## Estrutura do Projeto
```
PROJETO_SISTEMA_BANCO/
│
├── docs/                                   # Documentação central do projeto
│   ├── requisitos/
│   │   ├── requisitos_funcionais.md
│   │   ├── requisitos_nao_funcionais.md
│   │   └── casos_de_uso.md
│   │
│   ├── gestao_configuracao/
│   │   ├── identificacao_configuracao.md
│   │   ├── controle_baseline.md
│   │   └── plano_gestao_configuracao.md
│   │
│   ├── change_requests/                    # Solicitações de Mudança
│   │   ├── DSM-2025-001.md                 # Login e Segurança Multi-plataforma
│   │   ├── DSM-2025-002.md                 # Futuras mudanças
│   │   └── template_dsm.md
│   │
│   ├── architecture/
│   │   ├── arquitetura_sistema.md
│   │   ├── diagrama_componentes.png
│   │   └── fluxo_dados.md
│   │
│   ├── manuais/
│   │   ├── manual_usuario_web.md
│   │   ├── manual_usuario_mobile.md
│   │   ├── manual_usuario_desktop.md
│   │   └── manual_desenvolvedor.md
│   │
│   └── testes/
│       ├── plano_testes.md
│       ├── casos_teste_web.md
│       ├── casos_teste_mobile.md
│       └── casos_teste_desktop.md
│
├── src/                                    # Código-fonte por plataforma
│   │
│   ├── web/                                # Aplicação Web
│   │   ├── index.html
│   │   ├── css/
│   │   │   ├── styles.css
│   │   │   ├── login.css
│   │   │   └── dashboard.css
│   │   ├── js/
│   │   │   ├── main.js
│   │   │   ├── auth.js
│   │   │   ├── dashboard.js
│   │   │   └── crypto.js
│   │   ├── assets/
│   │   │   ├── images/
│   │   │   └── icons/
│   │   └── README_WEB.md
│   │
│   ├── mobile/                             # Aplicação Mobile
│   │   ├── android/
│   │   │   ├── MainActivity.java
│   │   │   ├── LoginActivity.java
│   │   │   ├── DashboardActivity.java
│   │   │   └── res/
│   │   │       ├── layout/
│   │   │       ├── values/
│   │   │       └── drawable/
│   │   │
│   │   ├── ios/
│   │   │   ├── ViewController.swift
│   │   │   ├── LoginViewController.swift
│   │   │   ├── DashboardViewController.swift
│   │   │   └── Assets.xcassets/
│   │   │
│   │   ├── shared/                        # Código compartilhado
│   │   │   ├── models/
│   │   │   ├── services/
│   │   │   └── utils/
│   │   │
│   │   └── README_MOBILE.md
│   │
│   ├── desktop/                           # Aplicação Desktop
│   │   ├── main.js                        # Electron main process
│   │   ├── preload.js
│   │   ├── renderer/
│   │   │   ├── index.html
│   │   │   ├── css/
│   │   │   ├── js/
│   │   │   └── assets/
│   │   ├── package.json
│   │   └── README_DESKTOP.md
│   │
│   └── shared/                            # Componentes compartilhados entre plataformas
│       ├── components/
│       │   ├── login_usuarios.txt
│       │   ├── conta_corrente.txt
│       │   ├── movimentacoes.txt
│       │   ├── extrato_bancario.txt
│       │   └── autenticacao_segura.txt
│       │
│       ├── config/
│       │   ├── configuracao.txt
│       │   ├── config.web.json
│       │   ├── config.mobile.json
│       │   └── config.desktop.json
│       │
│       └── utils/
│           ├── crypto_utils.js
│           ├── validation.js
│           └── constants.js
│
├── tests/                                 # Testes organizados por plataforma
│   ├── web/
│   │   ├── unit/
│   │   ├── integration/
│   │   └── e2e/
│   │
│   ├── mobile/
│   │   ├── unit/
│   │   ├── integration/
│   │   └── ui/
│   │
│   └── desktop/
│       ├── unit/
│       ├── integration/
│       └── e2e/
│
├── build/                                 # Builds por plataforma
│   ├── web/
│   ├── mobile/
│   │   ├── android/
│   │   └── ios/
│   └── desktop/
│       ├── windows/
│       ├── macos/
│       └── linux/
│
├── scripts/                               # Scripts de automação
│   ├── build_web.sh
│   ├── build_mobile.sh
│   ├── build_desktop.sh
│   ├── deploy_web.sh
│   └── run_tests.sh
│
├── .github/                              # CI/CD (se usar GitHub)
│   └── workflows/
│       ├── web-ci.yml
│       ├── mobile-ci.yml
│       └── desktop-ci.yml
│
├── README.md                             # README principal do projeto
├── CONTRIBUTING.md                       # Guia de contribuição
├── LICENSE                               # Licença do projeto
├── .gitignore                            # Arquivos ignorados pelo Git
└── CHANGELOG.md                          # Histórico de mudanças
```

## Como Usar

### Instalação

1. Clone o repositório ou baixe os arquivos
```bash
git clone https://github.com/seu-usuario/bank-system.git
```

2. Navegue até o diretório do projeto
```bash
cd bank-system
```

3. Abra o arquivo `index.html` em seu navegador

### Login (Ambiente de Testes)

Para acessar o sistema em modo de teste:

- **Usuário:** `teste`
- **Senha:** `1234`

Ou clique no link "Login Teste" na tela de login para preenchimento automático.

### Funcionalidades Disponíveis

1. Acesse o sistema usando as credenciais
2. Explore o dashboard com informações da conta
3. Navegue entre as seções usando o menu lateral
4. Visualize o saldo e transações recentes
5. Teste a responsividade redimensionando a janela do navegador

## Documentação

### Gestão de Configuração

O projeto segue rigorosas práticas de gestão de configuração:

#### 1. Identificação da Configuração
- Documento com itens identificados (componentes do sistema)
- Projeto versionado (v1.0)
- Todos os módulos documentados

#### 2. Controle da Configuração
- Documento de Solicitação de Mudança (DSM)
- Avaliação de impacto
- Processo de aprovação formal

### Documentos Principais

- **requisitos_do_sistema.txt**: Requisitos funcionais e não funcionais
- **manual_de_uso.txt**: Guia do usuário
- **identificacao_configuracao.txt**: Itens de configuração identificados
- **dsm_solicitacao_mudanca.txt**: Controle de mudanças

## Segurança

⚠️ **IMPORTANTE**: Este é um sistema de demonstração.

- O Login Teste é apenas para fins de teste
- Não utilize em ambiente de produção
- Não armazena dados reais
- Não implementa criptografia real
- Sem persistência de dados (usa apenas memória)

## Objetivos do Projeto

- Demonstrar interface moderna de sistema bancário
- Implementar responsividade completa
- Aplicar conceitos de gestão de configuração de software
- Criar ambiente de testes com Login
- Documentar adequadamente o projeto

## Versão

**Versão Atual:** v1.0  
**Data:** 20/10/2025  
**Tipo:** Evolutiva

## Contribuindo

Este é um projeto educacional. Sugestões e melhorias são bem-vindas.

## Contato

Para dúvidas ou sugestões sobre o projeto, entre em contato.

## Licença

Este projeto é de uso educacional e demonstrativo.

---

**Desenvolvido com foco em boas práticas de Gerência de Configuração e Mudanças .**
