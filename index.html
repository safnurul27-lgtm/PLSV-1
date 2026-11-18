<!doctype html>
<html lang="id">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>MPI Persamaan Linear</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Lexend:wght@400;600;800&family=Nunito+Sans:wght@400;600;700&display=swap">
<style>
/* Konsep: lembar kerja bergaris kotak (kertas milimeter) dengan panel besar untuk FPI; satu bagian tampil per tab */
:root{
  --bg:#eef3f1; --surface:#ffffff; --fg:#13262b; --muted:#53686d; --line:#c9d6d3;
  --ink:#0f5c63; --ink-soft:#d8ecec; --amber:#e39a00; --amber-soft:#fff0cc;
  --good:#1f8a57; --good-soft:#d9f2e4; --bad:#c8432b; --bad-soft:#fbe0da;
  --grid:rgba(15,92,99,.07);
  --font-d:"Lexend",system-ui,sans-serif; --font-b:"Nunito Sans",system-ui,sans-serif;
}
@media (prefers-color-scheme: dark){:root:not([data-theme="light"]){
  --bg:#0e1a1d; --surface:#16272b; --fg:#e8f1ef; --muted:#9db3b6; --line:#2c4247;
  --ink:#5cc3c9; --ink-soft:#18393d; --amber:#f2b73a; --amber-soft:#3b2f10;
  --good:#52c58a; --good-soft:#143525; --bad:#ff8b72; --bad-soft:#40201a;
  --grid:rgba(92,195,201,.08); color-scheme:dark}}
:root[data-theme="dark"]{
  --bg:#0e1a1d; --surface:#16272b; --fg:#e8f1ef; --muted:#9db3b6; --line:#2c4247;
  --ink:#5cc3c9; --ink-soft:#18393d; --amber:#f2b73a; --amber-soft:#3b2f10;
  --good:#52c58a; --good-soft:#143525; --bad:#ff8b72; --bad-soft:#40201a;
  --grid:rgba(92,195,201,.08); color-scheme:dark}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--fg);font-family:var(--font-b);font-size:19px;line-height:1.55;
  background-image:linear-gradient(var(--grid) 1px,transparent 1px),linear-gradient(90deg,var(--grid) 1px,transparent 1px);
  background-size:28px 28px;
  padding-left:max(16px,env(safe-area-inset-left,0px));padding-right:max(16px,env(safe-area-inset-right,0px));padding-block:0 48px}
.wrap{max-width:1200px;margin:0 auto}
h1,h2,h3{font-family:var(--font-d);line-height:1.2;text-wrap:balance;margin:0}
h1{font-size:clamp(28px,4vw,44px);font-weight:800}
h2{font-size:clamp(24px,3vw,34px);font-weight:800;color:var(--ink)}
h3{font-size:22px;font-weight:600}
p{margin:.5em 0}
header.top{padding:22px 0 10px;display:flex;gap:16px;align-items:center;justify-content:space-between;flex-wrap:wrap}
.meta{font-size:15px;color:var(--muted);display:flex;gap:8px;flex-wrap:wrap}
.chip{border:1.5px solid var(--line);border-radius:999px;padding:3px 12px;background:var(--surface);font-weight:600}
nav.tabs{position:sticky;top:env(safe-area-inset-top,0px);z-index:5;background:var(--bg);padding:8px 0;
  display:flex;gap:8px;overflow-x:auto;border-bottom:2px solid var(--line)}
nav.tabs a{flex:0 0 auto;text-decoration:none;color:var(--fg);font-family:var(--font-d);font-weight:600;font-size:17px;
  padding:12px 18px;border-radius:12px;border:2px solid transparent;min-height:48px;display:flex;align-items:center}
nav.tabs a:hover{background:var(--ink-soft)}
nav.tabs a[aria-current="page"]{background:var(--ink);color:var(--bg);border-color:var(--ink)}
nav.tabs a:focus-visible,button:focus-visible,input:focus-visible,summary:focus-visible{outline:3px solid var(--amber);outline-offset:2px}
section.view{display:none;padding-top:26px}
section.view.on{display:block}
.card{background:var(--surface);border:2px solid var(--line);border-radius:18px;padding:22px 24px}
.grid2{display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,420px),1fr));gap:20px}
.grid3{display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,280px),1fr));gap:16px}
.stack{display:flex;flex-direction:column;gap:18px}
.kicker{font-family:var(--font-d);font-size:14px;letter-spacing:.08em;text-transform:uppercase;color:var(--muted);font-weight:600}
.lead{font-size:22px}
.btn{font-family:var(--font-d);font-weight:600;font-size:18px;min-height:52px;padding:10px 20px;border-radius:12px;
  border:2px solid var(--ink);background:var(--ink);color:var(--bg);cursor:pointer}
.btn.alt{background:var(--surface);color:var(--ink)}
.btn.sm{min-height:44px;font-size:16px;padding:6px 14px}
.btn:disabled{opacity:.45;cursor:not-allowed}
.row{display:flex;gap:10px;flex-wrap:wrap;align-items:center}
.eq{font-family:var(--font-d);font-weight:600;font-size:clamp(26px,3.4vw,40px);letter-spacing:.02em}
.eq .x{color:var(--amber)}
.callout{border-left:8px solid var(--amber);background:var(--amber-soft);padding:14px 18px;border-radius:0 14px 14px 0}
.ok{background:var(--good-soft);border-left:8px solid var(--good);padding:12px 16px;border-radius:0 12px 12px 0}
.no{background:var(--bad-soft);border-left:8px solid var(--bad);padding:12px 16px;border-radius:0 12px 12px 0}
table{border-collapse:collapse;width:100%;font-size:18px}
th,td{border:1.5px solid var(--line);padding:8px 12px;text-align:left}
th{background:var(--ink-soft);font-family:var(--font-d);font-weight:600}
td.n,th.n{text-align:right;font-variant-numeric:tabular-nums}
.scroll{overflow-x:auto}
svg text{fill:var(--fg);font-family:var(--font-b)}
.opt{display:block;width:100%;text-align:left;font:inherit;font-size:20px;padding:14px 18px;margin:8px 0;border-radius:14px;
  border:2px solid var(--line);background:var(--surface);color:var(--fg);cursor:pointer;min-height:56px}
.opt:hover:not(:disabled){border-color:var(--ink)}
.opt.right{border-color:var(--good);background:var(--good-soft)}
.opt.wrong{border-color:var(--bad);background:var(--bad-soft)}
input[type=number],input[type=text]{font:inherit;font-size:22px;padding:8px 12px;border:2px solid var(--line);border-radius:12px;
  background:var(--surface);color:var(--fg);width:150px}
input[type=range]{width:100%;height:36px;accent-color:var(--ink)}
.step{display:grid;grid-template-columns:44px 1fr;gap:12px;align-items:start}
.step b{background:var(--ink);color:var(--bg);border-radius:50%;width:44px;height:44px;display:grid;place-items:center;font-family:var(--font-d)}
details{border:2px solid var(--line);border-radius:14px;padding:10px 16px;background:var(--surface)}
summary{cursor:pointer;font-family:var(--font-d);font-weight:600;min-height:40px;display:flex;align-items:center}
@media (prefers-reduced-motion:no-preference){.tilt{transition:transform .6s cubic-bezier(.3,1.4,.5,1)}}
@media (max-width:600px){body{font-size:17px}.card{padding:16px}}
</style>
</head>
<body>
<div class="wrap">
<header class="top">
  <div>
    <div class="kicker">Media Pembelajaran Interaktif · Matematika Kelas 8</div>
    <h1>Persamaan dan Pertidaksamaan Linear Satu Variabel</h1>
    <div class="meta" style="margin-top:8px"><span class="chip">3 JP × 40 menit</span><span class="chip">PBL</span><span class="chip">Cooperative Learning</span><span class="chip">Deep Learning</span></div>
  </div>
  <div class="card" style="padding:10px 16px" aria-label="Pengatur waktu kelas">
