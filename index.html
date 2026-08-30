<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Jogo da Forca</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Courier+Prime:wght@400;700&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0f0f0f;
    --paper: #1a1a1a;
    --accent: #e8c547;
    --red: #e84747;
    --text: #f0ead6;
    --muted: #555;
    --border: #333;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Courier Prime', monospace;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 30px 20px;
  }

  h1 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 3.5rem;
    letter-spacing: 8px;
    color: var(--accent);
    text-shadow: 4px 4px 0 #000;
    margin-bottom: 6px;
  }

  .subtitle {
    font-size: 0.75rem;
    letter-spacing: 4px;
    color: var(--muted);
    text-transform: uppercase;
    margin-bottom: 30px;
  }

  .game-container {
    display: flex;
    gap: 40px;
    flex-wrap: wrap;
    justify-content: center;
    max-width: 900px;
    width: 100%;
  }

  .gallows-section {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 16px;
  }

  canvas {
    border: 1px solid var(--border);
    background: var(--paper);
    border-radius: 4px;
  }

  .lives-display {
    font-size: 0.8rem;
    letter-spacing: 2px;
    color: var(--muted);
  }

  .lives-display span { color: var(--red); font-weight: 700; }

  .word-section {
    flex: 1;
    min-width: 280px;
    display: flex;
    flex-direction: column;
    gap: 24px;
  }

  .hint-box {
    background: var(--paper);
    border: 1px solid var(--border);
    border-left: 4px solid var(--accent);
    padding: 12px 16px;
    font-size: 0.8rem;
    color: var(--accent);
    letter-spacing: 1px;
  }

  .hint-box strong { color: var(--text); }

  /* TIMER */
  .timer-wrap {
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .timer-bar-bg {
    flex: 1;
    height: 8px;
    background: var(--border);
    border-radius: 4px;
    overflow: hidden;
  }

  .timer-bar {
    height: 100%;
    width: 100%;
    background: var(--accent);
    border-radius: 4px;
    transition: width 1s linear, background 0.5s;
  }

  .timer-bar.danger { background: var(--red); }

  .timer-count {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 1.6rem;
    letter-spacing: 2px;
    color: var(--accent);
    min-width: 38px;
    text-align: right;
    transition: color 0.3s;
  }

  .timer-count.danger { color: var(--red); animation: pulse 0.5s infinite alternate; }

  @keyframes pulse {
    from { opacity: 1; }
    to { opacity: 0.4; }
  }

  .word-display {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
    justify-content: center;
    padding: 20px 0;
  }

  .letter-slot { width: 36px; text-align: center; }

  .letter-slot .letter {
    font-size: 2rem;
    font-weight: 700;
    display: block;
    min-height: 40px;
    text-transform: uppercase;
    transition: all 0.3s;
    color: var(--text);
  }

  .letter-slot .underline {
    display: block;
    height: 2px;
    background: var(--accent);
    margin-top: 4px;
  }

  .wrong-letters {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
    min-height: 36px;
    align-items: center;
  }

  .wrong-tag {
    background: #2a1a1a;
    border: 1px solid var(--red);
    color: var(--red);
    padding: 2px 10px;
    font-size: 1rem;
    font-weight: 700;
    text-transform: uppercase;
    border-radius: 2px;
    animation: pop 0.2s ease;
  }

  @keyframes pop {
    0% { transform: scale(1.4); }
    100% { transform: scale(1); }
  }

  .keyboard {
    display: grid;
    grid-template-columns: repeat(9, 1fr);
    gap: 5px;
    max-width: 360px;
  }

  .key {
    background: var(--paper);
    border: 1px solid var(--border);
    color: var(--text);
    font-family: 'Courier Prime', monospace;
    font-size: 0.85rem;
    font-weight: 700;
    padding: 8px 4px;
    cursor: pointer;
    text-transform: uppercase;
    border-radius: 2px;
    transition: all 0.15s;
    letter-spacing: 1px;
  }

  .key:hover:not(:disabled) {
    background: var(--accent);
    color: #000;
    border-color: var(--accent);
    transform: translateY(-2px);
  }

  .key:disabled { opacity: 0.2; cursor: not-allowed; transform: none; }

  .message {
    display: none;
    text-align: center;
    padding: 20px;
    border: 2px solid var(--accent);
    background: var(--paper);
    border-radius: 4px;
  }

  .message.win { border-color: var(--accent); }
  .message.lose { border-color: var(--red); }

  .message h2 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 2.5rem;
    letter-spacing: 4px;
    margin-bottom: 8px;
  }

  .message.win h2 { color: var(--accent); }
  .message.lose h2 { color: var(--red); }
  .message p { color: var(--muted); font-size: 0.85rem; margin-bottom: 16px; }
  .message .answer { color: var(--text); font-size: 1rem; margin-bottom: 16px; }

  .btn-new {
    background: var(--accent);
    color: #000;
    border: none;
    font-family: 'Bebas Neue', sans-serif;
    font-size: 1.2rem;
    letter-spacing: 3px;
    padding: 10px 30px;
    cursor: pointer;
    border-radius: 2px;
    transition: all 0.2s;
  }

  .btn-new:hover { transform: scale(1.05); box-shadow: 0 4px 20px rgba(232,197,71,0.4); }

  .section-label {
    font-size: 0.65rem;
    letter-spacing: 3px;
    color: var(--muted);
    text-transform: uppercase;
    margin-bottom: 6px;
  }

  /* THEME TOGGLE */
  .theme-toggle {
    position: fixed;
    top: 16px;
    right: 16px;
    display: flex;
    align-items: center;
    gap: 8px;
    background: var(--paper);
    border: 1px solid var(--border);
    border-radius: 999px;
    padding: 6px 14px;
    cursor: pointer;
    font-family: 'Courier Prime', monospace;
    font-size: 0.75rem;
    letter-spacing: 2px;
    color: var(--text);
    transition: all 0.2s;
    z-index: 100;
  }

  .theme-toggle:hover { border-color: var(--accent); color: var(--accent); }

  .toggle-icon { font-size: 1rem; transition: transform 0.4s; }
  .theme-toggle:hover .toggle-icon { transform: rotate(20deg); }

  /* LIGHT THEME */
  body.light {
    --bg: #f5f0e8;
    --paper: #ffffff;
    --accent: #c8860a;
    --red: #c0392b;
    --text: #1a1a1a;
    --muted: #888;
    --border: #ccc;
  }

  body.light .wrong-tag { background: #fff0f0; }
  body.light h1 { text-shadow: 3px 3px 0 #ccc; }
</style>
</head>
<body>

<button class="theme-toggle" onclick="toggleTheme()">
  <span class="toggle-icon" id="theme-icon">☀️</span>
  <span id="theme-label">CLARO</span>
</button>

<h1>FORCA</h1>
<p class="subtitle">Adivinhe a palavra antes que seja tarde</p>

<div class="game-container">
  <div class="gallows-section">
    <canvas id="gallows" width="200" height="220"></canvas>
    <p class="lives-display">Erros: <span id="error-count">0</span> / 6</p>
  </div>

  <div class="word-section">
    <div class="hint-box">
      <strong>Dica:</strong> <span id="hint-text"></span>
    </div>

    <div>
      <p class="section-label">&#9201; Tempo restante</p>
      <div class="timer-wrap">
        <div class="timer-bar-bg">
          <div class="timer-bar" id="timer-bar"></div>
        </div>
        <span class="timer-count" id="timer-count">60</span>
      </div>
    </div>

    <div>
      <p class="section-label">Palavra</p>
      <div class="word-display" id="word-display"></div>
    </div>

    <div>
      <p class="section-label">Letras erradas</p>
      <div class="wrong-letters" id="wrong-letters"></div>
    </div>

    <div id="message" class="message">
      <h2 id="msg-title"></h2>
      <p id="msg-sub"></p>
      <p class="answer" id="msg-answer"></p>
      <button class="btn-new" onclick="newGame()">JOGAR NOVAMENTE</button>
    </div>

    <div>
      <p class="section-label">Teclado</p>
      <div class="keyboard" id="keyboard"></div>
    </div>
  </div>
</div>

<script>
const words = [
  { word: "COMPUTADOR", hint: "Maquina eletronica de processar dados" },
  { word: "PROGRAMACAO", hint: "Arte de escrever instrucoes para computadores" },
  { word: "INTERNET", hint: "Rede mundial de computadores" },
  { word: "TECLADO", hint: "Periferico de entrada com teclas" },
  { word: "JAVASCRIPT", hint: "Linguagem de programacao da web" },
  { word: "NAVEGADOR", hint: "Programa para acessar sites" },
  { word: "ALGORITMO", hint: "Sequencia de passos para resolver um problema" },
  { word: "VARIAVEL", hint: "Espaco na memoria para guardar valores" },
  { word: "FUNCAO", hint: "Bloco de codigo reutilizavel" },
  { word: "SERVIDOR", hint: "Computador que fornece servicos na rede" },
  { word: "INTERFACE", hint: "Ponto de interacao entre usuario e sistema" },
  { word: "PIXEL", hint: "Menor ponto de uma imagem digital" },
  { word: "APLICATIVO", hint: "Programa para celular ou computador" },
  { word: "CIBERSEGURANCA", hint: "Protecao de sistemas digitais contra ataques" },
  { word: "BANCO DE DADOS", hint: "Sistema para armazenar e organizar informacoes" },
];

const canvas = document.getElementById('gallows');
const ctx = canvas.getContext('2d');

let word, hint, guessed, wrong, gameOver;
let timeLeft, timerInterval;
const TOTAL_TIME = 60;

// ── TIMER ──────────────────────────────────────────
function startTimer() {
  clearInterval(timerInterval);
  timeLeft = TOTAL_TIME;
  updateTimerUI();
  timerInterval = setInterval(function() {
    timeLeft--;
    updateTimerUI();
    if (timeLeft <= 0) {
      clearInterval(timerInterval);
      endGame(false, true);
    }
  }, 1000);
}

function stopTimer() {
  clearInterval(timerInterval);
}

function updateTimerUI() {
  var bar = document.getElementById('timer-bar');
  var count = document.getElementById('timer-count');
  var pct = (timeLeft / TOTAL_TIME) * 100;
  bar.style.width = pct + '%';
  count.textContent = timeLeft;
  var danger = timeLeft <= 10;
  if (danger) {
    bar.classList.add('danger');
    count.classList.add('danger');
  } else {
    bar.classList.remove('danger');
    count.classList.remove('danger');
  }
}

// ── GALLOWS ────────────────────────────────────────
function drawGallows(errors) {
  ctx.clearRect(0, 0, 200, 220);
  ctx.strokeStyle = '#555';
  ctx.lineWidth = 3;
  ctx.lineCap = 'round';

  ctx.beginPath(); ctx.moveTo(20, 210); ctx.lineTo(180, 210); ctx.stroke();
  ctx.beginPath(); ctx.moveTo(60, 210); ctx.lineTo(60, 20); ctx.stroke();
  ctx.beginPath(); ctx.moveTo(60, 20); ctx.lineTo(130, 20); ctx.stroke();
  ctx.beginPath(); ctx.moveTo(130, 20); ctx.lineTo(130, 50); ctx.stroke();

  if (errors === 0) return;

  ctx.strokeStyle = errors >= 6 ? '#e84747' : '#e8c547';
  ctx.lineWidth = 2.5;

  if (errors >= 1) { ctx.beginPath(); ctx.arc(130, 65, 15, 0, Math.PI * 2); ctx.stroke(); }
  if (errors >= 2) { ctx.beginPath(); ctx.moveTo(130, 80); ctx.lineTo(130, 140); ctx.stroke(); }
  if (errors >= 3) { ctx.beginPath(); ctx.moveTo(130, 95); ctx.lineTo(105, 120); ctx.stroke(); }
  if (errors >= 4) { ctx.beginPath(); ctx.moveTo(130, 95); ctx.lineTo(155, 120); ctx.stroke(); }
  if (errors >= 5) { ctx.beginPath(); ctx.moveTo(130, 140); ctx.lineTo(105, 175); ctx.stroke(); }
  if (errors >= 6) {
    ctx.beginPath(); ctx.moveTo(130, 140); ctx.lineTo(155, 175); ctx.stroke();
    ctx.lineWidth = 2; ctx.strokeStyle = '#e84747';
    ctx.beginPath(); ctx.moveTo(122,60); ctx.lineTo(127,65); ctx.stroke();
    ctx.beginPath(); ctx.moveTo(127,60); ctx.lineTo(122,65); ctx.stroke();
    ctx.beginPath(); ctx.moveTo(133,60); ctx.lineTo(138,65); ctx.stroke();
    ctx.beginPath(); ctx.moveTo(138,60); ctx.lineTo(133,65); ctx.stroke();
  }
}

// ── KEYBOARD ───────────────────────────────────────
function buildKeyboard() {
  var kb = document.getElementById('keyboard');
  kb.innerHTML = '';
  'ABCDEFGHIJKLMNOPQRSTUVWXYZ'.split('').forEach(function(l) {
    var btn = document.createElement('button');
    btn.className = 'key';
    btn.textContent = l;
    btn.id = 'key-' + l;
    btn.onclick = function() { guess(l); };
    kb.appendChild(btn);
  });
}

// ── RENDER ─────────────────────────────────────────
function renderWord() {
  var display = document.getElementById('word-display');
  display.innerHTML = '';
  word.split('').forEach(function(ch) {
    var slot = document.createElement('div');
    slot.className = 'letter-slot';
    if (ch === ' ') {
      slot.style.width = '20px';
      slot.innerHTML = '<span class="letter">&nbsp;</span>';
    } else {
      var revealed = guessed.has(ch);
      slot.innerHTML = '<span class="letter">' + (revealed ? ch : '&nbsp;') + '</span><span class="underline"></span>';
    }
    display.appendChild(slot);
  });
}

function renderWrong() {
  var wr = document.getElementById('wrong-letters');
  wr.innerHTML = '';
  wrong.forEach(function(l) {
    var tag = document.createElement('span');
    tag.className = 'wrong-tag';
    tag.textContent = l;
    wr.appendChild(tag);
  });
  document.getElementById('error-count').textContent = wrong.size;
}

// ── GAME LOGIC ─────────────────────────────────────
function guess(letter) {
  if (gameOver || guessed.has(letter) || wrong.has(letter)) return;
  var btn = document.getElementById('key-' + letter);
  if (btn) btn.disabled = true;

  if (word.includes(letter)) {
    guessed.add(letter);
    renderWord();
    var allRevealed = word.split('').every(function(ch) { return ch === ' ' || guessed.has(ch); });
    if (allRevealed) endGame(true, false);
  } else {
    wrong.add(letter);
    renderWrong();
    drawGallows(wrong.size);
    if (wrong.size >= 6) endGame(false, false);
  }
}

function endGame(won, timeout) {
  gameOver = true;
  stopTimer();

  var bar = document.getElementById('timer-bar');
  bar.style.transition = 'none';

  var msg = document.getElementById('message');
  msg.style.display = 'block';
  msg.className = 'message ' + (won ? 'win' : 'lose');

  var title, sub;
  if (won) {
    title = 'VOCE GANHOU!';
    sub = 'Parabens! Voce acertou com ' + timeLeft + 's sobrando.';
  } else if (timeout) {
    title = 'TEMPO ESGOTADO!';
    sub = 'O tempo acabou! A palavra era:';
  } else {
    title = 'GAME OVER';
    sub = 'Que pena! A palavra era:';
  }

  document.getElementById('msg-title').textContent = title;
  document.getElementById('msg-sub').textContent = sub;
  document.getElementById('msg-answer').textContent = won ? '' : word;
}

function newGame() {
  var pick = words[Math.floor(Math.random() * words.length)];
  word = pick.word;
  hint = pick.hint;
  guessed = new Set();
  wrong = new Set();
  gameOver = false;

  document.getElementById('hint-text').textContent = hint;
  document.getElementById('message').style.display = 'none';

  var bar = document.getElementById('timer-bar');
  bar.style.transition = 'width 1s linear, background 0.5s';

  buildKeyboard();
  renderWord();
  renderWrong();
  drawGallows(0);
  startTimer();
}

newGame();

function toggleTheme() {
  var isLight = document.body.classList.toggle('light');
  document.getElementById('theme-icon').textContent = isLight ? '🌙' : '☀️';
  document.getElementById('theme-label').textContent = isLight ? 'ESCURO' : 'CLARO';
  drawGallows(wrong ? wrong.size : 0);
}

document.addEventListener('keydown', function(e) {
  var l = e.key.toUpperCase();
  if (/^[A-Z]$/.test(l)) guess(l);
});
</script>
</body>
</html>****
