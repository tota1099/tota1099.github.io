# Como publicar um novo post

Todo commit na `main` publica o site sozinho em 1 a 2 minutos. Você pode escrever o post pelo navegador, no próprio GitHub, ou no seu computador.

## Opção 1: pelo GitHub (navegador)

1. Abra a pasta [`content/blog`](https://github.com/tota1099/tota1099.github.io/tree/main/content/blog).
2. Clique em **Add file → Create new file**.
3. Dê ao arquivo um nome no formato `AAAA-MM-DD-assunto.md`, por exemplo `2026-10-10-meu-novo-post.md`.
4. Cole o [modelo](#modelo) abaixo e escreva o post.
5. Clique em **Commit changes**, deixe marcado *Commit directly to the main branch* e confirme.
6. Acompanhe a aba **Actions**. Quando ficar verde ✓, o post está no ar.

> 💡 Num computador, aperte a tecla **`.`** na página do repositório para abrir o **github.dev**, um VS Code no navegador. É mais confortável para textos longos e para mexer em vários arquivos de uma vez.

## Opção 2: no computador

```bash
hugo new content blog/2026-10-10-meu-novo-post.md   # cria o arquivo com o modelo (como rascunho)
hugo server -D                                       # pré-visualização em http://localhost:1313
```

Quando o post estiver pronto, remova a linha `draft: true` do cabeçalho e faça commit e push na `main`.

## Modelo

```markdown
---
title: Título do post
slug: titulo-do-post
date: 2026-10-10T10:00:00-03:00
description: "Resumo em uma frase, até 160 caracteres. É o que aparece no Google."
categories:
  - Tecnologia
tags:
  - exemplo
images:            # opcional: imagem da prévia ao compartilhar o link
  - /media/capa.jpg
---
Primeiro parágrafo do post.

## Um subtítulo

Texto com **negrito**, *itálico*, [links](https://exemplo.com) e listas:

- item 1
- item 2

![Descrição da imagem](/media/minha-foto.jpg)
```

O post fica em `https://tota1099.github.io/AAAA/MM/DD/<slug>/`, com o ano, o mês e o dia tirados do campo `date`.

### Campos do cabeçalho

| Campo | Obrigatório | Observação |
|---|---|---|
| `title` | sim | título exibido e usado no Google |
| `slug` | sim | parte final da URL: minúsculas, sem acento, palavras separadas por `-` |
| `date` | sim | data de publicação. **Uma data no futuro não é publicada** até um deploy depois dessa data |
| `description` | recomendado | até cerca de 160 caracteres, em uma linha só |
| `categories` | sim | use uma das existentes: **Tecnologia**, **Finanças** ou **Estilo de vida** (em inglês: Technology, Finance, Lifestyle) |
| `tags` | recomendado | minúsculas, com `-` no lugar de espaço. Reaproveite tags que já existem (veja `/tags/`) |
| `images` | não | imagem da prévia em redes sociais. Sem ela, é usada a sua foto |
| `draft` | não | `true` esconde o post do site |
| `comments` | não | `false` desliga os comentários do post |

## Imagens

1. Reduza a imagem para **no máximo 1600px** de largura antes de subir. Foto de celular sem tratamento pesa de 2 a 3 MB e pode conter a **localização GPS** de onde foi tirada (EXIF). Ferramentas como [Squoosh](https://squoosh.app) resolvem as duas coisas.
2. Suba o arquivo em [`static/media/`](https://github.com/tota1099/tota1099.github.io/tree/main/static/media) pelo **Add file → Upload files**.
3. No post, use `![descrição](/media/nome-do-arquivo.jpg)`.

## Versão em inglês (opcional)

Crie um segundo arquivo com o **mesmo nome** e o sufixo `.en.md`, por exemplo `2026-10-10-meu-novo-post.en.md`. Use o mesmo modelo, mas com `title`, `slug`, `description`, categorias e tags em inglês. A URL fica `/en/AAAA/MM/DD/<slug-em-ingles>/`.

O seletor de idioma passa a ligar as duas versões, e os comentários são compartilhados entre elas. Se você não criar o `.en.md`, o post aparece só em português.

## Se algo der errado

- **Deploy vermelho em Actions:** normalmente é um erro no cabeçalho, como um `---` faltando, uma aspa não fechada ou um recuo errado nas listas. Abra o job que falhou para ver o arquivo e a linha. O site continua na versão anterior até o próximo deploy dar certo.
- **O post não aparece:** confira se não ficou `draft: true` e se o `date` não está no futuro.
- **Imagem quebrada:** o caminho é `/media/...`, começando com `/`, e diferencia maiúsculas de minúsculas.
