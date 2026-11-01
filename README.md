# PIXORA-DIGITAL-APP
 Pixora Digital Creative Services App
# 1. Navigate to your project folder
cd ~/storage/shared/Download/PIXORA_ANDROID_PROJECT

# 2. Check the git status to see your modified index.html
git status

# 3. Add the changes
git add .

# 4. Commit with a message
git commit -m "Update index.html with creator bio and contact info"

# 5. Push to GitHub
git push origin main
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"><meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<meta name="theme-color" content="#10101a"><meta name="description" content="Pixora Digital creative services.">
<link rel="manifest" href="manifest.webmanifest"><link rel="icon" href="icon.svg">
<title>Pixora Digital</title>
<style>
:root{--bg:#0c0d14;--surface:#151722;--surface2:#1c2030;--line:#292d40;--text:#f7f7fc;--muted:#969bad;--accent:#9b79ff;--accent2:#704be8;--green:#62d6a1}
*{box-sizing:border-box}body{margin:0;background:var(--bg);color:var(--text);font:15px/1.45 Inter,system-ui,-apple-system,Segoe UI,sans-serif;padding-bottom:calc(82px + env(safe-area-inset-bottom))}
button,input,textarea,select{font:inherit}button{cursor:pointer}.app{max-width:760px;margin:auto;min-height:100vh}
.top{position:sticky;top:0;z-index:5;background:#0c0d14ed;backdrop-filter:blur(16px);padding:14px 18px;border-bottom:1px solid #ffffff0d;display:flex;align-items:center;justify-content:space-between}
.brand{display:flex;align-items:center;gap:10px}.logo{width:39px;height:39px;border-radius:13px;background:linear-gradient(135deg,#c7b4ff,#704be8);display:grid;place-items:center;color:#171024;font-weight:950;font-size:20px}.brand b{font-size:14px;letter-spacing:1px}.brand small{display:block;color:var(--muted);font-size:10px;letter-spacing:1.7px}.iconbtn{width:40px;height:40px;border:1px solid var(--line);border-radius:14px;background:var(--surface);color:white;font-size:18px}
main{padding:18px}.screen{display:none}.screen.active{display:block}.welcome{padding:22px 19px;border-radius:25px;background:radial-gradient(circle at 90% 10%,#8662d855,transparent 40%),linear-gradient(135deg,#24203a,#171725);border:1px solid #39314f;position:relative;overflow:hidden}.eyebrow{color:#c9b8ff;font-size:11px;font-weight:800;letter-spacing:2px;text-transform:uppercase}.welcome h1{font-size:32px;line-height:1.08;margin:10px 0}.welcome p{color:#c0bfd0;margin:0 0 18px;max-width:420px}.btn{border:0;border-radius:13px;padding:12px 16px;font-weight:750;background:var(--surface2);color:white}.btn.primary{background:linear-gradient(135deg,#a98aff,#704be8)}.btn.full{width:100%}.sectionhead{display:flex;align-items:center;justify-content:space-between;margin:24px 2px 12px}.sectionhead h2{font-size:18px;margin:0}.textbtn{background:none;border:0;color:#bba8ff;font-weight:700}
.quick{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-top:14px}.quick div{background:var(--surface);border:1px solid var(--line);border-radius:16px;padding:13px 8px;text-align:center;color:#d9d7e4;font-size:12px}.quick span{display:block;font-size:22px;margin-bottom:5px}
.grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:11px}.service{background:var(--surface);border:1px solid var(--line);border-radius:18px;padding:15px;display:flex;flex-direction:column;min-height:184px}.service .symbol{width:39px;height:39px;border-radius:13px;background:#30264b;display:grid;place-items:center;font-size:20px;margin-bottom:12px}.tag{font-size:10px;color:#c7b6ff;letter-spacing:1px;text-transform:uppercase;font-weight:800}.service h3{font-size:15px;margin:5px 0}.service p{font-size:12px;color:var(--muted);margin:0 0 10px;flex:1}.price{font-size:17px;font-weight:850;margin-bottom:11px}.service .btn{padding:9px;font-size:12px}
.search{width:100%;background:var(--surface);border:1px solid var(--line);border-radius:14px;padding:13px 15px;color:white;margin:8px 0 14px;outline:none}
.panel{background:var(--surface);border:1px solid var(--line);border-radius:19px;padding:17px;margin-bottom:12px}.panel h2{font-size:18px;margin:0 0 12px}.muted{color:var(--muted)}label{display:block;font-size:12px;color:#c9c9d5;margin:12px 0 6px}input,textarea,select{width:100%;padding:13px;border-radius:12px;border:1px solid #35394d;background:#10121c;color:white;outline:none}textarea{min-height:100px;resize:vertical}.order{padding:14px;border-radius:15px;background:var(--surface);border:1px solid var(--line);margin-bottom:10px}.orderhead{display:flex;justify-content:space-between;gap:10px}.status{font-size:10px;padding:5px 8px;border-radius:20px;background:#40351e;color:#ffd88c;height:max-content}.empty{text-align:center;padding:38px 15px;color:var(--muted)}.empty .emoji{font-size:35px;margin-bottom:8px}.profilehero{text-align:center;padding:25px 10px}.avatar{width:72px;height:72px;margin:auto;border-radius:25px;background:linear-gradient(135deg,#c7b4ff,#704be8);display:grid;place-items:center;color:#171024;font-size:32px;font-weight:900}.profilehero h2{margin:12px 0 2px}.rowitem{padding:15px 2px;border-bottom:1px solid var(--line);display:flex;justify-content:space-between;align-items:center;color:#e5e4ee}.rowitem:last-child{border:0}.bottom{position:fixed;bottom:0;left:0;right:0;z-index:8;background:#11121ded;backdrop-filter:blur(18px);border-top:1px solid var(--line);padding:8px 8px calc(8px + env(safe-area-inset-bottom));display:flex;justify-content:center}.nav{width:min(760px,100%);display:grid;grid-template-columns:repeat(4,1fr);gap:4px}.nav button{background:none;border:0;color:#85899b;padding:7px 2px 4px;border-radius:12px;font-size:10px;font-weight:700}.nav button span{display:block;font-size:20px;margin-bottom:2px}.nav button.active{color:#c4afff;background:#28213b}.notice{font-size:11px;color:var(--muted);line-height:1.5;margin-top:14px}.toast{position:fixed;bottom:95px;left:50%;transform:translateX(-50%);background:#f6f1ff;color:#1c142b;padding:11px 16px;border-radius:12px;font-weight:750;display:none;z-index:20;white-space:nowrap}
@media(min-width:600px){main{padding:24px}.welcome{padding:30px}.welcome h1{font-size:40px}.grid{grid-template-columns:repeat(2,minmax(0,1fr))}}
</style></head>
<body><div class="app">
<header class="top"><div class="brand"><div class="logo">P</div><div><b>PIXORA DIGITAL</b><small>CREATE · INSPIRE · DOMINATE</small></div></div><button class="iconbtn" onclick="go('profile')" aria-label="Profile">◉</button></header>
<main>
<section id="home" class="screen active">
 <div class="welcome"><div class="eyebrow">Your creative studio</div><h1>Bring your ideas<br>to life.</h1><p>Get standout designs and content for your brand, business or next big idea.</p><button class="btn primary" onclick="go('services')">Explore services&nbsp; →</button></div>
 <div class="quick"><div onclick="go('services')"><span>✦</span>Our services</div><div onclick="go('orders')"><span>▤</span>My requests</div><div onclick="go('profile')"><span>◉</span>My profile</div></div>
 <div class="sectionhead"><h2>Popular services</h2><button class="textbtn" onclick="go('services')">See all</button></div>
 <div id="featured" class="grid"></div>
 <p class="notice">Pixora Digital is currently a demo storefront. Order requests are saved on this device only and are not sent to the business.</p>
</section>
<section id="services" class="screen"><div class="eyebrow">Explore</div><h1 style="margin:6px 0">Our services</h1><p class="muted">Creative work to help your brand stand out.</p><input id="search" class="search" placeholder="⌕  Search services..." oninput="renderServices()"><div id="allServices" class="grid"></div></section>
<section id="orders" class="screen"><div class="eyebrow">Your activity</div><h1 style="margin:6px 0 18px">My requests</h1><div id="myOrders"></div></section>
<section id="profile" class="screen">
 <div class="profilehero"><div class="avatar">P</div><h2>Nayebare Kevin</h2><div class="muted">Creator &amp; Developer</div></div>
 <div class="panel">
  <h2>Creator Bio</h2>
  <p class="muted" style="font-size:13px;line-height:1.5;">
   Created by <b>Nayebare Kevin</b> (completed O-Level education)[span_2](start_span)[span_2](end_span). Operating under Ugandan standards using MTN and Airtel services[span_3](start_span)[span_3](end_span). Passionate creator, book author[span_4](start_span)[span_4](end_span), and digital developer.
  </p>
 </div>
 <div class="panel">
  <div class="rowitem"><span>✦ &nbsp; Browse services</span><span>›</span></div>
  <div class="rowitem" onclick="go('orders')"><span>▤ &nbsp; My requests</span><span>›</span></div>
  <div class="rowitem"><span>ⓘ &nbsp; About Pixora Digital</span><span>›</span></div>
  <div class="rowitem"><span>☎ &nbsp; Creator Support / Contact</span><a href="tel:0730229280" style="color:#bba8ff;text-decoration:none;font-weight:700">0730229280</a></div>
 </div>
 <div class="panel">
  <h2>About this app</h2>
  <p class="muted" style="font-size:13px">Pixora Digital connects customers with creative design services. Prices and service details are demo values and should be confirmed with the business.</p>
  <button class="btn full" onclick="installApp()">Install app</button>
  <p class="notice">Install appears when your browser supports app installation. This version does not yet include online payments or cloud-synced accounts.</p>
 </div>
</section>
<section id="request" class="screen"><button class="textbtn" onclick="go('services')">← Back to services</button><h1 style="margin:12px 0 5px">Create a request</h1><p class="muted">Tell us a little about your project.</p><div class="panel"><form id="orderForm"><label for="customer">Your name</label><input id="customer" required maxlength="60" placeholder="Enter your name"><label for="contact">WhatsApp or email</label><input id="contact" required maxlength="100" placeholder="How can we reach you?"><label for="serviceSelect">Choose a service</label><select id="serviceSelect" required></select><label for="details">Project details</label><textarea id="details" required maxlength="700" placeholder="Describe your idea, preferred colours, text and deadline..."></textarea><button class="btn primary full" style="margin-top:16px">Send request</button></form><p class="notice">Demo mode: this request is stored only in this browser. It is not delivered to Pixora Digital.</p></div></section>
</main>
<nav class="bottom"><div class="nav"><button class="active" data-screen="home" onclick="go('home')"><span>⌂</span>Home</button><button data-screen="services" onclick="go('services')"><span>✦</span>Services</button><button data-screen="orders" onclick="go('orders')"><span>▤</span>Requests</button><button data-screen="profile" onclick="go('profile')"><span>◉</span>Profile</button></div></nav>
<div class="toast" id="toast"></div></div>
<script>
const services=[
{name:"Business poster",price:10000,desc:"Promotions, events and announcements.",tag:"Quick design",icon:"▧"},
{name:"Logo design",price:20000,desc:"A simple identity for a new or growing brand.",tag:"Branding",icon:"✳"},
{name:"Promotional video",price:25000,desc:"Short-form promo edit for social media.",tag:"Video",icon:"▶"},
{name:"Social media package",price:50000,desc:"A starter set of branded social graphics.",tag:"Popular",icon:"▦"}];
const key="pixora_demo_v2";let orders=[];try{orders=JSON.parse(localStorage.getItem(key)||"[]")}catch(e){}
let installPrompt=null;window.addEventListener("beforeinstallprompt",e=>{e.preventDefault();installPrompt=e});
const money=n=>"UGX "+Number(n).toLocaleString("en-UG");
function card(s){return `<article class="service"><div class="symbol">${s.icon}</div><div class="tag">${s.tag}</div><h3>${s.name}</h3><p>${s.desc}</p><div class="price">${money(s.price)}</div><button class="btn primary" onclick="startOrder('${s.name}')">Request service</button></article>`}
function renderServices(){let q=(document.getElementById("search")?.value||"").toLowerCase();let html=services.filter(s=>(s.name+" "+s.desc+" "+s.tag).toLowerCase().includes(q)).map(card).join("");document.getElementById("allServices").innerHTML=html||'<div class="empty">No matching services.</div>'}
document.getElementById("featured").innerHTML=services.slice(0,2).map(card).join("");renderServices();
function go(id){document.querySelectorAll(".screen").forEach(x=>x.classList.toggle("active",x.id===id));document.querySelectorAll(".nav button").forEach(x=>x.classList.toggle("active",x.dataset.screen===id));if(id==="orders")renderOrders();window.scrollTo({top:0,behavior:"smooth"})}
function startOrder(name){document.getElementById("serviceSelect").innerHTML=services.map(s=>`<option ${s.name===name?"selected":""}>${s.name}</option>`).join("");go("request")}
document.getElementById("orderForm").addEventListener("submit",e=>{e.preventDefault();orders.unshift({id:Date.now(),name:document.getElementById("customer").value.trim(),contact:document.getElementById("contact").value.trim(),service:document.getElementById("serviceSelect").value,details:document.getElementById("details").value.trim(),date:new Date().toLocaleString(),status:"Request saved"});localStorage.setItem(key,JSON.stringify(orders));e.target.reset();renderOrders();toast("Request saved on this device");go("orders")});
function renderOrders(){let el=document.getElementById("myOrders");el.innerHTML=orders.length?orders.map(o=>`<div class="order"><div class="orderhead"><strong>${o.service}</strong><span class="status">${o.status}</span></div><p class="muted" style="font-size:12px;margin:7px 0">${o.date}</p><div style="font-size:13px">${o.details.replace(/[&<>"']/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[c]))}</div></div>`).join(""):'<div class="empty"><div class="emoji">▤</div><b>No requests yet</b><p>Services you request will appear here.</p><button class="btn primary" onclick="go('services')">Explore services</button></div>'}
function toast(t){let x=document.getElementById("toast");x.textContent=t;x.style.display="block";setTimeout(()=>x.style.display="none",2300)}
async function installApp(){if(installPrompt){installPrompt.prompt();installPrompt=null}else toast("Use your browser menu and choose Add to Home screen")}
if("serviceWorker" in navigator && location.protocol!=="file:")window.addEventListener("load",()=>navigator.serviceWorker.register("./sw.js").catch(()=>{}));
</script></body></html>
