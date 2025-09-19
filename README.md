# Formulário de Cadastro — exemplo-01

Um formulário de cadastro simples, profissional e acessível. Implementado com HTML semântico e CSS moderno usando variáveis, layout responsivo e foco visível.

## Demo local

Abra o arquivo `index.html` diretamente no navegador.

Se preferir um servidor local (live reload recomendado):

- VS Code: use a extensão Live Server e clique em “Go Live”.
- Ou via Python (opcional):

```powershell
# Dentro da pasta do projeto
python -m http.server 5500
```

Depois, acesse http://localhost:5500/

## Estrutura do projeto

```
exemplo-01/
├─ index.html                # Página principal com HTML semântico
└─ assets/
   ├─ css/
   │  └─ styles.css          # Estilos com variáveis CSS e responsividade
   └─ img/
      └─ image.png           # Imagem usada no bloco visual (hero)
```

## Tecnologias

- HTML5 semântico (main, section, aside, fieldset/legend)
- CSS3 com variáveis (custom properties), grid layout e media queries
- Padrões de acessibilidade: labels associados, foco visível, contraste adequado

## Personalização rápida

Edite as variáveis em `assets/css/styles.css` (seção `:root`):

- Cores
  - `--color-primary`: cor principal (botões, foco)
  - `--color-bg`, `--color-surface`, `--color-text`, `--color-border`
- Espaçamentos
  - `--space-*` (4px, 8px, 12px, etc.)
- Tipografia
  - `--font-family`, `--font-size-base`, `--line-height`
- Bordas e sombras
  - `--radius-md`, `--radius-lg`, `--shadow-1`

Exemplo de alteração de tema (azul para roxo):

```css
:root {
  --color-primary: #7c3aed;     /* roxo */
  --color-primary-600: #6d28d9; /* hover */
}
```

## Acessibilidade

- Campos com label e atributos `for/id`
- Grupos de opções com `fieldset` e `legend`
- Estados de foco com `:focus-visible` e área de foco ampliada
- Suporte a `prefers-reduced-motion`

## Layout e responsividade

- Grid 2 colunas (imagem/hero + conteúdo)
- Em telas menores (< 960px), o layout empilha (imagem acima, formulário abaixo)

## Integração (backend)

O formulário (`#signup-form`) está com `action="#"` e `method="post"` prontos para integração.
Sugestões:
- Validar no servidor (email, senha mínima de 8, data, etc.)
- Implementar mensagens de sucesso/erro e feedback de campo
- Adicionar máscara/normalização se necessário (ex.: telefone)

## Próximos passos sugeridos

- Validações client-side leves (ex.: força de senha, mensagens inline)
- Estados de erro/sucesso visuais no CSS
- Internacionalização (i18n) e mensagens dinâmicas
- Testes de acessibilidade automatizados (axe, Lighthouse)

## Licença

Este projeto é fornecido “como está”. Use e adapte livremente.
