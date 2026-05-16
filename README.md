<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>UniMind — One Chat. All AI. One Platform.</title>
<meta name="description" content="UniMind unites all your AI assistants in one smart group chat. Pick your specialists, ask once, get expert answers instantly — no switching, no copy-pasting. One platform. Infinite intelligence.">
<meta property="og:title" content="UniMind — One Chat. All AI.">
<meta property="og:description" content="UniMind unites all your AI assistants in one smart group chat. Try it free!">
<meta name="twitter:card" content="summary_large_image">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Clash+Display:wght@400;500;600;700&family=Plus+Jakarta+Sans:ital,wght@0,300;0,400;0,500;0,600;1,300&display=swap" rel="stylesheet">
<style>
/* ═══════════════════════════════════════════
   TOKENS
═══════════════════════════════════════════ */
:root {
  --ink:       #0f1117;
  --ink-soft:  #1e2433;
  --ink-mute:  #3a4259;
  --fog:       #8492b0;
  --mist:      #b8c4d8;
  --cloud:     #e8edf5;
  --snow:      #f4f7fc;
  --white:     #ffffff;

  --blue:      #2563eb;
  --blue-lt:   #3b7ff5;
  --blue-pale: #dbeafe;
  --indigo:    #4f46e5;
  --teal:      #0d9488;
  --emerald:   #059669;
  --amber:     #d97706;
  --rose:      #e11d48;
  --violet:    #7c3aed;
  --cyan:      #0891b2;
  --pink:      #db2777;

  --r: 14px;
  --r-lg: 20px;
  --r-xl: 28px;
  --shadow-sm: 0 1px 3px rgba(15,17,23,0.08), 0 1px 2px rgba(15,17,23,0.05);
  --shadow:    0 4px 16px rgba(15,17,23,0.1),  0 2px 6px rgba(15,17,23,0.06);
  --shadow-lg: 0 12px 40px rgba(15,17,23,0.14), 0 4px 12px rgba(15,17,23,0.08);
  --shadow-xl: 0 24px 64px rgba(15,17,23,0.18), 0 8px 24px rgba(15,17,23,0.1);
}

/* ═══════════════════════════════════════════
   RESET & BASE
═══════════════════════════════════════════ */
*,*::before,*::after { box-sizing:border-box; margin:0; padding:0; }
html { scroll-behavior: smooth; }
body {
  font-family: 'Plus Jakarta Sans', sans-serif;
  background: var(--snow);
  color: var(--ink);
  min-height: 100vh;
  overflow-x: hidden;
  -webkit-font-smoothing: antialiased;
}

/* ═══════════════════════════════════════════
   BACKGROUND — soft airy gradient
═══════════════════════════════════════════ */
body::before {
  content: '';
  position: fixed; inset: 0; z-index: 0; pointer-events: none;
  background:
    radial-gradient(ellipse 60% 50% at 0% 0%,   rgba(37,99,235,0.06) 0%, transparent 65%),
    radial-gradient(ellipse 50% 40% at 100% 80%, rgba(79,70,229,0.05) 0%, transparent 60%),
    radial-gradient(ellipse 40% 30% at 50% 50%,  rgba(13,148,136,0.03) 0%, transparent 55%);
}

/* ═══════════════════════════════════════════
   NAV
═══════════════════════════════════════════ */
nav {
  position: sticky; top: 0; z-index: 200;
  display: flex; align-items: center; justify-content: space-between;
  padding: 0 32px; height: 64px;
  background: rgba(255,255,255,0.9);
  backdrop-filter: blur(20px);
  border-bottom: 1px solid var(--cloud);
  box-shadow: var(--shadow-sm);
}

.nav-logo { display: flex; align-items: center; gap: 10px; text-decoration: none; }
.nav-wordmark {
  font-family: 'Clash Display', sans-serif;
  font-weight: 700; font-size: 21px; letter-spacing: -0.5px;
  background: linear-gradient(135deg, var(--blue) 0%, var(--indigo) 100%);
  -webkit-background-clip: text; -webkit-text-fill-color: transparent;
}
.nav-pill {
  font-size: 10px; font-weight: 600; letter-spacing: 1px; text-transform: uppercase;
  padding: 3px 8px; border-radius: 6px;
  background: var(--blue-pale); color: var(--blue);
  -webkit-text-fill-color: var(--blue);
}

.nav-share-btn {
  display: flex; align-items: center; gap: 8px;
  background: var(--blue); color: white;
  border: none; border-radius: var(--r); padding: 9px 20px;
  font-family: 'Plus Jakarta Sans', sans-serif;
  font-size: 13px; font-weight: 600; cursor: pointer;
  transition: all 0.2s; box-shadow: 0 2px 12px rgba(37,99,235,0.3);
}
.nav-share-btn:hover { background: var(--blue-lt); transform: translateY(-1px); box-shadow: 0 4px 20px rgba(37,99,235,0.4); }

/* ═══════════════════════════════════════════
   HERO
═══════════════════════════════════════════ */
.hero {
  position: relative; z-index: 1;
  max-width: 780px; margin: 0 auto;
  padding: 64px 24px 48px;
  text-align: center;
}

.hero-eyebrow {
  display: inline-flex; align-items: center; gap: 8px;
  font-size: 12px; font-weight: 600; letter-spacing: 0.5px;
  color: var(--blue); background: var(--blue-pale);
  padding: 6px 16px; border-radius: 20px; margin-bottom: 24px;
  animation: riseIn 0.5s ease both;
}
.eyebrow-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--emerald); box-shadow: 0 0 6px var(--emerald); }

.hero h1 {
  font-family: 'Clash Display', sans-serif;
  font-size: clamp(34px, 5.5vw, 64px);
  font-weight: 700; line-height: 1.08; letter-spacing: -1.5px;
  color: var(--ink); margin-bottom: 20px;
  animation: riseIn 0.5s 0.08s ease both;
}
.hero h1 em {
  font-style: normal;
  background: linear-gradient(135deg, var(--blue) 0%, var(--indigo) 60%, var(--teal) 100%);
  -webkit-background-clip: text; -webkit-text-fill-color: transparent;
}

/* ═══════════════════════════════════════════
   300-CHAR DESCRIPTION
═══════════════════════════════════════════ */
.hero-desc {
  font-size: 17px; color: var(--fog); line-height: 1.7; font-weight: 400;
  max-width: 560px; margin: 0 auto 36px;
  animation: riseIn 0.5s 0.16s ease both;
}
.hero-desc strong { color: var(--ink-mute); font-weight: 600; }

/* ═══════════════════════════════════════════
   SHARE STRIP
═══════════════════════════════════════════ */
.share-strip {
  position: relative; z-index: 1;
  max-width: 880px; margin: 0 auto 36px; padding: 0 20px;
  animation: riseIn 0.5s 0.22s ease both;
}
.share-inner {
  background: white; border: 1px solid var(--cloud); border-radius: var(--r-lg);
  padding: 16px 20px; display: flex; align-items: center; gap: 14px; flex-wrap: wrap;
  box-shadow: var(--shadow-sm);
}
.share-label {
  font-size: 12px; font-weight: 700; color: var(--ink-mute);
  white-space: nowrap; display: flex; align-items: center; gap: 6px;
}
.share-btns { display: flex; gap: 7px; flex-wrap: wrap; flex: 1; }
.sbtn {
  display: flex; align-items: center; gap: 6px;
  padding: 7px 14px; border-radius: 10px; border: 1px solid var(--cloud);
  background: var(--snow); color: var(--ink-mute);
  font-family: 'Plus Jakarta Sans', sans-serif;
  font-size: 12px; font-weight: 500; cursor: pointer; transition: all 0.16s;
  white-space: nowrap; text-decoration: none;
}
.sbtn:hover { background: white; border-color: var(--mist); box-shadow: var(--shadow-sm); transform: translateY(-1px); }
.sbtn.s-wa:hover  { background: #f0fdf4; border-color: #86efac; color: #16a34a; }
.sbtn.s-tg:hover  { background: #eff6ff; border-color: #93c5fd; color: #2563eb; }
.sbtn.s-tw:hover  { background: #f8fafc; border-color: #cbd5e1; color: #0f172a; }
.sbtn.s-fb:hover  { background: #eff6ff; border-color: #93c5fd; color: #1d4ed8; }
.sbtn.s-li:hover  { background: #eff6ff; border-color: #93c5fd; color: #1d4ed8; }
.sbtn.s-cp:hover  { background: #eff6ff; border-color: #93c5fd; color: var(--blue); }
.sbtn.copied { background: #f0fdf4; border-color: #86efac; color: #16a34a; }

/* ═══════════════════════════════════════════
   HOW IT WORKS — 3 steps
═══════════════════════════════════════════ */
.steps {
  position: relative; z-index: 1;
  max-width: 880px; margin: 0 auto 36px; padding: 0 20px;
  display: grid; grid-template-columns: repeat(3,1fr); gap: 12px;
  animation: riseIn 0.5s 0.28s ease both;
}
.step-card {
  background: white; border: 1px solid var(--cloud); border-radius: var(--r-lg);
  padding: 20px; box-shadow: var(--shadow-sm); text-align: center;
}
.step-num {
  width: 36px; height: 36px; border-radius: 50%; display: flex; align-items: center; justify-content: center;
  font-family: 'Clash Display', sans-serif; font-weight: 700; font-size: 15px;
  background: var(--blue-pale); color: var(--blue); margin: 0 auto 12px;
}
.step-icon { font-size: 26px; margin-bottom: 8px; }
.step-title { font-weight: 700; font-size: 14px; color: var(--ink); margin-bottom: 5px; }
.step-desc  { font-size: 12px; color: var(--fog); line-height: 1.55; }

/* ═══════════════════════════════════════════
   MAIN APP LAYOUT
═══════════════════════════════════════════ */
.app {
  position: relative; z-index: 1;
  max-width: 1100px; margin: 0 auto; padding: 0 20px 80px;
  display: grid; grid-template-columns: 256px 1fr; gap: 16px;
  animation: riseIn 0.6s 0.34s ease both;
}

/* ═══════════════════════════════════════════
   SIDEBAR — AGENT LIBRARY
═══════════════════════════════════════════ */
.sidebar { display: flex; flex-direction: column; gap: 8px; }

.sidebar-header {
  background: white; border: 1px solid var(--cloud); border-radius: var(--r-lg);
  padding: 14px 16px; box-shadow: var(--shadow-sm); margin-bottom: 2px;
}
.sidebar-title {
  font-family: 'Clash Display', sans-serif; font-weight: 700; font-size: 14px;
  color: var(--ink); margin-bottom: 4px;
}
.sidebar-hint { font-size: 11.5px; color: var(--fog); line-height: 1.5; }

.agent-card {
  background: white; border: 1.5px solid var(--cloud); border-radius: var(--r-lg);
  padding: 14px 16px; cursor: pointer; transition: all 0.18s; user-select: none;
  position: relative; overflow: hidden; box-shadow: var(--shadow-sm);
}
.agent-card:hover {
  border-color: var(--mist); box-shadow: var(--shadow); transform: translateY(-2px);
}
.agent-card.active {
  border-color: var(--agent-color, var(--blue));
  background: linear-gradient(135deg, rgba(37,99,235,0.03), rgba(79,70,229,0.03));
  box-shadow: 0 0 0 3px rgba(37,99,235,0.08), var(--shadow);
}
.agent-card.dragging { opacity: 0.4; transform: scale(0.97); }

.agent-row { display: flex; align-items: center; gap: 10px; }
.agent-icon {
  width: 36px; height: 36px; border-radius: 10px;
  display: flex; align-items: center; justify-content: center;
  font-size: 18px; flex-shrink: 0;
  background: var(--agent-bg); border: 1px solid var(--agent-border);
}
.agent-info { flex: 1; min-width: 0; }
.agent-name { font-weight: 700; font-size: 13px; color: var(--ink); margin-bottom: 2px; }
.agent-specialty { font-size: 11px; color: var(--fog); line-height: 1.4; }
.agent-badge {
  font-size: 9px; font-weight: 700; padding: 2px 7px; border-radius: 6px;
  background: #dcfce7; color: #16a34a; letter-spacing: 0.5px; flex-shrink: 0;
}
.agent-card.active .agent-badge { background: var(--blue-pale); color: var(--blue); }
.agent-card.active .agent-badge::before { content: '✓ '; }

/* ═══════════════════════════════════════════
   WORKSPACE
═══════════════════════════════════════════ */
.workspace { display: flex; flex-direction: column; gap: 14px; }

/* ── ACTIVE TEAM BAR ── */
.team-bar {
  background: white; border: 1.5px dashed var(--mist); border-radius: var(--r-lg);
  padding: 16px 20px; transition: all 0.2s; min-height: 74px;
  box-shadow: var(--shadow-sm);
}
.team-bar.drag-over { border-color: var(--blue); background: var(--blue-pale); }
.team-bar-top {
  display: flex; align-items: center; justify-content: space-between; margin-bottom: 12px;
}
.team-bar-label {
  font-size: 12px; font-weight: 700; color: var(--ink-mute); letter-spacing: 0.3px;
  display: flex; align-items: center; gap: 7px;
}
.team-count {
  display: inline-flex; align-items: center; justify-content: center;
  width: 20px; height: 20px; border-radius: 50%;
  background: var(--blue); color: white; font-size: 10px; font-weight: 700;
}
.team-clear {
  font-size: 11px; color: var(--fog); background: none; border: none;
  cursor: pointer; padding: 3px 8px; border-radius: 6px; transition: all 0.15s;
  font-family: 'Plus Jakarta Sans', sans-serif;
}
.team-clear:hover { background: #fff1f2; color: var(--rose); }

.team-chips { display: flex; flex-wrap: wrap; gap: 7px; }
.team-empty {
  display: flex; align-items: center; gap: 8px;
  color: var(--fog); font-size: 13px; padding: 4px 0;
}
.team-empty-icon { font-size: 18px; }

.chip {
  display: flex; align-items: center; gap: 6px;
  background: white; border: 1.5px solid var(--cloud);
  border-radius: 24px; padding: 5px 10px 5px 8px;
  font-size: 12px; font-weight: 600; animation: popIn 0.28s cubic-bezier(0.34,1.56,0.64,1);
  box-shadow: var(--shadow-sm);
}
.chip-x {
  width: 16px; height: 16px; border-radius: 50%;
  background: var(--cloud); border: none; color: var(--fog);
  cursor: pointer; font-size: 9px; display: flex; align-items: center; justify-content: center;
  transition: all 0.15s; margin-left: 1px;
}
.chip-x:hover { background: #fee2e2; color: var(--rose); }

/* ── WORKFLOW ── */
.workflow-bar {
  background: white; border: 1px solid var(--cloud); border-radius: var(--r);
  padding: 12px 18px; display: none; box-shadow: var(--shadow-sm);
}
.wf-label { font-size: 11px; font-weight: 700; color: var(--fog); letter-spacing: 1px; text-transform: uppercase; margin-bottom: 9px; }
.wf-row { display: flex; align-items: center; flex-wrap: wrap; gap: 6px; }
.wf-node {
  display: flex; align-items: center; gap: 5px;
  background: var(--snow); border: 1px solid var(--cloud); border-radius: 8px;
  padding: 5px 12px; font-size: 11.5px; color: var(--ink-mute); font-weight: 500;
}
.wf-arrow { color: var(--mist); font-size: 12px; }

/* ═══════════════════════════════════════════
   CHAT PANEL — THE MAIN EVENT
═══════════════════════════════════════════ */
.chat-panel {
  background: white; border: 1px solid var(--cloud); border-radius: var(--r-xl);
  overflow: hidden; display: flex; flex-direction: column;
  min-height: 500px; box-shadow: var(--shadow-lg); flex: 1;
}

/* Chat Header */
.chat-head {
  padding: 16px 20px; border-bottom: 1px solid var(--cloud);
  display: flex; align-items: center; justify-content: space-between;
  background: white;
}
.chat-head-left { display: flex; align-items: center; gap: 10px; }
.chat-head-icon {
  width: 38px; height: 38px; border-radius: 12px;
  background: linear-gradient(135deg, var(--blue), var(--indigo));
  display: flex; align-items: center; justify-content: center;
  box-shadow: 0 2px 10px rgba(37,99,235,0.3);
}
.chat-head-title { font-family: 'Clash Display', sans-serif; font-weight: 700; font-size: 15px; color: var(--ink); }
.chat-head-sub { font-size: 11.5px; color: var(--fog); margin-top: 1px; }
.live-badge {
  display: flex; align-items: center; gap: 5px;
  background: #f0fdf4; border: 1px solid #bbf7d0; border-radius: 8px;
  padding: 4px 10px; font-size: 11px; font-weight: 600; color: #16a34a;
}
.live-dot { width: 6px; height: 6px; border-radius: 50%; background: #16a34a; animation: pulse 2s infinite; }

/* Messages */
.messages {
  flex: 1; overflow-y: auto; padding: 20px 20px 8px;
  display: flex; flex-direction: column; gap: 16px; scroll-behavior: smooth;
}
.messages::-webkit-scrollbar { width: 4px; }
.messages::-webkit-scrollbar-track { background: transparent; }
.messages::-webkit-scrollbar-thumb { background: var(--cloud); border-radius: 4px; }

/* User message */
.msg-user { display: flex; justify-content: flex-end; animation: riseIn 0.3s ease; }
.msg-user-bub {
  max-width: 75%; background: linear-gradient(135deg, var(--blue), var(--indigo));
  color: white; padding: 12px 16px; border-radius: 18px 18px 4px 18px;
  font-size: 14px; line-height: 1.6; box-shadow: 0 2px 12px rgba(37,99,235,0.25);
}

/* Agent message */
.msg-agent { display: flex; gap: 10px; align-items: flex-start; animation: riseIn 0.3s ease; }
.msg-agent-av {
  width: 36px; height: 36px; border-radius: 11px; flex-shrink: 0;
  display: flex; align-items: center; justify-content: center; font-size: 17px;
  border: 1.5px solid var(--cloud); background: var(--snow);
  box-shadow: var(--shadow-sm);
}
.msg-agent-body { flex: 1; max-width: calc(100% - 46px); }
.msg-agent-meta {
  display: flex; align-items: center; gap: 8px; margin-bottom: 6px;
}
.msg-agent-name { font-weight: 700; font-size: 12px; color: var(--ink-mute); }
.msg-agent-time { font-size: 10px; color: var(--mist); }
.msg-agent-bub {
  background: var(--snow); border: 1px solid var(--cloud);
  padding: 13px 16px; border-radius: 4px 18px 18px 18px;
  font-size: 13.5px; line-height: 1.65; color: var(--ink);
  box-shadow: var(--shadow-sm);
}
.msg-agent-bub strong { color: var(--blue); font-weight: 700; }
.msg-agent-bub em { color: var(--ink-mute); }
.msg-agent-bub ul { margin: 8px 0 0 18px; }
.msg-agent-bub li { margin-bottom: 4px; }

/* Share response */
.msg-share-row { display: flex; gap: 7px; margin-top: 7px; flex-wrap: wrap; }
.msg-action-btn {
  display: flex; align-items: center; gap: 5px;
  background: none; border: 1px solid var(--cloud); border-radius: 8px;
  padding: 4px 10px; color: var(--fog); font-size: 11px; font-weight: 500;
  cursor: pointer; transition: all 0.15s; font-family: 'Plus Jakarta Sans', sans-serif;
}
.msg-action-btn:hover { background: white; border-color: var(--mist); color: var(--ink-mute); box-shadow: var(--shadow-sm); }

/* System / divider */
.msg-sys {
  text-align: center; font-size: 11px; color: var(--mist);
  display: flex; align-items: center; gap: 10px;
  animation: riseIn 0.3s ease;
}
.msg-sys::before,.msg-sys::after { content:''; flex:1; height:1px; background: var(--cloud); }

/* Typing */
.typing-row { display: flex; gap: 10px; align-items: flex-start; animation: riseIn 0.25s ease; }
.typing-bub {
  background: var(--snow); border: 1px solid var(--cloud);
  padding: 12px 16px; border-radius: 4px 18px 18px 18px;
  display: flex; align-items: center; gap: 9px; box-shadow: var(--shadow-sm);
}
.typing-lbl { font-size: 12px; color: var(--fog); font-weight: 500; }
.dots-wrap { display: flex; gap: 4px; }
.dot { width: 5px; height: 5px; border-radius: 50%; background: var(--blue); animation: bounce 1.1s infinite; }
.dot:nth-child(2){animation-delay:.18s}
.dot:nth-child(3){animation-delay:.36s}

/* ═══════════════════════════════════════════
   INPUT AREA — REDESIGNED
═══════════════════════════════════════════ */
.input-area {
  padding: 16px 20px 20px; border-top: 1px solid var(--cloud); background: white;
}

/* No-agent warning */
.no-agent-tip {
  display: flex; align-items: center; gap: 10px; margin-bottom: 12px;
  background: #fffbeb; border: 1px solid #fde68a; border-radius: var(--r);
  padding: 10px 14px; font-size: 12.5px; color: #92400e; font-weight: 500;
  transition: all 0.3s;
}
.no-agent-tip.hidden { display: none; }

/* Quick prompts */
.quick-prompts { display: flex; gap: 7px; margin-bottom: 12px; flex-wrap: wrap; }
.qp {
  display: flex; align-items: center; gap: 6px;
  background: var(--snow); border: 1px solid var(--cloud); border-radius: 20px;
  padding: 6px 13px; font-size: 12px; color: var(--ink-mute); font-weight: 500;
  cursor: pointer; transition: all 0.16s; font-family: 'Plus Jakarta Sans', sans-serif;
}
.qp:hover { background: white; border-color: var(--blue); color: var(--blue); box-shadow: var(--shadow-sm); }

/* Input box */
.input-box {
  display: flex; gap: 10px; align-items: flex-end;
  background: var(--snow); border: 1.5px solid var(--cloud); border-radius: 18px;
  padding: 6px 6px 6px 16px; transition: all 0.2s;
}
.input-box:focus-within {
  border-color: var(--blue); background: white;
  box-shadow: 0 0 0 4px rgba(37,99,235,0.08);
}
.chat-textarea {
  flex: 1; background: none; border: none; outline: none;
  font-family: 'Plus Jakarta Sans', sans-serif; font-size: 14px; color: var(--ink);
  resize: none; min-height: 40px; max-height: 120px; line-height: 1.55; padding: 8px 0;
}
.chat-textarea::placeholder { color: var(--mist); }

.input-actions { display: flex; align-items: flex-end; gap: 6px; padding-bottom: 4px; }
.send-btn {
  width: 40px; height: 40px; border-radius: 13px; flex-shrink: 0;
  background: linear-gradient(135deg, var(--blue), var(--indigo));
  border: none; cursor: pointer;
  display: flex; align-items: center; justify-content: center;
  font-size: 16px; color: white; transition: all 0.18s;
  box-shadow: 0 2px 10px rgba(37,99,235,0.35);
}
.send-btn:hover { transform: scale(1.06); box-shadow: 0 4px 18px rgba(37,99,235,0.45); }
.send-btn:active { transform: scale(0.96); }
.send-btn:disabled { opacity: 0.35; cursor: not-allowed; transform: none; box-shadow: none; }

.input-footer {
  display: flex; align-items: center; justify-content: space-between;
  margin-top: 9px; padding: 0 4px;
}
.input-hint-txt { font-size: 11px; color: var(--mist); }
.input-hint-txt kbd {
  background: var(--snow); border: 1px solid var(--cloud); border-radius: 4px;
  padding: 1px 5px; font-size: 10px; color: var(--fog);
}
.char-counter { font-size: 11px; color: var(--mist); }

/* ═══════════════════════════════════════════
   SHARE MODAL
═══════════════════════════════════════════ */
.overlay {
  position: fixed; inset: 0; z-index: 500;
  background: rgba(15,17,23,0.5); backdrop-filter: blur(8px);
  display: flex; align-items: center; justify-content: center; padding: 20px;
  opacity: 0; pointer-events: none; transition: opacity 0.22s;
}
.overlay.open { opacity: 1; pointer-events: all; }

.modal {
  background: white; border-radius: var(--r-xl); padding: 32px;
  max-width: 460px; width: 100%; position: relative;
  box-shadow: var(--shadow-xl);
  transform: scale(0.9) translateY(20px);
  transition: transform 0.28s cubic-bezier(0.34,1.3,0.64,1);
}
.overlay.open .modal { transform: scale(1) translateY(0); }

.modal-close {
  position: absolute; top: 16px; right: 16px;
  width: 32px; height: 32px; border-radius: 10px;
  background: var(--snow); border: 1px solid var(--cloud);
  cursor: pointer; font-size: 14px; color: var(--fog);
  display: flex; align-items: center; justify-content: center; transition: all 0.15s;
}
.modal-close:hover { background: #fff1f2; color: var(--rose); border-color: #fecaca; }

.modal-logo-row { display: flex; align-items: center; gap: 12px; margin-bottom: 6px; }
.modal-brand {
  font-family: 'Clash Display', sans-serif; font-weight: 700; font-size: 22px;
  background: linear-gradient(135deg, var(--blue), var(--indigo));
  -webkit-background-clip: text; -webkit-text-fill-color: transparent;
}
.modal-tagline { font-size: 13px; color: var(--fog); margin-bottom: 22px; }

.modal-url-bar {
  display: flex; gap: 8px; margin-bottom: 22px;
}
.modal-url-txt {
  flex: 1; background: var(--snow); border: 1px solid var(--cloud); border-radius: 10px;
  padding: 10px 14px; font-size: 12px; color: var(--fog); font-family: monospace;
  overflow: hidden; text-overflow: ellipsis; white-space: nowrap;
}
.modal-copy-btn {
  background: var(--blue); color: white; border: none; border-radius: 10px;
  padding: 10px 18px; font-family: 'Plus Jakarta Sans', sans-serif;
  font-size: 12px; font-weight: 700; cursor: pointer; transition: all 0.18s; white-space: nowrap;
}
.modal-copy-btn:hover { background: var(--blue-lt); box-shadow: 0 2px 12px rgba(37,99,235,0.35); }

.modal-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 8px; margin-bottom: 22px; }
.modal-btn {
  display: flex; align-items: center; gap: 11px;
  background: var(--snow); border: 1.5px solid var(--cloud); border-radius: var(--r-lg);
  padding: 13px 16px; cursor: pointer; transition: all 0.18s; text-decoration: none;
  font-family: 'Plus Jakarta Sans', sans-serif;
}
.modal-btn:hover { background: white; border-color: var(--mist); box-shadow: var(--shadow); transform: translateY(-2px); }
.modal-btn-icon { font-size: 22px; flex-shrink: 0; }
.modal-btn-name { font-weight: 700; font-size: 13px; color: var(--ink); }
.modal-btn-sub  { font-size: 10px; color: var(--fog); margin-top: 1px; }

.modal-footer { text-align: center; font-size: 11.5px; color: var(--fog); padding-top: 16px; border-top: 1px solid var(--cloud); }
.modal-footer strong { color: var(--ink-mute); }

/* ═══════════════════════════════════════════
   TOAST
═══════════════════════════════════════════ */
.toast {
  position: fixed; bottom: 28px; left: 50%;
  transform: translateX(-50%) translateY(16px);
  background: #f0fdf4; border: 1px solid #86efac; border-radius: 12px;
  padding: 12px 22px; font-size: 13px; font-weight: 600; color: #16a34a;
  z-index: 1000; opacity: 0; transition: all 0.24s;
  box-shadow: var(--shadow-lg); display: flex; align-items: center; gap: 8px;
}
.toast.show { opacity: 1; transform: translateX(-50%) translateY(0); }

/* FOOTER */
footer {
  position: relative; z-index: 1; text-align: center;
  padding: 28px; color: var(--fog); font-size: 12px;
  border-top: 1px solid var(--cloud); background: white;
}
footer a { color: var(--blue); text-decoration: none; font-weight: 600; }

/* ═══════════════════════════════════════════
   ANIMATIONS
═══════════════════════════════════════════ */
@keyframes riseIn   { from{opacity:0;transform:translateY(12px)} to{opacity:1;transform:translateY(0)} }
@keyframes popIn    { from{opacity:0;transform:scale(0.65)} to{opacity:1;transform:scale(1)} }
@keyframes bounce   { 0%,60%,100%{transform:translateY(0)} 30%{transform:translateY(-5px)} }
@keyframes pulse    { 0%,100%{opacity:1} 50%{opacity:0.4} }

/* ═══════════════════════════════════════════
   RESPONSIVE
═══════════════════════════════════════════ */
@media(max-width:780px){
  nav { padding: 0 16px; }
  .hero { padding: 48px 16px 36px; }
  .steps { grid-template-columns: 1fr; }
  .app { grid-template-columns: 1fr; padding: 0 14px 60px; }
  .sidebar { display: grid; grid-template-columns: 1fr 1fr; }
  .sidebar-header { grid-column: 1/-1; }
  .modal-grid { grid-template-columns: 1fr; }
  .hero h1 { letter-spacing: -1px; }
}
</style>
</head>
<body>

<!-- ═══════════════════ NAV ═══════════════════ -->
<nav>
  <a class="nav-logo" href="#">
    <svg width="32" height="32" viewBox="0 0 48 48" fill="none">
      <defs>
        <linearGradient id="g1" x1="0" y1="0" x2="48" y2="48" gradientUnits="userSpaceOnUse">
          <stop offset="0%"   stop-color="#2563eb"/>
          <stop offset="55%"  stop-color="#4f46e5"/>
          <stop offset="100%" stop-color="#0d9488"/>
        </linearGradient>
      </defs>
      <circle cx="24" cy="24" r="22" fill="rgba(37,99,235,0.08)" stroke="url(#g1)" stroke-width="1.5"/>
      <circle cx="24" cy="24" r="5"   fill="url(#g1)"/>
      <circle cx="24" cy="7"  r="3.2" fill="url(#g1)" opacity="0.85"/>
      <circle cx="39" cy="32" r="3.2" fill="url(#g1)" opacity="0.72"/>
      <circle cx="9"  cy="32" r="3.2" fill="url(#g1)" opacity="0.72"/>
      <line x1="24" y1="19" x2="24"  y2="10.2" stroke="url(#g1)" stroke-width="1.5" opacity="0.55"/>
      <line x1="28" y1="27" x2="36.2" y2="30"  stroke="url(#g1)" stroke-width="1.5" opacity="0.55"/>
      <line x1="20" y1="27" x2="11.8" y2="30"  stroke="url(#g1)" stroke-width="1.5" opacity="0.55"/>
      <circle cx="24" cy="24" r="15.5" stroke="url(#g1)" stroke-width="0.7" stroke-dasharray="2.5 4" opacity="0.3"/>
    </svg>
    <span class="nav-wordmark">UniMind</span>
    <span class="nav-pill">BETA</span>
  </a>
  <button class="nav-share-btn" onclick="openModal()">🚀 Share UniMind</button>
</nav>

<!-- ═══════════════════ HERO ═══════════════════ -->
<div class="hero">
  <div class="hero-eyebrow"><div class="eyebrow-dot"></div> Built by Mridul · Narayanganj, Bangladesh 🇧🇩</div>
  <h1>Stop juggling AI tools.<br><em>Let them work as a team.</em></h1>
  <!-- ★ 300-CHARACTER DESCRIPTION ★ -->
  <p class="hero-desc">
    UniMind brings all your AI specialists into <strong>one group chat</strong>. Pick your team — Writer, Coder, Researcher and more — ask once, and every AI contributes its best. <strong>No switching. No copy-pasting. Just results.</strong>
  </p>
</div>

<!-- ═══════════════════ SHARE STRIP ═══════════════════ -->
<div class="share-strip">
  <div class="share-inner">
    <div class="share-label">📢 Share free</div>
    <div class="share-btns">
      <button class="sbtn s-wa" onclick="goWA()">💬 WhatsApp</button>
      <button class="sbtn s-tg" onclick="goTG()">✈️ Telegram</button>
      <button class="sbtn s-tw" onclick="goTW()">𝕏 Twitter</button>
      <button class="sbtn s-fb" onclick="goFB()">👍 Facebook</button>
      <button class="sbtn s-li" onclick="goLI()">💼 LinkedIn</button>
      <button class="sbtn s-cp" id="cpBtn" onclick="copyLink(this)">🔗 Copy Link</button>
    </div>
  </div>
</div>

<!-- ═══════════════════ HOW IT WORKS ═══════════════════ -->
<div class="steps">
  <div class="step-card">
    <div class="step-icon">🤖</div>
    <div class="step-num">1</div>
    <div class="step-title">Pick your AI team</div>
    <div class="step-desc">Click any agent card on the left to add them to your active team. Mix and match specialists.</div>
  </div>
  <div class="step-card">
    <div class="step-icon">💬</div>
    <div class="step-num">2</div>
    <div class="step-title">Ask one question</div>
    <div class="step-desc">Type your question in the chat box below. Press Enter or tap Send — that's it.</div>
  </div>
  <div class="step-card">
    <div class="step-icon">✨</div>
    <div class="step-num">3</div>
    <div class="step-title">Get expert answers</div>
    <div class="step-desc">Each AI specialist replies with their own expertise. All in one place, no switching required.</div>
  </div>
</div>

<!-- ═══════════════════ APP ═══════════════════ -->
<div class="app">

  <!-- SIDEBAR -->
  <div class="sidebar">
    <div class="sidebar-header">
      <div class="sidebar-title">🤖 AI Agent Library</div>
      <div class="sidebar-hint">Tap any card to add it to your team. Tap again to remove.</div>
    </div>

    <div class="agent-card" draggable="true" data-id="writer"
      style="--agent-color:#2563eb;--agent-bg:#eff6ff;--agent-border:#bfdbfe">
      <div class="agent-row">
        <div class="agent-icon">✍️</div>
        <div class="agent-info">
          <div class="agent-name">Writer AI</div>
          <div class="agent-specialty">Blog posts, emails, scripts, stories</div>
        </div>
        <div class="agent-badge">READY</div>
      </div>
    </div>

    <div class="agent-card" draggable="true" data-id="coder"
      style="--agent-color:#059669;--agent-bg:#f0fdf4;--agent-border:#a7f3d0">
      <div class="agent-row">
        <div class="agent-icon">💻</div>
        <div class="agent-info">
          <div class="agent-name">Coder AI</div>
          <div class="agent-specialty">Python, JS, debugging, web dev</div>
        </div>
        <div class="agent-badge">READY</div>
      </div>
    </div>

    <div class="agent-card" draggable="true" data-id="researcher"
      style="--agent-color:#d97706;--agent-bg:#fffbeb;--agent-border:#fde68a">
      <div class="agent-row">
        <div class="agent-icon">🔍</div>
        <div class="agent-info">
          <div class="agent-name">Research AI</div>
          <div class="agent-specialty">Facts, market analysis, insights</div>
        </div>
        <div class="agent-badge">READY</div>
      </div>
    </div>

    <div class="agent-card" draggable="true" data-id="designer"
      style="--agent-color:#db2777;--agent-bg:#fdf2f8;--agent-border:#f9a8d4">
      <div class="agent-row">
        <div class="agent-icon">🎨</div>
        <div class="agent-info">
          <div class="agent-name">Designer AI</div>
          <div class="agent-specialty">UI/UX, branding, visual direction</div>
        </div>
        <div class="agent-badge">READY</div>
      </div>
    </div>

    <div class="agent-card" draggable="true" data-id="business"
      style="--agent-color:#7c3aed;--agent-bg:#f5f3ff;--agent-border:#c4b5fd">
      <div class="agent-row">
        <div class="agent-icon">📊</div>
        <div class="agent-info">
          <div class="agent-name">Business AI</div>
          <div class="agent-specialty">Strategy, startups, pitch decks</div>
        </div>
        <div class="agent-badge">READY</div>
      </div>
    </div>

    <div class="agent-card" draggable="true" data-id="translator"
      style="--agent-color:#0891b2;--agent-bg:#ecfeff;--agent-border:#a5f3fc">
      <div class="agent-row">
        <div class="agent-icon">🌐</div>
        <div class="agent-info">
          <div class="agent-name">Translator AI</div>
          <div class="agent-specialty">100+ languages, localisation</div>
        </div>
        <div class="agent-badge">READY</div>
      </div>
    </div>
  </div>

  <!-- WORKSPACE -->
  <div class="workspace">

    <!-- Team Bar -->
    <div class="team-bar" id="teamBar">
      <div class="team-bar-top">
        <div class="team-bar-label">
          👥 Your Active Team
          <span class="team-count" id="teamCount">0</span>
        </div>
        <button class="team-clear" onclick="clearAll()">Clear all</button>
      </div>
      <div class="team-chips" id="teamChips">
        <div class="team-empty" id="teamEmpty">
          <span class="team-empty-icon">☝️</span>
          <span>No agents yet — tap an agent card to add them here</span>
        </div>
      </div>
    </div>

    <!-- Workflow -->
    <div class="workflow-bar" id="wfBar">
      <div class="wf-label">⚙ Workflow</div>
      <div class="wf-row" id="wfRow"></div>
    </div>

    <!-- ★ CHAT PANEL ★ -->
    <div class="chat-panel">

      <!-- Chat Header -->
      <div class="chat-head">
        <div class="chat-head-left">
          <div class="chat-head-icon">
            <svg width="20" height="20" viewBox="0 0 48 48" fill="none">
              <circle cx="24" cy="24" r="5"   fill="white" opacity="0.95"/>
              <circle cx="24" cy="10" r="3"   fill="white" opacity="0.8"/>
              <circle cx="37" cy="31" r="3"   fill="white" opacity="0.7"/>
              <circle cx="11" cy="31" r="3"   fill="white" opacity="0.7"/>
              <line x1="24" y1="19" x2="24"  y2="13" stroke="white" stroke-width="1.5" opacity="0.6"/>
              <line x1="28" y1="27" x2="34.5" y2="30" stroke="white" stroke-width="1.5" opacity="0.6"/>
              <line x1="20" y1="27" x2="13.5" y2="30" stroke="white" stroke-width="1.5" opacity="0.6"/>
            </svg>
          </div>
          <div>
            <div class="chat-head-title">UniMind Chat</div>
            <div class="chat-head-sub" id="headSub">Add agents above to get started</div>
          </div>
        </div>
        <div class="live-badge"><div class="live-dot"></div> Live</div>
      </div>

      <!-- Messages -->
      <div class="messages" id="messages">
        <!-- Welcome -->
        <div class="msg-agent">
          <div class="msg-agent-av" style="background:linear-gradient(135deg,#eff6ff,#f5f3ff);border-color:#bfdbfe">
            <svg width="20" height="20" viewBox="0 0 48 48" fill="none">
              <defs><linearGradient id="wg" x1="0" y1="0" x2="48" y2="48" gradientUnits="userSpaceOnUse"><stop offset="0%" stop-color="#2563eb"/><stop offset="100%" stop-color="#4f46e5"/></linearGradient></defs>
              <circle cx="24" cy="24" r="5" fill="url(#wg)"/>
              <circle cx="24" cy="10" r="3" fill="url(#wg)" opacity="0.8"/>
              <circle cx="37" cy="31" r="3" fill="url(#wg)" opacity="0.7"/>
              <circle cx="11" cy="31" r="3" fill="url(#wg)" opacity="0.7"/>
              <line x1="24" y1="19" x2="24" y2="13"  stroke="url(#wg)" stroke-width="1.5" opacity="0.55"/>
              <line x1="28" y1="27" x2="34.5" y2="30" stroke="url(#wg)" stroke-width="1.5" opacity="0.55"/>
              <line x1="20" y1="27" x2="13.5" y2="30" stroke="url(#wg)" stroke-width="1.5" opacity="0.55"/>
            </svg>
          </div>
          <div class="msg-agent-body">
            <div class="msg-agent-meta">
              <span class="msg-agent-name">UniMind</span>
              <span class="msg-agent-time">Just now</span>
            </div>
            <div class="msg-agent-bub">
              <strong>Welcome to UniMind! 👋</strong><br><br>
              Here's how to get started in 3 easy steps:<br><br>
              <strong>Step 1 →</strong> Tap any <em>agent card</em> on the left to add AI specialists to your team.<br>
              <strong>Step 2 →</strong> Type your question in the box below.<br>
              <strong>Step 3 →</strong> Hit <em>Send</em> — each AI expert will reply with their best advice!<br><br>
              💡 <strong>Try this:</strong> Add Writer AI + Business AI, then ask <em>"Help me start a small business with no money."</em>
            </div>
          </div>
        </div>
      </div>

      <!-- ★ INPUT AREA ★ -->
      <div class="input-area">

        <!-- Warning when no agents -->
        <div class="no-agent-tip" id="noAgentTip">
          ⚠️ <span>Please add at least one AI agent above before sending a message.</span>
        </div>

        <!-- Quick prompts -->
        <div class="quick-prompts">
          <button class="qp" onclick="fillPrompt(this)">✍️ Write a business plan</button>
          <button class="qp" onclick="fillPrompt(this)">🔍 Research the AI market</button>
          <button class="qp" onclick="fillPrompt(this)">💡 Give me startup ideas</button>
          <button class="qp" onclick="fillPrompt(this)">🌐 Translate to Bengali</button>
        </div>

        <!-- Input box -->
        <div class="input-box" id="inputBox">
          <textarea
            class="chat-textarea"
            id="chatInput"
            placeholder="Ask your AI team anything — press Enter to send…"
            rows="1"
          ></textarea>
          <div class="input-actions">
            <button class="send-btn" id="sendBtn" onclick="sendMessage()" title="Send (Enter)">➤</button>
          </div>
        </div>

        <div class="input-footer">
          <span class="input-hint-txt">Press <kbd>Enter</kbd> to send &nbsp;·&nbsp; <kbd>Shift+Enter</kbd> for new line</span>
          <span class="char-counter" id="charCount">0 / 500</span>
        </div>
      </div>

    </div><!-- /chat-panel -->
  </div><!-- /workspace -->
</div><!-- /app -->

<!-- ═══════════════════ FOOTER ═══════════════════ -->
<footer>
  <strong>UniMind</strong> — Original concept &amp; prototype by <strong>Mridul</strong>, Narayanganj, Bangladesh · May 2026 &nbsp;·&nbsp;
  <a href="#" onclick="openModal();return false">Share UniMind 🚀</a><br>
  © 2026 Mridul. All Rights Reserved.
</footer>

<!-- ═══════════════════ SHARE MODAL ═══════════════════ -->
<div class="overlay" id="overlay" onclick="bgClose(event)">
  <div class="modal">
    <button class="modal-close" onclick="closeModal()">✕</button>

    <div class="modal-logo-row">
      <svg width="42" height="42" viewBox="0 0 48 48" fill="none">
        <defs><linearGradient id="mg" x1="0" y1="0" x2="48" y2="48" gradientUnits="userSpaceOnUse"><stop offset="0%" stop-color="#2563eb"/><stop offset="55%" stop-color="#4f46e5"/><stop offset="100%" stop-color="#0d9488"/></linearGradient></defs>
        <circle cx="24" cy="24" r="22" fill="rgba(37,99,235,0.07)" stroke="url(#mg)" stroke-width="1.5"/>
        <circle cx="24" cy="24" r="5"   fill="url(#mg)"/>
        <circle cx="24" cy="7"  r="3.2" fill="url(#mg)" opacity="0.85"/>
        <circle cx="39" cy="32" r="3.2" fill="url(#mg)" opacity="0.72"/>
        <circle cx="9"  cy="32" r="3.2" fill="url(#mg)" opacity="0.72"/>
        <line x1="24" y1="19" x2="24"  y2="10.2" stroke="url(#mg)" stroke-width="1.5" opacity="0.55"/>
        <line x1="28" y1="27" x2="36.2" y2="30"  stroke="url(#mg)" stroke-width="1.5" opacity="0.55"/>
        <line x1="20" y1="27" x2="11.8" y2="30"  stroke="url(#mg)" stroke-width="1.5" opacity="0.55"/>
        <circle cx="24" cy="24" r="15.5" stroke="url(#mg)" stroke-width="0.7" stroke-dasharray="2.5 4" opacity="0.28"/>
      </svg>
      <div>
        <div class="modal-brand">UniMind</div>
        <div style="font-size:12px;color:var(--fog)">One Chat. All AI. One Platform.</div>
      </div>
    </div>

    <p class="modal-tagline">Help UniMind reach everyone — share it with your friends, family &amp; network! 🌍</p>

    <div class="modal-url-bar">
      <div class="modal-url-txt" id="modalUrl">unimind prototype — share this link</div>
      <button class="modal-copy-btn" id="modalCopyBtn" onclick="copyLink(this, true)">📋 Copy</button>
    </div>

    <div class="modal-grid">
      <button class="modal-btn" onclick="goWA()">
        <span class="modal-btn-icon">💬</span>
        <div><div class="modal-btn-name">WhatsApp</div><div class="modal-btn-sub">Send to contacts</div></div>
      </button>
      <button class="modal-btn" onclick="goTG()">
        <span class="modal-btn-icon">✈️</span>
        <div><div class="modal-btn-name">Telegram</div><div class="modal-btn-sub">Share to channels</div></div>
      </button>
      <button class="modal-btn" onclick="goTW()">
        <span class="modal-btn-icon">𝕏</span>
        <div><div class="modal-btn-name">Twitter / X</div><div class="modal-btn-sub">Tweet it out</div></div>
      </button>
      <button class="modal-btn" onclick="goFB()">
        <span class="modal-btn-icon">👍</span>
        <div><div class="modal-btn-name">Facebook</div><div class="modal-btn-sub">Post to timeline</div></div>
      </button>
      <button class="modal-btn" onclick="goLI()">
        <span class="modal-btn-icon">💼</span>
        <div><div class="modal-btn-name">LinkedIn</div><div class="modal-btn-sub">Share with network</div></div>
      </button>
      <button class="modal-btn" onclick="goEmail()">
        <span class="modal-btn-icon">📧</span>
        <div><div class="modal-btn-name">Email</div><div class="modal-btn-sub">Send the link</div></div>
      </button>
    </div>

    <div class="modal-footer">Made with 💙 by <strong>Mridul</strong> · Age 19 · Narayanganj, Bangladesh</div>
  </div>
</div>

<!-- Toast -->
<div class="toast" id="toast">✅ Link copied!</div>

<!-- ═══════════════════ SCRIPT ═══════════════════ -->
<script>
/* ── AGENT DEFINITIONS ── */
const AGENTS = {
  writer:     { name:'Writer AI',     icon:'✍️', color:'#2563eb', chipBg:'#eff6ff', chipBorder:'#bfdbfe', chipColor:'#1d4ed8',
    sys:`You are Writer AI inside UniMind. Focus only on writing, content, and copy. Be practical and concise (3–5 sentences or a short bullet list). Start your reply with "✍️ Writer AI:" — give immediately usable content output.` },
  coder:      { name:'Coder AI',      icon:'💻', color:'#059669', chipBg:'#f0fdf4', chipBorder:'#a7f3d0', chipColor:'#065f46',
    sys:`You are Coder AI inside UniMind. Focus only on coding and technical implementation. Be practical and concise. Start your reply with "💻 Coder AI:" — give specific code snippets or clear technical steps.` },
  researcher: { name:'Research AI',   icon:'🔍', color:'#d97706', chipBg:'#fffbeb', chipBorder:'#fde68a', chipColor:'#92400e',
    sys:`You are Research AI inside UniMind. Focus only on research, data, and factual insights. Be concise (3–5 key findings). Start your reply with "🔍 Research AI:" — give specific, credible information.` },
  designer:   { name:'Designer AI',   icon:'🎨', color:'#db2777', chipBg:'#fdf2f8', chipBorder:'#f9a8d4', chipColor:'#9d174d',
    sys:`You are Designer AI inside UniMind. Focus only on visual design, UX, and branding. Be concise (3–5 sentences). Start your reply with "🎨 Designer AI:" — give specific, actionable design direction.` },
  business:   { name:'Business AI',   icon:'📊', color:'#7c3aed', chipBg:'#f5f3ff', chipBorder:'#c4b5fd', chipColor:'#4c1d95',
    sys:`You are Business AI inside UniMind. Focus only on strategy, monetisation, and startup advice. Be sharp and concise. Start your reply with "📊 Business AI:" — give specific strategic recommendations.` },
  translator: { name:'Translator AI', icon:'🌐', color:'#0891b2', chipBg:'#ecfeff', chipBorder:'#a5f3fc', chipColor:'#0e7490',
    sys:`You are Translator AI inside UniMind. Focus only on translation and language localisation. Be concise. Start your reply with "🌐 Translator AI:" — give a practical translation or language-specific advice.` }
};

let active = [];
let busy = false;
const pageURL = window.location.href;
const ENC = encodeURIComponent;
const MSG = ENC("🤯 I just tried UniMind — one platform where ALL your AI assistants work as a team! Built by a 19-year-old from Bangladesh 🇧🇩 Try it free:");

/* ── DRAG & DROP + CLICK TOGGLE ── */
document.querySelectorAll('.agent-card').forEach(c => {
  c.setAttribute('draggable', true);
  c.addEventListener('dragstart', e => { e.dataTransfer.setData('id', c.dataset.id); c.classList.add('dragging'); });
  c.addEventListener('dragend',   () => c.classList.remove('dragging'));
  c.addEventListener('click',     () => active.includes(c.dataset.id) ? removeAgent(c.dataset.id) : addAgent(c.dataset.id));
});
const tb = document.getElementById('teamBar');
tb.addEventListener('dragover',  e => { e.preventDefault(); tb.classList.add('drag-over'); });
tb.addEventListener('dragleave', () => tb.classList.remove('drag-over'));
tb.addEventListener('drop', e => {
  e.preventDefault(); tb.classList.remove('drag-over');
  const id = e.dataTransfer.getData('id');
  if (id && !active.includes(id)) addAgent(id);
});

function addAgent(id) {
  if (active.includes(id)) return;
  active.push(id);
  const a = AGENTS[id];

  document.getElementById('teamEmpty')?.remove();
  document.querySelector(`[data-id="${id}"]`).classList.add('active');

  const chip = document.createElement('div');
  chip.className = 'chip'; chip.id = `chip-${id}`;
  chip.style.cssText = `background:${a.chipBg};border-color:${a.chipBorder};color:${a.chipColor}`;
  chip.innerHTML = `<span>${a.icon}</span><span style="font-weight:700">${a.name}</span><button class="chip-x" onclick="removeAgent('${id}')">✕</button>`;
  document.getElementById('teamChips').appendChild(chip);

  updateUI();
  sysMsg(`${a.icon} ${a.name} joined your team`);
}

function removeAgent(id) {
  active = active.filter(x => x !== id);
  document.getElementById(`chip-${id}`)?.remove();
  document.querySelector(`[data-id="${id}"]`).classList.remove('active');
  if (!active.length) {
    const e = document.createElement('div'); e.className = 'team-empty'; e.id = 'teamEmpty';
    e.innerHTML = '<span class="team-empty-icon">☝️</span><span>No agents yet — tap an agent card to add them here</span>';
    document.getElementById('teamChips').appendChild(e);
  }
  updateUI();
}

function clearAll() {
  [...active].forEach(id => removeAgent(id));
}

function updateUI() {
  // Count badge
  document.getElementById('teamCount').textContent = active.length;
  // No-agent tip
  document.getElementById('noAgentTip').classList.toggle('hidden', active.length > 0);
  // Header sub
  document.getElementById('headSub').textContent = active.length
    ? active.map(id => AGENTS[id].name).join(' · ')
    : 'Add agents above to get started';
  // Workflow
  const wf = document.getElementById('wfBar');
  const wr = document.getElementById('wfRow');
  if (!active.length) { wf.style.display = 'none'; return; }
  wf.style.display = 'block'; wr.innerHTML = '';
  const steps = ['👤 You', ...active.map(id => AGENTS[id].icon + ' ' + AGENTS[id].name), '✅ Result'];
  steps.forEach((s, i) => {
    const n = document.createElement('div'); n.className = 'wf-node'; n.textContent = s; wr.appendChild(n);
    if (i < steps.length-1) { const arr = document.createElement('div'); arr.className = 'wf-arrow'; arr.textContent = '→'; wr.appendChild(arr); }
  });
}

/* ── CHAT ── */
function sysMsg(txt) {
  const d = document.createElement('div'); d.className = 'msg-sys'; d.textContent = txt;
  append(d);
}
function userMsg(txt) {
  const d = document.createElement('div'); d.className = 'msg-user';
  d.innerHTML = `<div class="msg-user-bub">${esc(txt)}</div>`;
  append(d);
}
function agentMsg(id, text) {
  const a = AGENTS[id];
  const d = document.createElement('div'); d.className = 'msg-agent';
  d.innerHTML = `
    <div class="msg-agent-av" style="background:${a.chipBg};border-color:${a.chipBorder}">${a.icon}</div>
    <div class="msg-agent-body">
      <div class="msg-agent-meta">
        <span class="msg-agent-name" style="color:${a.color}">${a.name}</span>
        <span class="msg-agent-time">${now()}</span>
      </div>
      <div class="msg-agent-bub">${fmt(text)}</div>
      <div class="msg-share-row">
        <button class="msg-action-btn" onclick="quickShare(this,'${id}')">🔗 Share this reply</button>
        <button class="msg-action-btn" onclick="copyReply(this)">📋 Copy</button>
      </div>
    </div>`;
  append(d);
}
function showTyping(id) {
  const a = AGENTS[id];
  const d = document.createElement('div'); d.className = 'typing-row'; d.id = `ty-${id}`;
  d.innerHTML = `
    <div class="msg-agent-av" style="background:${a.chipBg};border-color:${a.chipBorder}">${a.icon}</div>
    <div class="typing-bub">
      <span class="typing-lbl">${a.name} is thinking</span>
      <div class="dots-wrap"><div class="dot"></div><div class="dot"></div><div class="dot"></div></div>
    </div>`;
  append(d);
}
function hideTyping(id) { document.getElementById(`ty-${id}`)?.remove(); }
function append(el) {
  const m = document.getElementById('messages'); m.appendChild(el); m.scrollTop = m.scrollHeight;
}

async function sendMessage() {
  if (busy) return;
  const inp = document.getElementById('chatInput');
  const txt = inp.value.trim();
  if (!txt) return;
  if (!active.length) { document.getElementById('noAgentTip').classList.remove('hidden'); return; }

  busy = true;
  document.getElementById('sendBtn').disabled = true;
  inp.value = ''; inp.style.height = 'auto';
  document.getElementById('charCount').textContent = '0 / 500';
  userMsg(txt);

  for (const id of active) {
    showTyping(id);
    try {
      const res = await fetch('https://api.anthropic.com/v1/messages', {
        method: 'POST', headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ model:'claude-sonnet-4-20250514', max_tokens:1000,
          system: AGENTS[id].sys, messages:[{role:'user',content:txt}] })
      });
      const data = await res.json();
      hideTyping(id);
      agentMsg(id, data.content?.map(b=>b.text||'').join('') || 'Something went wrong. Please try again.');
    } catch {
      hideTyping(id);
      agentMsg(id, `${AGENTS[id].icon} I'm ready to assist — in the full product this would show real ${AGENTS[id].name.toLowerCase().replace(' ai','')} expertise for your question.`);
    }
    await new Promise(r => setTimeout(r, 350));
  }

  busy = false;
  document.getElementById('sendBtn').disabled = false;
}

function quickShare(btn, agentId) {
  const bub = btn.closest('.msg-agent-body').querySelector('.msg-agent-bub');
  const t = ENC(`${AGENTS[agentId].icon} ${AGENTS[agentId].name} said on UniMind:\n\n"${bub.innerText.slice(0,180)}..."\n\nTry UniMind free → ${pageURL}`);
  window.open(`https://wa.me/?text=${t}`, '_blank');
}
function copyReply(btn) {
  const bub = btn.closest('.msg-agent-body').querySelector('.msg-agent-bub');
  navigator.clipboard.writeText(bub.innerText).then(() => { showToast('📋 Reply copied!'); });
}
function fillPrompt(el) { document.getElementById('chatInput').value = el.textContent.replace(/^[^\s]+\s/,''); document.getElementById('chatInput').focus(); }

/* ── TEXTAREA ── */
document.getElementById('chatInput').addEventListener('input', function() {
  this.style.height = 'auto';
  this.style.height = Math.min(this.scrollHeight, 120) + 'px';
  document.getElementById('charCount').textContent = `${Math.min(this.value.length,500)} / 500`;
  if (this.value.length > 500) this.value = this.value.slice(0, 500);
});
document.getElementById('chatInput').addEventListener('keydown', e => {
  if (e.key === 'Enter' && !e.shiftKey) { e.preventDefault(); sendMessage(); }
});

/* ── MODAL ── */
function openModal() {
  if (navigator.share) {
    navigator.share({ title:'UniMind — All your AIs in one chat', text:'Try UniMind free!', url: pageURL }).catch(()=>{});
    return;
  }
  document.getElementById('modalUrl').textContent = pageURL;
  document.getElementById('overlay').classList.add('open');
}
function closeModal() { document.getElementById('overlay').classList.remove('open'); }
function bgClose(e)   { if (e.target === document.getElementById('overlay')) closeModal(); }
document.addEventListener('keydown', e => { if (e.key === 'Escape') closeModal(); });

/* ── SHARE FUNCTIONS ── */
function goWA()    { window.open(`https://wa.me/?text=${MSG}%20${ENC(pageURL)}`, '_blank'); }
function goTG()    { window.open(`https://t.me/share/url?url=${ENC(pageURL)}&text=${MSG}`, '_blank'); }
function goTW()    { window.open(`https://twitter.com/intent/tweet?text=${MSG}&url=${ENC(pageURL)}`, '_blank'); }
function goFB()    { window.open(`https://www.facebook.com/sharer/sharer.php?u=${ENC(pageURL)}`, '_blank'); }
function goLI()    { window.open(`https://www.linkedin.com/sharing/share-offsite/?url=${ENC(pageURL)}`, '_blank'); }
function goEmail() { window.open(`mailto:?subject=Try UniMind — All your AIs in one chat!&body=${decodeURIComponent(MSG)}%0A${pageURL}`, '_blank'); }

function copyLink(btn, isModal = false) {
  navigator.clipboard.writeText(pageURL).then(() => {
    if (isModal) {
      const orig = btn.textContent; btn.textContent = '✅ Copied!';
      setTimeout(() => btn.textContent = orig, 2200);
    } else {
      btn.classList.add('copied');
      const orig = btn.innerHTML; btn.innerHTML = '✅ Copied!';
      setTimeout(() => { btn.classList.remove('copied'); btn.innerHTML = orig; }, 2200);
    }
    showToast('🔗 Link copied — share everywhere! 🚀');
  }).catch(() => showToast('Copy the URL from your address bar!'));
}

/* ── TOAST ── */
function showToast(msg) {
  const t = document.getElementById('toast'); t.textContent = msg; t.classList.add('show');
  setTimeout(() => t.classList.remove('show'), 3000);
}

/* ── UTILS ── */
function now() {
  const d = new Date(); return d.getHours().toString().padStart(2,'0') + ':' + d.getMinutes().toString().padStart(2,'0');
}
function esc(t) { return t.replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;'); }
function fmt(t) {
  return esc(t)
    .replace(/\*\*(.*?)\*\*/g, '<strong>$1</strong>')
    .replace(/\*(.*?)\*/g,     '<em>$1</em>')
    .replace(/\n/g, '<br>');
}

/* ── INIT ── */
updateUI();
</script>
</body>
</html>
