# 🏆 Arena Limoeiro — Free Fire 4x4

Landing Page estática oficial do campeonato de Free Fire 4x4 Arena Limoeiro.

---

## ⚡ Como Rodar e Testar Localmente

Por se tratar de um site estático (HTML, CSS e JavaScript puros), não é necessário nenhum banco de dados ou backend complexo.

Você pode abrir o arquivo `index.html` diretamente no seu navegador, ou rodar um servidor local simples:

```bash
# Com Python:
python -m http.server 3000

# Ou com Node.js (npx serve):
npx serve .
```

Acesse: `http://localhost:3000`

---

## 🚀 Como Publicar no Vercel (Sem Banco de Dados)

O projeto já está configurado com `vercel.json` para rodar diretamente na **Vercel** de forma 100% gratuita.

### Método 1: Direto pelo GitHub (Recomendado)
1. Acesse [vercel.com](https://vercel.com) e faça login com sua conta do GitHub.
2. Clique em **"Add New..."** > **"Project"** (ou acesse [vercel.com/new](https://vercel.com/new)).
3. Localize o repositório **`campeonato_ff_arena_limoeiro`** e clique em **"Import"**.
4. Não precisa alterar nenhuma configuração de Build ou Framework (ele detectará como projeto estático).
5. Clique em **"Deploy"**.
6. Pronto! Em poucos segundos o seu site estará no ar com link público (ex: `campeonato-ff-arena-limoeiro.vercel.app`).
   > *Toda vez que você fizer `git push` no repositório, a Vercel atualiza o site automaticamente!*

### Método 2: Pelo Terminal (Vercel CLI)
Abra o terminal na pasta do projeto e execute:
```bash
cmd /c vercel login
cmd /c vercel --prod
```

---

## 🔘 Como Modificar os Botões e Links Privados

Todos os botões do site podem ser personalizados no arquivo `index.html`:

### 1. Botões da Seção de Inscrição (Final da Página)
Procure pela seção `<section class="cta" id="inscricao">`:
```html
<div class="btn-stack">
  <!-- Botão 1: Link de Formulário / Inscrição -->
  <a class="btn big" id="link" href="https://seu-link-aqui.com" target="_blank" rel="noopener">
    Fazer minha inscrição <span>↗</span>
  </a>

  <!-- Botão 2: Link Privado (WhatsApp, Grupo VIP, Tabela, etc.) -->
  <a class="btn big btn-orange" href="https://seu-link-privado.com" target="_blank" rel="noopener">
    Entrar no Grupo / Link Privado <span>↗</span>
  </a>

  <!-- Botão 3: Link Extra / Contorno -->
  <!--
  <a class="btn big btn-outline" href="https://outro-link.com" target="_blank" rel="noopener">
    Canal Exclusivo <span>↗</span>
  </a>
  -->
</div>
```

### 2. Estilos Disponíveis de Botões
Você pode combinar as classes abaixo em qualquer tag `<a>`:
- `class="btn"`: Botão verde limão padrão da arena.
- `class="btn btn-orange"`: Botão com destaque em cor laranja.
- `class="btn btn-outline"`: Botão transparente com borda verde.
- `class="btn btn-outline-orange"`: Botão transparente com borda laranja.
- `class="btn big"`: Botão em destaque largo com setinha (ideal para chamadas principais).
- `class="btn big btn-orange"`: Botão grande na cor laranja.
- `class="btn big btn-outline"`: Botão grande vazado/discreto.
