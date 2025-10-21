# BankSystem - Aplicação Mobile

## Descrição

Aplicação mobile nativa do Sistema Bancário BankSystem para plataformas Android e iOS, proporcionando acesso completo às funcionalidades bancárias em dispositivos móveis.

---

## Tecnologias Utilizadas

### Android
- **Java/Kotlin**: Linguagem de desenvolvimento
- **Android SDK**: Framework nativo
- **Material Design**: Design System do Google
- **Gradle**: Gerenciador de build

### iOS
- **Swift**: Linguagem de desenvolvimento
- **UIKit/SwiftUI**: Framework de interface
- **Human Interface Guidelines**: Design System da Apple
- **Xcode**: IDE oficial

### Compartilhado
- **REST API**: Comunicação com backend
- **Criptografia**: Segurança de dados
- **Padrão MVC/MVVM**: Arquitetura

---

## Pré-requisitos

### Para Android
- Android Studio Arctic Fox ou superior
- JDK 11 ou superior
- Android SDK (API 21+)
- Dispositivo físico ou emulador Android

### Para iOS
- macOS 12+ (Monterey ou superior)
- Xcode 13+ 
- CocoaPods (gerenciador de dependências)
- Dispositivo físico ou simulador iOS 13+

---

## Como Executar

### Android

#### 1. Configuração Inicial
```bash
# Clone o projeto
cd src/mobile/android

# Abra no Android Studio
# File > Open > Selecione a pasta android/
```

#### 2. Executar no Emulador
1. No Android Studio, clique em "AVD Manager"
2. Crie um novo dispositivo virtual (recomendado: Pixel 5 - API 30)
3. Clique no botão "Run" (▶️) ou pressione Shift+F10
4. Aguarde o build e instalação

#### 3. Executar no Dispositivo Físico
1. Habilite "Modo Desenvolvedor" no dispositivo Android
2. Ative "Depuração USB"
3. Conecte o dispositivo via USB
4. Selecione o dispositivo na lista e clique em "Run"

---

### iOS

#### 1. Configuração Inicial
```bash
# Clone o projeto
cd src/mobile/ios

# Instale dependências (se usar CocoaPods)
pod install

# Abra o workspace no Xcode
open BankSystem.xcworkspace
```

#### 2. Executar no Simulador
1. No Xcode, selecione um simulador (iPhone 14, por exemplo)
2. Clique no botão "Run" (▶️) ou pressione Cmd+R
3. Aguarde o build e abertura do simulador

#### 3. Executar no Dispositivo Físico
1. Conecte o iPhone via cabo
2. Selecione o dispositivo na lista de destinos
3. Configure o "Signing & Capabilities" com sua Apple ID
4. Clique em "Run"

---

## Login (Ambiente de Testes)

Para acessar o sistema em modo de demonstração:

- **Usuário:** `teste`
- **Senha:** `1234`

Toque no botão **"Login de Teste"** para preenchimento automático.

---

## 📂 Estrutura de Arquivos

```
mobile/
│
├── android/
│   ├── app/
│   │   ├── src/
│   │   │   ├── main/
│   │   │   │   ├── java/
│   │   │   │   │   └── com/banksystem/
│   │   │   │   │       ├── MainActivity.java
│   │   │   │   │       ├── LoginActivity.java
│   │   │   │   │       └── DashboardActivity.java
│   │   │   │   ├── res/
│   │   │   │   │   ├── layout/          # Layouts XML
│   │   │   │   │   ├── values/          # Strings, colors
│   │   │   │   │   └── drawable/        # Imagens
│   │   │   │   └── AndroidManifest.xml
│   │   └── build.gradle
│   └── PLACEHOLDER.txt                   # Implementação planejada
│
├── ios/
│   ├── BankSystem/
│   │   ├── ViewControllers/
│   │   │   ├── ViewController.swift
│   │   │   ├── LoginViewController.swift
│   │   │   └── DashboardViewController.swift
│   │   ├── Models/
│   │   ├── Views/
│   │   ├── Assets.xcassets/
│   │   └── Info.plist
│   └── PLACEHOLDER.txt                   # Implementação planejada
│
├── shared/
│   ├── models/                          # Modelos compartilhados
│   ├── services/                        # Serviços (API, auth)
│   └── utils/                           # Utilitários
│
└── README_MOBILE.md                     # Este arquivo
```

---

## ✨ Funcionalidades Implementadas

### Tela de Login
- Autenticação de usuários
- Login para testes
- Validação de campos
- Feedback visual de erros
- Transições animadas

### Dashboard
- Visualização de saldo em tempo real
- Lista de transações recentes
- Ações rápidas (Transferir, Depositar, Sacar)
- Menu de navegação inferior
- Pull-to-refresh

### Segurança
- Criptografia de dados sensíveis
- Armazenamento seguro de credenciais
- Timeout de sessão
- Logout automático

---

## 📱 Design Responsivo

### Android
- Suporte a diferentes tamanhos de tela (phones e tablets)
- Layouts adaptativos usando ConstraintLayout
- Material Design Components

### iOS
- Suporte a diferentes tamanhos de iPhone (SE, 12, 14, 15)
- iPad otimizado (landscape e portrait)
- Dark Mode automático

---

## 🧪 Testes

### Android
```bash
# Testes unitários
./gradlew test

# Testes instrumentados
./gradlew connectedAndroidTest
```

### iOS
```bash
# Testes unitários no Xcode
Cmd+U

# Ou via terminal
xcodebuild test -workspace BankSystem.xcworkspace -scheme BankSystem
```

---

## Segurança

⚠️ **IMPORTANTE**: Esta é uma aplicação de demonstração.

- Login apenas para ambiente de testes
- Não conecta a APIs reais
- Dados armazenados apenas em memória
- Sem integração com serviços bancários reais

---

## Build e Deploy

### Android - Gerar APK
```bash
# Debug APK
./gradlew assembleDebug

# Release APK (necessita configuração de keystore)
./gradlew assembleRelease
```

### iOS - Gerar IPA
1. No Xcode: Product > Archive
2. Selecione "Distribute App"
3. Escolha método de distribuição (Ad Hoc, Enterprise, App Store)
4. Siga os passos do assistente

---

## Problemas Conhecidos

- **Android:** Requer API 21+ (Android 5.0 Lollipop)
- **iOS:** Requer iOS 13+ para suporte completo

---

## Documentação Relacionada

- [README Principal](../../README.md)
- [Documentação Completa](../../docs/README-DOCS.md)
- [DSM-2025-001](../../docs/change_requests/DSM-2025-001.md)
- [Manual do Usuário Mobile](../../docs/manuais/)

---

## Suporte

Para problemas técnicos:
1. Consulte a documentação oficial (Android/iOS)
2. Verifique os logs de erro
3. Consulte a equipe de desenvolvimento

---

**Versão:** 1.0  
**Data:** 20/10/2025  
**Plataformas:** Android 5.0+ / iOS 13+  
**Status:** Em desenvolvimento (estrutura planejada)
