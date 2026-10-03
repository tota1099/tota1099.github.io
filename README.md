# Renan Porto Blog

Blog pessoal em português e inglês, publicado em **https://tota1099.github.io**.

Feito com [Hugo](https://gohugo.io/) e o tema [Hextra](https://imfing.github.io/hextra/), hospedado no GitHub Pages.

👉 **Quer publicar um post? Veja [docs/publicar-post.md](docs/publicar-post.md).**

## Rodando localmente

Requisitos: [Hugo extended](https://gohugo.io/installation/) 0.166+ e [Go](https://go.dev/dl/) (o tema é baixado como módulo Go).

```bash
hugo server            # http://localhost:1313, recarrega ao salvar
hugo server -D         # inclui rascunhos (draft: true)
hugo --gc --minify     # build de produção em public/
```

## Deploy

Todo push na `main` dispara o workflow [`.github/workflows/pages.yml`](.github/workflows/pages.yml), que faz o build e publica no GitHub Pages em 1 a 2 minutos. O andamento aparece na aba **Actions**.

Em **Settings → Pages**, o *Source* precisa estar em **GitHub Actions**.

## Estrutura

```
content/
  _index.md / _index.en.md   home (intro + posts recentes)
  about.md / about.en.md     página Sobre
  blog/                      posts (AAAA-MM-DD-assunto.md + tradução .en.md)
static/
  media/                     imagens dos posts (/media/arquivo.jpg)
  photo.jpg                  foto da home e imagem padrão de compartilhamento
  favicon*, images/logo.svg  ícones e logo "RP"
layouts/
  _shortcodes/recent-posts.html          lista de posts da home
  _partials/custom/head-end.html         hreflang, JSON-LD e verificação do Google
  _partials/components/giscus.html       comentários (pt/en compartilham a discussão)
  robots.txt
assets/css/custom.css        estilos da home
i18n/pt.yaml, i18n/en.yaml   textos do menu e rodapé
archetypes/blog.md           modelo usado por `hugo new content blog/...`
hugo.yaml                    configuração do site
```

## Idiomas

O português fica na raiz (`/`) e o inglês em `/en/`. A tradução de um post é o mesmo arquivo com o sufixo `.en.md`, e o Hugo liga as duas versões automaticamente (seletor de idioma, `hreflang`). Um post sem `.en.md` só aparece em português.

## Comentários

Os comentários usam o [giscus](https://giscus.app) e ficam salvos nas [Discussions](https://github.com/tota1099/tota1099.github.io/discussions) do repositório, na categoria *Announcements*. Para moderar ou apagar um comentário, abra a discussão no GitHub. Para desligar os comentários de uma página, coloque `comments: false` no cabeçalho dela.

## SEO

- Sitemap: `/sitemap.xml`, com um sitemap por idioma.
- Propriedade no Google Search Console do tipo *Prefixo do URL*, verificada pela meta tag em `params.googleSiteVerification` no `hugo.yaml`. Não remova essa configuração.
- Cada post tem descrição, Open Graph, `hreflang` e JSON-LD (`BlogPosting`).
