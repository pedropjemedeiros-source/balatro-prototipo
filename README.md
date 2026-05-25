# 🃏 Balatro Online

Versão multiplayer do Balatro rodando 100% no navegador, sem servidor ou instalação. Comunicação entre jogadores via **WebRTC P2P** usando [PeerJS](https://peerjs.com/).

## 🚀 Como Jogar

1. Abra o `index.html` no Chrome (ou qualquer navegador moderno)
2. Digite seu nome
3. **Criar Sala** → compartilhe o código de 4 letras com seus amigos
4. **Entrar na Sala** → cole o código que o host enviou
5. O host configura a meta de pontuação e inicia o jogo

## ⚙️ Configurações da Sala (host)

| Opção | Descrição |
|-------|-----------|
| ⚡ 1.000 pts | Partida rápida |
| 🃏 2.500 pts | Partida normal |
| 🎰 5.000 pts | Partida longa (padrão) |
| 🏆 10.000 pts | Partida épica |

## 🃏 Combinações e Pontuação

> **Pontuação = (Valor das cartas + Chips extras) × Mult**

| Mão | Chips extras | Mult |
|-----|:-----------:|:----:|
| Straight Flush | +100 | ×8 |
| Quadra | +60 | ×7 |
| Full House | +40 | ×4 |
| Flush | +35 | ×4 |
| Sequência | +30 | ×4 |
| Trinca | +20 | ×3 |
| Dois Pares | +20 | ×2 |
| Par | +10 | ×2 |
| Carta Alta | +5 | ×1 |

## 🎲 Coringas

Há 30% de chance de ganhar um coringa aleatório após cada jogada (máximo 3 por jogador):

| Coringa | Efeito |
|---------|--------|
| 🃏 Coringa Base | +50 Chips em qualquer mão |
| 👑 Rei do Flush | +4 Mult em Flush |
| 💕 Amante dos Pares | +30 Chips em Par |

## 🎮 Regras

- Até **4 jogadores** simultâneos
- Cada jogador recebe **8 cartas**; a mão é reabastecida após cada jogada
- **4 mãos** e **3 descartes** por rodada
- Quando o deck esgota, um novo baralho é embaralhado automaticamente 🔀
- Primeiro a atingir a meta de pontuação configurada vence
- Ao fim de cada rodada, os jogadores podem continuar ou reiniciar

## 🛠 Tecnologias

- HTML + CSS + JavaScript puro — sem framework, sem build
- [PeerJS 1.5.4](https://cdn.jsdelivr.net/npm/peerjs@1.5.4/) para WebRTC P2P
- Google Fonts (Cinzel + Crimson Pro)

## 📁 Estrutura

```
index.html   ← Jogo completo (HTML + CSS + JS em arquivo único)
README.md
```

## ⚠️ Limitações

- Requer internet para o servidor de sinalização do PeerJS
- Melhor experiência no **Chrome** (desktop ou Android)
- NAT simétrico pode bloquear conexões P2P em algumas redes corporativas

## 🌐 Como hospedar no GitHub Pages

1. Crie um repositório público no GitHub
2. Suba os arquivos (`index.html` e `README.md`)
3. Vá em **Settings → Pages → Source: main branch → / (root)**
4. Acesse em `https://seu-usuario.github.io/nome-do-repo`
