# Documentação BankSystem 📚

## Índice Geral da Documentação

Este diretório contém toda a documentação técnica e gerencial do projeto BankSystem - Sistema Bancário Multi-Plataforma.

---

## Estrutura de Documentação

### 1️⃣ `/requisitos` - Especificações do Sistema
Documentos que definem o que o sistema deve fazer.

- **requisitos_funcionais.md**: Funcionalidades do sistema (login, dashboard, transações)
- **requisitos_nao_funcionais.md**: Performance, segurança, usabilidade, escalabilidade
- **casos_de_uso.md**: Cenários de uso e interações do usuário

---

### 2️⃣ `/gestao_configuracao` - Gestão de Configuração
Controle e rastreamento de mudanças no projeto.

- **identificacao_configuracao.md**: Itens de configuração identificados (v1.0)
- **controle_baseline.md**: Controle de versões e baselines do projeto
- **plano_gestao_configuracao.md**: Estratégias e processos de gestão

---

### 3️⃣ `/change_requests` - Solicitações de Mudança ⭐
Documentos de Solicitação de Mudança (DSM) organizados e numerados.

- **DSM-2025-001.md**: Implementação de Login Fake e Segurança Multi-plataforma
- **DSM-2025-002.md**: Futuras solicitações de mudança
- **template_dsm.md**: Template padrão para novos DSMs

**Status:** Aprovado ✅  
**Última Atualização:** 20/10/2025

---

### 4️⃣ `/architecture` - Arquitetura do Sistema
Visão técnica da estrutura e design do sistema.

- **arquitetura_sistema.md**: Visão geral da arquitetura (cliente-servidor, APIs)
- **diagrama_componentes.png**: Diagramas visuais de componentes
- **fluxo_dados.md**: Fluxo de dados entre módulos e plataformas

---

### 5️⃣ `/manuais` - Manuais de Usuário e Desenvolvedor
Guias práticos para usuários finais e desenvolvedores.

#### Manuais de Usuário
- **manual_usuario_web.md**: Como usar a aplicação web
- **manual_usuario_mobile.md**: Como usar a aplicação mobile (Android/iOS)
- **manual_usuario_desktop.md**: Como usar a aplicação desktop (Windows/macOS/Linux)

#### Manual de Desenvolvedor
- **manual_desenvolvedor.md**: Guia técnico para desenvolvedores
  - Configuração do ambiente
  - Padrões de código
  - Como contribuir
  - APIs e integrações

---

### 6️⃣ `/testes` - Documentação de Testes
Planejamento e execução de testes por plataforma.

- **plano_testes.md**: Estratégia geral de testes (unitários, integração, E2E)
- **casos_teste_web.md**: Casos de teste para aplicação web
- **casos_teste_mobile.md**: Casos de teste para Android e iOS
- **casos_teste_desktop.md**: Casos de teste para desktop

---

## Navegação Rápida

### Por Papel no Projeto

#### Gerentes de Projeto
- [Requisitos Funcionais](requisitos/requisitos_funcionais.md)
- [Gestão de Configuração](gestao_configuracao/plano_gestao_configuracao.md)
- [Solicitações de Mudança (DSMs)](change_requests/)

#### Desenvolvedores
- [Manual do Desenvolvedor](manuais/manual_desenvolvedor.md)
- [Arquitetura do Sistema](architecture/arquitetura_sistema.md)
- [Plano de Testes](testes/plano_testes.md)
- [README Web](../src/web/README_WEB.md)
- [README Mobile](../src/mobile/README_MOBILE.md)
- [README Desktop](../src/desktop/README_DESKTOP.md)

#### Usuários Finais
- [Manual Web](manuais/manual_usuario_web.md)
- [Manual Mobile](manuais/manual_usuario_mobile.md)
- [Manual Desktop](manuais/manual_usuario_desktop.md)

#### QA/Testadores
- [Plano de Testes](testes/plano_testes.md)
- [Casos de Teste Web](testes/casos_teste_web.md)
- [Casos de Teste Mobile](testes/casos_teste_mobile.md)
- [Casos de Teste Desktop](testes/casos_teste_desktop.md)

---

## Processo de Documentação

### Criação de Novos Documentos

1. Identifique a categoria apropriada
2. Use o template correspondente (se disponível)
3. Siga os padrões de nomenclatura:
   - Nomes em minúsculas
   - Palavras separadas por underscore (`_`)
   - Extensão `.md` (Markdown)

### Atualização de Documentos

1. Sempre atualize a data de modificação
2. Incremente o número da versão
3. Documente mudanças no histórico do arquivo
4. Revise links e referências cruzadas

---

## Processo de Mudanças (DSM)

Para solicitar mudanças no sistema:

1. **Criar DSM**: Use o template em `/change_requests/template_dsm.md`
2. **Numerar**: Seguir sequência `DSM-YYYY-XXX`
3. **Preencher**: Todas as seções obrigatórias
4. **Aprovar**: Obter aprovação dos responsáveis
5. **Implementar**: Após aprovação formal
6. **Atualizar Baseline**: Registrar mudança no controle de versão

---

## Métricas de Documentação

- **Total de Documentos:** 15+
- **Última Atualização:** 20/10/2025
- **Versão do Sistema:** 1.0
- **DSMs Ativos:** 1 (DSM-2025-001 - Aprovado)

---

## Links Úteis

### Documentação Externa
- [Markdown Guide](https://www.markdownguide.org/)
- [Electron Documentation](https://www.electronjs.org/docs)
- [Android Developer Docs](https://developer.android.com/docs)
- [iOS Developer Docs](https://developer.apple.com/documentation/)

### Recursos do Projeto
- [README Principal](../README.md)
- [Repositório GitHub](#) (adicionar link quando disponível)
- [Changelog](../CHANGELOG.md)

---

## Suporte

Para dúvidas sobre a documentação:
- Consulte o [Manual do Desenvolvedor](manuais/manual_desenvolvedor.md)
- Entre em contato com a equipe de documentação
- Abra uma issue no repositório

---

## 📌 Notas Importantes

⚠️ **Atenção:**
- Todos os documentos devem ser mantidos atualizados
- Documentação desatualizada deve ser marcada como obsoleta
- Sempre referencie a versão do sistema nos documentos
- Use linguagem clara e objetiva

✅ **Boas Práticas:**
- Documente enquanto desenvolve
- Use exemplos práticos
- Mantenha formatação consistente
- Inclua diagramas e imagens quando apropriado

---

**Versão da Documentação:** 1.0  
**Data:** 20/10/2025  
**Responsável:** Equipe BankSystem  
**Status:** Ativo e em manutenção contínua
