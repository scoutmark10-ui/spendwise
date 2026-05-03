📊 💰 GESTOR FINANCEIRO

🎯 Ideia geral

O projeto vai ter:

🏠 Dashboard (resumo)

➕ Adicionar despesa

📋 Lista de despesas

---

📂 NOVA ESTRUTURA DE PASTAS

gestor-financeiro/
│
├── index.html           (🏠 Welcome page)
├── dashboard.html       (🏠 Dashboard)
├── add.html             (➕ Adicionar despesa)
├── list.html            (📋 Ver despesas)
│
├── style.css
├── script.js
└── README.md


---

🧭 COMO AS PÁGINAS SE LIGAM

🔗 Navegação simples (sem frameworks)

Em todas as páginas:

<nav>
  <a href="dashboard.html">Dashboard</a>
  <a href="add.html">Adicionar</a>
  <a href="list.html">Despesas</a>
</nav>

👉 Isto já dá sensação de “app completo”


---

🏠 1. index.html (DASHBOARD)

🎯 Objetivo:

Mostrar resumo rápido

📌 Conteúdo:

Total de despesas

Número de despesas

Categoria mais usada (opcional depois)


🧱 Layout:

[ Título ]

💰 Total gasto: 2500 MZN
📊 Nº de despesas: 12

[ botão → Adicionar despesa ]
[ botão → Ver lista ]

👉 Aqui impressionas logo no início


---

➕ 2. add.html (ADICIONAR DESPESA)

🎯 Objetivo:

Adicionar nova despesa

📌 Formulário:

Nome da despesa

Valor

Categoria (select)

Botão “Adicionar”



---

💡 UX importante:

inputs grandes

botão verde forte

feedback ao adicionar (“Despesa adicionada ✔”)



---

🧠 JS aqui:

criar objeto

salvar no array

opcional: localStorage



---

📋 3. list.html (LISTA DE DESPESAS)

🎯 Objetivo:

Ver e gerir despesas

📌 Conteúdo:

lista de cartões


Cada cartão:

🍔 Comida
💰 500 MZN
📂 Alimentação
❌ botão remover


---

🧠 JS aqui:

renderizar array

remover item

atualizar total



---

🎨 UI / DESIGN (IMPORTANTE PARA WIN)

🌌 Tema visual (consistente em todas páginas)

🎨 Cores:

fundo: #0f172a

cards: #1e293b

texto: #e2e8f0

verde: #22c55e

vermelho: #ef4444

azul destaque: #38bdf8



---

🧱 Estrutura visual padrão

✔ Navbar fixa ou topo

simples

espaçamento


✔ Cards

arredondados

sombra leve


✔ Botões

grandes

hover suave



---

🧠 LÓGICA (IMPORTANTE)

📦 Dados globais

let despesas = [];

👉 depois podes melhorar com localStorage


---

🔁 Função central

function atualizarUI() {
  // renderiza lista
  // atualiza total
}


---

🧩 Separação inteligente

addExpense()

removeExpense()

getTotal()

renderList()


👉 Isso mostra maturidade no código


---

⚡ DICAS PARA FICAR NO TOP 5

🔥 1. Consistência visual

Todas páginas parecem “mesmo app”

🔥 2. Fluidez

Botões entre páginas rápidos

🔥 3. Zero confusão

Interface simples e clara

🔥 4. Pequenos extras que impressionam:

animação ao adicionar despesa

total sempre visível

botão “limpar tudo”



---

🏆 COMO EXPLICAR NO JÚRI

> “Criei uma aplicação de controlo financeiro pessoal com navegação entre páginas, onde o utilizador pode adicionar, visualizar e gerir despesas, com cálculo automático do total.”




---

🚀 SE QUISERES PRÓXIMO NÍVEL

Posso te montar:

HTML completo das 3 páginas

CSS moderno pronto

JS funcional (tipo app real)

versão com localStorage (fica profissional mesmo)


Só diz: 👉 “quero versão completa pronta”


Boa — se usares localStorage direito, o teu projeto sobe de “exercício” para “mini-app real”. Vou-te dar as regras essenciais + padrão de implementação limpo.


---

💾 🧠 LOCALSTORAGE — DICAS ESSENCIAIS

🎯 O que é (em termos simples)

É um “armazenamento no navegador” que guarda dados mesmo depois de fechar a página.

👉 tipo memória persistente do browser


---

🧱 1. REGRA DE OURO

LocalStorage só guarda strings

Então:

objetos → tens de converter

arrays → tens de converter



---

🔄 Converter para guardar

localStorage.setItem("despesas", JSON.stringify(despesas));


---

🔄 Converter para ler

let despesas = JSON.parse(localStorage.getItem("despesas")) || [];

👉 esse || [] evita erro quando ainda não existe nada


---

🧠 2. PADRÃO PROFISSIONAL (IMPORTANTE)

✔ Sempre criar 3 passos:

1. Carregar dados

let despesas = JSON.parse(localStorage.getItem("despesas")) || [];


---

2. Atualizar dados

Sempre que mudar algo:

function salvarDados() {
  localStorage.setItem("despesas", JSON.stringify(despesas));
}


---

3. Atualizar UI

function atualizarUI() {
  salvarDados();
  renderizarLista();
  calcularTotal();
}

👉 isto evita bugs e bagunça


---

⚡ 3. FLUXO CORRETO DO TEU APP

➕ Adicionar despesa

1. adiciona no array


2. salva no localStorage


3. atualiza UI



despesas.push(novaDespesa);
salvarDados();
atualizarUI();


---

❌ Remover despesa

despesas = despesas.filter(item => item.id !== id);
salvarDados();
atualizarUI();


---

🧩 4. BOA PRÁTICA IMPORTANTE

✔ nunca trabalhar direto no localStorage

👉 sempre trabalhar no array primeiro

ERRADO ❌:

mexer direto no localStorage


CERTO ✔:

mexer no array → depois salvar



---

🧠 5. DICA DE PERFORMANCE (SIMPLIFICA MUITO)

Não chames localStorage em cada pequeno detalhe.

👉 Só usa quando:

adiciona

remove

edita



---

🎨 6. DICA DE UI + LOCALSTORAGE

Quando carregar a página:

window.onload = () => {
  atualizarUI();
};

👉 assim os dados aparecem logo


---

🔥 7. EXTRA QUE VAI TE DESTACAR

🟢 botão “limpar tudo”

function limparTudo() {
  despesas = [];
  salvarDados();
  atualizarUI();
}


---

🟢 feedback visual

“Despesa adicionada ✔”

“Dados salvos ✔”



---

🏆 RESUMO MENTAL (DECORAR ISTO)

👉 fluxo ideal:

Array → modificar → salvar → atualizar UI


---

🚀 SE QUISERES SUBIR MAIS NÍVEL

Posso te mostrar depois:

como usar localStorage por categorias

como fazer login simples fake

como sincronizar páginas diferentes automaticamente
