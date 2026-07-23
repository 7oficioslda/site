# Site 7 Ofícios LDA

Site institucional da 7 Ofícios (construção civil, remodelações, canalizações, esgotos e pladur), com formulário de orçamento pronto a funcionar no Netlify.

## Estrutura

```
index.html          -> página única do site
images/
  logo.jpg           -> logótipo
  construcao.jpg      -> foto de obra real
  casa-banho.jpg       -> foto de obra real
```

## Como publicar (GitHub + Netlify, com deploy automático)

### 1. Criar o repositório no GitHub
1. Cria conta em https://github.com (se ainda não tiveres).
2. Clica em "New repository", dá o nome `7oficios-site`, deixa como "Public", não adiciones ficheiros extra.
3. Na página do repositório vazio, usa o botão "uploading an existing file" e arrasta o `index.html` e a pasta `images` (com os 3 ficheiros lá dentro).
4. Clica em "Commit changes".

### 2. Ligar ao Netlify
1. Cria conta em https://netlify.com (podes usar login com a conta do GitHub).
2. No painel, clica em "Add new site" > "Import an existing project".
3. Escolhe "GitHub" e autoriza o acesso.
4. Seleciona o repositório `7oficios-site`.
5. Não precisas de configurar "build command" nem "publish directory" (deixa em branco ou `/`), é um site estático simples.
6. Clica em "Deploy site".

A partir daqui, o site fica publicado num link tipo `nome-aleatorio.netlify.app`. Sempre que alterares o `index.html` no GitHub, o Netlify publica a nova versão sozinho em segundos.

### 3. Ligar o domínio próprio
1. Depois de comprares o domínio (ex: `7oficioslda.pt`), vai a "Site settings" > "Domain management" no Netlify.
2. Clica em "Add custom domain" e escreve o teu domínio.
3. O Netlify mostra os registos DNS que precisas de configurar no sítio onde compraste o domínio (normalmente um registo `A` ou `CNAME`).
4. Depois de configurado, o Netlify emite automaticamente o certificado HTTPS grátis (pode demorar algumas horas a propagar).

### 4. Ver os pedidos de orçamento
Depois do primeiro deploy, os envios do formulário aparecem em "Forms" no menu do site, dentro do Netlify. Podes ativar notificações por email em "Forms" > "Settings and usage" > "Form notifications", para receberes um email sempre que alguém pedir orçamento.

## Alterar conteúdo mais tarde
Basta editar o `index.html` (texto, fotos, contactos) e fazer upload da nova versão no GitHub — o site atualiza-se sozinho.
