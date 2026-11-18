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
    <div class="kicker">Timer kelas</div>
    <div class="row">
      <span id="tmr" class="eq" aria-live="off" style="min-width:110px">05:00</span>
      <button class="btn sm alt" data-t="60">1&prime;</button><button class="btn sm alt" data-t="180">3&prime;</button><button class="btn sm alt" data-t="300">5&prime;</button><button class="btn sm alt" data-t="600">10&prime;</button>
      <button class="btn sm" id="tmrGo">Mulai</button>
    </div>
  </div>
</header>

<nav class="tabs" aria-label="Bagian pembelajaran">
  <a href="#alur">Alur</a><a href="#pemantik">Pemantik</a><a href="#apersepsi">Apersepsi</a><a href="#materi">Materi</a>
  <a href="#simulasi">Simulasi</a><a href="#masalah">Masalah PBL</a><a href="#kuis">Kuis</a><a href="#refleksi">Refleksi</a>
</nav>

<!-- ALUR -->
<section class="view" id="v-alur"><div class="stack">
  <div class="grid2">
    <div class="card"><div class="kicker">Tujuan pembelajaran</div>
      <ul style="padding-left:1.2em;margin:.4em 0">
        <li>Memahami konsep persamaan linear satu variabel (PLSV).</li>
        <li>Menyelesaikan model matematika dan masalah nyata yang berkaitan dengan PLSV.</li>
        <li>Mengenal pertidaksamaan linear satu variabel (PtLSV) sebagai perluasan konsep.</li>
      </ul></div>
    <div class="card"><div class="kicker">Pendekatan</div>
      <p><b>Mindful:</b> siswa sadar mengapa menyeimbangkan kedua ruas itu perlu.<br>
      <b>Meaningful:</b> konsep dibangun dari timbangan, tarif ojek, dan tabungan.<br>
      <b>Joyful:</b> simulasi, kuis tim, dan presentasi antarkelompok.</p></div>
  </div>
  <div class="card scroll">
    <h2 style="margin-bottom:12px">Alur 3 JP (120 menit)</h2>
    <table>
      <tr><th>JP</th><th>Menit</th><th>Tahap PBL</th><th>Kegiatan siswa (cooperative learning)</th><th>Tab</th></tr>
      <tr><td rowspan="3">1</td><td>0–10</td><td>Orientasi pada masalah</td><td>Think–Pair–Share atas pertanyaan pemantik</td><td><a href="#pemantik">Pemantik</a></td></tr>
      <tr><td>10–20</td><td>Apersepsi</td><td>Menebak nilai yang belum diketahui, mengingat istilah aljabar</td><td><a href="#apersepsi">Apersepsi</a></td></tr>
      <tr><td>20–40</td><td>Membangun konsep</td><td>Menemukan sifat kesetaraan bersama pasangan, mengisi tabel</td><td><a href="#materi">Materi</a></td></tr>
      <tr><td rowspan="2">2</td><td>40–60</td><td>Eksplorasi</td><td>Berpasangan memakai timbangan: coba-coba nilai x lalu langkah penyelesaian</td><td><a href="#simulasi">Simulasi</a></td></tr>
      <tr><td>60–80</td><td>Mengorganisasi dan menyelidiki</td><td>Kelompok 4 orang memodelkan dan menyelesaikan satu masalah nyata (LKPD)</td><td><a href="#masalah">Masalah PBL</a></td></tr>
      <tr><td rowspan="3">3</td><td>80–95</td><td>Menyajikan solusi</td><td>Penyaji kelompok menjelaskan model, langkah, dan pemeriksaan; kelompok lain menanggapi</td><td><a href="#masalah">Masalah PBL</a></td></tr>
      <tr><td>95–110</td><td>Penilaian</td><td>Kuis interaktif, skor tim (Numbered Heads Together)</td><td><a href="#kuis">Kuis</a></td></tr>
      <tr><td>110–120</td><td>Refleksi</td><td>Menilai pemahaman dan kerja sama tim</td><td><a href="#refleksi">Refleksi</a></td></tr>
    </table>
  </div>
  <div class="card"><h3>Peran dalam kelompok (bergilir tiap tugas)</h3>
    <div class="grid3" style="margin-top:12px">
      <div class="callout"><b>Ketua</b><br>Memastikan semua anggota ikut berpikir.</div>
      <div class="callout"><b>Penulis</b><br>Mencatat model dan langkah di LKPD.</div>
      <div class="callout"><b>Pengecek</b><br>Memeriksa jawaban dengan substitusi.</div>
      <div class="callout"><b>Penyaji</b><br>Menjelaskan hasil kelompok ke kelas.</div>
    </div></div>
</div></section>

<!-- PEMANTIK -->
<section class="view" id="v-pemantik"><div class="stack">
  <div class="kicker">Think · Pair · Share</div>
  <div class="grid2">
    <div class="card">
      <h2>Berapa berat sekantong jeruk?</h2>
      <svg viewBox="0 0 420 260" width="100%" role="img" aria-label="Timbangan seimbang: sekantong jeruk dan 3 beban 1 kg di kiri, beban 8 kg di kanan">
        <rect x="200" y="70" width="20" height="150" rx="6" fill="#8a9a9d"/>
        <rect x="140" y="214" width="140" height="14" rx="7" fill="#8a9a9d"/>
        <rect x="40" y="64" width="340" height="12" rx="6" fill="#0f5c63"/>
        <path d="M70 76 L40 150 H130 Z M350 76 L320 150 H380 Z" fill="none" stroke="#0f5c63" stroke-width="3"/>
        <rect x="30" y="150" width="110" height="10" rx="5" fill="#0f5c63"/><rect x="310" y="150" width="110" height="10" rx="5" fill="#0f5c63"/>
        <circle cx="62" cy="128" r="20" fill="#e39a00"/><circle cx="92" cy="130" r="18" fill="#f0b030"/><circle cx="76" cy="108" r="17" fill="#e39a00"/>
        <text x="92" y="190" text-anchor="middle" font-size="16" font-weight="700">jeruk = x</text>
        <rect x="100" y="136" width="12" height="14" fill="#c8432b"/><rect x="114" y="136" width="12" height="14" fill="#c8432b"/><rect x="128" y="136" width="12" height="14" fill="#c8432b"/>
        <text x="120" y="126" text-anchor="middle" font-size="13">3 × 1 kg</text>
        <rect x="340" y="116" width="50" height="34" rx="6" fill="#5b6b8c"/><text x="365" y="139" text-anchor="middle" font-size="16" font-weight="700" style="fill:#fff">8 kg</text>
        <text x="210" y="50" text-anchor="middle" font-size="20" font-weight="700">x + 3 = 8</text>
      </svg>
    </div>
    <div class="card stack">
      <div class="step"><b>1</b><div>Timbangan dalam keadaan <u>seimbang</u>. Di kiri: sekantong jeruk (berat x) dan 3 beban 1 kg. Di kanan: beban 8 kg. <b>Berapa kg sekantong jeruk?</b></div></div>
      <div class="step"><b>2</b><div>Jika 3 kg diambil dari sisi kiri saja, apa yang terjadi? Apa yang harus dilakukan agar tetap seimbang?</div></div>
      <div class="step"><b>3</b><div>Kapan kamu pernah mencari angka yang belum diketahui, misalnya uang kembalian, sisa pulsa, atau jarak ke sekolah?</div></div>
      <details><summary>Petunjuk untuk guru (buka setelah diskusi)</summary>
        <p>Arahkan siswa menyatakan: apa pun yang dilakukan pada satu sisi harus dilakukan juga pada sisi lain. Ini cikal bakal sifat kesetaraan: x + 3 = 8 menjadi x = 8 − 3 = 5.</p>
        <button class="btn sm" id="revealJeruk">Tampilkan jawaban</button>
        <p id="jerukAns" hidden class="ok"><b>x = 5 kg.</b> Kurangi 3 di kedua sisi: x + 3 − 3 = 8 − 3.</p>
      </details>
    </div>
  </div>
</div></section>

<!-- APERSEPSI -->
<section class="view" id="v-apersepsi"><div class="stack">
  <h2>Mengingat kembali</h2>
  <div class="grid2">
    <div class="card">
      <h3>Istilah dalam bentuk aljabar</h3>
      <div class="eq" style="margin:14px 0">3<span class="x">x</span> + 5 = 20</div>
      <table>
        <tr><th>Istilah</th><th>Pada 3x + 5 = 20</th><th>Artinya</th></tr>
        <tr><td>Variabel</td><td class="eq" style="font-size:22px"><span class="x">x</span></td><td>Lambang bilangan yang belum diketahui</td></tr>
        <tr><td>Koefisien</td><td style="font-size:22px">3</td><td>Bilangan yang mengalikan variabel</td></tr>
        <tr><td>Konstanta</td><td style="font-size:22px">5</td><td>Bilangan tanpa variabel</td></tr>
        <tr><td>Ruas kiri / kanan</td><td style="font-size:22px">3x + 5 / 20</td><td>Sisi kiri dan kanan tanda &ldquo;=&rdquo;</td></tr>
      </table>
    </div>
    <div class="card stack">
      <h3>Tebak nilai yang hilang</h3>
      <p>Tulis jawabanmu, lalu tekan <b>Periksa</b>.</p>
      <div class="mini" data-ans="7"><span class="eq">□ + 5 = 12</span><div class="row"><input type="number" aria-label="Jawaban 1"><button class="btn sm">Periksa</button><span class="fb"></span></div></div>
      <div class="mini" data-ans="7"><span class="eq">3 × □ = 21</span><div class="row"><input type="number" aria-label="Jawaban 2"><button class="btn sm">Periksa</button><span class="fb"></span></div></div>
      <div class="mini" data-ans="11"><span class="eq">□ − 7 = 4</span><div class="row"><input type="number" aria-label="Jawaban 3"><button class="btn sm">Periksa</button><span class="fb"></span></div></div>
      <div class="mini" data-ans="-3"><span class="eq">2 × □ + 1 = −5</span><div class="row"><input type="number" aria-label="Jawaban 4"><button class="btn sm">Periksa</button><span class="fb"></span></div></div>
    </div>
  </div>
  <div class="callout"><b>Pertanyaan jembatan:</b> Tebakan bekerja untuk bilangan kecil. Bagaimana jika persamaannya 7x − 13 = 3x + 51? Kita butuh cara yang pasti, bukan menebak.</div>
</div></section>

<!-- MATERI -->
<section class="view" id="v-materi"><div class="stack">
  <div class="grid2">
    <div class="card">
      <div class="kicker">1 · Konsep</div>
      <h2>Apa itu PLSV?</h2>
      <p class="lead">Persamaan linear satu variabel adalah kalimat matematika dengan tanda &ldquo;=&rdquo; yang hanya memuat <b>satu variabel</b> berpangkat <b>satu</b>.</p>
      <table style="margin-top:10px">
        <tr><th>Persamaan</th><th>PLSV?</th><th>Alasan</th></tr>
        <tr><td>2x + 3 = 11</td><td>Ya</td><td>Satu variabel, pangkat 1</td></tr>
        <tr><td>x² − 4 = 0</td><td>Bukan</td><td>Pangkat 2</td></tr>
        <tr><td>x + y = 7</td><td>Bukan</td><td>Dua variabel</td></tr>
        <tr><td>5(a − 2) = 15</td><td>Ya</td><td>Satu variabel, pangkat 1</td></tr>
      </table>
    </div>
    <div class="card">
      <div class="kicker">2 · Sifat kesetaraan</div>
      <h2>Jaga timbangan tetap seimbang</h2>
      <p>Persamaan tetap benar jika kedua ruas diberi perlakuan yang sama:</p>
      <ul style="padding-left:1.2em">
        <li><b>Ditambah</b> bilangan yang sama</li>
        <li><b>Dikurangi</b> bilangan yang sama</li>
        <li><b>Dikali</b> bilangan yang sama</li>
        <li><b>Dibagi</b> bilangan yang sama, kecuali nol</li>
      </ul>
      <div class="callout">Tujuan akhirnya: membuat variabel sendirian di satu ruas, yaitu x = &hellip;</div>
    </div>
  </div>

  <div class="card">
    <div class="kicker">3 · Contoh langkah penyelesaian</div>
    <h2>Selesaikan 3x + 5 = 20</h2>
    <div class="grid3" style="margin-top:14px">
      <div class="stack"><div class="eq">3x + 5 = 20</div><p class="kicker">Persamaan awal</p></div>
      <div class="stack"><div class="eq">3x + 5 − 5 = 20 − 5<br>3x = 15</div><p class="kicker">Kurangi 5 di kedua ruas</p></div>
      <div class="stack"><div class="eq">3x ÷ 3 = 15 ÷ 3<br><span class="x">x = 5</span></div><p class="kicker">Bagi 3 di kedua ruas</p></div>
    </div>
    <div class="ok" style="margin-top:14px"><b>Periksa:</b> 3(5) + 5 = 15 + 5 = 20. Ruas kiri sama dengan ruas kanan, jadi x = 5 benar.</div>
  </div>

  <div class="grid2">
    <div class="card">
      <div class="kicker">4 · Tabel nilai</div>
      <h2>Mencari x yang membuat 2x + 3 = 11</h2>
      <div class="scroll"><table>
        <tr><th class="n">x</th><th class="n">2x + 3</th><th>Dibanding 11</th></tr>
        <tr><td class="n">0</td><td class="n">3</td><td>lebih kecil</td></tr>
        <tr><td class="n">1</td><td class="n">5</td><td>lebih kecil</td></tr>
        <tr><td class="n">2</td><td class="n">7</td><td>lebih kecil</td></tr>
        <tr><td class="n">3</td><td class="n">9</td><td>lebih kecil</td></tr>
        <tr style="background:var(--good-soft)"><td class="n"><b>4</b></td><td class="n"><b>11</b></td><td><b>sama (=)</b></td></tr>
        <tr><td class="n">5</td><td class="n">13</td><td>lebih besar</td></tr>
        <tr><td class="n">6</td><td class="n">15</td><td>lebih besar</td></tr>
      </table></div>
    </div>
    <div class="card">
      <div class="kicker">5 · Grafik</div>
      <h2>Titik potong dua garis</h2>
      <svg id="gMat" viewBox="0 0 460 320" width="100%" role="img" aria-label="Grafik garis y = 2x + 3 dan y = 11 berpotongan di x = 4"></svg>
      <p>Penyelesaian PLSV adalah nilai x tempat garis y = 2x + 3 bertemu garis y = 11, yaitu <b>x = 4</b>.</p>
    </div>
  </div>

  <div class="card">
    <div class="kicker">6 · Dari cerita ke persamaan</div>
    <h2>Empat langkah membuat model matematika</h2>
    <div class="grid2" style="margin-top:12px">
      <div class="stack">
        <div class="step"><b>1</b><div><b>Pahami.</b> Apa yang diketahui dan apa yang ditanyakan?</div></div>
        <div class="step"><b>2</b><div><b>Pilih variabel.</b> Misalkan yang ditanya sebagai x.</div></div>
        <div class="step"><b>3</b><div><b>Susun persamaan</b> dari hubungan dalam cerita.</div></div>
        <div class="step"><b>4</b><div><b>Selesaikan dan periksa,</b> lalu jawab dalam kalimat.</div></div>
      </div>
      <div class="callout"><b>Contoh.</b> &ldquo;Tarif ojek Rp8.000 ditambah Rp3.000 tiap km. Bu Ani membayar Rp29.000.&rdquo;<br>
        Misal jarak = x km. Model: <b>8.000 + 3.000x = 29.000</b>. Maka 3.000x = 21.000, sehingga x = 7. Jaraknya 7 km.</div>
    </div>
  </div>

  <div class="card">
    <div class="kicker">7 · Perluasan</div>
    <h2>Pertidaksamaan linear satu variabel</h2>
    <p>Tanda &ldquo;=&rdquo; diganti <b>&lt;</b>, <b>&gt;</b>, <b>≤</b>, atau <b>≥</b>. Hasilnya berupa banyak nilai, bukan satu nilai. Contoh: x + 3 &lt; 8 berarti x &lt; 5.</p>
    <div class="grid2" style="margin-top:10px">
      <div class="stack">
        <p>Atur tanda dan batasnya, lihat garis bilangannya:</p>
        <div class="row" id="signBtns">
          <button class="btn sm alt" data-s="<">x &lt; b</button><button class="btn sm alt" data-s="<=">x ≤ b</button>
          <button class="btn sm alt" data-s=">">x &gt; b</button><button class="btn sm alt" data-s=">=">x ≥ b</button>
        </div>
        <label for="thr">Batas b = <b id="thrVal">5</b></label>
        <input type="range" id="thr" min="-5" max="10" value="5">
        <div class="eq" id="ineqText">x &lt; 5</div>
      </div>
      <div><svg id="nl" viewBox="0 0 480 110" width="100%" role="img" aria-label="Garis bilangan penyelesaian pertidaksamaan"></svg>
        <p class="kicker">Lingkaran kosong: batas tidak termasuk. Lingkaran penuh: batas termasuk.</p></div>
    </div>
    <div class="no" style="margin-top:12px"><b>Awas.</b> Jika kedua ruas dikali atau dibagi bilangan <u>negatif</u>, tanda pertidaksamaan dibalik. Contoh: −2x &lt; 6 menjadi x &gt; −3.</div>
  </div>
</div></section>

<!-- SIMULASI -->
<section class="view" id="v-simulasi"><div class="stack">
  <div class="row"><h2>Simulasi timbangan persamaan</h2></div>
  <div class="row" id="presets" aria-label="Pilih persamaan"></div>
  <div class="grid2">
    <div class="card">
      <div class="kicker">Kegiatan 1 · Coba-coba nilai x</div>
      <svg id="bal" viewBox="0 0 440 280" width="100%" role="img" aria-label="Timbangan persamaan"></svg>
      <label for="xs">Nilai x = <b id="xv">0</b></label>
      <input type="range" id="xs" min="-5" max="15" step="1" value="0">
      <div id="balMsg" class="callout" aria-live="polite"></div>
      <p class="kicker" style="margin-top:10px">Geser x sampai timbangan seimbang. Catat nilai x di buku tulis.</p>
    </div>
    <div class="card stack">
      <div class="kicker">Kegiatan 2 · Langkah penyelesaian</div>
      <div class="eq" id="stepEq" aria-live="polite"></div>
      <div class="row">
        <label for="opN">Bilangan n =</label><input type="number" id="opN" value="1" step="1">
      </div>
      <div class="row">
        <button class="btn sm" data-op="add">Tambah n</button><button class="btn sm" data-op="sub">Kurang n</button>
        <button class="btn sm" data-op="mul">Kali n</button><button class="btn sm" data-op="div">Bagi n</button>
      </div>
      <div class="row"><button class="btn sm alt" id="undo">Urungkan</button><button class="btn sm alt" id="resetSteps">Ulangi dari awal</button></div>
      <div id="stepMsg" aria-live="polite"></div>
      <ol id="hist" style="margin:0;padding-left:1.4em"></ol>
      <p class="kicker">Setiap operasi diterapkan ke <b>kedua ruas</b> sekaligus. Selesai jika bentuknya x = &hellip;</p>
    </div>
  </div>
  <div class="card"><h3>Diskusikan berpasangan</h3>
    <p>1) Mengapa timbangan miring saat x kurang atau lebih dari nilai penyelesaian? 2) Operasi apa yang pertama kali kamu pilih, dan mengapa? 3) Bagaimana kamu memastikan hasilnya benar tanpa timbangan?</p></div>
</div></section>

<!-- MASALAH PBL -->
<section class="view" id="v-masalah"><div class="stack">
  <div class="row"><h2>Masalah nyata untuk kelompok</h2></div>
  <p>Setiap kelompok memilih satu masalah (A–D). Kerjakan LKPD berurutan, lalu siapkan presentasi 3 menit.</p>
  <div class="row" id="pbBtns" aria-label="Pilih masalah"></div>
  <div id="pbBody" class="stack"></div>
</div></section>

<!-- KUIS -->
<section class="view" id="v-kuis"><div class="stack">
  <h2>Kuis interaktif tim</h2>
  <div class="card">
    <div class="kicker">Papan skor (Numbered Heads Together: guru memanggil nomor, wakil tim menjawab)</div>
    <div class="grid3" id="board" style="margin-top:10px"></div>
    <div class="row" style="margin-top:10px"><button class="btn sm alt" id="boardReset">Setel ulang skor tim</button></div>
  </div>
  <div class="card" id="quiz"></div>
</div></section>

<!-- REFLEKSI -->
<section class="view" id="v-refleksi"><div class="stack">
  <h2>Refleksi dan penutup</h2>
  <div class="grid2">
    <div class="card stack">
      <h3>Seberapa yakin kamu sekarang?</h3>
      <p class="kicker">1 = belum paham · 4 = bisa menjelaskan ke teman</p>
      <div id="selfBox" class="stack"></div>
      <button class="btn" id="selfGo">Lihat ringkasan</button>
      <div id="selfOut" aria-live="polite"></div>
    </div>
    <div class="card stack">
      <h3>Pertanyaan refleksi</h3>
      <div class="step"><b>1</b><div>Apa kesalahan awal yang kamu atau timmu buat, dan bagaimana memperbaikinya?</div></div>
      <div class="step"><b>2</b><div>Mengapa kedua ruas harus diperlakukan sama? Jelaskan dengan gambar timbangan.</div></div>
      <div class="step"><b>3</b><div>Di mana lagi kamu akan memakai persamaan seperti ini di luar kelas?</div></div>
      <div class="step"><b>4</b><div>Apa yang membuat kerja kelompok hari ini berjalan baik atau kurang baik?</div></div>
    </div>
  </div>
  <div class="card scroll">
    <h3 style="margin-bottom:10px">Rubrik penilaian presentasi kelompok</h3>
    <table>
      <tr><th>Aspek</th><th>Perlu bimbingan (1)</th><th>Cakap (2)</th><th>Mahir (3)</th></tr>
      <tr><td>Model matematika</td><td>Persamaan belum sesuai cerita</td><td>Persamaan sesuai, variabel kurang jelas</td><td>Variabel dan persamaan tepat dan jelas</td></tr>
      <tr><td>Penyelesaian</td><td>Langkah banyak yang keliru</td><td>Benar, alasan tiap langkah belum disebut</td><td>Benar dan tiap langkah beralasan sifat kesetaraan</td></tr>
      <tr><td>Pemeriksaan dan tafsir</td><td>Tidak memeriksa</td><td>Memeriksa tanpa menjawab kalimat</td><td>Memeriksa dan menjawab sesuai konteks</td></tr>
      <tr><td>Kerja sama</td><td>Satu orang mengerjakan</td><td>Sebagian ikut</td><td>Semua berperan dan saling membantu</td></tr>
    </table>
  </div>
  <div class="callout"><b>Tindak lanjut:</b> Buat satu soal cerita dari kehidupanmu yang modelnya berbentuk ax + b = c, lalu tukarkan dengan temanmu untuk diselesaikan.</div>
</div></section>
</div>
<script>
(function(){
const $=(s,r=document)=>r.querySelector(s), $$=(s,r=document)=>[...r.querySelectorAll(s)];
const NAMES=['alur','pemantik','apersepsi','materi','simulasi','masalah','kuis','refleksi'];

/* Navigasi tab lewat hash */
function route(){
  let h=(location.hash||'').replace('#','');
  if(!NAMES.includes(h)) h='alur';
  NAMES.forEach(n=>$('#v-'+n).classList.toggle('on',n===h));
  $$('nav.tabs a').forEach(a=>{ if(a.getAttribute('href')==='#'+h) a.setAttribute('aria-current','page'); else a.removeAttribute('aria-current'); });
  window.scrollTo(0,0);
}
window.addEventListener('hashchange',route); route();

/* Timer kelas */
let secs=300, run=null;
const tmr=$('#tmr'), go=$('#tmrGo');
const fmt=s=>String(Math.floor(s/60)).padStart(2,'0')+':'+String(s%60).padStart(2,'0');
function beep(){ try{ const c=new (window.AudioContext||window.webkitAudioContext)(); const o=c.createOscillator(); o.frequency.value=880; o.connect(c.destination); o.start(); setTimeout(()=>{o.stop();c.close();},500);}catch(e){} }
function showT(){ tmr.textContent=fmt(secs); }
function stopT(){ clearInterval(run); run=null; go.textContent='Mulai'; }
$$('[data-t]').forEach(b=>b.addEventListener('click',()=>{ stopT(); secs=+b.dataset.t; tmr.style.color=''; showT(); }));
go.addEventListener('click',()=>{
  if(run){ stopT(); return; }
  if(secs<=0) return;
  go.textContent='Jeda';
  run=setInterval(()=>{ secs--; showT(); if(secs<=0){ stopT(); tmr.textContent='Waktu!'; tmr.style.color='var(--bad)'; beep(); } },1000);
});
showT();

/* Pemantik */
$('#revealJeruk').addEventListener('click',()=>{ $('#jerukAns').hidden=false; });

/* Apersepsi: tebak nilai */
$$('.mini').forEach(m=>{
  const inp=$('input',m), fb=$('.fb',m);
  const check=()=>{
    if(inp.value==='') { fb.textContent=''; return; }
    const ok=Number(inp.value)===Number(m.dataset.ans);
    fb.textContent=ok?'Benar':'Coba lagi';
    fb.style.color=ok?'var(--good)':'var(--bad)'; fb.style.fontWeight='700';
  };
  $('button',m).addEventListener('click',check);
  inp.addEventListener('keydown',e=>{ if(e.key==='Enter') check(); });
});

/* Grafik garis sederhana */
function chart(svg,o){
  const W=o.W||460,H=o.H||320,l=64,r=18,t=18,b=46;
  const sx=x=>l+(x-o.xmin)/(o.xmax-o.xmin)*(W-l-r), sy=y=>H-b-(y-o.ymin)/(o.ymax-o.ymin)*(H-t-b);
  svg.setAttribute('viewBox',`0 0 ${W} ${H}`);
  let s='';
  for(let x=o.xmin;x<=o.xmax+1e-9;x+=o.xs){ s+=`<line x1="${sx(x)}" y1="${t}" x2="${sx(x)}" y2="${H-b}" style="stroke:var(--line)" stroke-width="1"/><text x="${sx(x)}" y="${H-b+20}" text-anchor="middle" font-size="14">${x}</text>`; }
  for(let y=o.ymin;y<=o.ymax+1e-9;y+=o.ys){ s+=`<line x1="${l}" y1="${sy(y)}" x2="${W-r}" y2="${sy(y)}" style="stroke:var(--line)" stroke-width="1"/><text x="${l-8}" y="${sy(y)+5}" text-anchor="end" font-size="14">${o.fy?o.fy(y):y}</text>`; }
  s+=`<line x1="${l}" y1="${H-b}" x2="${W-r}" y2="${H-b}" style="stroke:var(--fg)" stroke-width="2"/><line x1="${l}" y1="${t}" x2="${l}" y2="${H-b}" style="stroke:var(--fg)" stroke-width="2"/>`;
  if(o.xl) s+=`<text x="${(l+W-r)/2}" y="${H-6}" text-anchor="middle" font-size="14" font-weight="700">${o.xl}</text>`;
  if(o.hline!=null) s+=`<line x1="${l}" y1="${sy(o.hline)}" x2="${W-r}" y2="${sy(o.hline)}" style="stroke:var(--amber)" stroke-width="3" stroke-dasharray="8 6"/>`;
  (o.lines||[]).forEach(L=>{ s+=`<line x1="${sx(o.xmin)}" y1="${sy(L.f(o.xmin))}" x2="${sx(o.xmax)}" y2="${sy(L.f(o.xmax))}" style="stroke:${L.c}" stroke-width="4" stroke-linecap="round"/>`; });
  if(o.mark){ const mx=sx(o.mark.x),my=sy(o.mark.y);
    s+=`<line x1="${mx}" y1="${my}" x2="${mx}" y2="${H-b}" style="stroke:var(--good)" stroke-width="2" stroke-dasharray="4 4"/><circle cx="${mx}" cy="${my}" r="8" style="fill:var(--good)"/><text x="${mx+(o.mark.dx||12)}" y="${my+(o.mark.dy||-12)}" font-size="15" font-weight="700" style="fill:var(--good)">${o.mark.t}</text>`; }
  let ly=t+16; (o.legend||[]).forEach(L=>{ s+=`<rect x="${l+10}" y="${ly-11}" width="14" height="14" rx="3" style="fill:${L.c}"/><text x="${l+30}" y="${ly+1}" font-size="14">${L.t}</text>`; ly+=20; });
  svg.innerHTML=s;
}
window.__chart=chart;

chart($('#gMat'),{xmin:0,xmax:6,ymin:0,ymax:16,xs:1,ys:4,xl:'x',
  lines:[{f:x=>2*x+3,c:'var(--ink)'}],hline:11,mark:{x:4,y:11,t:'x = 4',dx:10,dy:26},
  legend:[{c:'var(--ink)',t:'y = 2x + 3'},{c:'var(--amber)',t:'y = 11'}]});

/* Garis bilangan pertidaksamaan */
let sign='<';
function drawNL(){
  const b=+$('#thr').value, svg=$('#nl'); $('#thrVal').textContent=b;
  const lo=-6,hi=12,x0=24,x1=456, sx=v=>x0+(v-lo)/(hi-lo)*(x1-x0), y=56;
  const sym={'<':'<','<=':'≤','>':'>','>=':'≥'}[sign];
  $('#ineqText').textContent='x '+sym+' '+b;
  const incl=sign.includes('='), left=sign.startsWith('<');
  let s=`<line x1="8" y1="${y}" x2="472" y2="${y}" style="stroke:var(--fg)" stroke-width="2"/><path d="M472 ${y} l-9 -5 v10z" style="fill:var(--fg)"/><path d="M8 ${y} l9 -5 v10z" style="fill:var(--fg)"/>`;
  for(let v=lo;v<=hi;v++){ s+=`<line x1="${sx(v)}" y1="${y-5}" x2="${sx(v)}" y2="${y+5}" style="stroke:var(--fg)" stroke-width="1.5"/>`; if(v%2===0) s+=`<text x="${sx(v)}" y="${y+26}" text-anchor="middle" font-size="13">${v}</text>`; }
  const end=left?8:472;
  s+=`<line x1="${sx(b)}" y1="${y}" x2="${end}" y2="${y}" style="stroke:var(--amber)" stroke-width="7" stroke-linecap="round"/>`;
  s+=`<circle cx="${sx(b)}" cy="${y}" r="8" stroke-width="3" style="stroke:var(--amber);fill:${incl?'var(--amber)':'var(--surface)'}"/>`;
  svg.innerHTML=s;
}
$$('#signBtns button').forEach(bt=>bt.addEventListener('click',()=>{ sign=bt.dataset.s; drawNL(); }));
$('#thr').addEventListener('input',drawNL); drawNL();
})();
</script>
<script>
(function(){
const $=(s,r=document)=>r.querySelector(s), $$=(s,r=document)=>[...r.querySelectorAll(s)];
const chart=window.__chart;

/* Pecahan sederhana untuk tampilan */
function fr(n){
  if(Math.abs(n-Math.round(n))<1e-9) return String(Math.round(n));
  for(let q=2;q<=12;q++){ const p=n*q; if(Math.abs(p-Math.round(p))<1e-9) return Math.round(p)+'/'+q; }
  return String(Math.round(n*100)/100);
}
const minus=s=>s.replace('-','−');
function eqText(A,B,C){
  let l=(A===1?'x':A===-1?'−x':minus(fr(A))+'x');
  if(Math.abs(B)>1e-9) l+=(B>0?' + ':' − ')+fr(Math.abs(B));
  return `<span class="x">${l.replace(/x/g,'x')}</span> = ${minus(fr(C))}`.replace('<span class="x">','<span>');
}

/* SIMULASI */
const PRE=[{a:1,b:3,c:8},{a:2,b:1,c:11},{a:3,b:-4,c:14},{a:4,b:5,c:-7},{a:5,b:-10,c:25}];
let cur=PRE[0], hist=[], st={A:1,B:3,C:8};
const lbl=p=>minus((p.a===1?'x':p.a+'x')+(p.b>0?' + '+p.b:' − '+Math.abs(p.b))+' = '+p.c);
const presets=$('#presets');
PRE.forEach((p,i)=>{ const b=document.createElement('button'); b.className='btn sm alt'; b.textContent=lbl(p); b.dataset.i=i;
  b.addEventListener('click',()=>pick(i)); presets.appendChild(b); });
function pick(i){
  cur=PRE[i]; $$('#presets button').forEach((b,j)=>{ b.className='btn sm'+(j===i?'':' alt'); });
  $('#xs').value=0; resetSteps(); drawBal();
}
function drawBal(){
  const x=+$('#xs').value; $('#xv').textContent=minus(String(x));
  const L=cur.a*x+cur.b, R=cur.c, d=L-R;
  const deg=-Math.max(-14,Math.min(14,d*1.5)), th=deg*Math.PI/180, h=140, px=220, py=70;
  const lx=px-h*Math.cos(th), ly=py-h*Math.sin(th), rx=px+h*Math.cos(th), ry=py+h*Math.sin(th);
  const pan=(cx,cy,t1,t2,col)=>`<g class="pan" transform="translate(${cx} ${cy})"><line x1="0" y1="0" x2="-48" y2="92" style="stroke:var(--ink)" stroke-width="2"/><line x1="0" y1="0" x2="48" y2="92" style="stroke:var(--ink)" stroke-width="2"/><rect x="-58" y="90" width="116" height="10" rx="5" style="fill:var(--ink)"/><rect x="-44" y="${72-Math.min(60,Math.abs(t2)*3)}" width="88" height="${18+Math.min(60,Math.abs(t2)*3)}" rx="8" style="fill:${col};opacity:.9"/><text x="0" y="124" text-anchor="middle" font-size="15" font-weight="700">${t1}</text></g>`;
  $('#bal').innerHTML=
    `<rect x="212" y="${py}" width="16" height="170" rx="6" style="fill:var(--muted)"/><rect x="150" y="238" width="140" height="14" rx="7" style="fill:var(--muted)"/>`+
    `<line x1="${lx}" y1="${ly}" x2="${rx}" y2="${ry}" style="stroke:var(--ink)" stroke-width="12" stroke-linecap="round"/><circle cx="${px}" cy="${py}" r="11" style="fill:var(--amber)"/>`+
    pan(lx,ly,minus(`${cur.a===1?'':cur.a}x${cur.b>0?'+':'−'}${Math.abs(cur.b)} = ${L}`),L,'var(--amber)')+
    pan(rx,ry,minus(String(R)),R,'var(--ink)');
  const m=$('#balMsg');
  if(d===0){ m.className='ok'; m.textContent=minus(`Seimbang. x = ${x} membuat ruas kiri (${L}) sama dengan ruas kanan (${R}).`); }
  else { m.className='callout'; m.textContent=minus(`Ruas kiri = ${L}, ruas kanan = ${R}. Ruas ${d>0?'kiri lebih berat':'kanan lebih berat'}. Ubah x.`); }
}
$('#xs').addEventListener('input',drawBal);

function showSteps(){
  $('#stepEq').innerHTML=eqText(st.A,st.B,st.C);
  $('#hist').innerHTML=hist.map(h=>`<li>${h.d}: <b>${h.e}</b></li>`).join('');
  const m=$('#stepMsg');
  if(Math.abs(st.A-1)<1e-9 && Math.abs(st.B)<1e-9){
    const v=st.C, ok=Math.abs(cur.a*v+cur.b-cur.c)<1e-9;
    m.className='ok'; m.innerHTML=`<b>Selesai: x = ${minus(fr(v))}.</b> Periksa: ${minus(`${cur.a===1?'':cur.a}(${fr(v)}) ${cur.b>0?'+':'−'} ${Math.abs(cur.b)} = ${fr(cur.a*v+cur.b)}`)}, sama dengan ${minus(String(cur.c))}. ${ok?'Benar.':''}`;
  } else { m.className=''; m.textContent=''; }
}
function resetSteps(){ st={A:cur.a,B:cur.b,C:cur.c}; hist=[]; showSteps(); }
const OPN={add:'Tambah',sub:'Kurang',mul:'Kali',div:'Bagi'};
$$('[data-op]').forEach(b=>b.addEventListener('click',()=>{
  const n=Number($('#opN').value), op=b.dataset.op, m=$('#stepMsg');
  if(!isFinite(n)||$('#opN').value===''){ m.className='no'; m.textContent='Isi bilangan n lebih dulu.'; return; }
  if((op==='mul'||op==='div')&&n===0){ m.className='no'; m.textContent='Tidak boleh mengalikan atau membagi dengan nol.'; return; }
  hist.push({s:{...st},d:`${OPN[op]} ${minus(String(n))} di kedua ruas`,e:''});
  if(op==='add'){st.B+=n;st.C+=n;} if(op==='sub'){st.B-=n;st.C-=n;}
  if(op==='mul'){st.A*=n;st.B*=n;st.C*=n;} if(op==='div'){st.A/=n;st.B/=n;st.C/=n;}
  hist[hist.length-1].e=eqText(st.A,st.B,st.C).replace(/<[^>]+>/g,'');
  showSteps();
}));
$('#undo').addEventListener('click',()=>{ const h=hist.pop(); if(h){ st=h.s; showSteps(); } });
$('#resetSteps').addEventListener('click',resetSteps);
pick(0);

/* MASALAH PBL */
const nf=n=>Number.isInteger(n)?n.toLocaleString('id-ID'):n.toLocaleString('id-ID',{maximumFractionDigits:2});
const rb=y=>'Rp'+y+'rb';
const PB=[
 {k:'A',t:'Tarif ojek online',lvl:'Dasar',
  story:'Tarif ojek online terdiri dari tarif dasar Rp8.000 ditambah Rp3.000 untuk setiap kilometer. Bu Ani membayar Rp29.000 untuk sekali perjalanan. Berapa kilometer jarak perjalanan Bu Ani?',
  vars:'x = jarak perjalanan (km)', model:'8.000 + 3.000x = 29.000', ans:7, unit:'km',
  steps:['3.000x = 29.000 − 8.000 = 21.000','x = 21.000 ÷ 3.000 = 7'], check:'8.000 + 3.000(7) = 8.000 + 21.000 = 29.000', sent:'Jarak perjalanan Bu Ani adalah 7 km.',
  cols:['Biaya (Rp)'], fns:[x=>8000+3000*x],
  ch:{xmin:0,xmax:10,ymin:0,ymax:40,xs:1,ys:10,fy:rb,xl:'Jarak (km)',lines:[{f:x=>8+3*x,c:'var(--ink)'}],hline:29,mark:{x:7,y:29,t:'7 km',dx:10,dy:26},legend:[{c:'var(--ink)',t:'Biaya = 8.000 + 3.000x'},{c:'var(--amber)',t:'Dibayar Rp29.000'}]}},
 {k:'B',t:'Menabung sepatu',lvl:'Dasar',
  story:'Rina memiliki tabungan Rp50.000. Setiap minggu ia menabung Rp15.000 untuk membeli sepatu seharga Rp200.000. Setelah berapa minggu uang Rina cukup untuk membeli sepatu itu?',
  vars:'x = banyak minggu menabung', model:'50.000 + 15.000x = 200.000', ans:10, unit:'minggu',
  steps:['15.000x = 200.000 − 50.000 = 150.000','x = 150.000 ÷ 15.000 = 10'], check:'50.000 + 15.000(10) = 50.000 + 150.000 = 200.000', sent:'Uang Rina cukup setelah 10 minggu.',
  cols:['Tabungan (Rp)'], fns:[x=>50000+15000*x],
  ch:{xmin:0,xmax:14,ymin:0,ymax:260,xs:2,ys:50,fy:rb,xl:'Minggu ke-',lines:[{f:x=>50+15*x,c:'var(--ink)'}],hline:200,mark:{x:10,y:200,t:'10 minggu',dx:-110,dy:26},legend:[{c:'var(--ink)',t:'Tabungan = 50.000 + 15.000x'},{c:'var(--amber)',t:'Harga sepatu Rp200.000'}]}},
 {k:'C',t:'Kebun persegi panjang',lvl:'Menengah',
  story:'Sebuah kebun berbentuk persegi panjang. Panjangnya (2x + 3) meter dan lebarnya x meter. Keliling kebun 36 meter. Tentukan x, lalu panjang dan lebar kebun.',
  vars:'x = lebar kebun (m)', model:'2((2x + 3) + x) = 36', ans:5, unit:'m',
  steps:['2(3x + 3) = 36, sehingga 6x + 6 = 36','6x = 30, sehingga x = 5','Panjang = 2(5) + 3 = 13 m, lebar = 5 m'], check:'Keliling = 2(13 + 5) = 36 m', sent:'x = 5. Panjang kebun 13 m dan lebarnya 5 m.',
  cols:['Keliling (m)'], fns:[x=>6*x+6],
  ch:{xmin:0,xmax:8,ymin:0,ymax:60,xs:1,ys:10,xl:'Nilai x (m)',lines:[{f:x=>6*x+6,c:'var(--ink)'}],hline:36,mark:{x:5,y:36,t:'x = 5',dx:10,dy:26},legend:[{c:'var(--ink)',t:'Keliling = 6x + 6'},{c:'var(--amber)',t:'Keliling 36 m'}]}},
 {k:'D',t:'Memilih paket data',lvl:'Tantangan',
  story:'Paket A: Rp10.000 ditambah Rp2.000 per GB. Paket B: Rp4.000 ditambah Rp3.500 per GB. Pada pemakaian berapa GB biaya kedua paket sama? Paket mana yang lebih hemat jika kamu memakai 10 GB?',
  vars:'x = pemakaian data (GB)', model:'10.000 + 2.000x = 4.000 + 3.500x', ans:4, unit:'GB',
  steps:['10.000 − 4.000 = 3.500x − 2.000x','6.000 = 1.500x, sehingga x = 4','Untuk 10 GB: A = 30.000, B = 39.000, jadi Paket A lebih hemat'], check:'A: 10.000 + 2.000(4) = 18.000 dan B: 4.000 + 3.500(4) = 18.000', sent:'Biaya sama pada 4 GB. Untuk 10 GB, Paket A lebih hemat (Rp30.000 dibanding Rp39.000).',
  cols:['Paket A (Rp)','Paket B (Rp)'], fns:[x=>10000+2000*x,x=>4000+3500*x],
  ch:{xmin:0,xmax:8,ymin:0,ymax:40,xs:1,ys:10,fy:rb,xl:'Pemakaian (GB)',lines:[{f:x=>10+2*x,c:'var(--ink)'},{f:x=>4+3.5*x,c:'var(--amber)'}],mark:{x:4,y:18,t:'sama di 4 GB',dx:12,dy:28},legend:[{c:'var(--ink)',t:'Paket A'},{c:'var(--amber)',t:'Paket B'}]}}
];
const bt=$('#pbBtns'), body=$('#pbBody');
PB.forEach((p,i)=>{ const b=document.createElement('button'); b.className='btn sm alt'; b.textContent=`${p.k} · ${p.t}`; b.addEventListener('click',()=>showPB(i)); bt.appendChild(b); });
function showPB(i){
  const p=PB[i]; $$('#pbBtns button').forEach((b,j)=>{ b.className='btn sm'+(j===i?'':' alt'); });
  const xs=[]; for(let x=Math.max(0,p.ans-2);x<=p.ans+2;x++) xs.push(x);
  body.innerHTML=`
  <div class="card"><div class="row"><span class="chip">Tingkat: ${p.lvl}</span></div>
    <h3 style="margin:8px 0">Kelompok ${p.k}: ${p.t}</h3><p class="lead">${p.story}</p></div>
  <div class="grid2">
    <div class="card stack">
      <div class="kicker">LKPD</div>
      <div class="step"><b>1</b><div><b>Pahami.</b> Tulis yang diketahui dan yang ditanyakan dengan kata-katamu sendiri.</div></div>
      <div class="step"><b>2</b><div><b>Variabel.</b> Tentukan lambang untuk yang belum diketahui.
        <details style="margin-top:6px"><summary>Lihat contoh</summary>${p.vars}</details></div></div>
      <div class="step"><b>3</b><div><b>Model.</b> Susun persamaan dari ceritanya.
        <details style="margin-top:6px"><summary>Periksa modelmu</summary><b>${p.model}</b></details></div></div>
      <div class="step"><b>4</b><div><b>Selesaikan.</b> Tulis tiap langkah beserta sifat kesetaraannya.
        <div class="row" style="margin-top:8px"><label for="pbIn">x =</label><input type="number" id="pbIn" step="any"><button class="btn sm" id="pbChk">Periksa</button></div>
        <div id="pbFb" aria-live="polite" style="margin-top:8px"></div>
        <details style="margin-top:8px"><summary>Lihat langkah penyelesaian</summary><ol style="margin:6px 0;padding-left:1.3em">${p.steps.map(s=>`<li>${s}</li>`).join('')}</ol></details></div></div>
      <div class="step"><b>5</b><div><b>Periksa dan tafsir.</b> Substitusikan hasilnya, lalu jawab dalam kalimat.
        <details style="margin-top:6px"><summary>Lihat pemeriksaan</summary>${p.check}<br><b>${p.sent}</b></details></div></div>
      <div class="callout"><b>Pengembangan:</b> Ubah angka pada ceritamu, lalu tentukan sendiri jawaban barunya. Apa yang berubah pada grafik?</div>
    </div>
    <div class="card">
      <div class="kicker">Visual pendukung</div>
      <svg id="pbChart" viewBox="0 0 460 320" width="100%" role="img" aria-label="Grafik untuk masalah ${p.k}"></svg>
      <div class="scroll"><table style="margin-top:8px"><tr><th class="n">x (${p.unit})</th>${p.cols.map(c=>`<th class="n">${c}</th>`).join('')}</tr>
      ${xs.map(x=>`<tr${x===p.ans?' style="background:var(--good-soft)"':''}><td class="n">${x}</td>${p.fns.map(f=>`<td class="n">${nf(f(x))}</td>`).join('')}</tr>`).join('')}</table></div>
    </div>
  </div>`;
  chart($('#pbChart'),p.ch);
  const chk=()=>{ const v=$('#pbIn').value, fb=$('#pbFb'); if(v==='') return;
    if(Math.abs(Number(v)-p.ans)<1e-9){ fb.className='ok'; fb.textContent=`Benar, x = ${p.ans}. Lanjutkan ke langkah 5.`; }
    else { fb.className='no'; fb.textContent='Belum tepat. Periksa model dan setiap langkahmu, lalu coba lagi.'; } };
  $('#pbChk').addEventListener('click',chk); $('#pbIn').addEventListener('keydown',e=>{ if(e.key==='Enter') chk(); });
}
showPB(0);
})();
</script>
<script>
(function(){
const $=(s,r=document)=>r.querySelector(s), $$=(s,r=document)=>[...r.querySelectorAll(s)];

/* Papan skor tim */
const teams=['Tim 1','Tim 2','Tim 3','Tim 4'], pts=[0,0,0,0];
function drawBoard(){
  $('#board').innerHTML=teams.map((t,i)=>`<div class="card" style="padding:14px;text-align:center"><div class="kicker">${t}</div>
    <div class="eq" aria-live="polite">${pts[i]}</div>
    <div class="row" style="justify-content:center;margin-top:6px"><button class="btn sm alt" data-i="${i}" data-d="-1" aria-label="Kurangi skor ${t}">−1</button><button class="btn sm" data-i="${i}" data-d="1" aria-label="Tambah skor ${t}">+1</button></div></div>`).join('');
  $$('#board button').forEach(b=>b.addEventListener('click',()=>{ pts[+b.dataset.i]=Math.max(0,pts[+b.dataset.i]+ +b.dataset.d); drawBoard(); }));
}
$('#boardReset').addEventListener('click',()=>{ pts.fill(0); drawBoard(); });
drawBoard();

/* Kuis */
const Q=[
 {q:'Manakah yang merupakan persamaan linear satu variabel?',o:['x² + 2 = 11','3x − 4 = 11','x + y = 5','2x + 3'],a:1,e:'3x − 4 = 11 punya tanda "=", satu variabel, dan pangkat 1. Pilihan lain berpangkat 2, dua variabel, atau bukan persamaan.'},
 {q:'Penyelesaian dari 4x − 7 = 21 adalah ...',o:['x = 3,5','x = 7','x = 14','x = 28'],a:1,e:'Tambah 7: 4x = 28. Bagi 4: x = 7.'},
 {q:'Penyelesaian dari 5(x − 2) = 3x + 6 adalah ...',o:['x = 2','x = 4','x = 8','x = 16'],a:2,e:'5x − 10 = 3x + 6, maka 2x = 16, sehingga x = 8.'},
 {q:'Dari 2x = 14 diperoleh x = 7. Sifat kesetaraan yang dipakai adalah ...',o:['Kedua ruas dikurangi 2','Kedua ruas dikali 2','Kedua ruas dibagi 2','Kedua ruas ditambah 2'],a:2,e:'Koefisien x adalah 2, jadi kedua ruas dibagi 2.'},
 {q:'Model matematika untuk "dua kali suatu bilangan dikurangi 5 hasilnya 17" adalah ...',o:['2x + 5 = 17','2(x − 5) = 17','2x − 5 = 17','x − 10 = 17'],a:2,e:'Dua kali bilangan ditulis 2x, lalu dikurangi 5: 2x − 5 = 17. Bilangannya 11.'},
 {q:'Pak Budi membeli 4 buku dan 1 pulpen Rp3.000. Ia membayar Rp27.000. Harga satu buku adalah ...',o:['Rp4.500','Rp6.000','Rp7.500','Rp24.000'],a:1,e:'Misal harga buku x: 4x + 3.000 = 27.000, maka 4x = 24.000, sehingga x = 6.000.'},
 {q:'Bilangan bulat terbesar yang memenuhi 2x − 3 < 7 adalah ...',o:['3','4','5','6'],a:1,e:'2x < 10, maka x < 5. Bilangan bulat terbesar yang kurang dari 5 adalah 4.'},
 {q:'Penyelesaian dari −3x ≥ 12 adalah ...',o:['x ≥ −4','x ≤ −4','x ≥ 4','x ≤ 4'],a:1,e:'Dibagi −3 (bilangan negatif), tanda dibalik: x ≤ −4.'}
];
let qi=0, score=0, done=false;
const box=$('#quiz');
function drawQ(){
  if(qi>=Q.length){
    const pct=Math.round(score/Q.length*100);
    box.innerHTML=`<div class="kicker">Selesai</div><h2>Skor: ${score} dari ${Q.length} (${pct}%)</h2>
      <p class="lead">${pct>=75?'Pemahamanmu sudah kuat. Lanjutkan dengan membuat soal cerita sendiri.':'Ulangi bagian yang masih keliru lewat tab Simulasi atau Materi, lalu coba kuis lagi.'}</p>
      <button class="btn" id="qAgain">Ulangi kuis</button>`;
    $('#qAgain').addEventListener('click',()=>{ qi=0; score=0; drawQ(); });
    return;
  }
  const q=Q[qi]; done=false;
  box.innerHTML=`<div class="row" style="justify-content:space-between"><span class="kicker">Soal ${qi+1} dari ${Q.length}</span><span class="chip">Skor: ${score}</span></div>
    <h3 style="margin:10px 0 6px;font-size:26px">${q.q}</h3>
    <div id="opts">${q.o.map((t,i)=>`<button class="opt" data-i="${i}"><b>${'ABCD'[i]}.</b> ${t}</button>`).join('')}</div>
    <div id="qfb" aria-live="polite"></div>`;
  $$('#opts .opt').forEach(b=>b.addEventListener('click',()=>{
    if(done) return; done=true;
    const i=+b.dataset.i, ok=i===q.a; if(ok) score++;
    $$('#opts .opt').forEach((x,j)=>{ x.disabled=true; if(j===q.a) x.classList.add('right'); else if(j===i) x.classList.add('wrong'); });
    $('#qfb').innerHTML=`<div class="${ok?'ok':'no'}" style="margin-top:10px"><b>${ok?'Benar.':'Belum tepat.'}</b> ${q.e}</div>
      <div class="row" style="margin-top:12px"><button class="btn" id="qNext">${qi+1<Q.length?'Soal berikutnya':'Lihat skor'}</button><span class="kicker">Beri poin tim yang menjawab benar di papan skor.</span></div>`;
    $('#qNext').addEventListener('click',()=>{ qi++; drawQ(); });
  }));
}
drawQ();

/* Refleksi */
const SELF=['Saya bisa menjelaskan arti persamaan linear satu variabel.','Saya bisa memakai sifat kesetaraan untuk menyelesaikan persamaan.','Saya bisa mengubah soal cerita menjadi model matematika.','Saya bisa memeriksa apakah jawaban saya benar.'];
$('#selfBox').innerHTML=SELF.map((t,i)=>`<fieldset style="border:2px solid var(--line);border-radius:14px;padding:10px 14px"><legend style="font-weight:700;padding:0 6px">${t}</legend>
  <div class="row">${[1,2,3,4].map(n=>`<label style="display:flex;gap:6px;align-items:center;min-height:44px;font-size:20px"><input type="radio" name="s${i}" value="${n}" style="width:24px;height:24px;accent-color:var(--ink)"> ${n}</label>`).join('')}</div></fieldset>`).join('');
$('#selfGo').addEventListener('click',()=>{
  const v=SELF.map((_,i)=>{ const r=$(`input[name=s${i}]:checked`); return r?+r.value:0; });
  const out=$('#selfOut');
  if(v.includes(0)){ out.innerHTML='<div class="no">Isi keempat pernyataan lebih dulu.</div>'; return; }
  const low=v.indexOf(Math.min(...v)), avg=(v.reduce((a,b)=>a+b,0)/v.length).toFixed(1).replace('.',',');
  out.innerHTML=`<div class="callout"><b>Rata-rata: ${avg} dari 4.</b> Bagian yang paling perlu latihan: <i>${SELF[low].replace('Saya bisa ','')}</i></div>`;
});
})();
</script>

</body>
</html>
