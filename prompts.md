# prompts.md — Documentação dos Prompts Utilizados

> **Projeto:** RegEx Elite 2026 — Linguagens Regulares & Expressões Regulares  
> **Disciplina:** Linguagens Formais — CEULP/ULBRA  
> **Grupo:** Igor Gabriel Silva, Jonas Gabriel Amorim, Lucas Leal, Samuel Matsukami

---

## 1. Prompt de Entrada (Input)

O projeto foi gerado a partir da **combinação de dois prompts complementares**, mais o material de aula em PDF.

### Prompt Base (Prompt 1) — Estrutura Didática Completa

```
Crie um frontend completo em HTML, CSS e JavaScript, em um único arquivo, para demonstrar
de forma visual, interativa e didática o conteúdo de Linguagens Regulares, Conjuntos Regulares
e Expressões Regulares, usando também a ideia de inversão/reverso de cadeias.

A atividade deve seguir a seguinte proposta:
"Usando inversão, faça um frontend que mostre toda a conceituação de expressões regulares,
conjuntos regulares e linguagens regulares, além de demonstrar o funcionamento de expressões regulares."

[...seções detalhadas com conceitos, exemplos e requisitos...]

As quatro pessoas são:
1. Igor Gabriel Silva
2. Jonas Gabriel Amorim
3. Lucas Leal
4. Samuel Matsukami
```

**Características do Prompt 1:**
- Especificou todas as **seções obrigatórias** do frontend (11 seções)
- Listou todos os **conceitos de Linguagens Formais** a serem abordados
- Definiu os **exemplos obrigatórios** (DD*, DD*.D*, 1*01*, códigos HTTP, etc.)
- Exigiu entrega para **GitHub** com README.md e prompts.md
- Solicitou que o resultado fosse **sem bibliotecas externas**

### Prompt de Design (Prompt 2) — Especificações Visuais e Técnicas

```
# 🎭 PROMPT DE ENGENHARIA DE DESIGN: REGEX ELITE EXPERIENCE 2026

Objetivo: Criar um Web App (SPA) de altíssimo nível visual e técnico sobre Expressões Regulares,
baseado no material do Prof. Jackson Gomes de Souza (CEULP/ULBRA).

Contexto Teórico (Material Jackson):
- Conceito Central: Expressões Regulares como geradores de linguagens
- Hierarquia de Operadores: 1° Fechamento (*), 2° Concatenação (xy), 3° União (+ ou |)
- Exemplos Obrigatórios: Naturais (DD*), Reais (DD*.D* + D*.DD*), Subpalavra cc

Especificações UI/UX:
- Estética: "Cyber-Luxury Glassmorphism"
- Fundo com mesh gradients animados (azul safira e violeta profundo)
- Feedback visual: Match = brilho verde neon; Reject = rosa vibrante
- 13 Identidades de Kleene em grid interativo (flip/expand)

Funcionalidades de Engenharia:
1. Compilador Inteligente: + do Jackson → | do JavaScript
2. Explainer Visual: explicação de precedência aplicada
3. Knowledge Grid: identidades de Kleene expansíveis

Integrantes: Igor Gabriel Silva, Jonas Gabriel Amorim, Lucas Leal, Samuel Matsukami
```

**Características do Prompt 2:**
- Definiu a **identidade visual** com precisão (Cyber-Luxury Glassmorphism)
- Especificou o **compilador inteligente** de notação Jackson → JS
- Introduziu o **explainer de precedência**
- Citou explicitamente o material do Jackson como referência
- Pediu **comentários no código** explicando onde cada parte do material foi aplicada

### Arquivo Complementar — PDF da Aula

Além dos prompts textuais, foi fornecido o arquivo:
```
Linguagens_Formais___Conjuntos_e_Expressoes_Regulares.pdf
```
(Prof. Jackson Gomes de Souza, CEULP/ULBRA, 04/11/2021 — 20 slides)

Este arquivo foi a **fonte primária de todos os conceitos, exemplos e identidades** implementados.

---

## 2. Como o Prompt Foi Construído

### Estratégia de Construção

O prompt final foi elaborado em **três camadas complementares**:

| Camada | Fonte | Responsabilidade |
|--------|-------|-----------------|
| **Conteúdo** | Prompt 1 | O que ensinar (conceitos, seções, exemplos) |
| **Estética** | Prompt 2 | Como apresentar (design, animações, feedback) |
| **Referência** | PDF Jackson | Precisão acadêmica (slides, fórmulas, exemplos) |

### Processo de Síntese

1. **Mapeamento de requisitos:** Os dois prompts foram comparados para identificar sobreposições e complementaridades
2. **Prioridade ao material acadêmico:** O PDF do Jackson foi usado como árbitro final para todos os exemplos e fórmulas
3. **Resolução de conflitos:** O Prompt 1 pedia "sem bibliotecas externas"; o Prompt 2 usava Tailwind e Lucide. Optou-se por CSS nativo puro mantendo a estética solicitada
4. **Fusão das funcionalidades:** Compilador inteligente (Prompt 2) + inversão animada (Prompt 1) + todos os exemplos do Jackson (PDF)

### Decisões Técnicas Tomadas

| Decisão | Justificativa |
|---------|---------------|
| CSS puro (sem Tailwind) | Prompt 1 exige sem bibliotecas externas |
| Google Fonts (Syne + JetBrains Mono) | Única dependência externa, apenas tipografia |
| `+` como union na notação Jackson | Fiel ao slide 10 do PDF |
| IntersectionObserver para animações | Performance superior a listeners de scroll |
| Compilador regex como função separada | Manutenibilidade e testabilidade |
| 14 identidades (slide 19) | PDF lista 14, não 13 como o Prompt 2 indicou |

---

## 3. Prompt de Saída (Output) — Resumo do que foi Gerado

A IA gerou **3 arquivos completos**:

### `index.html` (arquivo principal)

Um único arquivo HTML/CSS/JS com:

- **10 seções navegáveis** com scroll suave e nav sticky
- **Animated Mesh Gradient Background** — gradientes orbitais animados em CSS puro
- **Glassmorphism cards** com backdrop-filter e bordas translúcidas
- **Compilador inteligente** `compileRegex()` que traduz a notação do Jackson (`+` → `|`, `D` → `[0-9]`)
- **8 presets** baseados diretamente nos slides 7, 8, 12, 13, 14 e 15 do material Jackson
- **Lab de Inversão** com animação flip 3D, separação simbólica e detecção de palíndromos
- **8 cards de exemplos** com ER, Conjunto Regular, linguagem descrita, aceitas e rejeitadas
- **14 Identidades de Kleene** em grid expansível (clique para expandir)
- **Tabela comparativa** ER × CR × LR
- **Stagger animations** via IntersectionObserver (entrada progressiva dos elementos)
- **Feedback visual** neon: verde para aceito, vermelho para rejeitado

### `README.md`

Documentação acadêmica completa contendo:
- Lista dos 4 integrantes
- Objetivo e proposta da atividade
- Tabela de conceitos → slides do Jackson → implementação
- Guia de uso do simulador
- Explicação da inversão
- Arquitetura do projeto
- Referência bibliográfica

### `prompts.md`

Este arquivo — documentação dos prompts utilizados.

---

## 4. Requisitos da Atividade e Atendimento

| Requisito | Atendido? | Onde |
|-----------|-----------|------|
| Tela inicial explicativa | ✅ | Seção 1 (Hero) |
| Conceitos básicos (ε, Σ*, Σ⁺) | ✅ | Seção 2 |
| Linguagens regulares | ✅ | Seções 1, 2 e 10 |
| Conjuntos regulares (def. recursiva) | ✅ | Seção 3 |
| Expressões regulares (operadores, precedência) | ✅ | Seção 4 |
| Tabela de operadores | ✅ | Seção 4 |
| Passo a passo de uso | ✅ | Seção 5 |
| Inversão de cadeias (interativa) | ✅ | Seção 6 |
| Simulador de ERs | ✅ | Seção 7 |
| Exemplos prontos (cards) | ✅ | Seção 8 |
| Identidades de Kleene | ✅ | Seção 9 |
| Relação ER × CR × LR | ✅ | Seção 10 |
| DD* (naturais) | ✅ | Preset + card (slide 7) |
| DD*.D* ∪ D*.DD* (reais) | ✅ | Preset + card (slide 8) |
| a(b\|c)* | ✅ | Preset + card (slide 12) |
| (ab\|c)* | ✅ | Preset + card (slide 12) |
| 1*01* | ✅ | Preset + card (slide 14) |
| (c+d)*(cc)(c+d)* | ✅ | Preset + card (slide 15) |
| (a\|b\|c)+ | ✅ | Preset (slide 13) |
| Códigos HTTP (4\|5)DD | ✅ | Preset extra |
| Compilador notação Jackson (+→\|, D→\d) | ✅ | `compileRegex()` |
| Animação de inversão | ✅ | Flip 3D CSS + JS |
| Sem bibliotecas externas | ✅ | CSS/JS nativos |
| Visual moderno e organizado | ✅ | Cyber-Luxury Design System |
| Comentários no JavaScript | ✅ | Todos os blocos comentados |
| index.html único | ✅ | Arquivo autocontido |
| README.md acadêmico | ✅ | Arquivo separado |
| prompts.md | ✅ | Este arquivo |
| Estrutura de pastas GitHub | ✅ | README + docs/ sugerido |

---

## 5. Explicação Técnica do Compilador de ER

O **compilador inteligente** `compileRegex()` é a peça técnica central do projeto.

### Problema
O Prof. Jackson usa `+` para representar **união** (como em `(c+d)*`), enquanto no JavaScript o `+` significa **um ou mais** (fecho transitivo).

### Solução Implementada

```javascript
function compileRegex(expr) {
  // 1. D → classe de dígitos JS
  let r = expr.replace(/\bD\b/g, '[0-9]');

  // 2. Ponto literal → escape (fora de [])
  r = r.replace(/\.(?![^\[]*\])/g, '\\.');

  // 3. + contextual:
  //    se seguido por letra/(  → é UNIÃO  → vira |
  //    se no fim ou antes de ) → é FECHO  → mantém +
  r = expr
    .replace(/\bD\b/g, '[0-9]')
    .replace(/\.(?![^\[]*\])/g, '\\.')
    .replace(/\+/g, (m, offset, str) => {
      const next = str[offset + 1];
      if (next && /[a-zA-Z0-9(]/.test(next)) return '|';
      return '+';
    });

  return r;
}
```

### Exemplos de Tradução

| Entrada (notação Jackson) | Saída (JS RegExp) |
|--------------------------|-------------------|
| `DD*` | `[0-9][0-9]*` |
| `DD*.D*` | `[0-9][0-9]*\.[0-9]*` |
| `(c+d)*(cc)(c+d)*` | `([cd])*([cc])([cd])*` → `(c\|d)*(cc)(c\|d)*` |
| `(4+5)DD` | `(4\|5)[0-9][0-9]` |
| `(a+b+c)+` | `(a\|b\|c)+` |

---

*Arquivo gerado com auxílio de IA generativa (Claude — Anthropic) como parte do processo de desenvolvimento do trabalho prático.*
