# SocialPRO - TODO List

## Phase 1: Database Schema
- [x] Migrar tabelas Drizzle ORM (instagram_accounts, user_plans, payments, instagram_metrics)
- [x] Executar migrações SQL no banco de dados
- [x] Validar schema e tipos TypeScript

## Phase 2: Backend - tRPC Routers
- [x] Criar roteador Instagram (OAuth, listagem, desconexão)
- [x] Criar roteador Pagamentos (MisticPay PIX, consulta de plano)
- [x] Criar roteador Métricas (sincronização, recuperação de dados)
- [x] Adicionar procedures ao server/routers.ts

## Phase 3: Frontend - Pages
- [x] Criar Dashboard com KPIs (5 abas: Dashboard, Insights, Engajamento, Conectar Contas, Configurações)
- [x] Criar Home page como landing page profissional
- [ ] Criar página de Pricing com planos
- [ ] Criar página de Audience Analytics (opcional)
- [ ] Criar página de Content Performance (opcional)
- [ ] Criar página de Posts Management (opcional)
- [ ] Criar página de Ads Management (opcional)

## Phase 4: Frontend - Hooks
- [x] Implementar useInstagram
- [x] Implementar usePayments
- [x] Implementar useMetrics

## Phase 5: App Configuration
- [x] Configurar App.tsx com todas as rotas
- [x] Implementar ThemeProvider com dark/light mode
- [x] Aplicar tema dark com gradiente azul/roxo

## Phase 6: Backend - Webhooks
- [x] Implementar webhook handler /api/webhooks/misticpay
- [x] Registrar webhook no Express

## Phase 7: Instagram OAuth Integration
- [x] Implementar fluxo OAuth real do Instagram
- [x] Corrigir escopos OAuth (instagram_business_profile, instagram_graph_user_profile)
- [x] Implementar callback com persistência de conta
- [x] Melhorar tratamento de erros no popup
- [x] Corrigir endpoint OAuth para usar Graph API v18.0
- [x] Testar conexão de contas (app publicado no Meta)
- [x] Sincronizar dados reais do Instagram (implementado)

## Phase 8: Deployment
- [x] Publicar projeto
- [x] Fornecer link de teste ao usuário

## Current Status
- **Phase**: 7 - Instagram OAuth Integration (Correções)
- **Progress**: 70%
- **Blockers**: Nenhum (aguardando teste do usuário com credenciais corretas)

## Próximas Prioridades
1. Criar Home page como landing page profissional
2. Implementar fluxo OAuth real do Instagram na aba "Conectar Contas"
3. Criar página de Pricing com planos
4. Testar todas as funcionalidades
5. Publicar e fornecer link ao usuário

## Completed
- [x] Phase 1: Schema Drizzle ORM com todas as tabelas
- [x] Phase 2: Roteadores tRPC (Instagram, Pagamentos, Métricas)
- [x] Phase 3.1: Dashboard Premium com 5 abas funcionais
- [x] Phase 4: Hooks customizados (useInstagram, usePayments, useMetrics)
- [x] Phase 5: App.tsx com rotas e ThemeProvider dark
- [x] Phase 6: Webhook handler MisticPay PIX

## In Progress
- [ ] Phase 3.2-3.7: Páginas adicionais (Home, Pricing, Audience, Content, Posts, Ads)
- [ ] Phase 7: Implementar OAuth real do Instagram
- [ ] Phase 8: Publicar e testar


## Bugs & Fixes Pendentes
- [x] Corrigir erro de import: `instagram_accounts` vs `instagramAccounts` no schema
- [x] Implementar callback completo do Instagram OAuth (receber code/state, persistir conta)
- [x] Adicionar tratamento de sucesso/erro no popup OAuth
- [x] Criar testes automatizados para fluxo OAuth
- [x] Validar sincronização de dados reais do Instagram após conexão
- [ ] Implementar página de Pricing com planos (opcional)
- [ ] Testar fluxo completo de pagamento MisticPay PIX
- [ ] Melhorar Dashboard para mostrar contas conectadas com métricas reais
- [ ] Implementar sincronização de dados do Instagram em background


## Correções Críticas (Priority)
- [ ] Implementar modo de teste para simular contas Instagram
- [ ] Atualizar Dashboard para mostrar contas conectadas com dados simulados
- [ ] Criar botão "Adicionar Conta de Teste" para teste sem OAuth real
- [ ] Implementar listagem de contas conectadas com opção de desconectar
- [ ] Corrigir fluxo de retorno após conexão (popup deve fechar e recarregar painel)
