# RegEx Elite 2026 — Linguagens Regulares & Expressões Regulares

> **Trabalho Prático — Linguagens Formais | CEULP/ULBRA**  
> Baseado no material do **Prof. Jackson Gomes de Souza** (4 de novembro de 2021)

---

## 👥 Integrantes do Grupo

| # | Nome |
|---|------|
| 1 | Igor Gabriel Silva |
| 2 | Jonas Gabriel Amorim |
| 3 | Lucas Leal Ferreira|
| 4 | Samuel Matsukami |

---

## 🎯 Objetivo do Projeto

Criar um **Web App (SPA) interativo e didático** que demonstre visualmente os conceitos de:

- **Linguagens Regulares** — definição, hierarquia e relação com autômatos finitos
- **Conjuntos Regulares** — definição recursiva, casos base e operações
- **Expressões Regulares** — notação, precedência dos operadores, exemplos do material
- **Inversão/Reverso de Cadeias** — operação wᴿ com animação interativa

O projeto usa a **inversão de cadeias** como fio condutor didático: após testar uma expressão regular, o sistema mostra a cadeia original e sua invertida, reforçando o conceito de reverso de linguagem.

---

## 📖 Proposta da Atividade

> *"Usando inversão, faça um frontend que mostre toda a conceituação de expressões regulares, conjuntos regulares e linguagens regulares, além de demonstrar o funcionamento de expressões regulares."*

O frontend resolve a proposta ao:

1. Apresentar todos os conceitos com linguagem simples e visual moderno
2. Incluir um **Simulador de ERs** com exemplos diretos do material do Jackson
3. Incluir um **Lab de Inversão** com animação de flip e análise simbólica
4. Mostrar a cadeia invertida em **todos os resultados** do simulador

---

## 🚀 Como Abrir/Executar o Projeto

O projeto é um **único arquivo HTML** — sem dependências externas, sem backend, sem build.

```bash
# Opção 1: Abrir diretamente no navegador
# Clique duas vezes em index.html ou arraste para o Chrome/Firefox

# Opção 2: Servir localmente (recomendado para evitar CORS)
npx serve .
# ou
python3 -m http.server 8080
# Acesse: http://localhost:8080
```

> ✅ Compatível com Chrome, Firefox, Edge, Safari (navegadores modernos)  
> ✅ Sem bibliotecas externas (apenas Google Fonts via CDN para tipografia)  
> ✅ 100% funcional offline se as fontes já estiverem em cache

---

## 📚 Conceitos Abordados

### Baseados diretamente no material do Prof. Jackson (slides 1–20):

| Conceito | Slide(s) | Implementação |
|----------|----------|---------------|
| Definição central: ER e CR como notações de LR | 4 | Hero / Seção 1 |
| Hierarquia Símbolo → Alfabeto → Cadeia → Linguagem | — | Cadeia visual |
| ε (cadeia vazia), Σ*, Σ⁺ | — | Seção 2 |
| D*, D⁺ e DD* — diferença | 7 | Cards explicativos |
| Conjuntos regulares — definição recursiva | 6 | Seção 3 |
| Casos base: ∅, {ε}, {σ} | 6 | Cards base |
| Operações: ∪, ·, *, () | 6 | Cards de operações |
| Naturais: N = DD* | 7 | Exemplo + card |
| Reais: R = DD*.D* ∪ D*.DD* | 8 | Exemplo + card |
| Expressões Regulares — definição recursiva | 10 | Seção 4 |
| Precedência: * > concat > \| | 11 | Tabela visual |
| Exemplos: (ab\|c*), a(b\|c)*, (ab\|c)* | 12 | Cards |
| Exemplo: Σ={a,b,c,d}, padrões variados | 13 | Simulador |
| Exemplo: 1*01* | 14 | Preset |
| Exemplo: (c+d)*(cc)(c+d)* | 15 | Preset |
| L(r) = GERA(r) — ER como gerador | 17 | Texto didático |
| 14 Identidades de Kleene | 19 | Grid interativo |

---

## 🛠️ Exemplos Implementados no Simulador

| Expressão | Descrição | Slide |
|-----------|-----------|-------|
| `DD*` | Números naturais decimais | 7 |
| `DD*.D* + D*.DD*` | Números reais decimais sem sinal | 8 |
| `a(b+c)*` | Cadeias sobre {a,b,c} que começam com 'a' | 12 |
| `(ab+c)*` | Blocos de 'ab' ou 'c', zero ou mais | 12 |
| `(a+b+c)+` | Cadeias sobre {a,b,c} com ≥1 símbolo | 13 |
| `1*01*` | Binárias com exatamente um 0 | 14 |
| `(c+d)*(cc)(c+d)*` | Cadeias em {c,d} com 'cc' como subpalavra | 15 |
| `(4+5)DD` | Códigos HTTP de erro (4xx ou 5xx) | Extra |

> **Notação Jackson:** No simulador, use `+` para **união** (equivale a `|` no JS) e `D` para qualquer dígito. O compilador traduz automaticamente.

---

## 🔄 Como Usar o Simulador de Expressões Regulares

1. Acesse a **Seção 7 — Simulador** na navegação
2. Escolha um **exemplo pré-definido** na lista lateral (baseados nos slides do Jackson)
3. Ou escreva sua própria **ER** no campo de entrada (use `+` para união, `D` para dígito)
4. Digite uma **cadeia de teste** no segundo campo
5. Clique em **▶ Testar Cadeia** ou pressione qualquer tecla (resultado em tempo real)
6. O resultado mostra:
   - ✅ Badge verde **ACEITA** ou ❌ Badge vermelho **REJEITADA**
   - Explicação do motivo com regras de precedência aplicadas
   - **wᴿ** — a cadeia invertida

---

## ↩️ Como Funciona a Inversão/Reverso de Cadeias

A **Seção 6** é dedicada ao conceito de inversão:

1. Digite qualquer cadeia no campo **w**
2. Os símbolos aparecem **separados visualmente** em chips coloridos
3. Clique em **↩ Inverter Cadeia** (ou pressione Enter)
4. O sistema exibe:
   - A **cadeia original** w
   - A **cadeia invertida** wᴿ com animação de flip 3D
   - O **comprimento** da cadeia
   - Se a cadeia é **palíndromo** (w = wᴿ)
   - Explicação simbólica: w[1], w[2], ..., w[n] → wᴿ

> **Conceito:** Se w = "abc", então wᴿ = "cba". O reverso de uma linguagem regular também é regular.

---

## 📐 Arquitetura do Frontend

```
index.html
├── CSS (embutido)
│   ├── Design System (variáveis CSS)
│   ├── Animated Mesh Gradient Background
│   ├── Glassmorphism Components
│   ├── Stagger Animations (IntersectionObserver)
│   └── Responsive Grid Layouts
├── HTML (estrutura)
│   ├── Seção 1: Hero / Tela Inicial
│   ├── Seção 2: Conceitos Básicos (ε, Σ*, Σ⁺, D)
│   ├── Seção 3: Conjuntos Regulares
│   ├── Seção 4: Expressões Regulares + Precedência
│   ├── Seção 5: Passo a Passo
│   ├── Seção 6: Lab de Inversão
│   ├── Seção 7: Simulador de ERs
│   ├── Seção 8: Cards de Exemplos
│   ├── Seção 9: 14 Identidades de Kleene
│   └── Seção 10: Tabela Comparativa ER × CR × LR
└── JavaScript (embutido)
    ├── compileRegex()   — Compilador Jackson → JS RegExp
    ├── testRegex()      — Motor de matching
    ├── runSimulator()   — Lógica do simulador + feedback visual
    ├── runInversion()   — Inversão + animação
    ├── buildExplainer() — Geração de texto explicativo
    └── IntersectionObserver — Animações de entrada
```

---

## 🗂️ Estrutura de Pastas

```
projeto-linguagens-regulares/
│
├── index.html       ← Frontend completo (HTML + CSS + JS)
├── README.md        ← Este arquivo
├── prompts.md       ← Prompts de entrada e saída
└── docs/
    └── prints/      ← (Opcional) Screenshots do projeto
```

---

## 🎨 Decisões de Design

- **Estética:** Cyber-Luxury Glassmorphism — fundo escuro profundo com gradientes animados em azul safira e violeta
- **Tipografia:** Syne (sans-serif, headings) + JetBrains Mono (código/fórmulas)
- **Feedback visual:** Input verde neon ao aceitar, vermelho vibrante ao rejeitar
- **Animações:** Stagger de entrada (IntersectionObserver), flip 3D na inversão, pop-in nos chips de símbolos
- **Sem dependências:** Apenas Google Fonts (pode ser removido para 100% offline)

---

## 📎 Referência Bibliográfica

> SOUZA, Jackson Gomes de. **Conjuntos e Expressões Regulares — Linguagens Formais**.  
> Centro Universitário Luterano de Palmas (CEULP/ULBRA), Departamento de Computação, 4 de novembro de 2021.
