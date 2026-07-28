# Prompt para o Claude Code — Site Pessoal da Alysia

Crie um site pessoal (portfólio + blog) usando **Next.js 15+ (App Router, TypeScript)** e **Tailwind CSS**, pronto para deploy na Vercel.

## Stack técnica
- Next.js com App Router e TypeScript
- Tailwind CSS para estilização
- **Sanity.io** como CMS headless — crie dois schemas:
  1. `post`: título, slug, corpo (rich text/portable text), tags, data de publicação
  2. `siteSettings`: bio curta, links de contato, cores do tema (documento único)
- Studio do Sanity embutido na rota `/studio`, funcionando como painel visual de edição (sem precisar mexer em código para publicar posts ou ajustar configurações)
- Estrutura de pastas organizada: `app/`, `components/`, `lib/`, `sanity/`

## Paleta de cores — Rosé Pine Moon
Configure como variáveis CSS / tema no Tailwind:
- `base` (fundo): `#232136`
- `surface` (cards/seções): `#2a273f`
- `overlay` (hover/bordas): `#393552`
- `text` (texto principal): `#e0def4`
- `subtle` (texto secundário): `#908caa`
- `muted` (texto apagado): `#6e6a86`
- `iris` (accent primário — links/CTA): `#c4a7e7`
- `foam` (accent secundário — tags): `#9ccfd8`
- `gold` (destaques pontuais): `#f6c177`
- `love` (hover/alertas): `#eb6f92`
- `pine` (accent terciário): `#3e8fb0`

## Design geral
- Dark mode como padrão, com toggle para light mode (ex: `next-themes`)
- Tipografia: sans-serif limpa (Inter ou IBM Plex Sans) para títulos e corpo; fonte monoespaçada (JetBrains Mono ou Fira Code) só em detalhes pontuais (tags de tecnologia, trechos de código)
- Visual sóbrio e profissional — o site é voltado a recrutadores do setor bancário/financeiro, então evite elementos "gamer" ou brincalhões
- Cards com cantos levemente arredondados, sombra suave, bastante espaço em branco
- Favicon/logo minimalista com um pequeno ícone de coelho (traço simples, discreto) como assinatura visual — use um SVG placeholder por enquanto

## Seções do site

### Hero
- Nome: Alysia
- Frase de posicionamento: "Estudante de CC apaixonada por segurança da informação, buscando unir tecnologia e proteção de dados no setor bancário"
- Dois botões CTA: **"Ver GitHub"** (link externo) e **"Baixar currículo"** (link para PDF, placeholder por enquanto)

### Sobre
> Sou a Alysia, estudante de Ciência da Computação na Unisinos, atualmente no 3º semestre. Tenho me dedicado a cybersecurity, com estudos práticos na HTB Academy, e nutro um interesse crescente por dados — entender como sistemas coletam, processam e protegem informação é algo que me motiva bastante. Sou proativa e movida pela vontade constante de aprender: gosto de ir atrás do conhecimento antes que ele bata à porta, e trato cada novo desafio como uma oportunidade de crescer tecnicamente.

### Habilidades
Lista simples, sem categorias: `Python` `C`
(Estruture o componente para que seja fácil adicionar mais itens depois)

### Trajetória
> Venho me envolvendo ativamente com a comunidade tech ao longo da graduação: participei do Code@Night na Unisinos (dezembro de 2025), um evento de imersão no ecossistema de tecnologia com palestra da ADP Brazil Labs e foco em networking estratégico, além da palestra "A vida real de um dev: o que ninguém te conta nos tutoriais", com Jhordan Pacheco, sobre os bastidores reais da carreira em desenvolvimento de software. Atualmente sou bolsista de Iniciação Científica (CNPq) no projeto Cidadania Viva, atuando como desenvolvedora de IA. Meu trabalho envolve construir pipelines de inteligência artificial para análise bioacústica — transformando gravações de áudio coletadas via ciência cidadã em dados que ajudam a monitorar a biodiversidade urbana da Região Metropolitana de Porto Alegre. Aplico técnicas de transfer learning e colaboro com especialistas de mais de 6 áreas do conhecimento (Direito, Arquitetura, Psicologia, entre outras), documentando todo o processo técnico para garantir reprodutibilidade.

### Projetos
Não incluir seção/link no menu ainda — deixe a rota/componente pronto mas comentado, para adicionar facilmente quando houver projetos para mostrar.

### Blog
- Lista de posts vindos do Sanity, ordenados por data (mais recente primeiro)
- Linha editorial: posts sobre experiências, especializações e trajetória de estudo — no mesmo espírito do que já é publicado no LinkedIn
- Cada post: título, data, tags, corpo em rich text

### Contato
- LinkedIn: linkedin.com/in/alys-muni/
- E-mail: alysia@lunalith.dev
- GitHub: github.com/Lunalith

## Navegação
Navbar fixa com: Sobre, Habilidades, Trajetória, Blog, Contato + toggle de dark/light mode

## Extras
- Site responsivo (mobile-first)
- SEO básico (meta tags, Open Graph)
- Performance otimizada (imagens via `next/image`, fontes otimizadas)

## Boas práticas de Git
- Use **Conventional Commits** para as mensagens (`feat:`, `fix:`, `docs:`, `style:`, `refactor:`, `chore:`, `test:`), sempre no mesmo padrão
- Faça commits pequenos e atômicos — cada commit deve representar uma mudança lógica isolada (ex: `feat: adiciona componente Hero`, em vez de um único commit com o site inteiro)
- Escreva mensagens que expliquem o "porquê" da mudança quando não for óbvio, não só o "o quê"
- Configure um `.gitignore` adequado desde o commit inicial (`node_modules`, `.env*`, `.next`, `.vercel`)
- Nunca commite segredos ou chaves de API — use `.env.local` para as variáveis do Sanity e confirme que está no `.gitignore`
- Trabalhe em branches (`feature/nome-da-funcionalidade`) para cada nova funcionalidade e mantenha a `main` sempre estável e deployável
- Ao concluir cada funcionalidade, abra um Pull Request (mesmo sendo projeto solo) e faça o merge — mantém o histórico organizado e é uma boa prática visível pra quem avaliar seu GitHub

---

Ao final, inicialize um repositório git seguindo essas práticas desde o primeiro commit, e me diga os próximos passos para: **(1)** criar um projeto no Sanity.io e conectar as variáveis de ambiente, **(2)** subir o repositório no GitHub, e **(3)** fazer o deploy na Vercel.
