# Guia de Configuração do App Meta/Instagram para SocialPRO

## Passo 1: Criar Novo App no Meta Developer

1. Acesse [Meta Developers](https://developers.facebook.com/)
2. Clique em **"Meus Apps"** > **"Criar App"**
3. Escolha **"Tipo de App"**: Selecione **"Consumidor"** ou **"Negócios"**
4. Preencha os dados:
   - **Nome do App**: `SocialPRO Analytics`
   - **Email de Contato**: seu email
   - **Finalidade do App**: Selecione **"Gerenciar e analisar contas do Instagram"**
5. Clique em **"Criar App"**

---

## Passo 2: Adicionar Produto "Instagram Graph API"

1. No dashboard do app, clique em **"+ Adicionar Produto"**
2. Procure por **"Instagram Graph API"**
3. Clique em **"Configurar"**
4. Selecione **"Instagram Business Account"** (para contas de negócio) ou **"Instagram Basic Display"** (para contas pessoais)
5. Clique em **"Próximo"**

---

## Passo 3: Configurar OAuth

### Configurações do App (Settings > Basic)

1. Vá para **"Configurações do App"** > **"Básico"**
2. Copie e guarde:
   - **App ID**: `[será fornecido automaticamente]`
   - **App Secret**: `[será fornecido automaticamente]`

### Configurar URIs de Redirecionamento

1. Vá para **"Configurações do App"** > **"Avançado"**
2. Procure por **"URIs de Redirecionamento do OAuth Válidos"**
3. Adicione a seguinte URL:
   ```
   https://socialpro-bv6xpdvz.manus.space/api/auth/instagram/callback
   ```
4. Clique em **"Salvar"**

### Configurar Login do OAuth

1. Vá para **"Produtos"** > **"Instagram Graph API"** > **"Configurações"**
2. Em **"Configurações de OAuth do Cliente"**, ative:
   - ✅ **"Login no OAuth do cliente"**
   - ✅ **"Login do OAuth na Web"**
   - ✅ **"Forçar HTTPS"**
3. Em **"URIs de Redirecionamento do OAuth Válidos"**, adicione:
   ```
   https://socialpro-bv6xpdvz.manus.space/api/auth/instagram/callback
   ```

---

## Passo 4: Adicionar Testadores (Importante!)

1. Vá para **"Funções"** > **"Testadores"**
2. Clique em **"Adicionar Testador"**
3. Adicione sua conta Instagram pessoal
4. Você receberá um convite - aceite-o na sua conta Instagram

---

## Passo 5: Configurar Permissões

1. Vá para **"Produtos"** > **"Instagram Graph API"** > **"Permissões"**
2. Certifique-se de que as seguintes permissões estão ativas:
   - ✅ `instagram_business_basic`

   Permissões adicionais como `instagram_business_manage_insights`,
   `instagram_business_manage_messages`, `instagram_business_manage_comments`
   e `instagram_business_content_publish` devem ser adicionadas em
   `INSTAGRAM_OAUTH_SCOPES` somente quando o app Meta já tiver acesso a elas.

---

## Passo 6: Publicar o App (Opcional, mas Recomendado)

1. Vá para **"Publicar"**
2. Complete todos os requisitos de revisão
3. Envie para revisão
4. Aguarde aprovação (geralmente 24-48 horas)

---

## Dados que Você Vai Receber

Após configurar tudo, você terá:

```
App ID: [seu app id]
App Secret: [seu app secret]
Redirect URI: https://socialpro-bv6xpdvz.manus.space/api/auth/instagram/callback
```

---

## Próximos Passos

1. Crie o novo app seguindo os passos acima
2. Copie o **App ID** e **App Secret**
3. Me envie esses dados
4. Vou atualizar o projeto SocialPRO com as novas credenciais
5. Teste a conexão novamente

---

## Troubleshooting

**Erro: "Invalid platform app"**
- Verifique se o App ID e App Secret estão corretos
- Verifique se a URL de redirecionamento está exatamente igual
- Verifique se sua conta Instagram está adicionada como testadora

**Erro: "Aplicação não publicada"**
- Você pode usar o app em Development Mode
- Basta adicionar sua conta como testadora
- Não precisa publicar para testar

**Erro: "Permissões insuficientes"**
- Verifique se todas as permissões estão ativadas
- Verifique se sua conta está adicionada como testadora
- Aguarde a aprovação da revisão (se enviou para revisão)

---

## Suporte

Se tiver dúvidas, consulte a [Documentação Oficial do Instagram Graph API](https://developers.facebook.com/docs/instagram-graph-api)
