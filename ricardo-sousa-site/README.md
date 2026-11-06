# Ricardo Sousa — Wise Real Estate Oliveira do Hospital

Landing page estática (HTML, CSS e JS num único ficheiro) do consultor imobiliário Ricardo Sousa.

## Estrutura

```
index.html          página principal
404.html            página de erro (GitHub Pages usa este ficheiro automaticamente)
assets/
  ricardo.png       foto do consultor
  wise-logo-dark.png / wise-logo-white.png / wise-logo-gold.png
```

Sem build, sem dependências. A única ligação externa é a fonte Manrope via Google Fonts.

## Publicar no GitHub Pages

1. Criar o repositório e enviar estes ficheiros para a raiz (ou para `/docs`).
2. Settings → Pages → Source: "Deploy from a branch" → branch `main`, pasta `/ (root)`.
3. Para domínio próprio, adicionar um ficheiro `CNAME` com o domínio e apontar o DNS para o GitHub Pages.

## Por preencher (marcadores `{{…}}` no `index.html`)

- `{{testemunho de cliente 1..3}}` e `{{nome, localidade}}` — secção de prova social
- `{{foto do imóvel}}` — 4 cartões de imóveis (substituir o bloco `.photo` por `<img>`)
- `{{AMI}}` — licença no rodapé

## Ligar o formulário ao GoHighLevel

No `index.html`, procurar o comentário `Integração: aqui liga ao webhook do GoHighLevel` dentro do handler `submit`. Substituir o `setTimeout` por um `fetch` POST para o webhook do GHL com os campos `nome`, `telemovel`, `email`, `localidade`, `tipo` e `mensagem`, e só depois mostrar o bloco `#success`.

## Links legais

"Política de privacidade" e "Termos e condições" no rodapé apontam para wise.pt. Substituir pelos URLs definitivos quando existirem.
