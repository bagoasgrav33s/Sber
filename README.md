<!doctype html>
<html lang="ru">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Свободный Я — Сбер-версия</title>

<style>
:root{
  --bg:#ffffff;
  --sber-green:#21A038;
  --sber-green-soft:#EAF7EE;
  --turq:#2EC4C6;
  --turq-soft:#BFEFEF;
  --yellow:#F2E39A;
  --text:#0B2B1E;
  --muted:#6E8F84;
  --card:#F7FBF9;
  --radius:20px;
}

*{box-sizing:border-box}

body{
  margin:0;
  background:var(--bg);
  font-family:Inter, system-ui, -apple-system, Segoe UI, Roboto, Arial;
  color:var(--text);
}

.app{
  max-width:1400px;
  margin:0 auto;
  padding:28px;
  display:grid;
  grid-template-columns:320px 1fr 360px;
  gap:24px;
}

/* ===== LEFT ===== */
.sidebar{
  background:var(--card);
  border-radius:var(--radius);
  padding:24px;
  display:flex;
  flex-direction:column;
  gap:22px;
  animation:fadeUp .6s ease;
}

.brand{
  display:flex;
  align-items:center;
  gap:12px;
  font-weight:700;
  font-size:18px;
}

.brand .logo{
  width:42px;height:42px;border-radius:50%;
  background:linear-gradient(135deg,var(--sber-green),var(--turq));
  display:grid;place-items:center;
  color:white;
  font-weight:800;
}

.avatar{
  width:150px;height:150px;border-radius:50%;
  margin:0 auto;
  background:
    radial-gradient(circle at 30% 30%, #ffffffcc, transparent 45%),
    linear-gradient(135deg,var(--sber-green),var(--turq));
  display:grid;place-items:center;
  animation:pulse 6s infinite;
}

.avatar svg{width:70px;opacity:.95}

.index{
  text-align:center;
}

.indexValue{
  font-size:44px;
  font-weight:800;
  background:linear-gradient(90deg,var(--turq),var(--yellow));
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}

.indexLabel{color:var(--muted)}

.missions{
  display:flex;
  flex-direction:column;
  gap:10px;
}

.mission{
  background:white;
  border-radius:14px;
  padding:12px 14px;
  display:flex;
  justify-content:space-between;
  align-items:center;
  transition:.3s;
}

.mission:hover{transform:translateY(-2px)}

.mission button{
  border:none;
  background:var(--turq-soft);
  color:#064E50;
  padding:6px 10px;
  border-radius:10px;
  cursor:pointer;
}

/* ===== CENTER ===== */
.center{
  display:flex;
  flex-direction:column;
  gap:24px;
}

.card{
  background:var(--card);
  border-radius:var(--radius);
  padding:24px;
}

/* Radar */
.radarWrap{
  display:flex;
  gap:24px;
  align-items:center;
}

canvas{max-width:360px}

.insights{
  flex:1;
}

.insight{
  background:white;
  border-left:4px solid var(--turq);
  padding:12px 14px;
  border-radius:12px;
  margin-bottom:10px;
  animation:fadeUp .4s ease;
}

/* ===== RIGHT / AI ===== */
.ai{
  background:var(--sber-green-soft);
  border-radius:var(--radius);
  padding:20px;
  display:flex;
  flex-direction:column;
  height:100%;
}

.aiHeader{
  font-weight:700;
  color:var(--sber-green);
  display:flex;
  align-items:center;
  gap:8px;
}

.aiLog{
  flex:1;
  margin-top:14px;
  display:flex;
  flex-direction:column;
  gap:10px;
  overflow:auto;
}

.msg{
  max-width:75%;
  padding:10px 14px;
  border-radius:14px;
  animation:fadeUp .3s ease;
}

.bot{
  background:white;
}

.user{
  background:var(--sber-green);
  color:white;
  align-self:flex-end;
}

.aiInput{
  display:flex;
  gap:8px;
  margin-top:12px;
}

.aiInput input{
  flex:1;
  padding:12px;
  border-radius:14px;
  border:none;
}

/* ===== ANIM ===== */
@keyframes fadeUp{
  from{opacity:0;transform:translateY(8px)}
  to{opacity:1;transform:none}
}

@keyframes pulse{
  0%,100%{box-shadow:0 0 0 0 rgba(33,160,56,.35)}
  50%{box-shadow:0 0 0 26px rgba(33,160,56,0)}
}

@media(max-width:1200px){
  .app{grid-template-columns:1fr}
}
</style>
</head>

<body>
<div class="app">

<!-- LEFT -->
<aside class="sidebar">
  <div class="brand">
    <div class="logo">S</div>
    Свободный Я
  </div>

  <div class="avatar">
    <svg viewBox="0 0 24 24" fill="white">
      <path d="M12 12c2.7 0 4.8-2.1 4.8-4.8S14.7 2.4 12 2.4 7.2 4.5 7.2 7.2 9.3 12 12 12zm0 2.4c-3.2 0-9.6 1.6-9.6 4.8v2.4h19.2v-2.4c0-3.2-6.4-4.8-9.6-4.8z"/>
    </svg>
  </div>
