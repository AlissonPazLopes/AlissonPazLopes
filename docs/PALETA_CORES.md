# 🎨 Tabela de Cores — Obsidian Violet (GitHub Profile)

Paleta oficial do perfil GitHub (`@AlissonPazLopes`) em **roxo & preto**, estruturada em *Design Tokens* para que você possa editar ou expandir suas cores no futuro em um único lugar.

---

## 1. Tokens da Paleta (Obsidian Violet)

### Base, Fundos e Bordas
| Token CSS | Hex | Amostra / Uso Principal |
| :--- | :--- | :--- |
| `--bg-void` | `#07050c` | Fundo mais profundo, sombra do mascote e contraste máximo |
| `--bg-canvas` | `#0d0a14` | Fundo principal do banner SVG e de todos os cards de estatísticas |
| `--bg-surface` | `#140f21` | Caixa de terminal interna, superfícies secundárias e badges |
| `--bg-halo` | `#1b1233` | Halo circular atrás do gato frajola e fundo da tela `>_` no peito |
| `--border-subtle` | `#2d1f47` | Bordas externas, divisória da janela OS e contorno dos cards |
| `--border-accent` | `#6d28d9` | Anel tracejado giratório, bordas de destaque e molduras |

### Tipografia e Destaques
| Token CSS | Hex | Uso Principal |
| :--- | :--- | :--- |
| `--text-primary` | `#f5f3ff` | Título principal (`olá, eu sou o Alisson!`), números de streak |
| `--text-secondary` | `#d8d0ec` | Texto de descrição nos cards, comandos no terminal e corpo |
| `--text-muted` | `#8e82a8` | Subtítulos, cabeçalho `ALISSON OS`, prompt e micro-tags |
| `--accent-primary` | `#a855f7` | Roxo elétrico principal (ícones, anel, coleira, eyebrow) |
| `--accent-bright` | `#c084fc` | Lilás brilhante (títulos dos cards, cursor, prompt `>`, fogo) |
| `--accent-soft` | `#e9d5ff` | Lavanda claro (estrelinhas cintilantes, reflexo suave) |

### Mascote Pixel-Art (Gato Frajola)
| Token CSS | Hex | Parte do Mascote |
| :--- | :--- | :--- |
| `--cat-black` | `#12101a` | Pelagem preta (orelhas, capuz, braços, corpo, rabo) |
| `--cat-outline` | `#3b2d5e` | Contorno pixelado sutil para destacar o pelo preto do fundo escuro |
| `--cat-white` | `#f8f7ff` | Pelagem branca (faixa na testa, bochechas, focinho, patinhas e ponta do rabo) |
| `--cat-white-shadow` | `#dcd4f0` | Sombreamento sutil nas patinhas e queixo branco |
| `--cat-ear-inner` | `#d8b4fe` | Interior das orelhas e focinho |

---

## 2. Bloco `:root` Pronto para SVGs

Copie/edite este bloco no início do `<style>` em [`banner-hero.svg`](../assets/banner-hero.svg) e [`footer-wave.svg`](../assets/footer-wave.svg):

```css
:root {
  --bg-void: #07050c;
  --bg-canvas: #0d0a14;
  --bg-surface: #140f21;
  --bg-halo: #1b1233;
  --border-subtle: #2d1f47;
  --border-accent: #6d28d9;
  --text-primary: #f5f3ff;
  --text-secondary: #d8d0ec;
  --text-muted: #8e82a8;
  --accent-primary: #a855f7;
  --accent-bright: #c084fc;
  --accent-soft: #e9d5ff;
  --cat-black: #12101a;
  --cat-outline: #3b2d5e;
  --cat-white: #f8f7ff;
  --cat-white-shadow: #dcd4f0;
  --cat-ear-inner: #d8b4fe;
}
```

---

## 3. Parâmetros Prontos para Cards e Badges (sem `#`)

Use estes blocos de query string nos endpoints do `README.md` para manter todos os cards sincronizados com a tabela acima:

- **GitHub Readme Stats (`api`, `top-langs`, `pin`):**
  ```text
  bg_color=0d0a14&title_color=c084fc&text_color=e2dff0&icon_color=a855f7&border_color=2d1f47&border_radius=12
  ```

- **GitHub Streak Stats (`streak-stats.demolab.com`):**
  ```text
  background=0d0a14&border=2d1f47&stroke=2d1f47&ring=a855f7&fire=c084fc&currStreakNum=f5f3ff&sideNums=f5f3ff&currStreakLabel=c084fc&sideLabels=a59bb8&dates=8b7fa3&border_radius=12
  ```

- **Badges de Contato (`img.shields.io`):**
  - Fundo do botão: `140f21`
  - Cor do bloco do ícone / destaque: `6d28d9` ou `a855f7`
  - Exemplo: `https://img.shields.io/badge/LinkedIn-140f21?style=for-the-badge&logo=linkedin&logoColor=c084fc`

---

## 4. Como Alterar sua Paleta Futuramente

1. Escolha os novos hexadecimais e atualize a tabela deste arquivo.
2. Substitua os valores dentro de `:root { ... }` no `banner-hero.svg` e no `footer-wave.svg` (atenção aos gradientes que usam `stop-color` inline ou `var(--...)` — nos SVGs deste kit, os gradientes também usam `stop-color: var(--...)` para atualizar automaticamente!).
3. Atualize os parâmetros de query string no `README.md` (fazendo um *Find & Replace* dos hexadecimais antigos pelos novos, sem `#`).
