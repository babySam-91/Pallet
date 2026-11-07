<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Palette Studio – color families, codes and themes</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
:root{--bg:#f6f5fb;--surf:#fff;--ink:#1d1b2e;--mute:#5f5c76;--line:#e1dfee;--acc:#5b4bd6;--accink:#fff;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#15141f;--surf:#1e1d2c;--ink:#ecebf7;--mute:#a7a4c0;--line:#34324b;--acc:#9a8cf8;--accink:#15141f}}
:root[data-theme="dark"]{--bg:#15141f;--surf:#1e1d2c;--ink:#ecebf7;--mute:#a7a4c0;--line:#34324b;--acc:#9a8cf8;--accink:#15141f}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--ink);font:16px/1.55 Inter,system-ui,-apple-system,Segoe UI,Roboto,sans-serif;padding-bottom:96px}
header{background:var(--surf);border-bottom:1px solid var(--line)}
.bar{max-width:1000px;margin:0 auto;padding:12px 16px;display:flex;align-items:center;gap:16px;flex-wrap:wrap}
.logo{font-weight:700;font-size:18px;margin-right:auto;display:flex;gap:8px;align-items:center}
.dots{display:flex}.dots i{width:12px;height:12px;border-radius:50%;margin-left:-3px;border:2px solid var(--surf)}
nav{display:flex;gap:4px}
nav a{color:var(--mute);text-decoration:none;padding:8px 14px;border-radius:8px;font-weight:500}
nav a.on{background:var(--acc);color:var(--accink)}
a:focus-visible,button:focus-visible{outline:3px solid var(--acc);outline-offset:2px}
main{max-width:1000px;margin:0 auto;padding:24px 16px}
.view{display:none}.view.on{display:block}
h1{font-size:clamp(28px,5vw,42px);line-height:1.15;margin:8px 0 12px;letter-spacing:-.02em}
h2{font-size:18px;margin:0 0 8px}
p{max-width:64ch;margin:0 0 12px}
.mute{color:var(--mute)}
.btn{display:inline-block;border:1px solid var(--acc);background:var(--acc);color:var(--accink);padding:10px 18px;border-radius:8px;font:600 15px Inter,sans-serif;cursor:pointer;text-decoration:none}
.btn.alt{background:transparent;color:var(--acc)}
.scroll{overflow-x:auto;padding-bottom:4px}
.row{display:grid;grid-template-columns:repeat(10,1fr);gap:4px;min-width:680px}
.sw{position:relative;border-radius:8px;height:92px}
.cp{all:unset;box-sizing:border-box;cursor:pointer;display:flex;flex-direction:column;justify-content:flex-end;width:100%;height:100%;padding:8px;font-size:12px;line-height:1.3;border-radius:8px}
.cp b{font-size:15px}
.cp:focus-visible{outline:3px solid var(--acc);outline-offset:2px}
.ad{position:absolute;top:4px;right:4px;width:24px;height:24px;border-radius:50%;border:0;background:rgba(255,255,255,.88);color:#222;cursor:pointer;font:700 15px/1 Inter,sans-serif;padding:0}
.ad.on{background:#222;color:#fff}
.fam{margin-bottom:22px}
.fam h2{display:flex;gap:10px;align-items:baseline}
.fam h2 small{font-weight:400;color:var(--mute);font-size:13px}
.steps{display:grid;gap:12px;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));margin:20px 0;padding:0;list-style:none;counter-reset:s}
.steps li{background:var(--surf);border:1px solid var(--line);border-radius:12px;padding:16px;counter-increment:s}
.steps li::before{content:counter(s);display:grid;place-items:center;width:28px;height:28px;border-radius:50%;background:var(--acc);color:var(--accink);font-weight:700;margin-bottom:8px}
.box{background:var(--surf);border:1px solid var(--line);border-radius:12px;padding:16px;margin-bottom:16px}
code{background:var(--bg);border:1px solid var(--line);border-radius:6px;padding:1px 6px;font-size:14px}
.chips{display:flex;gap:8px;margin:0 0 16px;flex-wrap:wrap}
.chip{border:1px solid var(--line);background:var(--surf);color:var(--ink);padding:6px 14px;border-radius:99px;cursor:pointer;font:500 14px Inter,sans-serif}
.chip.on{background:var(--acc);border-color:var(--acc);color:var(--accink)}
.themes{display:grid;gap:16px;grid-template-columns:repeat(auto-fill,minmax(300px,1fr))}
.th{background:var(--surf);border:1px solid var(--line);border-radius:12px;padding:16px}
.th h2{margin:0}
.tag{font-size:13px;color:var(--mute)}
.prop{display:flex;height:56px;border-radius:8px;overflow:hidden;margin:12px 0}
.list{list-style:none;margin:0 0 12px;padding:0;font-size:14px}
.list li{display:flex;align-items:center;gap:8px;padding:3px 0}
.list i{width:16px;height:16px;border-radius:4px;border:1px solid var(--line)}
.list span:first-of-type{width:68px;color:var(--mute)}
.use{font-size:14px;color:var(--mute);margin-bottom:12px}
.addrow{display:flex;gap:8px;flex-wrap:wrap;align-items:center}.addrow input{font:15px Inter,sans-serif;padding:9px 12px;border:1px solid var(--line);border-radius:8px;background:var(--bg);color:var(--ink);min-width:0}.addrow input[type=color]{padding:2px;width:48px;height:42px}.addrow #fh{width:110px}
#tray{position:fixed;left:0;right:0;bottom:0;background:var(--surf);border-top:1px solid var(--line);padding:10px 16px calc(10px + env(safe-area-inset-bottom,0px));display:flex;gap:12px;align-items:center}
#tray strong{font-size:14px;white-space:nowrap}
#chips{flex:1;display:flex;gap:6px;overflow-x:auto;align-items:center;min-height:40px}
.pc{flex:none;display:flex;align-items:center;border-radius:8px;border:1px solid var(--line);overflow:hidden}
.pc button{all:unset;cursor:pointer;padding:6px 8px;font-size:12px;line-height:1.2}
.pc button:focus-visible{outline:3px solid var(--acc)}
.pc .x{padding:6px 8px;background:rgba(255,255,255,.7);color:#222;font-weight:700}
#toast{position:fixed;left:50%;bottom:84px;transform:translateX(-50%);background:var(--ink);color:var(--bg);padding:8px 16px;border-radius:8px;font-size:14px;opacity:0;pointer-events:none;transition:opacity .2s}
#toast.on{opacity:1}
@media (prefers-reduced-motion:reduce){#toast{transition:none}}
</style>
</head>
<body>
<header><div class="bar">
  <div class="logo"><span class="dots" id="dots"></span>Palette Studio</div>
  <nav aria-label="Pages"><a href="#intro" data-v="intro">How to use</a><a href="#colors" data-v="colors">Colors</a><a href="#themes" data-v="themes">Themes</a></nav>
</div></header>

<main>
<section class="view" id="v-intro">
  <h1>Pick colors by family and shade number</h1>
  <p class="mute">Every color has a code like <code>Teal-500</code>. Use it to match paint, fabric or thread in interior and dress design. Here is one family, from lightest (50) to darkest (900):</p>
  <div class="scroll" id="hero"></div>
  <ol class="steps">
    <li><h2>Open Colors</h2><p>Browse 14 color families. Each has 10 shades numbered 50 to 900.</p></li>
    <li><h2>Copy or add</h2><p>Tap a shade to copy its hex code. Tap the + to add it to My palette at the bottom.</p></li>
    <li><h2>Try a theme</h2><p>Open Themes for ready-made combinations for rooms and outfits. Add one to My palette in one tap.</p></li>
    <li><h2>Take it with you</h2><p>Press Copy all in My palette to get codes with hex and RGB values to paste into notes or a design tool.</p></li>
  </ol>
  <div class="box"><h2>How shade numbers work</h2>
    <p>50 is almost white, 500 is the pure base color, 900 is nearly black. Smaller numbers suit large areas like walls and fabric backgrounds. Larger numbers suit furniture, trims and text.</p>
    <h2>The 60-30-10 rule</h2>
    <p>Use one main color for about 60% of the space, a supporting color for 30%, and an accent for 10%. Themes show this as a proportion bar.</p></div>
  <a class="btn" href="#colors">Browse colors</a> <a class="btn alt" href="#themes">See themes</a>
</section>

<section class="view" id="v-colors">
  <h1>Colors</h1>
  <p class="mute">Tap a shade to copy its hex code. Tap + to add it to My palette.</p>
  <div class="box"><h2>Add your own color family</h2><p class="mute">Enter a name and a base color. The 10 shades (50 to 900) are made for you, with your color as 500. Saved in this browser.</p><div class="addrow"><input id="fn" placeholder="Name, e.g. Sage" aria-label="Family name" maxlength="20"><input type="color" id="fp" value="#8FA48A" aria-label="Pick base color"><input id="fh" value="#8FA48A" aria-label="Base hex code" maxlength="7"><button class="btn" id="addfam">Add family</button></div></div>
  <div id="fams"></div>
</section>

<section class="view" id="v-themes">
  <h1>Theme suggestions</h1>
  <p class="mute">Each theme lists roles and shade codes. The bar shows how much of each color to use.</p>
  <div class="chips" id="filters" role="group" aria-label="Filter themes"></div>
  <div class="themes" id="themes"></div>
</section>
</main>

<div id="tray"><strong>My palette</strong><div id="chips"></div><button class="btn alt" id="copyall">Copy all</button><button class="btn alt" id="clear">Clear</button></div>
<div id="toast" role="status" aria-live="polite"></div>

<script>
const FAM={Red:"#E5484D",Orange:"#F76808",Amber:"#F5A623",Yellow:"#E8C500",Lime:"#8DB600",Green:"#30A46C",Teal:"#12A594",Sky:"#0EA5E9",Blue:"#3E63DD",Indigo:"#5B5BD6",Purple:"#8E4EC6",Pink:"#D6409F",Brown:"#A2745B",Gray:"#6B7280"};
const STEPS=[50,100,200,300,400,500,600,700,800,900];
const rgb=h=>[1,3,5].map(i=>parseInt(h.slice(i,i+2),16));
const hex=a=>"#"+a.map(v=>Math.round(v).toString(16).padStart(2,"0")).join("").toUpperCase();
const mix=(h,t,a)=>{const x=rgb(h),y=rgb(t);return hex(x.map((v,i)=>v*(1-a)+y[i]*a))};
const shade=(f,s)=>{const b=FAM[f];if(s===500)return b.toUpperCase();
  if(s<500)return mix(b,"#ffffff",{50:.9,100:.8,200:.6,300:.4,400:.2}[s]);
  return mix(b,"#000000",{600:.15,700:.3,800:.45,900:.6}[s])};
const ink=h=>{const [r,g,b]=rgb(h);return (0.299*r+0.587*g+0.114*b)>150?"#1d1b2e":"#ffffff"};
const rgbStr=h=>"rgb("+rgb(h).join(", ")+")";

let pal=[];
try{pal=JSON.parse(localStorage.getItem("ps-pal")||"[]")}catch(e){}
const save=()=>{try{localStorage.setItem("ps-pal",JSON.stringify(pal))}catch(e){}};
let custom={};
try{const c=JSON.parse(localStorage.getItem("ps-custom")||"{}");for(const k in c)if(/^#[0-9A-F]{6}$/i.test(c[k])){custom[k]=c[k];FAM[k]=c[k]}}catch(e){}
const saveC=()=>{try{localStorage.setItem("ps-custom",JSON.stringify(custom))}catch(e){}};

let tt;
function toast(m){const t=document.getElementById("toast");t.textContent=m;t.classList.add("on");clearTimeout(tt);tt=setTimeout(()=>t.classList.remove("on"),1600)}
async function copy(txt,msg){
  try{await navigator.clipboard.writeText(txt)}catch(e){
    const x=document.createElement("textarea");x.value=txt;document.body.appendChild(x);x.select();
    try{document.execCommand("copy")}catch(_){}x.remove()}
  toast(msg)}

function row(f){
  return `<div class="scroll"><div class="row">`+STEPS.map(s=>{
    const h=shade(f,s),c=f+"-"+s,on=pal.some(p=>p.c===c);
    return `<div class="sw" style="background:${h};color:${ink(h)}"><button class="cp" data-hex="${h}" title="Copy ${c} ${h}"><b>${s}</b><span>${h}</span></button><button class="ad${on?" on":""}" data-c="${c}" data-h="${h}" aria-label="${on?"Remove":"Add"} ${c}">${on?"✓":"+"}</button></div>`}).join("")+`</div></div>`}

function renderColors(){
  document.getElementById("fams").innerHTML=Object.keys(FAM).map(f=>`<section class="fam"><h2>${f} <small>${f}-50 to ${f}-900</small>${custom[f]?`<button class="chip" data-rmf="${f}">Remove family</button>`:""}</h2>${row(f)}</section>`).join("");
  document.getElementById("hero").innerHTML=row("Teal")}

const THEMES=[
{n:"Calm Scandinavian",t:"Interior",d:"Soft, airy and quiet. Good for bedrooms and living rooms.",u:"Walls and curtains in Main, sofa and rug in Support, cushions in Accent.",c:[["Main","Gray",100],["Support","Brown",300],["Neutral","Gray",700],["Accent","Teal",500],["Highlight","Amber",400]]},
{n:"Warm Earthy",t:"Interior",d:"Cozy and grounded, like clay and timber.",u:"Wood furniture in Support, wall paint in Main, plants and decor in Accent.",c:[["Main","Orange",100],["Support","Brown",400],["Neutral","Brown",800],["Accent","Green",700],["Highlight","Amber",500]]},
{n:"Coastal Fresh",t:"Interior",d:"Light and breezy. Works well in bright rooms and balconies.",u:"White-blue walls in Main, linen and sofa in Support, small decor in Highlight.",c:[["Main","Sky",100],["Support","Teal",300],["Neutral","Gray",50],["Accent","Blue",600],["Highlight","Yellow",300]]},
{n:"Modern Minimal",t:"Interior",d:"Neutral base with one confident accent.",u:"Keep walls neutral, add the Accent through one sofa or feature wall.",c:[["Main","Gray",50],["Support","Gray",300],["Neutral","Gray",900],["Accent","Indigo",500],["Highlight","Gray",600]]},
{n:"Spring Pastel",t:"Dress",d:"Fresh and gentle for daytime and festive wear.",u:"Main for the outfit, Support for dupatta or scarf, Highlight for jewelry.",c:[["Main","Pink",100],["Support","Lime",200],["Neutral","Sky",100],["Accent","Purple",200],["Highlight","Yellow",200]]},
{n:"Festive Bright",t:"Dress",d:"Rich, bold colors for celebrations and weddings.",u:"Main for the garment, Accent for borders, Highlight for embroidery.",c:[["Main","Red",600],["Support","Pink",500],["Neutral","Green",800],["Accent","Orange",500],["Highlight","Amber",400]]},
{n:"Autumn Classic",t:"Dress",d:"Deep warm tones that suit layers and knitwear.",u:"Main for coat or kurta, Support for inner layers, Neutral for bottoms.",c:[["Main","Brown",600],["Support","Orange",600],["Neutral","Gray",100],["Accent","Green",800],["Highlight","Amber",300]]},
{n:"Office Formal",t:"Dress",d:"Clean and professional with a quiet pop of blue.",u:"Navy as Main, gray as Support, a Blue shirt or tie as Accent.",c:[["Main","Blue",900],["Support","Gray",200],["Neutral","Gray",700],["Accent","Blue",500],["Highlight","Gray",50]]}
];
const W={Main:40,Support:25,Neutral:15,Accent:12,Highlight:8};
let filt="All";

function renderThemes(){
  document.getElementById("filters").innerHTML=["All","Interior","Dress"].map(k=>`<button class="chip${k===filt?" on":""}" data-f="${k}" aria-pressed="${k===filt}">${k}</button>`).join("");
  document.getElementById("themes").innerHTML=THEMES.map((t,i)=>({t,i})).filter(o=>filt==="All"||o.t.t===filt).map(({t,i})=>{
    const cs=t.c.map(([r,f,s])=>({r,c:f+"-"+s,h:shade(f,s)}));
    return `<article class="th"><h2>${t.n}</h2><div class="tag">${t.t}</div><p class="mute" style="margin-top:6px">${t.d}</p>
    <div class="prop" aria-hidden="true">${cs.map(x=>`<div style="flex:${W[x.r]};background:${x.h}"></div>`).join("")}</div>
    <ul class="list">${cs.map(x=>`<li><i style="background:${x.h}"></i><span>${x.r}</span><span>${x.c}</span><button class="chip cp2" data-hex="${x.h}" title="Copy ${x.h}">${x.h}</button></li>`).join("")}</ul>
    <p class="use">${t.u}</p><button class="btn" data-t="${i}">Use this theme</button></article>`}).join("")}

function renderTray(){
  document.getElementById("chips").innerHTML=pal.length?pal.map(p=>`<span class="pc" style="background:${p.h};color:${ink(p.h)}"><button data-hex="${p.h}" title="Copy ${p.h}"><b>${p.c}</b><br>${p.h}</button><button class="x" data-rm="${p.c}" aria-label="Remove ${p.c}">×</button></span>`).join(""):`<span class="mute" style="font-size:14px">Empty. Press + on any shade to add it.</span>`;
  document.getElementById("dots").innerHTML=["Indigo-500","Teal-400","Amber-400"].map(c=>{const [f,s]=c.split("-");return `<i style="background:${shade(f,+s)}"></i>`}).join("")}

function sync(){save();renderTray();renderColors()}

document.addEventListener("click",e=>{
  const b=e.target.closest("button");if(!b)return;
  if(b.dataset.hex){const h=b.dataset.hex;copy(h,"Copied "+h)}
  else if(b.classList.contains("ad")){const c=b.dataset.c,i=pal.findIndex(p=>p.c===c);
    if(i>-1)pal.splice(i,1);else if(pal.length<10)pal.push({c,h:b.dataset.h});else toast("My palette holds 10 colors");sync()}
  else if(b.dataset.rm){pal=pal.filter(p=>p.c!==b.dataset.rm);sync()}
  else if(b.dataset.t){pal=THEMES[+b.dataset.t].c.map(([r,f,s])=>({c:f+"-"+s,h:shade(f,s)}));sync();toast("Theme added to My palette")}
  else if(b.dataset.f){filt=b.dataset.f;renderThemes()}
  else if(b.dataset.rmf){const f=b.dataset.rmf;delete custom[f];delete FAM[f];pal=pal.filter(p=>!p.c.startsWith(f+"-"));saveC();sync()}
  else if(b.id==="addfam"){
    let n=document.getElementById("fn").value.replace(/[^A-Za-z0-9]/g,""),h=document.getElementById("fh").value.trim();
    if(h[0]!=="#")h="#"+h;
    if(/^#[0-9a-f]{3}$/i.test(h))h="#"+h.slice(1).replace(/./g,"$&$&");
    if(!n)return toast("Enter a family name");
    if(!/^#[0-9a-f]{6}$/i.test(h))return toast("Enter a hex code like #8FA48A");
    n=n[0].toUpperCase()+n.slice(1);
    if(FAM[n]&&!custom[n])return toast(n+" already exists");
    FAM[n]=custom[n]=h.toUpperCase();saveC();sync();document.getElementById("fn").value="";toast(n+" added at the end of the list")}
  else if(b.id==="clear"){pal=[];sync()}
  else if(b.id==="copyall"){if(!pal.length)return toast("My palette is empty");copy(pal.map(p=>p.c+"  "+p.h+"  "+rgbStr(p.h)).join("\n"),"Copied palette")}
});

function route(){
  let v=location.hash.slice(1);if(!["intro","colors","themes"].includes(v))v="intro";
  document.querySelectorAll(".view").forEach(s=>s.classList.toggle("on",s.id==="v-"+v));
  document.querySelectorAll("nav a").forEach(a=>{a.classList.toggle("on",a.dataset.v===v);if(a.dataset.v===v)a.setAttribute("aria-current","page");else a.removeAttribute("aria-current")});
  window.scrollTo(0,0)}
addEventListener("hashchange",route);
document.getElementById("fp").addEventListener("input",e=>{document.getElementById("fh").value=e.target.value.toUpperCase()});
document.getElementById("fh").addEventListener("input",e=>{const v=e.target.value.trim();if(/^#[0-9a-f]{6}$/i.test(v))document.getElementById("fp").value=v});
renderColors();renderThemes();renderTray();route();
</script>
</body>
</html>
