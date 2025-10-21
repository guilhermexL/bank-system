# BankSystem - Aplicação Desktop 💻

## 📋 Descrição

Aplicação desktop multiplataforma do Sistema Bancário BankSystem, desenvolvida para Windows, macOS e Linux. Oferece uma experiência rica e nativa para usuários de computadores desktop.

---

## 🔧 Tecnologias Utilizadas

- **Electron**: Framework para aplicações desktop multiplataforma
- **Node.js**: Runtime JavaScript
- **HTML5/CSS3/JavaScript**: Interface do usuário
- **IPC (Inter-Process Communication)**: Comunicação entre processos
- **Native APIs**: Acesso a funcionalidades do sistema operacional

---

## 🚀 Pré-requisitos

- **Node.js**: v16.0 ou superior
- **npm** ou **yarn**: Gerenciador de pacotes
- Sistema operacional:
  - Windows 10/11
  - macOS 10.13 (High Sierra) ou superior
  - Linux (Ubuntu 18.04+, Fedora 32+, Debian 10+)

---

## 📦 Instalação

### 1. Instalar Dependências

```bash
# Navegue até a pasta desktop
cd src/desktop

# Instale as dependências do projeto
npm install
# ou
yarn install
```

### 2. Estrutura de Pacotes

```json
{
  "dependencies": {
    "electron": "^27.0.0"
  },
  "devDependencies": {
    "electron-builder": "^24.0.0"
  }
}
```

---

## 🚀 Como Executar

### Modo Desenvolvimento

```bash
# Inicie a aplicação em modo dev
npm start
# ou
yarn start

# Com hot reload (se configurado)
npm run dev
# ou
yarn dev
```

### Build para Produção

```bash
# Build para Windows
npm run build:win

# Build para macOS
npm run build:mac

# Build para Linux
npm run build:linux

# Build para todas as plataformas
npm run build:all
```

---

## 🔐 Login Fake (Ambiente de Testes)

Para acessar o sistema em modo de demonstração:

- **Usuário:** `teste`
- **Senha:** `1234`

Clique no botão **"Login Fake"** para preenchimento automático.

---

## 📂 Estrutura de Arquivos

```
desktop/
│
├── main.js                          # Processo principal (Electron)
├── preload.js                       # Script de pré-carregamento
│
├── renderer/                        # Processo de renderização
│   ├── index.html                  # Interface principal
│   │
│   ├── css/
│   │   ├── styles.css              # Estilos globais
│   │   ├── login.css               # Tela de login
│   │   └── dashboard.css           # Dashboard
│   │
│   ├── js/
│   │   ├── main.js                 # Lógica principal
│   │   ├── auth.js                 # Autenticação
│   │   ├── dashboard.js            # Painel
│   │   └── ipc-renderer.js         # Comunicação IPC
│   │
│   └── assets/
│       ├── images/                 # Imagens
│       └── icons/                  # Ícones
│
├── build/                          # Configurações de build
│   ├── icon.png                    # Ícone da aplicação
│   ├── icon.ico                    # Ícone Windows
│   └── icon.icns                   # Ícone macOS
│
├── package.json                    # Dependências e scripts
├── electron-builder.yml            # Configuração do builder
└── README_DESKTOP.md              # Este arquivo
```

---

## ✨ Funcionalidades Implementadas

### Tela de Login
- Autenticação segura
- Login Fake para testes
- Validação de campos
- Feedback visual
- Lembrança de credenciais (opcional)

### Dashboard
- Visualização de saldo
- Transações recentes
- Ações rápidas (Transferir, Depositar, Sacar)
- Navegação lateral
- Notificações do sistema
- Atalhos de teclado

### Funcionalidades Nativas
- Janela redimensionável
- Minimizar para bandeja do sistema
- Notificações desktop
- Atalhos globais
- Menu de contexto
- Auto-update (em produção)

---

## 🖥️ Suporte Multi-Plataforma

### Windows
- Instalador `.exe` (NSIS)
- Suporte a Windows 10/11
- Integração com barra de tarefas
- Notificações do Windows

### macOS
- Pacote `.dmg`
- Assinatura de código (para distribuição)
- Suporte a M1/M2 (Apple Silicon)
- Integração com Dock
- Notificações do macOS

### Linux
- Pacotes `.AppImage`, `.deb`, `.rpm`
- Suporte a múltiplas distribuições
- Integração com gerenciadores de janelas
- Notificações do sistema

---

## ⚙️ Configuração

### electron-builder.yml

```yaml
appId: com.banksystem.app
productName: BankSystem
directories:
  output: build
  buildResources: resources
files:
  - renderer/**/*
  - main.js
  - preload.js
  - package.json
win:
  target: nsis
  icon: build/icon.ico
mac:
  target: dmg
  icon: build/icon.icns
  category: public.app-category.finance
linux:
  target:
    - AppImage
    - deb
    - rpm
  icon: build/icon.png
  category: Finance
```

---

## 🧪 Testes

```bash
# Testes unitários
npm test

# Testes de integração
npm run test:integration

# Testes E2E (Spectron)
npm run test:e2e
```

---

## 📦 Distribuição

### Gerar Instalador

```bash
# Windows
npm run dist:win
# Saída: dist/BankSystem-Setup-1.0.0.exe

# macOS
npm run dist:mac
# Saída: dist/BankSystem-1.0.0.dmg

# Linux
npm run dist:linux
# Saída: dist/BankSystem-1.0.0.AppImage
```

### Tamanho dos Instaladores (aproximado)

- Windows: ~80-100 MB
- macOS: ~90-110 MB
- Linux: ~85-105 MB

---

## 🔒 Segurança

⚠️ **IMPORTANTE**: Esta é uma aplicação de demonstração.

- Login Fake apenas para testes
- Não conecta a serviços reais
- Dados armazenados localmente (sem persistência)
- Sem comunicação com servidores externos

### Boas Práticas Implementadas

- Context Isolation ativado
- Node Integration desabilitado no renderer
- Preload script para comunicação segura
- CSP (Content Security Policy) configurado

---

## 🐛 Problemas Conhecidos

- **Windows:** Pode requerer permissões de administrador na primeira execução
- **macOS:** Aplicação não assinada pode exigir autorização manual em Preferências do Sistema
- **Linux:** Dependendo da distribuição, pode ser necessário instalar dependências adicionais

---

## 📝 Scripts Disponíveis

```json
{
  "start": "electron .",
  "dev": "electron . --watch",
  "build:win": "electron-builder --win",
  "build:mac": "electron-builder --mac",
  "build:linux": "electron-builder --linux",
  "build:all": "electron-builder -mwl",
  "test": "jest",
  "lint": "eslint ."
}
```

---

## 📄 Documentação Relacionada

- [README Principal](../../README.md)
- [Documentação Completa](../../docs/)
- [DSM-2025-001](../../docs/change_requests/DSM-2025-001.md)
- [Manual do Usuário Desktop](../../docs/manuais/manual_usuario_desktop.md)
- [Electron Documentation](https://www.electronjs.org/docs)

---

## 🆘 Troubleshooting

### Erro ao iniciar a aplicação
```bash
# Limpe o cache e reinstale
rm -rf node_modules package-lock.json
npm install
```

### Erro de permissão (Linux)
```bash
# Torne o AppImage executável
chmod +x BankSystem-1.0.0.AppImage
```

### Aplicação não abre (macOS)
```bash
# Remova a quarentena
xattr -cr /Applications/BankSystem.app
```

---

## 🔄 Atualizações

A aplicação suporta auto-update em ambiente de produção usando `electron-updater`. Em desenvolvimento, utilize:

```bash
npm run update
```

---

**Versão:** 1.0  
**Data:** 20/10/2025  
**Plataformas:** Windows 10+, macOS 10.13+, Linux (Ubuntu 18.04+)  
**Status:** Em desenvolvimento (estrutura planejada)  
**Electron:** v27.0.0
