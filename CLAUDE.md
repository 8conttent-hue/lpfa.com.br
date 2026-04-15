# CLAUDE.md — LPFA

Site gerado pelo **SF (Site Factory)** em 15/04/2026.

## Contexto do Site

**Nome:** LPFA
**Nicho:** Esportes e Fitness
**Keywords:** Nos da instituicao Educacional IPFA decidimos criar esse Blog como um meio
**Paleta de cores:** gold | **Fonte:** outfit

Nós, da instituição Educacional IPFA, decidimos criar esse Blog como um meio de informação acessível por milhares de atletas em todo o Brasil. Vimos que a comunicação através do Blog se tornou fundamental para muitas empresas e multiplicadores de conteúdo, a muito tempo deixou de ser apenas entretenimento. Também temos como objetivo estabelecer uma relação de proximidade, onde as informações possam chegar com maior clareza e rapidez, priorizando sempre as opiniões sinceras dos fatos para o desenvolvimento de uma sociedade com mais educação, sensatez, justiça e solidariedade. Se queremos um futuro melhor no nosso país devemos plantar isso, e o tempo ideal pra fazer isso é justamente agora. A ação mais rápida a ser feita também é criarmos mídias de conteúdos agora! Apesar de tudo, de sermos conhecidos como instituição totalmente séria, muitas vezes passamos uma imagem errada. Nosso foco também será testar novos formatos de conteúdos, como vídeos animados, entretenimento em detrimento da informação e conteúdos visuais.



## Componentes visuais usados

| Seção | Variante |
|-------|----------|
| Header | Header-E |
| Hero | Hero-G |
| Features | Features-C |
| About Section | About-G |
| Posts | Posts-E |
| Footer | Footer-D |
| Página Sobre | Sobre-G |
| Página Contato | Contato-J |

## Estrutura do projeto

```
src/
  sections/        # Layout escolhido pelo SF — Header, Hero, Features, About, Posts, Footer, Sobre, Contato
  data/            # JSONs com todo o conteúdo editável
  content/blog/    # Posts em Markdown
  pages/           # Rotas Astro (index, sobre, contato, blog, privacidade, termos)
  layouts/         # BaseLayout com fonte e cores dinâmicas
  styles/          # global.css com variáveis CSS de cor
public/
  images/          # hero.jpg, about.jpg, blog/*.jpg — inseridos automaticamente via Pexels
```

## O que editar

### Textos e conteúdo
- **`src/data/home.json`** — hero (título, subtítulo, botão), features (título, items), about section (título, desc, stats), posts
- **`src/data/sobre.json`** — conteúdo completo da página Sobre (hero, texto, missão)
- **`src/data/contato.json`** — título, subtítulo, email, tempo de resposta
- **`src/data/siteConfig.json`** — nome, slug, email, redes sociais, menu

### Imagens
Imagens já estão em `public/images/` (via Pexels). Para substituir, mantenha os mesmos nomes de arquivo:
- `hero.jpg` — imagem de fundo do Hero
- `about.jpg` — imagem da seção About (home)
- `sobre.jpg` — imagem de fundo da página Sobre
- `blog/{slug}.jpg` — imagens dos posts

### Posts do blog
Arquivos em `src/content/blog/`. Ajuste o tom de voz, adicione dados específicos do nicho e personalize conforme a identidade do site.

### Cores
Variáveis em `src/styles/global.css`: `--color-primary`, `--color-accent`, `--color-dark`.

## Deploy

```bash
bun install
bun run build
# Faça upload da pasta dist/ para Netlify, Vercel ou hosting estático
```
