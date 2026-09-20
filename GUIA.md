# Como publicar o ícone do app (passo a passo)

Isso aqui é uma "página-casca": um mini site fora do Apps Script que só mostra
sua logo por 1 segundo e manda a pessoa direto pro sistema de verdade. Como
ela fica fora do Apps Script, o celular consegue enxergar o ícone da marca
quando o aluno faz "Adicionar à tela de início" — o que dentro do Apps Script
não é possível.

É gratuito, dá pra fazer sem saber programar, e depois de pronto não precisa
mexer de novo.

## 1. Antes de tudo: pegue o link do seu sistema

É o mesmo link que você já usa hoje pra abrir o Performance & Saúde (algo do
tipo `https://script.google.com/macros/s/AKfycb.../exec`).

## 2. Edite um arquivo

Abra o arquivo **index.html** desta pasta em qualquer editor de texto simples
(no Windows pode ser o Bloco de Notas; no Mac, o TextEdit em modo texto puro).

Procure esta linha, perto do topo:

```
var URL_DO_SISTEMA = "COLE_AQUI_O_LINK_DO_SEU_SISTEMA";
```

Troque `COLE_AQUI_O_LINK_DO_SEU_SISTEMA` pelo link do passo 1, mantendo as
aspas. Fica assim, por exemplo:

```
var URL_DO_SISTEMA = "https://script.google.com/macros/s/AKfycbXXXXXXX/exec";
```

Salve o arquivo.

## 3. Crie uma conta gratuita no GitHub (se ainda não tiver)

Acesse **github.com**, clique em "Sign up" e crie uma conta grátis. Não
precisa de cartão nem nada pago.

## 4. Crie um repositório novo

- Clique no `+` no canto superior direito → **New repository**.
- Dê um nome, por exemplo `performance-saude-app`.
- Deixe marcado como **Public**.
- Clique em **Create repository**.

## 5. Suba os arquivos desta pasta

Na página do repositório recém-criado, clique em **"uploading an existing
file"** (ou "Add file" → "Upload files") e arraste estes 6 arquivos:

- `index.html`
- `manifest.json`
- `icon-192.png`
- `icon-512.png`
- `apple-touch-icon.png`
- `favicon.png`

Clique em **Commit changes** pra confirmar o envio.

## 6. Ative o GitHub Pages

- No repositório, vá em **Settings** (aba no topo).
- No menu da esquerda, clique em **Pages**.
- Em "Branch", selecione **main** (ou **master**) e pasta **/ (root)**.
- Clique em **Save**.

Espere cerca de 1 minuto. A própria página vai mostrar um link assim:

```
https://SEU-USUARIO.github.io/performance-saude-app/
```

## 7. Pronto — esse é o novo link pra mandar pros alunos

Esse link (do passo 6) é o que você vai divulgar e usar na hora de instalar
o app. Teste abrindo ele no celular: deve aparecer rapidinho a logo e depois
cair direto no sistema. Faça "Adicionar à tela de início" a partir *desse*
link — é aí que o ícone da marca vai aparecer certinho.

## Se um dia o link do Apps Script mudar

Só repetir o passo 2 (editar o `index.html` com o novo link) e subir o
arquivo atualizado no mesmo repositório (Add file → Upload files, substituindo
o antigo). O endereço do GitHub Pages continua o mesmo — os alunos não
precisam refazer nada.
