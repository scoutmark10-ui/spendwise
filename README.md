# SpendWise

O **SpendWise** e um projeto de gestor financeiro pessoal feito com HTML e CSS (JavaScript ainda sera evoluido).

A ideia e simples: ajudar a pessoa a visualizar melhor para onde o dinheiro esta indo e manter controle das despesas do dia a dia.

## O que ja existe hoje

- Tela inicial (`index.html`) com proposta do app e secoes de beneficios
- Estrutura inicial de dashboard (`dashboard.html`)
- Organizacao de estilos por arquivos em `css/` (variaveis, utilitarios, componentes e pagina)
- Base do projeto pronta para continuar evoluindo com funcionalidades reais

## Como executar localmente

Como o projeto e estatico, nao precisa instalar dependencia.

1. Abra a pasta do projeto.
2. Execute o arquivo `index.html` no navegador.
3. Para testar outras telas, abra `dashboard.html`, `add.html` e `list.html`.

## Estrutura do projeto

```txt
spendwise/
  index.html
  dashboard.html
  add.html
  list.html
  css/
    main.css
    variables.css
    reset.css
    components.css
    utilities.css
    layout.css
    pages/
      welcome.css
  js/
    main.js
```

## Status atual

Projeto em fase inicial de interface.

- `index.html` esta mais avancada
- `dashboard.html`, `add.html`, `list.html` e `js/main.js` ainda estao em construcao

## Proximos passos sugeridos

- Criar formulario de cadastro de despesas em `add.html`
- Listar despesas em `list.html`
- Mostrar resumo no `dashboard.html` (total gasto, categorias, periodo)
- Implementar persistencia com `localStorage` no `js/main.js`

## Autor

Feito por **Handerson Diniz**.
