# BankSystem - Aplicação Web 🌐

## Descrição

Aplicação web responsiva do Sistema Bancário BankSystem, desenvolvida com tecnologias front-end modernas para proporcionar uma experiência de usuário fluida e profissional em navegadores.

---

## Tecnologias Utilizadas

- **HTML5**: Estrutura semântica e acessível
- **CSS3**: Estilização moderna com Flexbox e Grid
- **JavaScript (ES6+)**: Lógica de interação e navegação
- **Responsive Design**: Media queries para adaptação multi-dispositivo

---

## Como Executar

### Método 1: Abrir Diretamente
1. Navegue até a pasta `/src/web`
2. Abra o arquivo `index.html` no seu navegador preferido
3. A aplicação será carregada imediatamente

### Método 2: Servidor Local (Recomendado)
```bash
# Usando Python 3
cd src/web
python -m http.server 8000

# Usando Node.js (http-server)
cd src/web
npx http-server -p 8000

# Acesse: http://localhost:8000
```

---

## Login (Ambiente de Testes)

Para acessar o sistema em modo de demonstração:

- **Usuário:** `teste`
- **Senha:** `1234`

Ou clique no link **"Login Fake"** na tela de login para preenchimento automático.

---

## 📂 Estrutura de Arquivos

```
web/
│
├── index.html                    # Página principal
│
├── css/
│   ├── styles.css               # Estilos globais
│   ├── login.css                # Estilos da tela de login
│   └── dashboard.css            # Estilos do painel
│
├── js/
│   ├── main.js                  # Inicialização da aplicação
│   ├── auth.js                  # Lógica de autenticação
│   ├── dashboard.js             # Funcionalidades do painel
│   └── crypto.js                # Segurança e criptografia
│
├── assets/
│   ├── images/                  # Imagens do sistema
│   └── icons/                   # Ícones e logos
│
└── README_WEB.md               # Este arquivo
```

---

## Responsividade

A aplicação foi desenvolvida com abordagem **mobile-first** e suporta:

### Mobile (320px - 480px)
- Menu hambúrguer
- Sidebar deslizante com overlay
- Cards em coluna única
- Botões otimizados para toque (44px mínimo)
- Espaçamentos reduzidos

### Tablet (481px - 768px)
- Sidebar colapsável
- Layout de 2 colunas para cards
- Espaçamentos médios
- Navegação aprimorada

### Desktop (769px+)
- Sidebar fixa sempre visível
- Layout multi-colunas (2-3 colunas)
- Espaçamentos completos
- Efeitos hover em elementos interativos

---

## Funcionalidades Implementadas

### Tela de Login
- Validação de campos
- Feedback visual de erros
- Login para testes
- Design moderno com gradiente

### Dashboard
- Visualização de saldo
- Últimas 3 transações
- Ações rápidas (Transferir, Depositar, Sacar, Pagar)
- Navegação lateral
- Logout seguro

---

## Testes

Para testar a responsividade:

1. Abra o DevTools do navegador (F12)
2. Ative o modo de dispositivo (Ctrl+Shift+M)
3. Teste diferentes resoluções:
   - iPhone SE (375px)
   - iPad (768px)
   - Desktop (1920px)

---

## Segurança

⚠️ **IMPORTANTE**: Esta é uma aplicação de demonstração.

- Login Fake apenas para testes
- Não armazena dados reais
- Não utiliza APIs externas
- Sem persistência (apenas memória)

---

## Notas de Desenvolvimento

- Não requer instalação de dependências
- Compatível com navegadores modernos (Chrome, Firefox, Safari, Edge)
- JavaScript puro (sem frameworks)
- CSS3 moderno (sem pré-processadores)

---

## Problemas Conhecidos

Nenhum problema crítico identificado. Para reportar bugs, consulte a documentação principal do projeto.

---

## Documentação Relacionada

- [README Principal](../../README.md)
- [Documentação Completa](../../docs/)
- [DSM-2025-001](../../docs/change_requests/DSM-2025-001.md)

---

**Versão:** 1.0  
**Data:** 20/10/2025  
**Plataforma:** Web  
**Status:** Implementado e funcional
