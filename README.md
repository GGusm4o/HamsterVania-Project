# 🐹⚔️ HamsterVania: O Cavaleiro Valente

> **A vingança contra o vampiro.** Um jogo de plataforma 2D estilo *Metroidvania / boss rush*, feito em **um único arquivo HTML** com JavaScript puro. Sem instalação, sem dependências, joga direto no navegador — no **PC** ou no **celular**.

![HTML5](https://img.shields.io/badge/HTML5-Canvas-e34f26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-f7df1e?logo=javascript&logoColor=black)
![Sem dependências](https://img.shields.io/badge/depend%C3%AAncias-nenhuma-success)
![PC e Mobile](https://img.shields.io/badge/plataformas-PC%20%7C%20Mobile-blue)

---

## 📖 História

O temível **Conde Drácula** e seu exército de monstros roubaram todo o estoque secreto de sementes douradas da hamster cavaleira **Jujuba**. Decidida a recuperar o que é seu, ela ergue a espada mágica e parte em uma jornada por **8 regiões traiçoeiras** — de salões góticos a florestas sombrias, criptas, fossos de lava e o trono final — enfrentando um **chefão lendário** em cada uma delas.

---

## ✨ Recursos

- 🗺️ **8 fases** com temas visuais únicos e **8 chefões** com padrões de ataque diferentes
- ⚔️ **Combate completo:** espada, magia (consome MP) e **dash invulnerável** (consome estamina)
- 🔒 **Sala do chefão trancada:** um portão fecha atrás de você até o chefão cair; ao vencer, você segue para a próxima fase
- 💾 **Sistema de save:** o progresso é salvo a cada fase nova, com **CONTINUAR** e **NOVO JOGO**
- ⏸️ **Menu de pause:** continuar, reiniciar fase, ligar/desligar a música e voltar ao menu
- 📱 **Responsivo:** joga em qualquer tela, com controles touch multitoque no celular e tablet
- 🎨 **Arte e som 100% por código:** gráficos desenhados no Canvas e áudio sintetizado com a Web Audio API — nenhum arquivo de imagem ou som

---

## 🚀 Como jogar

### Opção 1 — Direto no navegador

1. Baixe o arquivo [`HamsterVania.html`](HamsterVania.html).
2. Abra com um navegador moderno (Chrome, Edge, Firefox ou Safari).
3. Clique em **JOGAR** (ou aperte **Enter**).

### Opção 2 — Clonando o repositório

```bash
git clone https://github.com/GGusm4o/HamsterVania-Project.git
cd HamsterVania-Project
```

Depois é só abrir o `HamsterVania.html` no navegador. Não precisa de servidor nem de build.

> 💡 A fonte *Press Start 2P* é carregada do Google Fonts. Sem internet o jogo funciona normalmente, com uma fonte de reserva.

---

## 🎮 Controles

### Teclado (PC)

| Ação | Teclas |
|---|---|
| Mover | `A` / `D` ou `←` / `→` |
| Pular | `W`, `Espaço` ou `↑` |
| Atacar (espada) | `J` ou `Z` |
| Dash (invulnerável) | `K` ou `X` |
| Magia | `L` ou `C` |
| Pausar / retomar | `Esc` ou `P` |
| Começar / avançar / recomeçar | `Enter` |

### Touch (celular e tablet)

- **D-pad** à esquerda para andar (dá para **deslizar o dedo** entre ◀ e ▶).
- Botões **MAGIA**, **DASH**, **PULAR** e **ATACAR** à direita — todos funcionam ao mesmo tempo (multitoque).
- Botão **II** no centro, embaixo, para pausar.
- Em **paisagem** o jogo ocupa a tela toda e os botões ficam sobre ele; em **retrato** os botões ficam embaixo, maiores. Para a melhor experiência, **jogue em paisagem** e use o botão **TELA CHEIA** da tela inicial (quando disponível).

---

## 🧙 Mecânicas

| Mecânica | Como funciona |
|---|---|
| **Vida (HP)** | Chega a 0 → *Game Over*, e você recomeça a fase atual |
| **Mana (MP)** | A magia custa 25 MP; o MP regenera sozinho |
| **Estamina (ST)** | Cada dash custa 34 de estamina (dá para encadear 2 dashes). Ela recarrega após uma breve pausa; sem estamina suficiente a barra fica cinza |
| **Dash** | Investida curta e **invulnerável** — ótimo para atravessar ataques |
| **Chefão** | Só ataca quando você entra na arena. Ao entrar, o portão se fecha; ao derrotá-lo, ele abre e você avança |
| **Fase 3** | Em vez de inimigos comuns, há um NPC misterioso... aperte **ATACAR** perto dele e veja o que acontece |

---

## 💾 Save

O progresso é gravado automaticamente no navegador (`localStorage`) **sempre que uma fase nova começa** — ou seja, depois de derrotar cada chefão.

- **CONTINUAR - FASE N** retoma a partir da fase salva (a fase começa do início, com vida, mana e estamina cheias).
- **NOVO JOGO** apaga o save (pede confirmação).
- O save é **por navegador e por aparelho**. Limpar os dados do site apaga o progresso.
- Ao zerar o jogo, o save é removido.

---

## 🛠️ Tecnologias

- **HTML5 + CSS3** — interface, menus e layout responsivo (container queries, `clamp()`, safe areas)
- **JavaScript (vanilla)** — lógica do jogo, loop de passo fixo a 60 atualizações/s
- **Canvas 2D** — toda a arte é desenhada por código
- **Web Audio API** — efeitos sonoros e música sintetizados
- **Pointer Events** — controles touch multitoque
- **localStorage** — save e preferência de música

### Compatibilidade

Navegadores modernos com suporte a container queries: Chrome/Edge 105+, Safari 16+, Firefox 110+.

---

## 📁 Estrutura do projeto

```
HamsterVania-Project/
├── HamsterVania.html             # O jogo completo (HTML + CSS + JS)
├── HamsterVania-DOCUMENTACAO.md  # Documentação técnica detalhada
└── README.md                     # Este arquivo
```

---

## 📚 Documentação técnica

Quer entender ou modificar o código? A documentação completa está em [`HamsterVania-DOCUMENTACAO.md`](HamsterVania-DOCUMENTACAO.md) e cobre:

- estrutura do arquivo, interface e layout responsivo
- loop principal, física, jogador, inimigos e chefões (com os padrões de ataque de cada um)
- áudio, save, pause e fluxo de telas
- referência de todas as funções e tabela de balanceamento
- guia para estender o jogo (novos chefões, temas, ações) e limitações conhecidas

### Truques para testar (console do navegador)

```js
player.x = BOSS_ARENA_X + 100;   // teleporta para a sala do chefão
damageBoss(99999);               // derrota o chefão e avança de fase
player.hp = 100;                 // restaura a vida
```

---

## 🗺️ Ideias futuras

- Salvar posição e status no meio da fase (checkpoints)
- Colisão lateral e de teto nas plataformas
- Mais inimigos e tipos de plataforma
- Suporte a controle (gamepad)

---

## 👤 Autor

Feito por **GGusmão** e **Gustavo Meireles** — [@GGusm4o](https://github.com/GGusm4o)

Se curtiu o jogo, deixe uma ⭐ no repositório!
