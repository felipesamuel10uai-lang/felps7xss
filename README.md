# Portfólio — Editor de Vídeo (Gaming)

Site em um único arquivo (`index.html`), sem dependências externas além de fontes do Google Fonts. Abre em qualquer navegador, sem servidor.

## Como usar

1. Abra `index.html` no navegador pra ver como ficou.
2. Edite o arquivo com qualquer editor de texto (Notepad, VS Code, etc).
3. Use Ctrl+F (ou Cmd+F) pra achar rapidamente os textos abaixo e trocar.

## O que trocar

### Nome
Aparece em 3 lugares — troque `seu nome` por:
- No topo (menu)
- No título grande (hero)
- No rodapé

### Contatos
Na seção "Contato", troque:
- `seu id` → seu Discord (ex: `usuario#1234` ou `usuario.gg`)
- `seu email` → seu e-mail
- `seu twitter` → seu @ do Twitter/X

Se quiser que os cards de contato sejam clicáveis (abrir o app/link direto), troque a div `<div class="contact-card">` por um link `<a class="contact-card" href="...">`, exemplos:
```html
<a class="contact-card" href="mailto:seuemail@exemplo.com">
<a class="contact-card" href="https://twitter.com/seuusuario">
<a class="contact-card" href="https://discord.com/users/SEU_ID">
```

### Vídeos (grid 2x2)
Cada vídeo é um bloco `.video-card`. Tem 4 no total. Para cada um, troque:
- `nome do projeto` → título do vídeo
- `highlight · gameplay` (e variações) → categoria/descrição curta
- `03:12` (e variações) → duração

**Para usar um vídeo real do YouTube no lugar da miniatura:**
Troque o conteúdo de `<div class="video-thumb">...</div>` por um iframe:
```html
<iframe
  width="100%" height="100%"
  src="https://www.youtube.com/embed/ID_DO_VIDEO"
  frameborder="0" allowfullscreen
  style="position:absolute; inset:0;">
</iframe>
```
(pegue o `ID_DO_VIDEO` da URL do YouTube, a parte depois de `v=`)

**Para usar uma thumbnail (imagem) real:**
Adicione dentro de `.video-thumb`:
```html
<img src="caminho-da-imagem.jpg" style="position:absolute;inset:0;width:100%;height:100%;object-fit:cover;">
```
e coloque essa linha *antes* do `<div class="play-btn">`.

## Sobre o visual

- Paleta: preto (`#0b0b0c`) + laranja (`#ff5a1f` / `#ffb07c`), como pedido.
- Efeito de blur: só um, atrás do título (glow laranja) — de propósito, pra manter o site leve.
- Sem animações pesadas: só transições suaves de hover, nada que rode sozinho na tela.
- Detalhe de "timeline/timecode" no topo e nos cards remete a edição de vídeo sem apelar pra clichê de neon/glitch de gaming.
- Responsivo: funciona em celular (grid vira 1 coluna).

## Publicar o site

Formas simples e gratuitas de colocar no ar:
- **Netlify Drop**: arraste a pasta em https://app.netlify.com/drop
- **GitHub Pages**: suba os arquivos num repositório e ative Pages nas configurações
- **Vercel**: importe a pasta pelo painel da Vercel
