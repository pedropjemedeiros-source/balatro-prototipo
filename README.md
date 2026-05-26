[README.md](https://github.com/user-attachments/files/28241749/README.md)
# 🃏 Balatro Online

Um fan-made multiplayer do Balatro rodando direto no navegador — sem servidor, sem instalação, sem conta. Basta abrir o arquivo HTML e jogar com seus amigos em tempo real via WebRTC (PeerJS).

> **Aviso:** Este é um projeto não oficial, criado por fãs para fins educacionais e de entretenimento. Balatro é uma marca registrada da [LocalThunk](https://www.playbalatro.com/).

---

## ✨ Funcionalidades

### 🌐 Multiplayer P2P
- Conexão direta entre dispositivos via **WebRTC (PeerJS)** — sem servidor de jogo
- Até **4 jogadores** por sala
- Código de sala de 4 letras para compartilhar com amigos
- Funciona entre **dispositivos diferentes** (celular, computador, tablet)

### 🤖 Modo Solo vs Bot
- Jogue contra **1 a 3 bots** com inteligência artificial
- Três níveis de dificuldade: **Fácil 😴 · Médio 🎯 · Difícil 💀**
- Bots jogam automaticamente com estratégias baseadas na dificuldade

### 🃏 Coringas (Jokers)
- **22 coringas únicos** com efeitos variados
- Bônus de chips, multiplicadores, efeitos por naipe, por rank e por tipo de mão
- Configuração livre: ative ou desative cada coringa antes de iniciar a partida
- Jogadores ganham coringas aleatórios ao longo da partida

### ⚙️ Configuração da Partida
- **Pontuação para vencer** — de 500 a 999.999 pts (atalhos rápidos incluídos)
- **Mãos por rodada** — de 1 a 10
- Configurações alteráveis pelo host também na sala de espera

### 🔒 Controle de Acesso à Sala
- Botão **Abrir/Fechar sala** disponível durante o jogo e na sala de espera
- 🔓 **Sala Aberta** — qualquer pessoa com o código pode entrar
- 🔒 **Sala Fechada** — novos jogadores são bloqueados; quem já está continua normalmente
- Ao retornar ao lobby após um game over, a sala fecha automaticamente

### 🎮 Fluxo do Jogo
- Rodadas com meta de pontuação crescente (blind goal)
- Mãos avaliadas com as combinações clássicas de poker
- Descartes para substituir cartas indesejadas
- Placar em tempo real de todos os jogadores
- Ao fim do jogo: opção de **Revanche**, **Voltar ao Lobby** ou **Menu Principal**

---

## 🚀 Como Jogar

### Multiplayer com amigos

1. Abra o arquivo `balatro_prototipo_.html` no **Google Chrome**
2. Digite seu nome e clique em **Criar Sala**
3. Compartilhe o **código de 4 letras** com seus amigos
4. Os amigos abrem o mesmo arquivo, digitam o nome e o código, e clicam em **Entrar na Sala**
5. Quando todos estiverem na sala, o host clica em **Iniciar Jogo**

### Solo vs Bot

1. Abra o arquivo no Chrome
2. Digite seu nome
3. Na seção **Jogar Solo vs Bot**, escolha o número de bots e a dificuldade
4. Clique em **Iniciar Partida Solo ▶**

> **Dica:** Para jogar entre dispositivos diferentes na mesma rede local ou pela internet, todos precisam abrir o mesmo arquivo HTML. A conexão é feita diretamente entre os navegadores.

---

## 🃏 Combinações de Cartas

| Combinação | Chips base | Multiplicador |
|---|---|---|
| Carta Alta | chips + 5 | ×1 |
| Par | chips + 10 | ×2 |
| Dois Pares | chips + 20 | ×2 |
| Trinca | chips + 20 | ×3 |
| Sequência | chips + 30 | ×4 |
| Flush | chips + 35 | ×4 |
| Full House | chips + 40 | ×4 |
| Quadra | chips + 60 | ×7 |
| Straight Flush | chips + 100 | ×8 |

> Os coringas modificam chips e multiplicador antes do cálculo final: **Score = Chips × Mult**

---

## 🧩 Tecnologias

- **HTML + CSS + JavaScript** puro — zero dependências de build
- **[PeerJS](https://peerjs.com/)** (v1.5.4) para conexão WebRTC P2P
- **Google Fonts** — Cinzel + Crimson Pro
- **LocalStorage** como backup de estado local

---

## 📁 Estrutura

```
balatro-online/
└── balatro_prototipo_.html   # Jogo completo em arquivo único
└── README.md
```

Tudo em um único arquivo HTML autocontido. Sem npm, sem build, sem servidor.

---

## ⚠️ Requisitos

- **Google Chrome** (recomendado — WebRTC mais estável)
- Conexão com a internet (necessária para o servidor de sinalização PeerJS e fontes do Google)
- Não requer nenhuma instalação ou conta

---

## 🛠️ Limitações conhecidas

- A conexão P2P pode falhar em redes corporativas com firewall restritivo
- O estado do jogo não persiste entre recarregamentos de página
- Suporte a mobile funciona, mas a experiência é otimizada para desktop

---

## 📝 Licença

Este projeto é um **fan-made não comercial**. Todo o crédito pelo jogo original vai para [LocalThunk](https://www.playbalatro.com/). Este repositório não tem nenhuma afiliação oficial com os criadores do Balatro.

Distribuído sob a licença **MIT** para o código desenvolvido aqui.
