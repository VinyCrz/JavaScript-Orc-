document.addEventListener("DOMContentLoaded", () => {
  
  let hero = {
    nome: "Vinicius Nunes da Cruz",
    classe: "Garoto de programa 2.0",
    nivel: 1,
    xp: 445
  };

  const xpPorNivel = 500;

  const nomeEl = document.getElementById("hero-nome");
  const classeEl = document.getElementById("hero-classe");
  const nivelEl = document.getElementById("hero-nivel");
  const xpEl = document.getElementById("hero-xp");

  function atualizarPainel() {
    nomeEl.textContent = hero.nome;
    classeEl.textContent = hero.classe;
    nivelEl.textContent = hero.nivel;
    xpEl.textContent = hero.xp;
  }

  const painelHeroi = document.getElementById("painel-heroi");

  painelHeroi.addEventListener("click", () => {
    ganharXp(50);
  });

  const formContato = document.querySelector("#contato form");

  formContato.addEventListener("submit", (event) => {
    event.preventDefault(); 

    const nome = document.getElementById("nome").value;

    alert(`Obrigado pela mensagem, ${nome}!`);
    formContato.reset();

    ganharXp(100);
  });
  atualizarPainel();
});
