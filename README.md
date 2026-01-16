# Projeto Ofertas de Crédito - Mercado Livre

## 🚀 Deploy na Vercel

Este projeto está pronto para deploy na Vercel. Siga os passos abaixo:

### Deploy Automático

1. Faça login na [Vercel](https://vercel.com)
2. Clique em "Add New Project"
3. Importe o repositório do GitHub/GitLab ou faça upload do projeto
4. A Vercel detectará automaticamente as configurações
5. Clique em "Deploy"

### Deploy via CLI

```bash
# Instalar Vercel CLI
npm i -g vercel

# Fazer login
vercel login

# Deploy
vercel
```

## 📁 Estrutura do Projeto

```
/
├── index.html          # Página inicial (redireciona para /cartao)
├── cartao.html         # Página principal do cartão
├── importancia.html    # Quiz de qualificação
├── conta-digital.html  # Termos e condições
├── form.html           # Formulário de cadastro
├── redirect1.html      # Aprovação - Parte 1
├── redirect2.html      # Aprovação - Parte 2
├── personalize.html    # Personalização do cartão
├── brinde.html         # Seleção de brinde
├── obrigado.html       # Cadastro de gerente
├── endereco.html       # Endereço de entrega
├── envio.html          # Escolha de método de envio
├── taxa-de-envio.html  # Confirmação de frete
├── aprovado.html       # Página final de aprovação
├── adesao.html         # Adesão final
├── vercel.json         # Configuração Vercel
└── package.json        # Configuração NPM
```

## 🔄 Fluxo de Navegação

1. **/** → Redireciona para `/cartao`
2. **/cartao** → Página inicial de apresentação
3. **/importancia** → Quiz de qualificação (4 perguntas)
4. **/conta-digital** → Aceite de termos
5. **/form** → Formulário de dados (nome, CPF, email)
6. **/redirect1** → Aprovação e benefícios
7. **/redirect2** → Escolha de vencimento
8. **/personalize** → Personalização de cor do cartão
9. **/brinde** → Escolha de cor da garrafa térmica
10. **/obrigado** → Cadastro de WhatsApp e gerente
11. **/endereco** → Endereço de entrega
12. **/envio** → Método de envio
13. **/taxa-de-envio** → Confirmação de taxa
14. **/aprovado** → Processamento final
15. **/adesao** → Página de pagamento

## ⚙️ Funcionalidades

- ✅ Páginas HTML estáticas
- ✅ Design responsivo
- ✅ Integração com scripts de tracking (Utmify, Pixel)
- ✅ LocalStorage para persistência de dados
- ✅ Validação de formulários
- ✅ Busca de CEP automática (BrasilAPI/ViaCEP)
- ✅ Máscaras de input (CPF, telefone, CEP)
- ✅ Animações e loaders
- ✅ Integração com FormSubmit para emails

## 🌐 Domínio Customizado

Para configurar seu domínio customizado na Vercel:

1. Vá em "Settings" > "Domains"
2. Adicione seu domínio (ex: ofertasdecredito.digital)
3. Configure os DNS conforme instruções da Vercel

## 📊 Tracking

O projeto inclui integração com:
- Utmify (tracking de UTMs)
- Pixel de conversão
- FormSubmit (envio de formulários por email)

## 🔒 Segurança

- Validação de geolocalização (apenas Brasil)
- Proteção contra timezone manipulation
- Validação de formulários client-side
- HTTPS automático pela Vercel

## 📝 Notas

- O projeto usa apenas HTML, CSS e JavaScript vanilla
- Não requer build process
- Deploy instantâneo
- Totalmente compatível com Vercel
- Todas as rotas configuradas no `vercel.json`

## 🆘 Suporte

Em caso de problemas com o deploy, verifique:
1. Se todos os arquivos .html estão presentes
2. Se o vercel.json está configurado corretamente
3. Se não há erros no console do browser
4. Se as rotas estão funcionando corretamente

## 📞 Contato

Para suporte técnico ou dúvidas, consulte a documentação da Vercel:
https://vercel.com/docs
