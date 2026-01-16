# 🚀 Guia Completo de Deploy na Vercel

## Passo a Passo Rápido

### Método 1: Deploy Direto pelo GitHub (Recomendado)

1. **Criar Repositório no GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit - Projeto adaptado para Vercel"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
   git push -u origin main
   ```

2. **Conectar na Vercel**
   - Acesse [vercel.com](https://vercel.com)
   - Clique em "Add New Project"
   - Importe seu repositório do GitHub
   - A Vercel detectará automaticamente as configurações
   - Clique em "Deploy"

3. **Pronto!** 🎉
   - Sua aplicação estará no ar em segundos
   - URL automática: `https://seu-projeto.vercel.app`

### Método 2: Deploy via CLI

1. **Instalar Vercel CLI**
   ```bash
   npm install -g vercel
   ```

2. **Login**
   ```bash
   vercel login
   ```

3. **Deploy**
   ```bash
   vercel
   ```

4. **Deploy para Produção**
   ```bash
   vercel --prod
   ```

### Método 3: Upload Direto (Sem Git)

1. Acesse [vercel.com](https://vercel.com)
2. Clique em "Add New Project"
3. Escolha "Continue with Upload"
4. Arraste a pasta do projeto
5. Clique em "Deploy"

## 🌐 Configurar Domínio Customizado

1. Na dashboard da Vercel, vá em seu projeto
2. Clique em "Settings" > "Domains"
3. Adicione seu domínio: `ofertasdecredito.digital`
4. Configure os seguintes registros DNS:

   **Opção A: CNAME (Recomendado)**
   ```
   Type: CNAME
   Name: @
   Value: cname.vercel-dns.com
   ```

   **Opção B: A Record**
   ```
   Type: A
   Name: @
   Value: 76.76.21.21
   ```

5. Aguarde propagação DNS (até 48h, geralmente 15min)

## ⚙️ Variáveis de Ambiente (Opcional)

Se você quiser adicionar variáveis de ambiente:

1. Na Vercel, vá em "Settings" > "Environment Variables"
2. Adicione as variáveis necessárias
3. Redesploy o projeto

Exemplo de variáveis úteis:
```
VITE_SUPABASE_URL=sua-url-supabase
VITE_SUPABASE_ANON_KEY=sua-chave-anonima
FORMSEND_EMAIL=seu-email@example.com
```

## 🔄 Deploys Automáticos

Com GitHub conectado:
- Cada push na branch `main` = deploy automático em produção
- Cada pull request = preview deploy automático
- Rollback instantâneo para versões anteriores

## 📊 Monitoramento

A Vercel oferece:
- ✅ Analytics gratuito
- ✅ Logs em tempo real
- ✅ Métricas de performance
- ✅ Monitoramento de erros

Acesse em: "Analytics" e "Logs" no menu do projeto

## 🐛 Solução de Problemas

### Erro 404 nas Rotas

Se as rotas não funcionarem:
1. Verifique se o `vercel.json` está na raiz do projeto
2. Confirme que todos os arquivos `.html` existem
3. Redesploy o projeto

### Erro de Build

```bash
vercel --debug
```

### Limpar Cache

```bash
vercel --force
```

### Verificar Logs

Na dashboard da Vercel > seu projeto > "Logs"

## 📱 Testar Localmente

Para testar localmente antes do deploy:

```bash
# Instalar servidor local
npm install -g serve

# Rodar servidor
serve .

# Ou usar Python
python -m http.server 8000
```

Acesse: `http://localhost:8000`

## ✅ Checklist Pré-Deploy

- [ ] Todos os arquivos `.html` renomeados corretamente
- [ ] `vercel.json` configurado
- [ ] `package.json` presente
- [ ] Imagens e assets no local correto
- [ ] Links internos usando rotas corretas (`/cartao` em vez de `/cartao.html`)
- [ ] Scripts de tracking configurados
- [ ] Testado localmente

## 🎯 Próximos Passos

Após o deploy:

1. **Testar todas as páginas**
   - Navegue por todo o fluxo
   - Teste formulários
   - Verifique tracking

2. **Configurar domínio customizado**
   - Adicione seu domínio
   - Configure DNS
   - Ative SSL automático (gratuito)

3. **Monitorar performance**
   - Ative Vercel Analytics
   - Configure alertas
   - Monitore conversões

4. **Backups**
   - Mantenha código no GitHub
   - Configure backups regulares
   - Documente mudanças

## 📞 Suporte

- Documentação Vercel: https://vercel.com/docs
- Comunidade: https://github.com/vercel/vercel/discussions
- Status: https://www.vercel-status.com

## 🎉 Sucesso!

Seu projeto está pronto para o mundo! A Vercel oferece:
- 🚀 Deploy instantâneo
- 🌐 CDN global
- 🔒 SSL gratuito
- ⚡ Performance otimizada
- 📊 Analytics incluído
- 🆓 Plano gratuito generoso

**Boa sorte com seu projeto!** 🎊
