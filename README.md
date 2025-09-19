# Formulário de Cadastro — exemplo-01

Formulário de cadastro profissional e acessível, feito com HTML semântico e CSS moderno (variáveis, grid e responsividade).

## Como usar

1) Abra o arquivo `index.html` no navegador.

2) Opcional (recomendado para desenvolvimento): use a extensão “Live Server” no VS Code e clique em “Go Live”.

> O formulário está com `action="#"` e `method="post"` aguardando integração com seu backend.

## Estrutura

```
exemplo-01/
├─ index.html                # Página principal com HTML semântico
└─ assets/
   ├─ css/
   │  └─ styles.css          # Estilos com variáveis e responsividade
   └─ img/
      └─ image.png           # Imagem do bloco visual (hero)
```

## O que foi melhorado

- HTML semântico: `<main>`, `<section>`, `<aside>`, `fieldset`/`legend`
- Acessibilidade: labels conectados, foco visível (`:focus-visible`), `prefers-reduced-motion`
- Layout: grid 2 colunas (hero + formulário) e empilhamento em telas menores
- CSS limpo: variáveis para cores/spacing/tipografia, componentes reutilizáveis

## Personalização

Altere as variáveis no `:root` de `assets/css/styles.css`:

- Cores: `--color-primary`, `--color-bg`, `--color-surface`, `--color-text`, `--color-border`
- Espaçamentos: `--space-*`
- Tipografia: `--font-family`, `--font-size-base`, `--line-height`
- Bordas e sombras: `--radius-*`, `--shadow-1`

Exemplo (tema roxo):

```css
:root {
  --color-primary: #7c3aed;
  --color-primary-600: #6d28d9;
}
```

## Integração (backend)

Sugestões para quando integrar:

- Validar dados no servidor (email, senha >= 8, data, etc.)
- Exibir mensagens de erro/sucesso e feedback por campo
- Normalizar/máscara conforme necessidade (ex.: telefone)

## Próximas melhorias

- Validações client-side leves (força da senha, mensagens inline)
- Estados visuais de erro/sucesso no CSS
- Internacionalização (i18n)
- Auditorias de acessibilidade (axe, Lighthouse)
