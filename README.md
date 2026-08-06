# 🌻 Girassol Animado

Página romântica de presente: um girassol animado em HTML/CSS puro que floresce na tela, com referência à cena **01:04:20** do filme *Shrek* (2001). Inclui sol com raios, nuvens em movimento, partículas de pólen, um jardineiro que rega a planta e um personagem do Shrek que faz balanço.

Acesse a demo: **https://rubensdj.github.io/girassol/**

---

## ✨ Funcionalidades

- **Girassol CSS puro** — 16 pétalas frontais + 16 traseiras, núcleo com sementes, caule com textura e folhas
- **Cenário vivo** — sol com raios rotativos, nuvens em movimento, partículas flutuantes, grama dinâmica
- **Personagens** — jardineiro com regador animado e Shrek que balança ao lado do girassol
- **Fluxo interativo** — após 8 segundos, pergunta se a pessoa tem Netflix:
  - **Sim** → mostra onde assistir (Netflix, tempo exato 01:04:20)
  - **Não** → oferece links de streaming + caixa de senha para ver a cena embutida
- **Cena embutida** — digite a senha `NEOQEAV` para reproduzir `shrek.mp4` em fullscreen
- **Mensagem final** — após o vídeo, exibe "NEOQEAV" com efeito glow + mensagem de amor
- **Responsivo** — adapta-se a mobile (flex-direction column, escala reduzida)
- **Acessível** — respeita `prefers-reduced-motion: reduce`
- **SEO** — Open Graph tags, favicon SVG inline, preconnect a fontes

---

## 🚀 Deploy no GitHub Pages

1. Faça fork ou clone este repositório
2. Vá em **Settings → Pages**
3. Em **Source**, selecione a branch `main` e a pasta `/root`
4. Salve — o site ficará disponível em `https://seuusuario.github.io/girassol/`

O arquivo `.nojekyll` já está incluído para evitar processamento Jekyll desnecessário.

---

## 🎨 Como personalizar

### Trocar a senha de desbloqueio

Em `index.html`, localize a linha:

```js
const SENHA_CORRETA = 'NEOQEAV';
```

Substitua `NEOQEAV` pela senha que desejar.

### Trocar o vídeo da cena

Substitua o arquivo `shrek.mp4` por outro vídeo MP4 de sua escolha (mantenha o mesmo nome ou atualize as referências em `index.html` e `video.html`).

### Trocar os links de streaming

Em `index.html`, procure por:

```html
<a class="link-netflix" href="https://www.netflix.com/title/60000733" target="_blank">
```

Substitua a URL pela sua plataforma de streaming preferida.

### Trocar a mensagem final

Procure por:

```html
<div class="amor">Nunca esqueça o quanto eu amo você <span>💗</span></div>
```

### Trocar o tempo da cena

Procure por `01:04:20` (aparece em alguns pontos) e substitua pelo tempo desejado. Também atualize o bilhete:

```html
<div class="bilhete">Shrek 01:04:20</div>
```

---

## 📁 Estrutura do projeto

```
girassol/
├── index.html       # Página principal com todo o CSS e JS embutido
├── video.html       # Player de vídeo standalone (fullscreen)
├── shrek.mp4        # Cena do filme (fallback de senha)
├── 404.html         # Redireciona páginas 404 para a home
├── .nojekyll        # Desativa processamento Jekyll no GitHub Pages
└── README.md        # Este arquivo
```

---

## 🛠️ Tecnologias

- **HTML5** — estrutura semântica
- **CSS3** — animações (`@keyframes`), `radial-gradient`, `conic-gradient`, `transform 3D`, `backdrop-filter`
- **JavaScript vanilla** — interatividade do overlay, validação de senha, gerador de grama
- **Google Fonts** — Creepster, Inter, MedievalSharp
- **Zero dependências** — Não usa frameworks, bundlers ou npm

---

## 📝 Notas

- A senha `NEOQEAV` fica visível no código-fonte (front-end puro). Para um sistema realmente seguro, seria necessário um backend. Como este é um presente romântico, a "segurança" é simbólica.
- O arquivo `shrek.mp4` (~2.3MB) é carregado apenas quando a cena é desbloqueada, não no carregamento inicial.
- Suporta `prefers-reduced-motion` — usuários que preferem menos movimento veem animação mínima.

---

## 🧑‍💻 Autor

**Rubens Pereira Fernandes** — [GitHub: @Rubensdj](https://github.com/Rubensdj)

Um presente para Hellen. 💛
