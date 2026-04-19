<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Chrono Voix — Suivi du temps</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Mono:wght@400;500&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #0f0e0c;
    --paper: #f5f0e8;
    --cream: #ede6d6;
    --accent: #c8401a;
    --accent2: #2a6b4f;
    --gold: #c9933a;
    --muted: #8a7e6e;
    --line: #d4cabb;
    --white: #faf8f4;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--paper);
    color: var(--ink);
    min-height: 100vh;
    background-image: 
      radial-gradient(ellipse at 20% 0%, rgba(200,64,26,0.06) 0%, transparent 50%),
      radial-gradient(ellipse at 80% 100%, rgba(42,107,79,0.06) 0%, transparent 50%);
  }

  header {
    background: var(--ink);
    color: var(--paper);
    padding: 20px 32px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 16px;
    border-bottom: 3px solid var(--accent);
  }

  .logo {
    font-family: 'DM Serif Display', serif;
    font-size: 1.6rem;
    letter-spacing: -0.5px;
  }
  .logo span { color: var(--accent); font-style: italic; }

  .header-date {
    font-family: 'DM Mono', monospace;
    font-size: 0.75rem;
    color: var(--muted);
    text-align: right;
  }

  nav {
    display: flex;
    gap: 4px;
    padding: 12px 32px;
    background: var(--cream);
    border-bottom: 1px solid var(--line);
  }

  .tab {
    padding: 8px 20px;
    border-radius: 4px;
    border: none;
    background: transparent;
    font-family: 'DM Sans', sans-serif;
    font-size: 0.85rem;
    font-weight: 500;
    color: var(--muted);
    cursor: pointer;
    transition: all 0.2s;
  }
  .tab:hover { background: var(--line); color: var(--ink); }
  .tab.active {
    background: var(--ink);
    color: var(--paper);
  }

  .page { display: none; padding: 32px; max-width: 860px; margin: 0 auto; }
  .page.active { display: block; }

  /* ===== SAISIE VOIX ===== */
  .voice-card {
    background: var(--white);
    border: 1px solid var(--line);
    border-radius: 12px;
    padding: 32px;
    margin-bottom: 24px;
    box-shadow: 0 2px 12px rgba(15,14,12,0.06);
  }

  .voice-btn-wrap {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 16px;
    margin-bottom: 28px;
  }

  #voiceBtn {
    width: 96px; height: 96px;
    border-radius: 50%;
    border: 3px solid var(--accent);
    background: var(--white);
    cursor: pointer;
    display: flex; align-items: center; justify-content: center;
    transition: all 0.25s;
    position: relative;
    box-shadow: 0 4px 20px rgba(200,64,26,0.15);
  }
  #voiceBtn:hover { background: var(--accent); }
  #voiceBtn:hover svg path { fill: white; }
  #voiceBtn.listening {
    background: var(--accent);
    animation: pulse 1.4s infinite;
    border-color: var(--accent);
  }
  #voiceBtn.listening svg path { fill: white; }

  @keyframes pulse {
    0%, 100% { box-shadow: 0 0 0 0 rgba(200,64,26,0.4); }
    50% { box-shadow: 0 0 0 16px rgba(200,64,26,0); }
  }

  .voice-status {
    font-size: 0.8rem;
    color: var(--muted);
    font-family: 'DM Mono', monospace;
    text-transform: uppercase;
    letter-spacing: 0.08em;
  }
  .voice-status.active { color: var(--accent); }

  #transcript {
    background: var(--paper);
    border: 1px dashed var(--line);
    border-radius: 8px;
    padding: 16px;
    min-height: 60px;
    font-family: 'DM Mono', monospace;
    font-size: 0.9rem;
    color: var(--ink);
    margin-bottom: 20px;
    line-height: 1.6;
  }
  #transcript.placeholder { color: var(--muted); font-style: italic; }

  .hint-box {
    background: rgba(42,107,79,0.07);
    border-left: 3px solid var(--accent2);
    border-radius: 0 8px 8px 0;
    padding: 12px 16px;
    font-size: 0.82rem;
    color: var(--accent2);
    margin-bottom: 24px;
    line-height: 1.6;
  }
  .hint-box strong { font-weight: 600; }

  /* Form fields */
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 16px; }
  .form-row.thirds { grid-template-columns: 1fr 1fr 1fr; }
  .field { display: flex; flex-direction: column; gap: 6px; }
  .field label { font-size: 0.75rem; font-weight: 500; color: var(--muted); text-transform: uppercase; letter-spacing: 0.06em; }
  .field input, .field select, .field textarea {
    padding: 10px 14px;
    border: 1px solid var(--line);
    border-radius: 6px;
    background: var(--paper);
    font-family: 'DM Sans', sans-serif;
    font-size: 0.9rem;
    color: var(--ink);
    transition: border 0.2s;
  }
  .field input:focus, .field select:focus, .field textarea:focus {
    outline: none;
    border-color: var(--accent);
  }
  .field textarea { min-height: 70px; resize: vertical; }

  .btn-row { display: flex; gap: 12px; justify-content: flex-end; margin-top: 8px; }

  .btn {
    padding: 10px 24px;
    border: none;
    border-radius: 6px;
    font-family: 'DM Sans', sans-serif;
    font-size: 0.9rem;
    font-weight: 500;
    cursor: pointer;
    transition: all 0.2s;
  }
  .btn-primary { background: var(--accent); color: white; }
  .btn-primary:hover { background: #a33316; }
  .btn-secondary { background: var(--cream); color: var(--ink); border: 1px solid var(--line); }
  .btn-secondary:hover { background: var(--line); }

  /* Today list */
  .section-title {
    font-family: 'DM Serif Display', serif;
    font-size: 1.2rem;
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 10px;
    padding-bottom: 10px;
    border-bottom: 1px solid var(--line);
  }
  .section-title .badge {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    background: var(--ink);
    color: var(--paper);
    padding: 3px 8px;
    border-radius: 20px;
  }

  .entry-list { display: flex; flex-direction: column; gap: 10px; }
  .entry-item {
    background: var(--white);
    border: 1px solid var(--line);
    border-radius: 10px;
    padding: 14px 18px;
    display: flex;
    align-items: center;
    gap: 16px;
    animation: slideIn 0.25s ease;
  }
  @keyframes slideIn {
    from { opacity: 0; transform: translateY(-8px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .entry-time {
    font-family: 'DM Mono', monospace;
    font-size: 0.8rem;
    color: var(--muted);
    min-width: 50px;
  }
  .entry-client {
    background: var(--ink);
    color: var(--paper);
    font-size: 0.75rem;
    font-weight: 500;
    padding: 3px 10px;
    border-radius: 20px;
    white-space: nowrap;
  }
  .entry-hours {
    font-family: 'DM Serif Display', serif;
    font-size: 1.15rem;
    color: var(--accent);
    min-width: 50px;
  }
  .entry-desc {
    flex: 1;
    font-size: 0.85rem;
    color: var(--ink);
  }
  .entry-del {
    background: none;
    border: none;
    cursor: pointer;
    color: var(--line);
    padding: 4px;
    border-radius: 4px;
    transition: color 0.2s;
    font-size: 1rem;
    line-height: 1;
  }
  .entry-del:hover { color: var(--accent); }

  .day-total {
    text-align: right;
    font-family: 'DM Mono', monospace;
    font-size: 0.8rem;
    color: var(--muted);
    margin-top: 10px;
  }
  .day-total strong { color: var(--accent); font-size: 1rem; }

  /* ===== RAPPORT MENSUEL ===== */
  .month-selector {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 28px;
  }
  .month-selector select {
    padding: 8px 16px;
    border: 1px solid var(--line);
    border-radius: 6px;
    background: var(--white);
    font-family: 'DM Sans', sans-serif;
    font-size: 0.9rem;
    color: var(--ink);
  }
  .month-selector button {
    padding: 8px 18px;
    background: var(--accent);
    color: white;
    border: none;
    border-radius: 6px;
    font-family: 'DM Sans', sans-serif;
    font-size: 0.85rem;
    font-weight: 500;
    cursor: pointer;
  }

  .client-block {
    background: var(--white);
    border: 1px solid var(--line);
    border-radius: 12px;
    margin-bottom: 20px;
    overflow: hidden;
    box-shadow: 0 2px 8px rgba(15,14,12,0.04);
  }

  .client-header {
    background: var(--ink);
    color: var(--paper);
    padding: 14px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .client-header h3 {
    font-family: 'DM Serif Display', serif;
    font-size: 1.1rem;
  }
  .client-total {
    font-family: 'DM Mono', monospace;
    font-size: 0.9rem;
    color: var(--gold);
  }

  .client-entries {
    padding: 0;
  }
  .client-entry-row {
    display: grid;
    grid-template-columns: 90px 120px 1fr;
    gap: 12px;
    padding: 12px 20px;
    border-bottom: 1px solid var(--line);
    font-size: 0.85rem;
    align-items: center;
  }
  .client-entry-row:last-child { border-bottom: none; }
  .client-entry-row:nth-child(even) { background: var(--paper); }
  .col-date { font-family: 'DM Mono', monospace; font-size: 0.78rem; color: var(--muted); }
  .col-h { font-family: 'DM Serif Display', serif; color: var(--accent); font-size: 1rem; }
  .col-desc { color: var(--ink); }

  .rapport-summary {
    background: var(--ink);
    color: var(--paper);
    border-radius: 12px;
    padding: 20px 24px;
    margin-bottom: 24px;
    display: flex;
    gap: 32px;
  }
  .sum-item { display: flex; flex-direction: column; gap: 4px; }
  .sum-label { font-size: 0.7rem; text-transform: uppercase; letter-spacing: 0.08em; color: var(--muted); }
  .sum-value { font-family: 'DM Serif Display', serif; font-size: 1.8rem; color: var(--gold); }

  .empty-state {
    text-align: center;
    padding: 60px 20px;
    color: var(--muted);
  }
  .empty-state .icon { font-size: 3rem; margin-bottom: 12px; }
  .empty-state p { font-size: 0.9rem; }

  /* ===== CLIENTS ===== */
  .client-list-manage {
    display: flex;
    flex-direction: column;
    gap: 10px;
    margin-bottom: 24px;
  }
  .client-manage-item {
    background: var(--white);
    border: 1px solid var(--line);
    border-radius: 8px;
    padding: 12px 18px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .client-manage-item span { font-weight: 500; }
  .client-manage-item button {
    background: none;
    border: none;
    cursor: pointer;
    color: var(--muted);
    font-size: 1rem;
    transition: color 0.2s;
  }
  .client-manage-item button:hover { color: var(--accent); }

  .add-client-row {
    display: flex;
    gap: 10px;
  }
  .add-client-row input {
    flex: 1;
    padding: 10px 14px;
    border: 1px solid var(--line);
    border-radius: 6px;
    background: var(--paper);
    font-family: 'DM Sans', sans-serif;
    font-size: 0.9rem;
  }

  @media (max-width: 600px) {
    .form-row, .form-row.thirds { grid-template-columns: 1fr; }
    .rapport-summary { flex-wrap: wrap; gap: 16px; }
    .client-entry-row { grid-template-columns: 80px 80px 1fr; }
    header { flex-direction: column; align-items: flex-start; gap: 4px; }
    nav { padding: 12px 16px; flex-wrap: wrap; }
    .page { padding: 20px 16px; }
  }
</style>
</head>
<body>

<header>
  <div class="logo">Chrono<span>Voix</span></div>
  <div class="header-date" id="headerDate"></div>
</header>

<nav>
  <button class="tab active" onclick="showTab('saisie')">🎙 Saisie</button>
  <button class="tab" onclick="showTab('rapport')">📊 Rapport mensuel</button>
  <button class="tab" onclick="showTab('clients')">👥 Clients</button>
</nav>

<!-- PAGE SAISIE -->
<div class="page active" id="tab-saisie">
  <div class="voice-card">
    <div class="voice-btn-wrap">
      <button id="voiceBtn" onclick="toggleVoice()" title="Cliquer pour dicter">
        <svg width="36" height="36" viewBox="0 0 24 24" fill="none">
          <path d="M12 1C10.34 1 9 2.34 9 4V12C9 13.66 10.34 15 12 15C13.66 15 15 13.66 15 12V4C15 2.34 13.66 1 12 1ZM19 12C19 15.87 15.87 19 12 19C8.13 19 5 15.87 5 12H3C3 16.97 6.93 21.07 11.9 21.48V23H13.1V21.48C18.07 21.07 22 16.97 22 12H19Z" fill="#c8401a"/>
        </svg>
      </button>
      <div class="voice-status" id="voiceStatus">Appuyer pour dicter</div>
    </div>

    <div id="transcript" class="placeholder">Votre texte dicté apparaîtra ici…</div>

    <div class="hint-box">
      <strong>💡 Dites par exemple :</strong><br>
      « <em>Client Dupont, deux heures trente, réunion de suivi et mise à jour du dossier</em> »<br>
      « <em>Client Martin, une heure, appel téléphonique</em> »
    </div>

    <div class="form-row thirds">
      <div class="field">
        <label>Client</label>
        <select id="fieldClient">
          <option value="">— Choisir —</option>
        </select>
      </div>
      <div class="field">
        <label>Heures (ex: 1.5)</label>
        <input type="number" id="fieldHours" step="0.25" min="0.25" max="24" placeholder="0.00">
      </div>
      <div class="field">
        <label>Date</label>
        <input type="date" id="fieldDate">
      </div>
    </div>
    <div class="form-row">
      <div class="field" style="grid-column:1/-1">
        <label>Description du travail</label>
        <textarea id="fieldDesc" placeholder="Décrivez brièvement la tâche effectuée…"></textarea>
      </div>
    </div>
    <div class="btn-row">
      <button class="btn btn-secondary" onclick="clearForm()">Effacer</button>
      <button class="btn btn-primary" onclick="saveEntry()">✓ Enregistrer</button>
    </div>
  </div>

  <div class="section-title">
    Journée du <span id="todayLabel" style="font-style:italic;color:var(--muted);margin-left:6px;"></span>
    <span class="badge" id="todayCount">0 entrée</span>
  </div>
  <div class="entry-list" id="entryList">
    <div class="empty-state"><div class="icon">📋</div><p>Aucune entrée pour aujourd'hui</p></div>
  </div>
  <div class="day-total" id="dayTotal"></div>
</div>

<!-- PAGE RAPPORT -->
<div class="page" id="tab-rapport">
  <div class="month-selector">
    <select id="monthSelect"></select>
    <button onclick="genReport()">Générer le rapport</button>
    <button onclick="exportCSV()" style="background:var(--accent2);">⬇ CSV</button>
  </div>
  <div id="reportContent"></div>
</div>

<!-- PAGE CLIENTS -->
<div class="page" id="tab-clients">
  <div class="voice-card">
    <div class="section-title">Mes clients <span class="badge" id="clientCount">0</span></div>
    <div class="client-list-manage" id="clientListManage"></div>
    <div class="add-client-row">
      <input type="text" id="newClientInput" placeholder="Nom du nouveau client…" onkeydown="if(event.key==='Enter')addClient()">
      <button class="btn btn-primary" onclick="addClient()">+ Ajouter</button>
    </div>
  </div>
</div>

<script>
// ===================== STORAGE =====================
let entries = JSON.parse(localStorage.getItem('cv_entries') || '[]');
let clients = JSON.parse(localStorage.getItem('cv_clients') || '["Dupont","Martin","Durand"]');

function save() {
  localStorage.setItem('cv_entries', JSON.stringify(entries));
  localStorage.setItem('cv_clients', JSON.stringify(clients));
}

// ===================== INIT =====================
function init() {
  const now = new Date();
  document.getElementById('headerDate').textContent = now.toLocaleDateString('fr-FR', {weekday:'long',day:'numeric',month:'long',year:'numeric'});
  document.getElementById('fieldDate').value = toISO(now);
  document.getElementById('todayLabel').textContent = now.toLocaleDateString('fr-FR',{weekday:'long',day:'numeric',month:'long'});
  populateMonthSelect();
  renderClients();
  renderToday();
  renderClientDropdown();
}

function toISO(d) {
  return d.toISOString().split('T')[0];
}

// ===================== TABS =====================
function showTab(name) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
  document.getElementById('tab-' + name).classList.add('active');
  event.target.classList.add('active');
  if (name === 'rapport') genReport();
}

// ===================== VOICE =====================
let recognition = null;
let isListening = false;

function setupRecognition() {
  const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
  if (!SpeechRecognition) return null;
  const r = new SpeechRecognition();
  r.lang = 'fr-FR';
  r.continuous = false;
  r.interimResults = true;
  r.onresult = (e) => {
    const t = Array.from(e.results).map(r => r[0].transcript).join('');
    const el = document.getElementById('transcript');
    el.textContent = t;
    el.classList.remove('placeholder');
    if (e.results[e.results.length-1].isFinal) parseVoice(t);
  };
  r.onend = () => stopListening();
  r.onerror = (e) => { stopListening(); alert('Erreur micro: ' + e.error); };
  return r;
}

function toggleVoice() {
  if (!isListening) startListening(); else stopListening();
}

function startListening() {
  recognition = setupRecognition();
  if (!recognition) { alert("Votre navigateur ne supporte pas la reconnaissance vocale. Essayez Chrome."); return; }
  recognition.start();
  isListening = true;
  document.getElementById('voiceBtn').classList.add('listening');
  document.getElementById('voiceStatus').textContent = '● En écoute…';
  document.getElementById('voiceStatus').classList.add('active');
}

function stopListening() {
  if (recognition) { try { recognition.stop(); } catch(e){} }
  isListening = false;
  document.getElementById('voiceBtn').classList.remove('listening');
  document.getElementById('voiceStatus').textContent = 'Appuyer pour dicter';
  document.getElementById('voiceStatus').classList.remove('active');
}

// ===================== VOICE PARSING =====================
const NUM_WORDS = {
  'zéro':0,'un':1,'une':1,'deux':2,'trois':3,'quatre':4,'cinq':5,'six':6,'sept':7,
  'huit':8,'neuf':9,'dix':10,'onze':11,'douze':12,'treize':13,'quatorze':14,'quinze':15,
  'seize':16,'dix-sept':17,'dixsept':17,'dix-huit':18,'dixhuit':18,'dix-neuf':19,'dixneuf':19,
  'vingt':20,'trente':30,'quarante':40,'cinquante':50
};
const FRAC_WORDS = {'demi':0.5,'demi-heure':0.5,'quart':0.25,'trois quarts':0.75,'trentième':0.5};

function parseVoice(text) {
  const lower = text.toLowerCase().trim();

  // Find client
  let foundClient = '';
  for (const c of clients) {
    if (lower.includes(c.toLowerCase())) {
      foundClient = c;
      break;
    }
  }

  // Find hours
  let hours = 0;
  // Numeric: "2.5", "2h30", "1,5"
  let m = lower.match(/(\d+)[h:](\d{2})/);
  if (m) hours = parseInt(m[1]) + parseInt(m[2])/60;
  else {
    m = lower.match(/(\d+[.,]\d+)\s*heure/);
    if (m) hours = parseFloat(m[1].replace(',','.'));
    else {
      m = lower.match(/(\d+)\s*heure/);
      if (m) hours = parseInt(m[1]);
    }
  }
  // Word numbers
  if (hours === 0) {
    for (const [word, val] of Object.entries(NUM_WORDS)) {
      const re = new RegExp('\\b' + word + '\\b.{0,20}heure', 'i');
      if (re.test(lower)) { hours = val; break; }
    }
  }
  // Fractions
  for (const [word, val] of Object.entries(FRAC_WORDS)) {
    if (lower.includes(word)) { hours += val; break; }
  }
  if (hours === 0 && lower.includes('demi')) hours += 0.5;
  if (hours === 0 && lower.includes('quart')) hours += 0.25;

  // Description: remove client and hours hints
  let desc = text;
  if (foundClient) desc = desc.replace(new RegExp(foundClient, 'i'), '');
  desc = desc.replace(/client\s*/i,'').replace(/[\d]+[h:]\d{2}/,'').replace(/[\d.,]+\s*heure[s]?/i,'');
  desc = desc.replace(/\b(un|une|deux|trois|quatre|cinq|six|sept|huit|neuf|dix)\b\s*heure[s]?/gi,'');
  desc = desc.replace(/demi[-\s]?heure/gi,'').replace(/\bquart\b/gi,'');
  desc = desc.replace(/,\s*,/g,',').replace(/\s{2,}/g,' ').trim();
  desc = desc.replace(/^[,\s]+|[,\s]+$/g,'').trim();

  if (foundClient) document.getElementById('fieldClient').value = foundClient;
  if (hours > 0) document.getElementById('fieldHours').value = hours.toFixed(2);
  if (desc) document.getElementById('fieldDesc').value = desc;
}

// ===================== ENTRIES =====================
function saveEntry() {
  const client = document.getElementById('fieldClient').value;
  const hours = parseFloat(document.getElementById('fieldHours').value);
  const date = document.getElementById('fieldDate').value;
  const desc = document.getElementById('fieldDesc').value.trim();
  if (!client) { alert('Veuillez sélectionner un client.'); return; }
  if (!hours || hours <= 0) { alert('Veuillez indiquer un nombre d\'heures valide.'); return; }
  if (!date) { alert('Veuillez indiquer une date.'); return; }

  entries.push({ id: Date.now(), client, hours, date, desc, createdAt: new Date().toISOString() });
  save();
  clearForm();
  renderToday();
  document.getElementById('transcript').textContent = 'Entrée enregistrée avec succès ✓';
  document.getElementById('transcript').classList.remove('placeholder');
  setTimeout(() => {
    document.getElementById('transcript').textContent = 'Votre texte dicté apparaîtra ici…';
    document.getElementById('transcript').classList.add('placeholder');
  }, 2000);
}

function clearForm() {
  document.getElementById('fieldClient').value = '';
  document.getElementById('fieldHours').value = '';
  document.getElementById('fieldDesc').value = '';
  document.getElementById('fieldDate').value = toISO(new Date());
  document.getElementById('transcript').textContent = 'Votre texte dicté apparaîtra ici…';
  document.getElementById('transcript').classList.add('placeholder');
}

function deleteEntry(id) {
  if (!confirm('Supprimer cette entrée ?')) return;
  entries = entries.filter(e => e.id !== id);
  save();
  renderToday();
}

function renderToday() {
  const today = toISO(new Date());
  const todayEntries = entries.filter(e => e.date === today);
  const list = document.getElementById('entryList');
  const count = document.getElementById('todayCount');
  const total = document.getElementById('dayTotal');

  count.textContent = todayEntries.length + (todayEntries.length > 1 ? ' entrées' : ' entrée');

  if (todayEntries.length === 0) {
    list.innerHTML = '<div class="empty-state"><div class="icon">📋</div><p>Aucune entrée pour aujourd\'hui</p></div>';
    total.innerHTML = '';
    return;
  }

  list.innerHTML = todayEntries.map(e => `
    <div class="entry-item">
      <div class="entry-time">${new Date(e.createdAt).toLocaleTimeString('fr-FR',{hour:'2-digit',minute:'2-digit'})}</div>
      <div class="entry-client">${e.client}</div>
      <div class="entry-hours">${formatH(e.hours)}</div>
      <div class="entry-desc">${e.desc || '<em style="color:var(--muted)">Sans description</em>'}</div>
      <button class="entry-del" onclick="deleteEntry(${e.id})" title="Supprimer">✕</button>
    </div>
  `).join('');

  const sum = todayEntries.reduce((a,e) => a + e.hours, 0);
  total.innerHTML = `Total du jour : <strong>${formatH(sum)}</strong>`;
}

function formatH(h) {
  const hh = Math.floor(h);
  const mm = Math.round((h - hh) * 60);
  return mm ? `${hh}h${mm.toString().padStart(2,'0')}` : `${hh}h`;
}

// ===================== RAPPORT =====================
function populateMonthSelect() {
  const sel = document.getElementById('monthSelect');
  const now = new Date();
  for (let i = 0; i < 12; i++) {
    const d = new Date(now.getFullYear(), now.getMonth() - i, 1);
    const val = `${d.getFullYear()}-${String(d.getMonth()+1).padStart(2,'0')}`;
    const label = d.toLocaleDateString('fr-FR', {month:'long', year:'numeric'});
    sel.innerHTML += `<option value="${val}" ${i===0?'selected':''}>${label.charAt(0).toUpperCase()+label.slice(1)}</option>`;
  }
}

function genReport() {
  const ym = document.getElementById('monthSelect').value;
  const [yr, mo] = ym.split('-').map(Number);
  const monthEntries = entries.filter(e => {
    const d = new Date(e.date);
    return d.getFullYear() === yr && d.getMonth()+1 === mo;
  });

  const el = document.getElementById('reportContent');

  if (monthEntries.length === 0) {
    el.innerHTML = '<div class="empty-state"><div class="icon">📭</div><p>Aucune entrée pour ce mois</p></div>';
    return;
  }

  // Group by client
  const byClient = {};
  for (const e of monthEntries) {
    if (!byClient[e.client]) byClient[e.client] = [];
    byClient[e.client].push(e);
  }

  const totalH = monthEntries.reduce((a,e) => a+e.hours, 0);
  const nbClients = Object.keys(byClient).length;

  let html = `
    <div class="rapport-summary">
      <div class="sum-item"><span class="sum-label">Total heures</span><span class="sum-value">${formatH(totalH)}</span></div>
      <div class="sum-item"><span class="sum-label">Clients</span><span class="sum-value">${nbClients}</span></div>
      <div class="sum-item"><span class="sum-label">Entrées</span><span class="sum-value">${monthEntries.length}</span></div>
    </div>
  `;

  for (const [client, ces] of Object.entries(byClient)) {
    const clientTotal = ces.reduce((a,e)=>a+e.hours,0);
    ces.sort((a,b) => a.date.localeCompare(b.date));
    html += `
      <div class="client-block">
        <div class="client-header">
          <h3>${client}</h3>
          <span class="client-total">${formatH(clientTotal)}</span>
        </div>
        <div class="client-entries">
          ${ces.map(e => `
            <div class="client-entry-row">
              <span class="col-date">${new Date(e.date+'T12:00:00').toLocaleDateString('fr-FR',{day:'2-digit',month:'2-digit'})}</span>
              <span class="col-h">${formatH(e.hours)}</span>
              <span class="col-desc">${e.desc || '—'}</span>
            </div>
          `).join('')}
        </div>
      </div>
    `;
  }

  el.innerHTML = html;
}

function exportCSV() {
  const ym = document.getElementById('monthSelect').value;
  const [yr, mo] = ym.split('-').map(Number);
  const monthEntries = entries.filter(e => {
    const d = new Date(e.date);
    return d.getFullYear() === yr && d.getMonth()+1 === mo;
  });
  if (monthEntries.length === 0) { alert('Aucune donnée pour ce mois.'); return; }
  const rows = [['Date','Client','Heures','Description']];
  monthEntries.sort((a,b)=>a.date.localeCompare(b.date)).forEach(e => {
    rows.push([e.date, e.client, e.hours.toFixed(2), e.desc]);
  });
  const csv = rows.map(r => r.map(c => `"${String(c).replace(/"/g,'""')}"`).join(';')).join('\n');
  const blob = new Blob(['\uFEFF'+csv], {type:'text/csv;charset=utf-8;'});
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url; a.download = `rapport_${ym}.csv`; a.click();
}

// ===================== CLIENTS =====================
function renderClients() {
  const el = document.getElementById('clientListManage');
  document.getElementById('clientCount').textContent = clients.length;
  if (clients.length === 0) {
    el.innerHTML = '<div style="color:var(--muted);font-size:0.85rem;padding:8px 0;">Aucun client. Ajoutez-en ci-dessous.</div>';
    return;
  }
  el.innerHTML = clients.map((c,i) => `
    <div class="client-manage-item">
      <span>${c}</span>
      <button onclick="deleteClient(${i})" title="Supprimer">✕</button>
    </div>
  `).join('');
  renderClientDropdown();
}

function renderClientDropdown() {
  const sel = document.getElementById('fieldClient');
  const cur = sel.value;
  sel.innerHTML = '<option value="">— Choisir —</option>';
  clients.forEach(c => {
    const opt = document.createElement('option');
    opt.value = c; opt.textContent = c;
    sel.appendChild(opt);
  });
  if (cur) sel.value = cur;
}

function addClient() {
  const input = document.getElementById('newClientInput');
  const name = input.value.trim();
  if (!name) return;
  if (clients.includes(name)) { alert('Ce client existe déjà.'); return; }
  clients.push(name);
  save();
  input.value = '';
  renderClients();
}

function deleteClient(i) {
  if (!confirm(`Supprimer le client "${clients[i]}" ? Ses entrées ne seront pas supprimées.`)) return;
  clients.splice(i, 1);
  save();
  renderClients();
}

init();
</script>
</body>
</html>
