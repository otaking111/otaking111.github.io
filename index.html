<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GTA Online — Garage Manager</title>
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;600;700&family=Share+Tech+Mono&display=swap" rel="stylesheet">
<style>
/* ── Reset & base ────────────────────────────────────────────────────────── */
*{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#0d0d1a; --panel:#12121f; --header:#1a1a30;
  --accent:#c8a227; --accent2:#5c9fd4;
  --text:#e8e8e8; --muted:#666688;
  --sel-bg:#1e1e2e; --divider:#2a2a45; --search-bg:#0a0a18;
  --col-m:#ff6eb4; --col-s:#5cb8ff;
  --sel-m:#ffb0d8; --sel-s:#a0d8ff;
  --tag-m-bg:#2a0a1a; --tag-s-bg:#0a1a2a;
  --hdr-garage:#1a1a30; --hdr-pegasus:#0d1a2a;
  --hdr-hangar:#0a1a0a; --hdr-special:#1a1a0a;
  --acc-garage:#c8a227; --acc-pegasus:#5cb8ff;
  --acc-hangar:#5dff9d; --acc-special:#ffd96e;
}
html,body{height:100%;overflow:hidden;background:var(--bg);color:var(--text);
  font-family:'Rajdhani',sans-serif;font-size:14px}

/* ── Top bar ──────────────────────────────────────────────────────────────── */
#topbar{display:flex;align-items:center;gap:8px;padding:0 14px;height:46px;
  background:var(--header);border-bottom:1px solid var(--divider);flex-shrink:0}
#app-title{color:var(--accent);font-size:14px;font-weight:700;letter-spacing:.08em;
  text-transform:uppercase;white-space:nowrap;margin-right:6px}

/* Tab switcher (Garage | Missing) */
.view-tabs{display:flex;gap:4px;margin-right:10px}
.view-tab{background:transparent;border:1px solid var(--divider);color:var(--muted);
  padding:4px 14px;font-family:'Rajdhani',sans-serif;font-weight:700;font-size:12px;
  letter-spacing:.08em;text-transform:uppercase;cursor:pointer;transition:all .15s}
.view-tab.active{background:var(--accent);color:#000;border-color:var(--accent)}
.view-tab:hover:not(.active){color:var(--text);border-color:var(--text)}

/* char filter */
.filter-group{display:flex;gap:2px}
.fbtn{background:var(--header);border:1px solid var(--divider);color:var(--muted);
  padding:3px 10px;font-family:'Rajdhani',sans-serif;font-weight:700;font-size:11px;
  letter-spacing:.06em;text-transform:uppercase;cursor:pointer;transition:all .15s}
.fbtn:hover{color:var(--text)}
.fbtn.active-all{background:var(--header);color:var(--accent);border-color:var(--accent)}
.fbtn.active-m{background:var(--tag-m-bg);color:var(--col-m);border-color:var(--col-m)}
.fbtn.active-s{background:var(--tag-s-bg);color:var(--col-s);border-color:var(--col-s)}
.fbtn.active-garage{background:var(--hdr-garage);color:var(--acc-garage);border-color:var(--acc-garage)}
.fbtn.active-pegasus{background:var(--hdr-pegasus);color:var(--acc-pegasus);border-color:var(--acc-pegasus)}
.fbtn.active-hangar{background:var(--hdr-hangar);color:var(--acc-hangar);border-color:var(--acc-hangar)}
.fbtn.active-special{background:var(--hdr-special);color:var(--acc-special);border-color:var(--acc-special)}

/* search */
#search-wrap{display:flex;align-items:center;margin-left:auto;gap:4px}
#search-wrap span{color:var(--muted);font-size:14px}
#searchInput{background:var(--search-bg);border:1px solid var(--divider);color:var(--text);
  font-family:'Share Tech Mono',monospace;font-size:12px;padding:4px 10px;
  outline:none;width:220px;transition:border-color .2s}
#searchInput:focus{border-color:var(--accent2)}
#searchInput::placeholder{color:var(--muted)}
#clearSearch{background:none;border:none;color:var(--muted);cursor:pointer;
  font-size:13px;padding:2px 4px}
#clearSearch:hover{color:var(--text)}

/* ── App body ─────────────────────────────────────────────────────────────── */
#app-body{display:flex;height:calc(100vh - 46px)}

/* ── Left sidebar ─────────────────────────────────────────────────────────── */
#sidebar{width:300px;min-width:200px;flex-shrink:0;background:var(--panel);
  border-right:1px solid var(--divider);display:flex;flex-direction:column}
#sidebar-label{color:var(--muted);font-size:10px;letter-spacing:.15em;
  text-transform:uppercase;padding:8px 10px 4px;font-family:'Share Tech Mono',monospace}
#loc-list{flex:1;overflow-y:auto;overflow-x:hidden}
#loc-list::-webkit-scrollbar{width:4px}
#loc-list::-webkit-scrollbar-track{background:var(--panel)}
#loc-list::-webkit-scrollbar-thumb{background:var(--divider)}

/* section separator */
.char-sep{height:2px;background:var(--accent)}
.char-header{padding:4px 8px;font-size:10px;font-weight:700;letter-spacing:.1em;
  font-family:'Share Tech Mono',monospace}
.char-header.m{background:var(--tag-m-bg);color:var(--col-m)}
.char-header.s{background:var(--tag-s-bg);color:var(--col-s)}
.type-header{padding:3px 12px;font-size:10px;letter-spacing:.1em;
  font-family:'Share Tech Mono',monospace;text-transform:uppercase}

/* garage rows */
.loc-row{display:flex;align-items:center;padding:4px 4px 4px 10px;
  cursor:pointer;transition:background .1s;gap:4px}
.loc-row:hover{background:#1a1a30}
.loc-row.selected{background:var(--sel-bg)}
.loc-row.child{padding-left:22px}
.loc-badge{font-size:9px;font-weight:700;padding:1px 4px;flex-shrink:0;
  font-family:'Share Tech Mono',monospace}
.loc-badge.m{background:var(--tag-m-bg);color:var(--col-m)}
.loc-badge.s{background:var(--tag-s-bg);color:var(--col-s)}
.loc-name{flex:1;font-size:12px;line-height:1.3}
.loc-count{font-size:10px;color:var(--muted);flex-shrink:0;
  font-family:'Share Tech Mono',monospace;padding-right:6px}
.loc-row.selected .loc-name{font-weight:700}
.loc-row.selected.m .loc-name,.loc-row.selected.m .loc-count{color:var(--sel-m)}
.loc-row.selected.s .loc-name,.loc-row.selected.s .loc-count{color:var(--sel-s)}
.loc-divider{height:1px;background:var(--divider);margin:0 8px}

/* ── Right panel ──────────────────────────────────────────────────────────── */
#right{flex:1;display:flex;flex-direction:column;overflow:hidden}
#detail-header{padding:8px 14px;display:flex;align-items:center;gap:10px;
  border-bottom:1px solid var(--divider);flex-shrink:0;min-height:42px}
#detail-title{font-size:14px;font-weight:700;letter-spacing:.04em}
#detail-count{margin-left:auto;font-size:10px;color:var(--muted);
  font-family:'Share Tech Mono',monospace;white-space:nowrap}

/* search result header */
#search-result-header{padding:8px 14px;border-bottom:1px solid var(--divider);
  flex-shrink:0;display:none}
#search-result-label{color:var(--accent2);font-size:13px;font-weight:700}

#car-list{flex:1;overflow-y:auto;overflow-x:hidden}
#car-list::-webkit-scrollbar{width:4px}
#car-list::-webkit-scrollbar-track{background:var(--bg)}
#car-list::-webkit-scrollbar-thumb{background:var(--divider)}

.car-row{display:flex;align-items:center;padding:6px 12px;gap:8px;
  border-bottom:1px solid var(--divider);transition:background .08s}
.car-row:hover{background:#14192a}
.car-num{font-family:'Share Tech Mono',monospace;font-size:11px;
  color:var(--muted);width:26px;text-align:right;flex-shrink:0}
.car-tag{font-size:9px;font-weight:700;padding:1px 4px;flex-shrink:0;
  font-family:'Share Tech Mono',monospace}
.car-tag.m{background:var(--tag-m-bg);color:var(--col-m)}
.car-tag.s{background:var(--tag-s-bg);color:var(--col-s)}
.car-name{font-size:14px;font-weight:600}
.car-name.highlight-m{color:var(--sel-m)}
.car-name.highlight-s{color:var(--sel-s)}
.car-name.normal-m{color:var(--col-m)}
.car-name.normal-s{color:var(--col-s)}

/* search result garage groups */
.srch-garage-hdr{display:flex;align-items:center;gap:8px;padding:6px 8px;
  margin:8px 6px 2px;border-left:3px solid}
.srch-garage-hdr.m{background:var(--tag-m-bg);border-color:var(--col-m)}
.srch-garage-hdr.s{background:var(--tag-s-bg);border-color:var(--col-s)}
.srch-garage-name{font-size:12px;font-weight:700}
.srch-garage-name.m{color:var(--col-m)}
.srch-garage-name.s{color:var(--col-s)}
.srch-view-btn{margin-left:auto;background:none;border:1px solid var(--divider);
  color:var(--accent);font-size:11px;cursor:pointer;padding:2px 8px;
  font-family:'Rajdhani',sans-serif}
.srch-view-btn:hover{border-color:var(--accent);background:var(--header)}
.srch-matches{font-size:10px;color:var(--muted);font-family:'Share Tech Mono',monospace}

/* ── Missing view ─────────────────────────────────────────────────────────── */
#missing-view{display:none;height:calc(100vh - 46px);flex-direction:column}
#missing-view.visible{display:flex}
#garage-view{display:flex;height:calc(100vh - 46px)}

/* missing top filters */
#missing-bar{display:flex;align-items:center;gap:8px;padding:8px 14px;
  background:var(--header);border-bottom:1px solid var(--divider);flex-shrink:0;flex-wrap:wrap}
#missing-search{background:var(--search-bg);border:1px solid var(--divider);
  color:var(--text);font-family:'Share Tech Mono',monospace;font-size:12px;
  padding:4px 10px;outline:none;width:180px;margin-left:auto}
#missing-search:focus{border-color:var(--accent2)}
#missing-search::placeholder{color:var(--muted)}

/* missing stats */
#missing-stats{display:flex;gap:0;border-bottom:1px solid var(--divider);flex-shrink:0}
.m-stat{flex:1;padding:10px 16px;border-right:1px solid var(--divider);text-align:center}
.m-stat:last-child{border-right:none}
.m-stat-num{font-size:28px;font-weight:700;color:var(--accent);
  font-family:'Share Tech Mono',monospace;line-height:1}
.m-stat-lbl{font-size:10px;color:var(--muted);letter-spacing:.1em;text-transform:uppercase;margin-top:2px}

/* missing table */
#missing-content{flex:1;overflow-y:auto}
#missing-content::-webkit-scrollbar{width:4px}
#missing-content::-webkit-scrollbar-track{background:var(--bg)}
#missing-content::-webkit-scrollbar-thumb{background:var(--divider)}

#missing-table{width:100%;border-collapse:collapse}
#missing-table thead th{
  background:var(--panel);border-bottom:2px solid var(--accent);
  padding:8px 14px;text-align:left;font-size:10px;letter-spacing:.15em;
  color:var(--accent);text-transform:uppercase;font-family:'Share Tech Mono',monospace;
  cursor:pointer;user-select:none;position:sticky;top:0;z-index:10}
#missing-table thead th:hover{color:#fff}
#missing-table thead th.sorted{color:var(--accent2)}
.sort-arr{margin-left:3px;opacity:.4}
#missing-table thead th.sorted .sort-arr{opacity:1}

#missing-table tbody tr{border-bottom:1px solid var(--divider);transition:background .08s}
#missing-table tbody tr:hover{background:#14192a}
#missing-table tbody tr.hidden{display:none}
#missing-table td{padding:8px 14px;vertical-align:middle}

.cls-badge{display:inline-block;padding:2px 8px;font-size:10px;font-weight:700;
  letter-spacing:.06em;text-transform:uppercase;border:1px solid;white-space:nowrap}
.v-name{font-size:14px;font-weight:600}

.cls-Sports      {color:#4fc3f7;border-color:#4fc3f7}
.cls-Muscle      {color:#ef5350;border-color:#ef5350}
.cls-Super       {color:#ab47bc;border-color:#ab47bc}
.cls-Classics    {color:#ffa726;border-color:#ffa726}
.cls-Sedans      {color:#78909c;border-color:#78909c}
.cls-SUVs        {color:#66bb6a;border-color:#66bb6a}
.cls-Coupes      {color:#ec407a;border-color:#ec407a}
.cls-Motorcycles {color:#ff7043;border-color:#ff7043}
.cls-OffRoad     {color:#8d6e63;border-color:#8d6e63}
.cls-Vans        {color:#7e57c2;border-color:#7e57c2}
.cls-Utility     {color:#bdbdbd;border-color:#bdbdbd}
.cls-Industrial  {color:#a1887f;border-color:#a1887f}
.cls-Service     {color:#80cbc4;border-color:#80cbc4}
.cls-Commercial  {color:#ffcc02;border-color:#ffcc02}
.cls-Emergency   {color:#ef5350;border-color:#ef5350}
.cls-Military    {color:#aed581;border-color:#aed581}
.cls-Boats       {color:#4dd0e1;border-color:#4dd0e1}
.cls-Planes      {color:#90caf9;border-color:#90caf9}

.no-results{text-align:center;padding:48px;color:var(--muted);
  font-family:'Share Tech Mono',monospace;font-size:12px}

/* ── Char vehicle counts ─────────────────────────────────────────────────── */
#char-counts{display:flex;align-items:center;gap:6px;margin-left:4px}
.vcount{display:flex;align-items:center;gap:3px;padding:3px 9px;
  border:1px solid var(--divider);background:var(--bg)}
.vcount.m{border-color:var(--col-m);background:var(--tag-m-bg)}
.vcount.s{border-color:var(--col-s);background:var(--tag-s-bg)}
.vcount.total{border-color:var(--accent);background:var(--header)}
.vcount-tag{font-family:'Share Tech Mono',monospace;font-size:9px;font-weight:700}
.vcount.m   .vcount-tag{color:var(--col-m)}
.vcount.s   .vcount-tag{color:var(--col-s)}
.vcount.total .vcount-tag{color:var(--accent)}
.vcount-num{font-family:'Share Tech Mono',monospace;font-size:13px;font-weight:700}
.vcount.m   .vcount-num{color:var(--col-m)}
.vcount.s   .vcount-num{color:var(--col-s)}
.vcount.total .vcount-num{color:var(--accent)}
</style>
</head>
<body>

<!-- TOP BAR -->
<div id="topbar">
  <div id="app-title">🏎 GTA Online — Garage Manager</div>

  <div class="view-tabs">
    <button class="view-tab active" id="tab-garage" onclick="switchView('garage')">🏠 Garages</button>
    <button class="view-tab" id="tab-missing" onclick="switchView('missing')">⚠ Missing</button>
  </div>

  <!-- Char filter -->
  <div class="filter-group" id="char-filters">
    <button class="fbtn active-all" data-char="ALL" onclick="setCharFilter('ALL')">All</button>
    <button class="fbtn" data-char="M" onclick="setCharFilter('M')">[M] Main</button>
    <button class="fbtn" data-char="S" onclick="setCharFilter('S')">[S] Secondary</button>
  </div>

  <!-- Type filter -->
  <div class="filter-group" id="type-filters">
    <button class="fbtn active-garage" data-type="ALL" onclick="setTypeFilter('ALL')">All Types</button>
    <button class="fbtn" data-type="garage" onclick="setTypeFilter('garage')">🏠 Properties</button>
    <button class="fbtn" data-type="pegasus" onclick="setTypeFilter('pegasus')">✈ Pegasus</button>
    <button class="fbtn" data-type="hangar" onclick="setTypeFilter('hangar')">🛫 Hangar</button>
    <button class="fbtn" data-type="special" onclick="setTypeFilter('special')">⭐ Special</button>
  </div>

  <!-- Vehicle counts -->
  <div id="char-counts">
    <span class="vcount m"><span class="vcount-tag">[M]</span><span class="vcount-num" id="count-m">—</span></span>
    <span class="vcount s"><span class="vcount-tag">[S]</span><span class="vcount-num" id="count-s">—</span></span>
    <span class="vcount total"><span class="vcount-tag">∑</span><span class="vcount-num" id="count-total">—</span></span>
  </div>

  <!-- Search -->
  <div id="search-wrap">
    <span>🔍</span>
    <input id="searchInput" type="text" placeholder="Search vehicle…" oninput="onSearch()">
    <button id="clearSearch" onclick="clearSearch()">✕</button>
  </div>
</div>

<!-- GARAGE VIEW -->
<div id="garage-view">
  <div id="sidebar">
    <div id="sidebar-label">Locations</div>
    <div id="loc-list"></div>
  </div>
  <div id="right">
    <div id="search-result-header">
      <div id="search-result-label"></div>
    </div>
    <div id="detail-header">
      <div id="detail-title">—</div>
      <div id="detail-count"></div>
    </div>
    <div id="car-list"></div>
  </div>
</div>

<!-- MISSING VEHICLES VIEW -->
<div id="missing-view">
  <div id="missing-bar">
    <div class="filter-group" id="cls-filters">
      <button class="fbtn active-all" data-cls="all" onclick="setClsFilter('all')">All</button>
      <button class="fbtn" data-cls="Sports" onclick="setClsFilter('Sports')">Sports</button>
      <button class="fbtn" data-cls="Muscle" onclick="setClsFilter('Muscle')">Muscle</button>
      <button class="fbtn" data-cls="Super" onclick="setClsFilter('Super')">Super</button>
      <button class="fbtn" data-cls="Sports Classics" onclick="setClsFilter('Sports Classics')">Classics</button>
      <button class="fbtn" data-cls="Sedans" onclick="setClsFilter('Sedans')">Sedans</button>
      <button class="fbtn" data-cls="SUVs" onclick="setClsFilter('SUVs')">SUVs</button>
      <button class="fbtn" data-cls="Coupes" onclick="setClsFilter('Coupes')">Coupes</button>
      <button class="fbtn" data-cls="Motorcycles" onclick="setClsFilter('Motorcycles')">Motos</button>
      <button class="fbtn" data-cls="Off-Road" onclick="setClsFilter('Off-Road')">Off-Road</button>
      <button class="fbtn" data-cls="other" onclick="setClsFilter('other')">Other</button>
    </div>
    <input id="missing-search" type="text" placeholder="Search…" oninput="renderMissing()">
  </div>
  <div id="missing-stats">
    <div class="m-stat"><div class="m-stat-num">860</div><div class="m-stat-lbl">Wiki Total</div></div>
    <div class="m-stat"><div class="m-stat-num">758</div><div class="m-stat-lbl">You Own</div></div>
    <div class="m-stat"><div class="m-stat-num" id="m-count">114</div><div class="m-stat-lbl">Showing Missing</div></div>
    <div class="m-stat"><div class="m-stat-num">88%</div><div class="m-stat-lbl">Complete</div></div>
  </div>
  <div id="missing-content">
    <table id="missing-table">
      <thead><tr>
        <th data-col="class" onclick="sortMissing('class')">Class <span class="sort-arr">↕</span></th>
        <th data-col="name" onclick="sortMissing('name')">Vehicle Name <span class="sort-arr">↕</span></th>
      </tr></thead>
      <tbody id="missing-tbody"></tbody>
    </table>
    <div class="no-results" id="no-results" style="display:none">No vehicles match.</div>
  </div>
</div>

<script>
// ═══════════════════════════════════════════════════════════════
// DATA
// ═══════════════════════════════════════════════════════════════
const GARAGES = [
  // ── MAIN CHARACTER ───────────────────────────────────────────
  {char:"M",type:"garage",name:"3 Alta St, Apt 57",cars:["Kuruma (Armored)","Insurgent","Vigilante","Firebolt ASP","JB 700W","Astron","Vigero ZX Convertible","Ignus","Arbiter GT","Endurex Race Bike","BMX","Cruiser"]},
  {char:"M",type:"garage",name:"Exceptionalists Way",cars:["Future Shock ZR380","Future Shock Issi","Future Shock Deathbike","Future Shock Brutus","Future Shock Scarab","Future Shock Imperator","Future Shock Slamvan","Scorcher","Tri-Cycles Race Bike","Endurex Race Bike"]},
  {char:"M",type:"garage",name:"2044 North Conker Ave",cars:["BMX","Whippet Race Bike","Cruiser"]},
  {char:"M",type:"garage",name:"Eclipse Towers, 3",cars:["Inductor","Junk Energy Inductor","Scorcher"]},
  {char:"M",type:"garage",name:"Eclipse, Penthouse Suite 3",cars:["Tri-Cycles Race Bike","Whippet Race Bike","Endurex Race Bike"]},
  {char:"M",type:"garage",name:"Hawick Clubhouse",cars:["Oppressor","Police Bike","Defiler","Shotaro","Nightblade","Cliffhanger","BF400","Sanctus"]},
  {char:"M",type:"garage",name:"Tinsel Towers, Apt 42",cars:["BMX","Tri-Cycles Race Bike","Cruiser"]},
  {char:"M",type:"garage",name:"Office Garages → Office Garage 1",cars:["Itali GTO","Squaddie","Super Diamond","Tempesta","XA-21","Penetrator","Schlagen GT","Pariah","Gauntlet Hellfire","Rebla GTS","Vagner","Clique","Desert Raid","Thrax","Krieger","Neon","Pisswasser Dominator","Emerus","Autarch","S80RR"]},
  {char:"M",type:"garage",name:"Office Garages → Office Garage 2",cars:["Nero","Dubsta 6x6","Duke O'Death","Itali RSX","Penumbra FF","Jugular","Paragon R","Castigator","Hellion","Cheetah Classic","8F Drafter","Cognoscenti (Armored)","GP1","Patriot Mil-Spec","Dukes","Virtue","Torero","Dynasty","Turismo R","Vagrant"]},
  {char:"M",type:"garage",name:"Office Garages → Office Garage 3",cars:["Lynx","Raiden","Viseris","Seminole Frontier","Omnis","Entity XXR","Tezeract","Kuruma","Tropos Rallye","Winky","Sugoi","Contender","Turismo Classic","Ruston","Trophy Truck","Drift Tampa","Manchez Scout","Go Go Monkey Blista","Blista Kanjo","Infernus Classic"]},
  {char:"M",type:"garage",name:"Land Act Reservoir Facility",cars:["Stromberg","Barrage","Caracara","Weaponized Tampa","APC","Technical Custom","Insurgent Pick-Up Custom","RCV","Chernobog","TM-02 Khanjali","Thruster"]},
  {char:"M",type:"garage",name:"Nightclub → Nightclub B2",cars:["Swinger","Jester Classic","Patriot Stretch","Asbo","Stafford","Freecrawler","Omnis e-GT","Comet Safari","Deveste Eight","Flash GT"]},
  {char:"M",type:"garage",name:"Nightclub → Nightclub B3",cars:["Michelli GT","Tigon","DR1","Stryder","Coquette D10","PR4","R88","V-STR","Komoda","Imorgon"]},
  {char:"M",type:"garage",name:"Nightclub → Nightclub B4",cars:["Tyrant","Novak","Locust","Neo","Deviant","GB200","Daemon","Landstalker XL","Club","Toros"]},
  {char:"M",type:"garage",name:"Arena → Arena Workshop",cars:["Bati 801RR","Hakuchou Drag","Oppressor Mk II","Bigfoot","Future Shock Bruiser","Future Shock Cerberus"]},
  {char:"M",type:"garage",name:"Arena → Arena Workshop B1",cars:["Dune FAV","Ardent","Zhaba","Slamtruck","Deluxo","Future Shock Dominator","Future Shock Impaler","Menacer","Apocalypse Cerberus"]},
  {char:"M",type:"garage",name:"Arena → Arena Workshop B2",cars:["V-STR","Reever","Sentinel Classic Widebody","Retinue Mk II","Hustler","Half-track","Weaponized Ignus","Shinobi","Hotring Everon","Nightmare Cerberus"]},
  {char:"M",type:"garage",name:"Casino Penthouse",cars:["Envisage","LM87","Comet Safari","Baller ST","Paragon R (Armored)","BR8","Sandking XL","Furia","Rampant Rocket","Zorrusso"]},
  {char:"M",type:"garage",name:"Arcade",cars:["Futo GTX","Dominator GTT","Jester RR","Issi Rally","Growler","Vorschlaghammer","Corsita","Dominator FX","Castigator","Yosemite 1500"]},
  {char:"M",type:"garage",name:"Eclipse, Penthouse Suite 1",cars:["Tri-Cycles Race Bike","Cruiser","BMX"]},
  {char:"M",type:"garage",name:"3655 Wild Oats Dr",cars:["Whippet Race Bike","Tri-Cycles Race Bike","Endurex Race Bike"]},
  {char:"M",type:"garage",name:"Auto Shop",cars:["Cypher","Vectre","Euros","Tailgater S","ZR350","Calico GTF","Dominator ASP","Warrener HKR","RT3000","Remus"]},
  {char:"M",type:"garage",name:"Agency",cars:["Buffalo Cruiser","Buffalo STX Pursuit","Windsor Drop","Buffalo STX","Deity","Terminus Patrol","Impaler SZ Cruiser","Speedo Custom","Caracara Pursuit","Park Ranger","Unmarked Cruiser","Dorado Cruiser","Greenwood Cruiser","Impaler LX Cruiser","Outreach Faction","Stanier LE Cruiser","Dominator FX Interceptor","Champion"]},
  {char:"M",type:"garage",name:"2862 Hillcrest Ave",cars:["Tri-Cycles Race Bike","Whippet Race Bike","Endurex Race Bike"]},
  {char:"M",type:"garage",name:"Eclipse, Penthouse Suite 2",cars:["Rhinehart","Cavalcade XL","Ratel","SM722","Walton L35","MonstroCiti","Panthere","Broadway","300R","Entity MT","Junk Energy Inductor","Inductor","Cruiser"]},
  {char:"M",type:"garage",name:"Eclipse Blvd Garage → Eclipse Blvd Garage B1",cars:["Pony","Pizza Boy","10F Widebody","Winky","Comet S2 Cabrio","Zeno","Dorado","Asterope GZ","Impaler LX","Vivanite"]},
  {char:"M",type:"garage",name:"Eclipse Blvd Garage → Eclipse Blvd Garage B2",cars:["Dominator GT","Brigham","FR36","Hotring Hellfire","Clique Wagon","Tahoma Coupe","Tulip M-100","Postlude","Ruiner ZZ-8","Granger 3600LX"]},
  {char:"M",type:"garage",name:"Eclipse Blvd Garage → Eclipse Blvd Garage B3",cars:["Kanjo SJ","Previon","Powersurge","Terminus","Greenwood","Eudora","Hotring Sabre","Brioso 300 Widebody","Impaler SZ","Boor"]},
  {char:"M",type:"garage",name:"Eclipse Blvd Garage → Eclipse Blvd Garage B4",cars:["Uranus LozSpeed","Banshee Topless","Ignus","S95","I-Wagen","Jubilee","Baller ST-D","Woodlander","Cinquemila","Nebula Turbo"]},
  {char:"M",type:"garage",name:"Eclipse Blvd Garage → Eclipse Blvd Garage B5",cars:["Minimus","Drift Walton L35","LSCM Cheetah Classic","Hardy Way","Tampa GT","Rapid GT X","Gauntlet Interceptor","Everon RS","Suzume","Sentinel GTS"]},
  {char:"M",type:"garage",name:"The Vinewood Club Garage → Basement Level 1",cars:["Clique","Comet Safari","811 Topless","RE-7B","Tyrus","Osiris","X80 Proto","Banshee 900R Topless","Adder","FMJ","Cheetah","T20","Roosevelt","Visione","Taipan","Roosevelt Valor","Fränken Stange","Baller LE LWB (Armored)","Lurcher","Verus"]},
  {char:"M",type:"garage",name:"The Vinewood Club Garage → Basement Level 2",cars:["Rumpo Custom","FCR 1000 Custom","Diabolus Custom","Zentorno","Entity XF","Cyclone","ETR1","Stirling GT","XLS (Armored)","Reaper","Coquette BlackFin Topless","Stinger GT","GT500","190z","Z-Type","Coquette Classic","Casco","Zion Classic","Hermes","Rapid GT Classic"]},
  {char:"M",type:"garage",name:"The Vinewood Club Garage → Basement Level 3",cars:["Chino Custom","Voodoo Custom","Minivan Custom","Slamvan Custom","Tornado Custom","Virgo Classic Custom","Buccaneer Custom Topless","Faction Custom Donk","Moonbeam Custom","Comet Retro Custom","Nero Custom","Elegy Retro Custom","Sabre Turbo Custom","Specter Custom","Itali GTB Custom","Weevil Custom","Manana Custom Topless","Peyote Custom Topless","Glendale Custom","Gauntlet Classic Custom"]},
  {char:"M",type:"garage",name:"The Vinewood Club Garage → Basement Level 4",cars:["Elegy RH8","Windsor (Livery)","Seven-70","Revolter","Nightshark","Gang Burrito","Stallion Topless","Savestra","Schafter LWB (Armored)","SC1","Yosemite Rancher","Youga Classic 4x4","Sultan RS","Bugstars Burrito","Sultan Classic","Drift Yosemite","Comet SR","Outlaw","Everon","Peyote Gasser Topless"]},
  {char:"M",type:"garage",name:"The Vinewood Club Garage → Basement Level 5",cars:["Lifeguard","Veto Modern","Veto Classic","Pipistrello","Coquette D1","Stinger TT","Buffalo EVX","La Coureuse","Aleutian","Turismo Omaggio","Paragon S","Euros X32","Niobe","Banshee GTS","LSCM Jester RR","Chavos V6","Draugur","Torero XO"]},
  {char:"M",type:"garage",name:"Bail Office",cars:["Coquette D10 Pursuit","Coquette D5"]},
  {char:"M",type:"garage",name:"Garment Factory",cars:["Firebolt ASP","Sultan RS Classic","Cyclone II"]},
  {char:"M",type:"garage",name:"Mansions → The Tongva Estate",cars:[]},
  {char:"M",type:"garage",name:"Mansions → Richman Villa",cars:["GT750","X-treme","FMJ MK V","Sentinel XS4","Luiva","Astrale","Itali Classic","Keitora"]},
  {char:"M",type:"garage",name:"Mansions → The Vinewood Residence",cars:[]},
  {char:"M",type:"garage",name:"Terrorbyte",cars:["Oppressor Mk II"]},
  {char:"M",type:"garage",name:"Kosatka",cars:["Sparrow","Avisa","Toreador"]},
  {char:"M",type:"pegasus",name:"Pegasus → Weaponized",cars:["Insurgent Pick-Up","Technical","Turreted Limo"]},
  {char:"M",type:"pegasus",name:"Pegasus → Military",cars:["Rhino Tank","Barracks","Crusader","Vetir"]},
  {char:"M",type:"pegasus",name:"Pegasus → Helicopters",cars:["Frogger","Maverick","Cargobob","Buzzard Attack Chopper","Annihilator","Swift Classic","Swift Flying Bravo","Valkyrie","Savage","Swift Deluxe","SuperVolito","SuperVolito Carbon","Volatus","Cargobob Jetsam"]},
  {char:"M",type:"pegasus",name:"Pegasus → Planes",cars:["Shamal","Mallard","Cuban 800","Duster","Luxor","Mammatus","Velum","Titan","Vestra","Besra","Miljet","Dodo","Hydra","Velum 5-Seater","Luxor Deluxe","Nimbus","P-996 LAZER"]},
  {char:"M",type:"pegasus",name:"Pegasus → Boats",cars:["Marquis","Jetmax","Squalo","Tropic","Seashark","Suntrap","Speeder","Dinghy","Toro","Tug","Longfin","Kurtz 31 Patrol Boat","Weaponized Dinghy","Police Predator"]},
  {char:"M",type:"pegasus",name:"Pegasus → Monster Trucks",cars:["Liberator","Marshall America","Marshall Australia","Marshall Brazil","Marshall Spain","Marshall Canada","Marshall France","Marshall Germany","Marshall Japan","Marshall Scotland","Marshall Great Britain","Marshall Italy","Marshall Switzerland","Marshall Jamaica","Marshall Colombia","Marshall Norway","Marshall Sweden","Marshall Belgium","Marshall Mexico","Marshall Austria","Marshall Russia","Marshall Argentina","Marshall Turkey","Marshall Ireland","Marshall Wales","Marshall England"]},
  {char:"M",type:"pegasus",name:"Pegasus → Trucks",cars:["Mule","Boxville","Mule","Brickade","Boxville","Boxville (LSDS)","Benson (Cluckin' Bell)"]},
  {char:"M",type:"pegasus",name:"Pegasus → Transport",cars:["Airport Bus","Bus","Dashound","Journey","Rental Shuttle Bus","Stretch","Prison Bus"]},
  {char:"M",type:"pegasus",name:"Pegasus → Service Vehicles",cars:["Dump","Dune Globe Oil","Dune Fukaru Rally"]},
  {char:"M",type:"pegasus",name:"Pegasus → Submarines",cars:["Kraken"]},
  {char:"M",type:"pegasus",name:"Pegasus → Blimps",cars:["Blimp Chepalle","Blimp eCola","Blimp Burger Shot","Blimp Redwood","Blimp Sprunk Xtreme","Blimp Pisswasser","Blimp Jackal Racing","Blimp Tony's Fun House"]},
  {char:"M",type:"pegasus",name:"Pegasus → Special",cars:["Festival Bus Be Cool Man","Taxi Custom","Dozer","Clown Van","Trashmaster","Fire Truck","Stockade","Taxi","Police Riot","Taco Van","Bobcat Security Stockade"]},
  {char:"M",type:"hangar",name:"Hangar",cars:["Havok","Sea Sparrow","FH-1 Hunter","DH-7 Iron Mule","B-11 Strikeforce","LF-22 Starling","Alpha-Z1","V-65 Molotok","Weaponized Conada","Savage","Streamer216","Tula","Annihilator Stealth","Volatol","Howard NX-25","Seabreeze","F-160 Raiju","Pyro","Ultralight","RO-86 Alkonost","Cargobob","RM-10 Bombushka","Buzzard","Titan 250 D","Hydra","Conada","Akula","P-45 Nokota","Mogul","P-996 LAZER","Duster 300-H","Rogue"]},
  {char:"M",type:"special",name:"Special Vehicles",cars:["Blazer Aqua","Speedo Custom","Mule Custom","Pounder Custom","Anti-Aircraft Trailer","Phantom Wedge","Ruiner 2000","Technical Aqua","Wastelander","Armored Boxville","Rocket Voltic","Ramp Buggy","Bail Office Transporter","Nano Drone","RC Bandito","RC Tank","RC Personal Vehicle","Avenger","Avenger Thruster","Mobile Operations Centre","Tow Truck (Chop Shop)","Acid Lab Brickade 6x6","Acid Lab Delivery Bike","Agency SuperVolito","Bunker Caddy","Terrorbyte (Vehicle)","Kosatka (Vehicle)","Duster (McKenzie)","Hauler Custom (Bunker MOC)"]},

  // ── SECONDARY CHARACTER ──────────────────────────────────────
  {char:"S",type:"garage",name:"3655 Wild Oats Dr",cars:["Kuruma (Armored)","Whippet Race Bike","Endurex Race Bike","Tri-Cycles Race Bike"]},
  {char:"S",type:"garage",name:"Eclipse, Penthouse Suite 2",cars:["FMJ MK V","Scramjet","Luiva","Rapid GT","Dominator GTX","Schwartzer","Buffalo","Sanchez","Banshee","Moonbeam"]},
  {char:"S",type:"garage",name:"Integrity Way, 35",cars:["X80 Proto","Kamacho Topless","Khamelion","Faction Custom","Peyote","Sandking XL","Fagaloa","Elegy RH8","Comet","Warrener","Whippet Race Bike","Cruiser","Scorcher"]},
  {char:"S",type:"garage",name:"3 Alta St, Apt 10",cars:["Stinger Topless","Insurgent","Sanchez (Livery)","Virgo","Schafter LWB","F620","Romero Hearse","Hakuchou","Dominator","Phoenix","BMX","Tri-Cycles Race Bike","Junk Energy Inductor"]},
  {char:"S",type:"garage",name:"Eclipse, Penthouse Suite 3",cars:["Zombie Bobber","Banshee Topless","Faggio Mod","Bestia GTS","Ellie","Esskey","Windsor Drop","Sentinel","Brawler","Dubsta","Endurex Race Bike","Cruiser","Whippet Race Bike"]},
  {char:"S",type:"garage",name:"Vinewood Clubhouse",cars:["Oppressor","Shotaro","Bati 801RR","Nightblade","Chimera","Lectro","Vindicator","Double-T","Vader"]},
  {char:"S",type:"garage",name:"4401 Procopio Dr",cars:["Super Diamond","Guardian","Tampa","Sovereign","Inductor","Whippet Race Bike"]},
  {char:"S",type:"garage",name:"Office Garages → Office Garage 1",cars:["Surano","Chino","Hexer","Sandking XL","Roosevelt Valor","Elegy Retro Custom","Kalahari","Akuma","Sentinel Classic","Massacro (Racecar)","Slamvan","Avarus","Jester (Racecar)","Hotknife","9F Cabrio","Turismo R","Monroe","Technical Custom","Sandking XL","Raptor"]},
  {char:"S",type:"garage",name:"Office Garages → Office Garage 2",cars:["Cognoscenti Cabrio","Huntley S","Hustler","Jackal","Infernus","Stallion Topless","Sultan RS","Sabre Turbo","XLS (Armored)","Gargoyle","Cliffhanger","Carbonizzare","Yosemite","Felon","Issi Classic","Nightshade","Pigalle","Desert Raid","Omnis","Brioso R/A"]},
  {char:"S",type:"garage",name:"Office Garages → Office Garage 3",cars:["BF400","Hot Rod Blazer","Serrano","GP1","Riata","Buccaneer","Zombie Chopper","Coquette Topless","Dubsta 6x6","Youga Classic","Daemon","Sultan","Bullet","Alpha","Turismo Classic","Furore GT","Baller","Bifta","Faggio","Duke O'Death"]},
  {char:"S",type:"garage",name:"Ron Wind Farm Facility",cars:["Insurgent Pick-Up Custom","APC","Deluxo","Stromberg","Barrage","Ardent","Menacer","RCV","Chernobog","TM-02 Khanjali","Thruster"]},
  {char:"S",type:"garage",name:"Nightclub → Nightclub B2",cars:["Future Shock Dominator","Future Shock Impaler","Future Shock Issi","Future Shock ZR380","Future Shock Slamvan","Romero Hearse","Impaler","Locust","Blazer Lifeguard","Future Shock Deathbike"]},
  {char:"S",type:"garage",name:"Nightclub → Nightclub B3",cars:["Revolter","Scramjet","Sanctus","Fränken Stange","Surfer Custom","Journey II","Vigero ZX","Kanjo SJ","Mamba Topless","10F"]},
  {char:"S",type:"garage",name:"Nightclub → Nightclub B4",cars:["Brioso 300","Gauntlet Classic","Manana","Specter","Itali GTB","FCR 1000","Faction","Primo","Voodoo","Virgo Classic"]},
  {char:"S",type:"garage",name:"Arena → Arena Workshop",cars:["Nightmare Slamvan","Future Shock Sasquatch","Apocalypse Slamvan","Apocalypse Deathbike","Nightmare Dominator","Apocalypse Impaler","Nightmare Impaler","Apocalypse Dominator","Future Shock Cerberus"]},
  {char:"S",type:"garage",name:"Arena → Arena Workshop B1",cars:["Apocalypse Issi","Apocalypse Sasquatch","Future Shock Bruiser","Nightmare Sasquatch","Nightmare Issi","Apocalypse ZR380","Nightmare Bruiser","Apocalypse Bruiser","Nightmare ZR380","Nightmare Cerberus"]},
  {char:"S",type:"garage",name:"Arena → Arena Workshop B2",cars:["Apocalypse Scarab","Future Shock Scarab","Nightmare Scarab","Apocalypse Brutus","Future Shock Brutus","Nightmare Brutus","Apocalypse Imperator","Future Shock Imperator","Nightmare Imperator","Apocalypse Cerberus"]},
  {char:"S",type:"garage",name:"Casino Penthouse",cars:["Schlagen GT","Weevil","Baller","BR8","DR1","PR4","R88","Rat-Truck","Impaler","Beater Dukes"]},
  {char:"S",type:"garage",name:"Arcade",cars:["Bugstars Burrito","Lifeguard","Baller","Caracara","Oracle","Washington","Clique","Comet Safari","Gresley","Vacca"]},
  {char:"S",type:"garage",name:"2045 North Conker Ave",cars:["Duneloader","Buffalo S","Issi Sport","Scorcher","Junk Energy Inductor","Inductor"]},
  {char:"S",type:"garage",name:"331 Supply St",cars:["Oppressor Mk II"]},
  {char:"S",type:"garage",name:"Auto Shop",cars:["Euros","ZR350","Tailgater S","Warrener HKR","Remus","Dominator GTT","Calico GTF","Jester RR","Futo GTX","RT3000"]},
  {char:"S",type:"garage",name:"Agency",cars:["Vigilante"]},
  {char:"S",type:"garage",name:"3677 Whispymound Dr",cars:["Inductor","Inductor","BMX"]},
  {char:"S",type:"garage",name:"2117 Milton Rd",cars:[]},
  {char:"S",type:"garage",name:"Eclipse Blvd Garage → Eclipse Blvd Garage B1",cars:["Felon GT","Baller","Felon","Sadler","Emperor","Prairie","PCJ 600","Seminole","Felon GT","Rusty Rebel"]},
  {char:"S",type:"garage",name:"Eclipse Blvd Garage → Eclipse Blvd Garage B2",cars:["Duneloader"]},
  {char:"S",type:"garage",name:"Eclipse Blvd Garage → Eclipse Blvd Garage B3",cars:[]},
  {char:"S",type:"garage",name:"Eclipse Blvd Garage → Eclipse Blvd Garage B4",cars:[]},
  {char:"S",type:"garage",name:"Eclipse Blvd Garage → Eclipse Blvd Garage B5",cars:[]},
  {char:"S",type:"garage",name:"The Vinewood Club Garage → Basement Level 1",cars:["Drift Walton L35","Walton L35 Stock","GT750","Ardent","BR8","Itali RSX","SC1","Sentinel GTS","Hakuchou Drag","Deity","Castigator","Impaler LX Cruiser","Neon","Coquette D5","Weaponized Tampa","Police Bike","Roosevelt","Rocoto","Verlierer","Glendale"]},
  {char:"S",type:"garage",name:"The Vinewood Club Garage → Basement Level 2",cars:["Wolfsbane","Innovation","Blade","Diabolus","FCR 1000","Futo","Daemon","Schwartzer","Street Blazer","Comet S2","Habanero","Blista","Issi","BeeJay XL","Granger","Surge","Cavalcade","Landstalker","Fusilade","Asterope"]},
  {char:"S",type:"garage",name:"The Vinewood Club Garage → Basement Level 3",cars:["Baller LE LWB","Baller LE LWB (Armored)","Schafter V12","Schafter V12 (Armored)","Youga","Stanier","Radius","Patriot","Minivan","Carbon RS","Fugitive","FQ 2","Zion Cabrio","Penumbra","Ruiner","Emperor","Vigero","Dilettante","Rancher XL","Stratum"]},
  {char:"S",type:"garage",name:"The Vinewood Club Garage → Basement Level 4",cars:["Ingot","Bobcat XL","Comet SR","Cheburek","Half-track","Powersurge","Baller ST","Nightmare Deathbike","La Coureuse","Sentinel XS","Premier","Mesa","Intruder","Exemplar","Rhapsody","Feltzer","Brioso R/A","Eudora","Envisage","Hellion"]},
  {char:"S",type:"garage",name:"The Vinewood Club Garage → Basement Level 5",cars:["Tailgater","Daemon","Kanjo SJ","Brigham","V-STR","Sprunk Buffalo","Revolter","Tahoma Coupe","Jackal","Taipan","JB 700","Sentinel","JB 700W","Park Ranger","Gauntlet","Primo Custom","Retinue","GB200","Panto","Streiter"]},
  {char:"S",type:"garage",name:"Bail Office",cars:["Gauntlet Interceptor","Coquette D10 Pursuit"]},
  {char:"S",type:"garage",name:"Garment Factory",cars:[]},
  {char:"S",type:"garage",name:"Mansions → The Tongva Estate",cars:[]},
  {char:"S",type:"garage",name:"Mansions → Richman Villa",cars:[]},
  {char:"S",type:"garage",name:"Mansions → The Vinewood Residence",cars:[]},
  {char:"S",type:"garage",name:"Terrorbyte",cars:["Oppressor Mk II"]},
  {char:"S",type:"garage",name:"Kosatka",cars:["Sparrow","Avisa","Toreador"]},
  {char:"S",type:"pegasus",name:"Pegasus → Weaponized",cars:["Insurgent Pick-Up","Technical","Turreted Limo"]},
  {char:"S",type:"pegasus",name:"Pegasus → Military",cars:["Rhino Tank","Barracks","Crusader","Vetir"]},
  {char:"S",type:"pegasus",name:"Pegasus → Helicopters",cars:["Frogger","Maverick","Cargobob","Buzzard Attack Chopper","Annihilator","Swift Classic","Swift Flying Bravo","Valkyrie","Savage","Swift Deluxe","SuperVolito","SuperVolito Carbon","Volatus","Cargobob Jetsam"]},
  {char:"S",type:"pegasus",name:"Pegasus → Planes",cars:["Shamal","Mallard","Cuban 800","Duster","Luxor","Mammatus","Velum","Titan","Vestra","Besra","Miljet","Dodo","Hydra","Velum 5-Seater","Luxor Deluxe","Nimbus","P-996 LAZER"]},
  {char:"S",type:"pegasus",name:"Pegasus → Boats",cars:["Marquis","Jetmax","Squalo","Tropic","Seashark","Suntrap","Speeder","Dinghy","Toro","Tug","Longfin","Kurtz 31 Patrol Boat","Weaponized Dinghy","Police Predator"]},
  {char:"S",type:"pegasus",name:"Pegasus → Monster Trucks",cars:["Liberator","Marshall America","Marshall Australia","Marshall Brazil","Marshall Spain","Marshall Canada","Marshall France","Marshall Germany","Marshall Japan","Marshall Scotland","Marshall Great Britain","Marshall Italy","Marshall Switzerland","Marshall Jamaica","Marshall Colombia","Marshall Norway","Marshall Sweden","Marshall Belgium","Marshall Mexico","Marshall Austria","Marshall Russia","Marshall Argentina","Marshall Turkey","Marshall Ireland","Marshall Wales","Marshall England"]},
  {char:"S",type:"pegasus",name:"Pegasus → Trucks",cars:["Mule","Boxville","Mule","Brickade","Boxville","Boxville (LSDS)","Benson (Cluckin' Bell)"]},
  {char:"S",type:"pegasus",name:"Pegasus → Transport",cars:["Airport Bus","Bus","Dashound","Journey","Rental Shuttle Bus","Stretch","Prison Bus"]},
  {char:"S",type:"pegasus",name:"Pegasus → Service Vehicles",cars:["Dump","Dune Globe Oil","Dune Fukaru Rally"]},
  {char:"S",type:"pegasus",name:"Pegasus → Submarines",cars:["Kraken"]},
  {char:"S",type:"pegasus",name:"Pegasus → Blimps",cars:["Blimp Chepalle","Blimp eCola","Blimp Burger Shot","Blimp Redwood","Blimp Sprunk Xtreme","Blimp Pisswasser","Blimp Jackal Racing","Blimp Maisonette Los Santos"]},
  {char:"S",type:"pegasus",name:"Pegasus → Special",cars:["Fire Truck","Stockade","Taxi","Police Riot","Taco Van","Bobcat Security Stockade"]},
  {char:"S",type:"hangar",name:"Hangar",cars:["Valkyrie","FH-1 Hunter","Savage","Titan 250 D","Akula","P-996 LAZER","Cuban 800","Havok","Velum 5-Seater","Swift","RO-86 Alkonost","Shamal","Conada","Buzzard Attack Chopper","DH-7 Iron Mule","P-996 LAZER","F-160 Raiju","Rogue","Sea Sparrow","Dodo","Streamer216","Vestra"]},
  {char:"S",type:"special",name:"Special Vehicles",cars:["Blazer Aqua","Speedo Custom","Mule Custom","Pounder Custom","Anti-Aircraft Trailer","Phantom Wedge","Ruiner 2000","Technical Aqua","Wastelander","Armored Boxville","Rocket Voltic","Ramp Buggy","Bail Office Transporter","Nano Drone","RC Bandito","RC Tank","RC Personal Vehicle","Avenger","Avenger Thruster","Mobile Operations Centre","Beater Tow Truck (Chop Shop)","Acid Lab Brickade 6x6","Acid Lab Delivery Bike","Agency SuperVolito","Bunker Caddy","Terrorbyte (Vehicle)","Kosatka (Vehicle)","Duster (McKenzie)","Phantom Custom (Bunker MOC)"]},
];

const MISSING = [
  ["Sports","9F (Car Meet)"],  ["Sports","Jester (Base) (Car Meet)"],  ["Sports","Massacro (Base) (Car Meet)"],  ["Muscle","Lost Slamvan (Casino Wheel)"],
  ["Muscle","Picador"],  ["Muscle","Tulip (Car Meet)"],  ["Muscle","Vamos (Car Meet)"],  ["Super","Voltic (Car Meet)"],
  ["Sports Classics","Tornado"],  ["Sports Classics","Tornado (Mariachi)"],  ["Sports Classics","Tornado (rusted)"],  ["Sports Classics","Tornado Rat Rod (Car Meet)"],
  ["Sedans","Asea"],  ["Sedans","Cognoscenti"],  ["Sedans","Cognoscenti 55 (Armored) (Car Meet)"],  ["Sedans","Cognoscenti 55 (Car Meet)"],
  ["Sedans","Hardy"],  ["Sedans","Regina"],  ["Sedans","Schafter (second generation)"],  ["SUVs","Astron Custom"],
  ["SUVs","XLS (Car Meet)"],  ["Coupes","Oracle XS"],  ["Motorcycles","Bagger"],  ["Motorcycles","Enduro (Car Meet)"],
  ["Motorcycles","Faggio Sport (Car Meet)"],  ["Motorcycles","Nemesis"],  ["Motorcycles","Rat Bike (Car Meet)"],  ["Motorcycles","Ruffian"],
  ["Motorcycles","Thrust (Car Meet)"],  ["Motorcycles","Vortex (Car Meet)"],  ["Off-Road","Bodhi"],  ["Off-Road","Dune Buggy"],
  ["Off-Road","Rebel"],  ["Off-Road","Sandking SWB"],  ["Off-Road","Space Docker (Obtain through Arena War)"],  ["Vans","Bison"],
];

const CLASS_ORDER = ["Sports","Muscle","Super","Sports Classics","Sedans","SUVs","Compacts",
  "Coupes","Motorcycles","Off-Road","Open Wheel","Cycles","Vans","Utility","Industrial",
  "Service","Commercial","Emergency","Military","Boats","Planes","Helicopters"];
const PRIMARY_CLS = new Set(["Sports","Muscle","Super","Sports Classics","Sedans","SUVs","Coupes","Motorcycles","Off-Road","Vans"]);

const TYPE_HDR   = {garage:"var(--hdr-garage)",pegasus:"var(--hdr-pegasus)",hangar:"var(--hdr-hangar)",special:"var(--hdr-special)"};
const TYPE_ACC   = {garage:"var(--acc-garage)",pegasus:"var(--acc-pegasus)",hangar:"var(--acc-hangar)",special:"var(--acc-special)"};
const TYPE_ICON  = {garage:"🏠",pegasus:"✈",hangar:"🛫",special:"⭐"};
const TYPE_LABEL = {garage:"Properties",pegasus:"Pegasus",hangar:"Hangar",special:"Special Vehicles"};

// ═══════════════════════════════════════════════════════════════
// STATE
// ═══════════════════════════════════════════════════════════════
let charFilter = "ALL", typeFilter = "ALL";
let selectedIdx = 0;
let searchMode = false;
let activeView = "garage";

// missing state
let clsFilter = "all", missingSortCol = "class", missingSortDir = 1;

// ═══════════════════════════════════════════════════════════════
// VIEW SWITCHING
// ═══════════════════════════════════════════════════════════════
function switchView(v) {
  activeView = v;
  document.getElementById('tab-garage').classList.toggle('active', v === 'garage');
  document.getElementById('tab-missing').classList.toggle('active', v === 'missing');
  document.getElementById('garage-view').style.display = v === 'garage' ? 'flex' : 'none';
  document.getElementById('missing-view').classList.toggle('visible', v === 'missing');
  // show/hide garage-specific controls
  document.getElementById('char-filters').style.display = v === 'garage' ? 'flex' : 'none';
  document.getElementById('type-filters').style.display = v === 'garage' ? 'flex' : 'none';
  document.getElementById('search-wrap').style.display  = v === 'garage' ? 'flex' : 'none';
  document.getElementById('char-counts').style.display   = v === 'garage' ? 'flex' : 'none';
}

// ═══════════════════════════════════════════════════════════════
// GARAGE: FILTERS
// ═══════════════════════════════════════════════════════════════
function setCharFilter(k) {
  charFilter = k;
  refreshCharBtns();
  buildLocList();
  const v = visibleGarages();
  if (v.length) selectGarage(v[0][0]);
}
function setTypeFilter(k) {
  typeFilter = k;
  refreshTypeBtns();
  buildLocList();
  const v = visibleGarages();
  if (v.length) selectGarage(v[0][0]);
  updateCharCounts();
}

function refreshCharBtns() {
  document.querySelectorAll('#char-filters .fbtn').forEach(b => {
    const k = b.dataset.char;
    b.className = 'fbtn' + (k === charFilter ? ` active-${k === 'ALL' ? 'all' : k.toLowerCase()}` : '');
  });
}
function refreshTypeBtns() {
  document.querySelectorAll('#type-filters .fbtn').forEach(b => {
    const k = b.dataset.type;
    b.className = 'fbtn' + (k === typeFilter ? ` active-${k === 'ALL' ? 'all' : k}` : '');
  });
}

function visibleGarages() {
  return GARAGES.map((g,i) => [i,g]).filter(([,g]) =>
    (charFilter === 'ALL' || g.char === charFilter) &&
    (typeFilter === 'ALL' || g.type === typeFilter));
}

// ═══════════════════════════════════════════════════════════════
// GARAGE: LOCATION LIST
// ═══════════════════════════════════════════════════════════════
function buildLocList() {
  const list = document.getElementById('loc-list');
  list.innerHTML = '';
  let lastChar = null, lastType = null;
  const visible = visibleGarages();

  visible.forEach(([origIdx, g]) => {
    const parts   = g.name.split(' → ');
    const display = parts.length > 1 ? parts[parts.length-1] : g.name;
    const isChild = parts.length > 1;

    if (charFilter === 'ALL' && g.char !== lastChar) {
      if (lastChar !== null) {
        const sep = document.createElement('div');
        sep.className = 'char-sep';
        list.appendChild(sep);
      }
      const ch = document.createElement('div');
      ch.className = `char-header ${g.char.toLowerCase()}`;
      ch.textContent = g.char === 'M' ? '[M] Main Character' : '[S] Secondary Character';
      list.appendChild(ch);
      lastType = null;
    }
    if (g.type !== lastType) {
      const th = document.createElement('div');
      th.className = 'type-header';
      th.style.background = TYPE_HDR[g.type];
      th.style.color = TYPE_ACC[g.type];
      th.textContent = `${TYPE_ICON[g.type]} ${TYPE_LABEL[g.type]}`;
      list.appendChild(th);
    }
    lastChar = g.char; lastType = g.type;

    if (!isChild) {
      const div = document.createElement('div');
      div.className = 'loc-divider';
      list.appendChild(div);
    }

    const row = document.createElement('div');
    row.className = `loc-row ${g.char.toLowerCase()}${isChild ? ' child' : ''}${origIdx === selectedIdx ? ' selected' : ''}`;
    row.dataset.idx = origIdx;
    row.innerHTML = `<span class="loc-badge ${g.char.toLowerCase()}">[${g.char}]</span><span class="loc-name">${display}</span><span class="loc-count">${g.cars.length}</span>`;
    row.onclick = () => selectGarage(origIdx);
    list.appendChild(row);
  });
}

// ═══════════════════════════════════════════════════════════════
// GARAGE: SELECT
// ═══════════════════════════════════════════════════════════════
function selectGarage(idx) {
  searchMode = false;
  document.getElementById('searchInput').value = '';
  selectedIdx = idx;
  clearSearch();
  // update sidebar highlight
  document.querySelectorAll('.loc-row').forEach(r => {
    const i = parseInt(r.dataset.idx);
    r.classList.toggle('selected', i === idx);
  });
  const g = GARAGES[idx];
  renderDetail(g);
}

function renderDetail(g) {
  // show detail header, hide search header
  document.getElementById('search-result-header').style.display = 'none';
  document.getElementById('detail-header').style.display = 'flex';
  const hdrBg = TYPE_HDR[g.type];
  const hdrAcc = TYPE_ACC[g.type];
  const dh = document.getElementById('detail-header');
  dh.style.background = hdrBg;
  dh.style.borderBottom = `1px solid ${hdrAcc}`;
  const tag = g.char === 'M' ? '[M]' : '[S]';
  const tagCls = g.char === 'M' ? 'car-tag m' : 'car-tag s';
  document.getElementById('detail-title').innerHTML =
    `<span class="${tagCls}">${tag}</span> ${TYPE_ICON[g.type]} ${g.name}`;
  document.getElementById('detail-title').style.color = g.char === 'M' ? 'var(--col-m)' : 'var(--col-s)';
  document.getElementById('detail-count').textContent = `${g.cars.length} vehicles`;
  renderCars(g.cars, g.char, g.type, null);
}

function renderCars(cars, char, gtype, highlight) {
  const list = document.getElementById('car-list');
  list.innerHTML = '';
  if (!cars.length) {
    list.innerHTML = '<div class="no-results">No vehicles recorded.</div>';
    return;
  }
  const sorted = ['pegasus','hangar','special'].includes(gtype) ? cars : [...cars].sort();
  const baseCol = char === 'M' ? 'normal-m' : 'normal-s';
  const hiCol   = char === 'M' ? 'highlight-m' : 'highlight-s';
  const tag     = char === 'M' ? '[M]' : '[S]';
  sorted.forEach((car, i) => {
    const hl = highlight && car.toLowerCase().includes(highlight.toLowerCase());
    const row = document.createElement('div');
    row.className = 'car-row';
    row.innerHTML = `<span class="car-num">${i+1}.</span><span class="car-tag ${char.toLowerCase()}">${tag}</span><span class="car-name ${hl ? hiCol : baseCol}">${car}</span>`;
    list.appendChild(row);
  });
}

// ═══════════════════════════════════════════════════════════════
// SEARCH
// ═══════════════════════════════════════════════════════════════
function onSearch() {
  const q = document.getElementById('searchInput').value.trim();
  if (!q) { clearSearch(); return; }
  searchMode = true;
  const ql = q.toLowerCase();
  const results = [];
  GARAGES.forEach((g, gi) => {
    if (charFilter !== 'ALL' && g.char !== charFilter) return;
    if (typeFilter !== 'ALL' && g.type !== typeFilter) return;
    g.cars.forEach(car => {
      if (car.toLowerCase().includes(ql)) results.push({car, garage: g.name, char: g.char, type: g.type, gi});
    });
  });
  // update headers
  document.getElementById('search-result-header').style.display = 'block';
  document.getElementById('detail-header').style.display = 'none';
  document.getElementById('search-result-label').textContent =
    `Search: "${q}" — ${results.length} result${results.length !== 1 ? 's' : ''}`;
  renderSearchResults(results, q);
}

function renderSearchResults(results, query) {
  const list = document.getElementById('car-list');
  list.innerHTML = '';
  if (!results.length) {
    list.innerHTML = `<div class="no-results">No vehicles found matching "${query}".</div>`;
    return;
  }
  // group by garage
  const byGarage = new Map();
  results.forEach(r => {
    const key = r.gi;
    if (!byGarage.has(key)) byGarage.set(key, {garage: r.garage, char: r.char, type: r.type, gi: r.gi, cars: []});
    byGarage.get(key).cars.push(r.car);
  });
  byGarage.forEach(({garage, char, type, gi, cars}) => {
    const cls = char.toLowerCase();
    const hdr = document.createElement('div');
    hdr.className = `srch-garage-hdr ${cls}`;
    hdr.innerHTML =
      `<span class="car-tag ${cls}">[${char}]</span>` +
      `<span class="srch-garage-name ${cls}">${TYPE_ICON[type]} ${garage}</span>` +
      `<span class="srch-matches">${cars.length} match${cars.length !== 1 ? 'es' : ''}</span>` +
      `<button class="srch-view-btn" onclick="selectGarage(${gi})">→ View</button>`;
    list.appendChild(hdr);
    cars.forEach(car => {
      const row = document.createElement('div');
      row.className = 'car-row';
      const hiCol = char === 'M' ? 'highlight-m' : 'highlight-s';
      row.innerHTML = `<span class="car-num">•</span><span class="car-tag ${cls}">[${char}]</span><span class="car-name ${hiCol}">${car}</span>`;
      list.appendChild(row);
    });
  });
}

function clearSearch() {
  document.getElementById('searchInput').value = '';
  searchMode = false;
  document.getElementById('search-result-header').style.display = 'none';
  document.getElementById('detail-header').style.display = 'flex';
  if (GARAGES[selectedIdx]) renderDetail(GARAGES[selectedIdx]);
}

// ═══════════════════════════════════════════════════════════════
// MISSING: FILTERS & RENDER
// ═══════════════════════════════════════════════════════════════
function setClsFilter(cls) {
  clsFilter = cls;
  document.querySelectorAll('#cls-filters .fbtn').forEach(b => {
    const k = b.dataset.cls;
    b.className = 'fbtn' + (k === cls ? ' active-all' : '');
  });
  renderMissing();
}

function sortMissing(col) {
  if (missingSortCol === col) missingSortDir *= -1;
  else { missingSortCol = col; missingSortDir = 1; }
  document.querySelectorAll('#missing-table thead th').forEach(th => {
    th.classList.toggle('sorted', th.dataset.col === col);
    const arr = th.querySelector('.sort-arr');
    if (arr) arr.textContent = th.dataset.col === col ? (missingSortDir === 1 ? '↓' : '↑') : '↕';
  });
  renderMissing();
}

function clsKey(c) { const i = CLASS_ORDER.indexOf(c); return i < 0 ? 99 : i; }
function clsCssKey(c) { return c.replace(/\s+/g,'').replace('-',''); }

function renderMissing() {
  const q = (document.getElementById('missing-search').value || '').toLowerCase().trim();
  let rows = MISSING.filter(([cls, name]) => {
    if (clsFilter !== 'all' && clsFilter !== 'other' && cls !== clsFilter) return false;
    if (clsFilter === 'other' && PRIMARY_CLS.has(cls)) return false;
    if (q && !name.toLowerCase().includes(q)) return false;
    return true;
  });
  rows.sort(([ac,an],[bc,bn]) => {
    const av = missingSortCol === 'class' ? clsKey(ac) : an.toLowerCase();
    const bv = missingSortCol === 'class' ? clsKey(bc) : bn.toLowerCase();
    return av < bv ? -missingSortDir : av > bv ? missingSortDir : 0;
  });
  const tbody = document.getElementById('missing-tbody');
  tbody.innerHTML = '';
  rows.forEach(([cls, name]) => {
    const tr = document.createElement('tr');
    const ck = clsCssKey(cls);
    tr.innerHTML = `<td><span class="cls-badge cls-${ck}">${cls}</span></td><td class="v-name">${name}</td>`;
    tbody.appendChild(tr);
  });
  document.getElementById('m-count').textContent = rows.length;
  document.getElementById('no-results').style.display = rows.length ? 'none' : 'block';
}


// ═══════════════════════════════════════════════════════════════
// CHAR COUNTS
// ═══════════════════════════════════════════════════════════════
function updateCharCounts() {
  let totalM = 0, totalS = 0;
  GARAGES.forEach(g => {
    if (typeFilter !== 'ALL' && g.type !== typeFilter) return;
    if (g.char === 'M') totalM += g.cars.length;
    else                totalS += g.cars.length;
  });
  document.getElementById('count-m').textContent     = totalM.toLocaleString();
  document.getElementById('count-s').textContent     = totalS.toLocaleString();
  document.getElementById('count-total').textContent = (totalM + totalS).toLocaleString();
}
// ═══════════════════════════════════════════════════════════════
// INIT
// ═══════════════════════════════════════════════════════════════
refreshCharBtns();
refreshTypeBtns();
buildLocList();
selectGarage(0);
renderMissing();
updateCharCounts();
// Set initial view
document.getElementById('garage-view').style.display = 'flex';
document.getElementById('missing-view').classList.remove('visible');
</script>
</body>
</html>
