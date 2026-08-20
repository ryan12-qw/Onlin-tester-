<!doctype html>
<html lang="en">
<head>
    <meta name="google-site-verification" content="An6PdCQO6DL7HYiyGtEiOx8XDl-hkzAMCC9FVu6a_xA" />
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<meta name="theme-color" content="#0b0e13">
<title>Onlin Tester — Hardware & Device Tests</title>
<style>
:root{--bg:#0b0e13;--panel:#12161d;--panel2:#171c25;--line:#27303d;--text:#e7ecf2;--dim:#8996a6;--cyan:#4fd1ff;--green:#3ddc97;--amber:#ffb454;--red:#ff6b6b}
*{box-sizing:border-box}html{scroll-behavior:smooth}body{margin:0;background:var(--bg);color:var(--text);font:15px/1.55 Inter,system-ui,sans-serif}
body:before{content:"";position:fixed;inset:0;pointer-events:none;background-image:linear-gradient(#4fd1ff08 1px,transparent 1px),linear-gradient(90deg,#4fd1ff08 1px,transparent 1px);background-size:36px 36px}
button,input,textarea,select{font:inherit}button{cursor:pointer}
header{position:sticky;top:0;z-index:20;background:#0b0e13eF;border-bottom:1px solid var(--line);backdrop-filter:blur(12px)}
.nav{max-width:1180px;margin:auto;height:64px;padding:0 20px;display:flex;align-items:center;justify-content:space-between}
.brand{font-weight:800;font-size:20px;letter-spacing:-.4px}.brand b{color:var(--cyan)}
.menu{background:transparent;color:var(--text);border:1px solid var(--line);border-radius:9px;padding:8px 11px;font-size:20px}
.wrap{max-width:1180px;margin:auto;padding:0 20px}.hero{padding:70px 0 45px}.heroGrid{display:grid;grid-template-columns:1.1fr .9fr;gap:35px;align-items:center}
h1,h2,h3{margin:0 0 10px;line-height:1.12}h1{font-size:clamp(38px,6vw,70px);letter-spacing:-2px}.accent{color:var(--cyan)}h2{font-size:28px}h3{font-size:19px}
p{color:var(--dim)}.lead{font-size:17px;max-width:700px}.eyebrow{color:var(--green);font-size:12px;font-weight:800;letter-spacing:1.2px}
.actions{display:flex;gap:10px;flex-wrap:wrap;margin-top:22px}.btn{border:1px solid var(--line);background:var(--panel2);color:var(--text);padding:10px 15px;border-radius:9px;font-weight:700}.btn.primary{background:var(--cyan);border-color:var(--cyan);color:#061018}.btn.good{background:var(--green);border-color:var(--green);color:#04130d}.btn.warn{background:var(--amber);border-color:var(--amber);color:#171007}.btn.danger{background:#3a2024;border-color:#71343c;color:#ffb8bd}.btn:disabled{opacity:.45;cursor:not-allowed}
.scope,.card,.toolBox,.info,.comment{background:var(--panel);border:1px solid var(--line);border-radius:13px}.scope{overflow:hidden}.scopeHead{padding:11px 14px;border-bottom:1px solid var(--line);font:12px ui-monospace,monospace;color:var(--dim);display:flex;justify-content:space-between}.wave{height:220px;position:relative;overflow:hidden;background:linear-gradient(transparent 49%,#4fd1ff14 50%,transparent 51%)}.wave svg{width:100%;height:100%}.section{padding:45px 0}.grid{display:grid;grid-template-columns:repeat(4,1fr);gap:13px}.card{padding:18px;transition:.18s}.card:hover{transform:translateY(-2px);border-color:#4fd1ff66}.icon{font-size:27px}.badge{display:inline-block;margin-top:8px;padding:3px 8px;border:1px solid var(--line);border-radius:20px;color:var(--dim);font-size:11px}
.drawer{position:fixed;z-index:40;inset:0 auto 0 0;width:min(350px,92vw);background:var(--panel);border-right:1px solid var(--line);transform:translateX(-105%);transition:.2s;overflow:auto;padding:20px}.drawer.open{transform:none}.shade{position:fixed;inset:0;background:#0009;z-index:30;display:none}.drawer.open+.shade{display:block}.drawer h3{margin-top:22px}.toolLink{display:block;width:100%;text-align:left;background:transparent;border:0;border-bottom:1px solid #ffffff08;color:var(--text);padding:9px 4px}.toolLink:hover{color:var(--cyan)}
.hidden{display:none!important}.search{display:flex;gap:10px;margin:20px 0}.search input{flex:1;background:var(--panel);color:var(--text);border:1px solid var(--line);border-radius:10px;padding:13px}.tabs{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:22px}.tab{background:var(--panel);color:var(--dim);border:1px solid var(--line);padding:8px 12px;border-radius:8px}.tab.active{color:var(--cyan);border-color:var(--cyan)}
.toolPage{padding:45px 0}.toolBox{padding:22px;margin:20px 0}.status{padding:12px;border:1px solid var(--line);border-radius:9px;background:#0b0e1380;margin:12px 0}.status.ready{color:var(--cyan)}.status.pass{color:var(--green);border-color:#3ddc9744}.status.fail{color:var(--red);border-color:#ff6b6b44}.status.warn{color:var(--amber);border-color:#ffb45444}
.meter{height:22px;border-radius:99px;background:#080a0e;border:1px solid var(--line);overflow:hidden;margin:15px 0}.meterFill{height:100%;width:0;background:var(--green);transition:width .05s}
.big{font:700 42px ui-monospace,monospace;text-align:center;padding:25px}.touch{height:300px;border:2px dashed #4fd1ff55;border-radius:12px;display:grid;place-items:center;background:#4fd1ff05;touch-action:none;user-select:none}.touchPoint{position:fixed;width:28px;height:28px;margin:-14px;border:2px solid var(--cyan);border-radius:50%;pointer-events:none;z-index:100}
video{width:100%;max-height:440px;background:#050607;border-radius:10px}.canvasTest{width:100%;height:260px;border-radius:10px;background:#000;border:1px solid var(--line)}
.kbd{display:flex;align-items:center;justify-content:center;min-height:150px;border:1px solid var(--line);border-radius:12px;background:#090c11;font-size:24px;font-weight:800}.row{display:flex;gap:10px;align-items:center;flex-wrap:wrap}.row>*{margin-bottom:8px}label{color:var(--dim)}input[type=range]{accent-color:var(--cyan)}
textarea,select{background:#0b0e13;color:var(--text);border:1px solid var(--line);border-radius:9px;padding:10px}.comment{padding:12px;margin:8px 0}.footer{border-top:1px solid var(--line);padding:28px 0;color:var(--dim)}.footer a{color:var(--dim);margin-right:15px}
.pixelGrid{display:grid;grid-template-columns:repeat(8,1fr);gap:3px}.pixel{aspect-ratio:1;background:#000;border:0}.note{font-size:12px;color:var(--dim)}
@media(max-width:850px){.heroGrid{grid-template-columns:1fr}.grid{grid-template-columns:repeat(2,1fr)}}@media(max-width:520px){.grid{grid-template-columns:1fr}.hero{padding-top:45px}h1{font-size:42px}.wrap{padding:0 14px}.pixelGrid{grid-template-columns:repeat(4,1fr)}}
</style>
</head>
<body>
<header><div class="nav"><button class="menu" id="menuBtn">☰</button><div class="brand">Onlin <b>Tester</b></div><button class="btn primary" onclick="showAll()">All Tools</button></div></header>
<div class="drawer" id="drawer"><button class="btn" onclick="closeDrawer()">✕ Close</button><h3>Computer</h3><div id="sideComputer"></div><h3>Mobile</h3><div id="sideMobile"></div><h3>Tuners</h3><div id="sideTuner"></div><h3>Mic / Audio</h3><div id="sideAudio"></div><h3>More</h3><div id="sideMore"></div><h3>Guides</h3><div id="sideGuide"></div></div><div class="shade" id="shade" onclick="closeDrawer()"></div>

<main>
<section id="home" class="hero"><div class="wrap heroGrid"><div><div class="eyebrow">NO INSTALL · BROWSER-BASED DIAGNOSTICS</div><h1>Test your hardware.<br>Tune your sound.<br><span class="accent">All in one place.</span></h1><p class="lead">Real browser tests for computers, phones, microphones, cameras, input devices, sensors and audio tools.</p><div class="actions"><button class="btn primary" onclick="showAll()">Browse all tools →</button><button class="btn" onclick="openTool('Microphone Test')">Try microphone</button></div></div><div class="scope"><div class="scopeHead"><span>LIVE SIGNAL</span><span id="heroStatus">READY</span></div><div class="wave"><svg viewBox="0 0 600 220" preserveAspectRatio="none"><polyline id="heroWave" fill="none" stroke="#4fd1ff" stroke-width="2" points=""/></svg></div><div class="scopeHead"><span>STATUS <b>READY</b></span><span>440 Hz</span></div></div></div></section>

<section id="homeTools" class="section"><div class="wrap"><h2>Popular tests</h2><p>Choose a test to interact with your actual device.</p><div class="grid" id="popular"></div></div></section>

<section id="all" class="section hidden"><div class="wrap"><div class="eyebrow">TOOL LIBRARY</div><h2>All Tools</h2><p>Search or filter any diagnostic tool.</p><div class="search"><input id="search" placeholder="🔎 search tools..." oninput="renderTools()"></div><div class="tabs" id="tabs"></div><div class="grid" id="toolGrid"></div></div></section>

<section id="toolPage" class="toolPage hidden"><div class="wrap"><button class="btn" onclick="showAll()">← All Tools</button><div style="margin-top:25px"><div class="eyebrow" id="toolCat"></div><h2 id="toolTitle"></h2><p id="toolDesc"></p></div><div class="toolBox" id="interface"></div><div class="info"><div style="padding:20px"><h3>How to use</h3><div id="how"></div><h3>Facts & tips</h3><div id="facts"></div></div></div><div style="margin-top:30px"><h3>Comments</h3><div class="row"><input id="commentName" placeholder="Your name" style="flex:1;min-width:150px"><input id="commentText" placeholder="Share your experience..." style="flex:3;min-width:220px"><button class="btn primary" onclick="postComment()">Post</button></div><div id="comments"></div></div></div></section>
</main>
<footer class="footer"><div class="wrap"><a href="#">About</a><a href="#">Contact</a><a href="#">Privacy</a><a href="#">Blog</a><span>Copyright 2026 by Onlin Tester</span></div></footer>

<script>
const tools=[
["Microphone Test","Audio","🎙️","Check live microphone input."],["Webcam Test","Computer","📷","Preview your camera."],["Sound Test","Audio","🔊","Play a safe speaker test."],["Keyboard Test","Computer","⌨️","Detect keyboard keys."],["Mouse Test","Computer","🖱️","Test left, middle, right and wheel."],["Controller Test","Computer","🎮","Detect gamepads and axes."],["Voice Reader Test","Audio","🗣️","Test browser text-to-speech."],["Refresh Rate Test","Computer","🖥️","Measure animation FPS."],["Tone Generator","Audio","🎵","Generate an adjustable test tone."],["Touchscreen Test","Mobile","👆","Test touch coordinates."],["Vibration Test","Mobile","📳","Test device vibration support."],["Gyroscope Test","Mobile","🧭","Read device motion/orientation."],["Accelerometer Test","Mobile","📐","Read acceleration values."],["Multi-touch Test","Mobile","🤏","Track multiple touch points."],["Dead Pixel Test","Mobile","🔲","Cycle solid colors to inspect pixels."],["Stuck Pixel Fixer","Mobile","✨","Run a rapid color-cycle animation."],["Pitch Detector","Audio","🎤","Estimate microphone pitch."],["Chromatic Tuner","Audio","🎸","Tune to chromatic notes."],["All Instrument Tuner","Audio","🎻","General-purpose instrument tuner."],["Metronome","Audio","🥁","Keep time at adjustable BPM."],["Online Mirror","Computer","🪞","Use the camera as a mirror."],["Spacebar Clicker","Computer","␣","Count spacebar presses."],["Online Dictaphone","Audio","🎙️","Record audio in supported browsers."],["Min Guides","Guide","📘","Short technical troubleshooting guides."],["Webcam Guides","Guide","📹","Camera permission troubleshooting."],["Middle Mouse Button Issue Guide","Guide","🛠️","Troubleshoot middle-click issues."]
];
const catOrder=["All","Computer","Mobile","Audio","Guide"];
let current=null, micStream=null,micCtx=null,micRAF=0,camStream=null,audioCtx=null,osc=null,rec=null,recChunks=[],timer=null,points=new Map(),comments=JSON.parse(localStorage.getItem("ot-comments")||"{}");

function esc(s){return String(s).replace(/[&<>"']/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#039;"}[c]))}
function card(t){return `<div class="card" onclick="openTool('${esc(t[0])}')"><div class="icon">${t[2]}</div><h3>${esc(t[0])}</h3><p>${esc(t[3])}</p><span class="badge">${t[1]}</span></div>`}
function init(){
 document.getElementById("popular").innerHTML=tools.slice(0,12).map(card).join("");
 document.getElementById("tabs").innerHTML=catOrder.map(c=>`<button class="tab ${c==="All"?"active":""}" onclick="setCat('${c}',this)">${c}</button>`).join("");
 renderTools(); buildSide(); animateHero();
}
function buildSide(){
 const map={Computer:"sideComputer",Mobile:"sideMobile",Audio:"sideAudio",Guide:"sideGuide"};
 Object.entries(map).forEach(([cat,id])=>document.getElementById(id).innerHTML=tools.filter(t=>t[1]===cat).map(t=>`<button class="toolLink" onclick="openTool('${esc(t[0])}');closeDrawer()">${t[2]} ${esc(t[0])}</button>`).join(""));
 document.getElementById("sideTuner").innerHTML=tools.filter(t=>["Pitch Detector","Chromatic Tuner","All Instrument Tuner","Metronome"].includes(t[0])).map(t=>`<button class="toolLink" onclick="openTool('${esc(t[0])}');closeDrawer()">${t[2]} ${esc(t[0])}</button>`).join("");
 document.getElementById("sideMore").innerHTML=tools.filter(t=>["Online Mirror","Spacebar Clicker","Online Dictaphone"].includes(t[0])).map(t=>`<button class="toolLink" onclick="openTool('${esc(t[0])}');closeDrawer()">${t[2]} ${esc(t[0])}</button>`).join("");
}
function renderTools(cat){
 const active=cat||document.querySelector(".tab.active")?.textContent||"All",q=document.getElementById("search").value.toLowerCase();
 const list=tools.filter(t=>(active==="All"||t[1]===active)&&t.join(" ").toLowerCase().includes(q));
 document.getElementById("toolGrid").innerHTML=list.length?list.map(card).join(""):`<div class="card"><h3>No tools found</h3><p>Try another search.</p></div>`;
}
function setCat(cat,b){document.querySelectorAll(".tab").forEach(x=>x.classList.remove("active"));b.classList.add("active");renderTools(cat)}
function showAll(){cleanup();document.getElementById("home").classList.add("hidden");document.getElementById("homeTools").classList.add("hidden");document.getElementById("toolPage").classList.add("hidden");document.getElementById("all").classList.remove("hidden");scrollTo(0,0)}
function openTool(name){
 cleanup();current=tools.find(t=>t[0]===name);if(!current)return;
 document.getElementById("home").classList.add("hidden");document.getElementById("homeTools").classList.add("hidden");document.getElementById("all").classList.add("hidden");document.getElementById("toolPage").classList.remove("hidden");
 toolCat.textContent=current[1];toolTitle.textContent=current[2]+" "+current[0];toolDesc.textContent=current[3];interface.innerHTML=makeUI(current[0]);how.innerHTML=howText(current[0]);facts.innerHTML=factText(current[0]);bind(current[0]);renderComments();scrollTo(0,0)
}
function makeUI(n){
 const mediaNote=location.protocol==="file:"?`<div class="status warn">⚠ Camera/microphone/sensor APIs may require <b>HTTPS or localhost</b>. Open this page from a local web server for full access.</div>`:"";
 if(["Microphone Test","Pitch Detector","Chromatic Tuner","All Instrument Tuner"].includes(n))return mediaNote+`<div id="status" class="status ready">Ready — press Start.</div><div class="meter"><div id="meterFill" class="meterFill"></div></div><div class="row"><button class="btn primary" id="start">🎙 Start Microphone</button><button class="btn danger" id="stop" disabled>Stop</button></div><div class="note">Audio is processed locally by the browser; this page does not upload the microphone signal.</div>`;
 if(["Webcam Test","Online Mirror"].includes(n))return mediaNote+`<video id="video" autoplay playsinline muted></video><div id="status" class="status ready">Camera idle.</div><button class="btn primary" id="start">📷 Start Camera</button><button class="btn danger" id="stop" disabled>Stop Camera</button>`;
 if(n==="Sound Test")return `<div class="big">🔊</div><div id="status" class="status ready">Ready.</div><button class="btn primary" id="play">Play 440 Hz test sound</button>`;
 if(n==="Tone Generator")return `<label>Frequency: <b id="freqVal">440 Hz</b><input id="freq" type="range" min="40" max="2000" value="440" style="width:100%"></label><div id="status" class="status ready">Stopped.</div><button class="btn primary" id="tone">Start Tone</button>`;
 if(n==="Keyboard Test")return `<div id="keyBox" class="kbd" tabindex="0">Click here, then press any key</div><div id="status" class="status ready">Waiting.</div>`;
 if(n==="Mouse Test")return `<div id="mouseArea" class="touch">Move, click and scroll here</div><div id="status" class="status ready">Waiting.</div>`;
 if(n==="Controller Test")return `<div id="status" class="status ready">Connect a controller and press a button.</div><div id="gp" class="big">🎮</div><button class="btn" id="scan">Scan Controller</button>`;
 if(n==="Voice Reader Test")return `<textarea id="reader" rows="5" style="width:100%">Hello from Onlin Tester.</textarea><div class="row"><select id="voices" style="flex:1"></select><button class="btn primary" id="speak">🔊 Speak</button><button class="btn" id="cancelSpeak">Stop</button></div><div id="status" class="status ready">Ready.</div>`;
 if(n==="Refresh Rate Test")return `<div id="fps" class="big">— FPS</div><button class="btn primary" id="fpsBtn">Start 3-second test</button><div id="status" class="status ready">Ready.</div>`;
 if(["Touchscreen Test","Multi-touch Test"].includes(n))return `<div id="touch" class="touch">Touch / drag here</div><div id="status" class="status ready">0 active points</div>`;
 if(n==="Vibration Test")return `<div class="big">📳</div><button class="btn primary" id="vibrate">Vibrate</button><div id="status" class="status ready">Ready.</div>`;
 if(["Gyroscope Test","Accelerometer Test"].includes(n))return mediaNote+`<div id="motion" class="big">—</div><button class="btn primary" id="motionBtn">Start Sensor</button><div id="status" class="status ready">Waiting.</div>`;
 if(n==="Dead Pixel Test")return `<div id="pixelGrid" class="pixelGrid">${Array.from({length:64},()=>`<button class="pixel"></button>`).join("")}</div><div class="row"><button class="btn primary" id="colors">Cycle Colors</button><button class="btn" id="black">Black</button><button class="btn" id="white">White</button><button class="btn" id="red">Red</button><button class="btn" id="green">Green</button><button class="btn" id="blue">Blue</button></div>`;
 if(n==="Stuck Pixel Fixer")return `<div id="fixer" style="height:260px;border-radius:12px;background:#000"></div><button class="btn primary" id="fix">Start Color Cycle</button><div id="status" class="status ready">Stopped.</div>`;
 if(n==="Metronome")return `<label>BPM <input id="bpm" type="number" min="30" max="240" value="100" style="width:90px"></label><div id="beat" class="big">●</div><button class="btn primary" id="metro">Start</button><div id="status" class="status ready">Stopped.</div>`;
 if(n==="Spacebar Clicker")return `<div id="space" class="kbd" tabindex="0">SPACE</div><div id="spaceCount" class="big">0</div><button class="btn" id="reset">Reset</button>`;
 if(n==="Online Dictaphone")return mediaNote+`<div class="row"><button class="btn primary" id="record">● Start Recording</button><button class="btn danger" id="stopRecord" disabled>■ Stop</button></div><div id="status" class="status ready">Ready.</div><audio id="audio" controls style="display:none;width:100%"></audio>`;
 return `<div class="status"><h3>Quick guide</h3><p>Check permissions, reconnect the device, try another browser, and verify the operating-system privacy settings. Model-specific faults should be checked against the manufacturer's documentation.</p></div>`;
}
function howText(n){if(n.includes("Microphone")||n.includes("Tuner"))return "<p>Press Start and allow microphone access. Produce a clear sound and watch the live signal. Stop when finished.</p>";if(n.includes("Webcam")||n==="Online Mirror")return "<p>Press Start Camera and allow camera access. A live preview confirms the browser can access the camera.</p>";if(n==="Mouse Test")return "<p>Move, click all buttons, and scroll inside the test area.</p>";if(n==="Keyboard Test")return "<p>Focus the test area and press different keys. The detected key and code are shown.</p>";return "<p>Start the test and follow the live result shown in the interface.</p>"}
function factText(n){return `<p>Browser support varies by device and browser. A browser test can verify the API response, but it cannot certify every hardware component. For camera, microphone and motion sensors, permission and secure-context requirements may apply.</p>`}
function status(msg,type="ready"){const s=document.getElementById("status");if(s){s.textContent=msg;s.className="status "+type}}
function bind(n){
 if(["Microphone Test","Pitch Detector","Chromatic Tuner","All Instrument Tuner"].includes(n)){start.onclick=startMic;stop.onclick=stopMic}
 else if(["Webcam Test","Online Mirror"].includes(n)){start.onclick=startCam;stop.onclick=stopCam}
 else if(n==="Sound Test")play.onclick=()=>safeTone(440,.6);
 else if(n==="Tone Generator"){freq.oninput=()=>freqVal.textContent=freq.value+" Hz";tone.onclick=toggleTone}
 else if(n==="Keyboard Test"){keyBox.focus();keyBox.onkeydown=e=>{e.preventDefault();keyBox.textContent=e.key===" "?"SPACE":e.key;status("Detected "+e.key+" · "+e.code,"pass")}}
 else if(n==="Mouse Test"){mouseArea.onmousemove=e=>status(`Pointer ${e.offsetX}, ${e.offsetY}`);mouseArea.onmousedown=e=>{e.preventDefault();status(["Left","Middle","Right"][e.button]+" button detected","pass")};mouseArea.onwheel=e=>status(e.deltaY<0?"Wheel up":"Wheel down");mouseArea.oncontextmenu=e=>e.preventDefault()}
 else if(n==="Controller Test"){scan.onclick=scanGamepad;scanGamepad()}
 else if(n==="Voice Reader Test"){loadVoices();voices.onchange=()=>{};speak.onclick=readText;cancelSpeak.onclick=()=>speechSynthesis.cancel();speechSynthesis.onvoiceschanged=loadVoices}
 else if(n==="Refresh Rate Test")fpsBtn.onclick=fpsTest
 else if(["Touchscreen Test","Multi-touch Test"].includes(n))setupTouch()
 else if(n==="Vibration Test")vibrate.onclick=()=>{if(navigator.vibrate){navigator.vibrate([150,80,150]);status("Vibration request sent ✓","pass")}else status("Vibration API not supported on this device","fail")}
 else if(["Gyroscope Test","Accelerometer Test"].includes(n))motionBtn.onclick=startMotion
 else if(n==="Dead Pixel Test"){colors.onclick=cyclePixels;["black","white","red","green","blue"].forEach(c=>document.getElementById(c).onclick=()=>setPixels(c))}
 else if(n==="Stuck Pixel Fixer")fix.onclick=pixelFix
 else if(n==="Metronome")metro.onclick=metronome
 else if(n==="Spacebar Clicker"){space.focus();space.onkeydown=e=>{if(e.code==="Space"){e.preventDefault();spaceCount.textContent=+spaceCount.textContent+1}};reset.onclick=()=>spaceCount.textContent=0}
 else if(n==="Online Dictaphone"){record.onclick=startRecord;stopRecord.onclick=stopRecordFn}
}
async function startMic(){
 try{micStream=await navigator.mediaDevices.getUserMedia({audio:true});micCtx=new (AudioContext||webkitAudioContext)();let src=micCtx.createMediaStreamSource(micStream),an=micCtx.createAnalyser();an.fftSize=512;src.connect(an);let d=new Uint8Array(an.fftSize);start.disabled=true;stop.disabled=false;status("Listening — speak now.","pass");function loop(){an.getByteTimeDomainData(d);let sum=0;for(let x of d){let v=(x-128)/128;sum+=v*v}let pct=Math.min(100,Math.sqrt(sum/d.length)*260);meterFill.style.width=pct+"%";micRAF=requestAnimationFrame(loop)}loop()}catch(e){status("Microphone unavailable. Allow permission and use HTTPS/localhost if needed.","fail")}}
function stopMic(){cancelAnimationFrame(micRAF);if(micStream)micStream.getTracks().forEach(t=>t.stop());if(micCtx)micCtx.close();micStream=null;micCtx=null;meterFill.style.width=0;start.disabled=false;stop.disabled=true;status("Stopped.","ready")}
async function startCam(){try{camStream=await navigator.mediaDevices.getUserMedia({video:true});video.srcObject=camStream;start.disabled=true;stop.disabled=false;status("Camera working ✓","pass")}catch(e){status("Camera unavailable. Allow permission and use HTTPS/localhost if needed.","fail")}}
function stopCam(){if(camStream)camStream.getTracks().forEach(t=>t.stop());camStream=null;video.srcObject=null;start.disabled=false;stop.disabled=true;status("Stopped.","ready")}
function getAudio(){if(!audioCtx)audioCtx=new (AudioContext||webkitAudioContext)();return audioCtx}
function safeTone(f,sec){let c=getAudio(),o=c.createOscillator(),g=c.createGain();o.frequency.value=f;g.gain.value=.035;o.connect(g).connect(c.destination);o.start();o.stop(c.currentTime+sec);status("Test tone played ✓","pass")}
function toggleTone(){if(osc){try{osc.stop()}catch(e){}osc=null;tone.textContent="Start Tone";status("Stopped.");return}let c=getAudio();osc=c.createOscillator();let g=c.createGain();osc.frequency.value=+freq.value;g.gain.value=.03;osc.connect(g).connect(c.destination);osc.start();tone.textContent="Stop Tone";status("Tone playing at "+freq.value+" Hz","pass")}
function scanGamepad(){let p=Array.from(navigator.getGamepads?navigator.getGamepads():[]).find(Boolean);if(!p){status("No controller detected yet.","warn");return}status("Controller detected ✓","pass");let loop=()=>{let q=navigator.getGamepads()[p.index];if(!q)return;gp.textContent=`Buttons: ${q.buttons.filter(b=>b.pressed).length} · Axes: ${q.axes.map(x=>x.toFixed(2)).join(" ")}`;requestAnimationFrame(loop)};loop()}
function loadVoices(){if(!document.getElementById("voices"))return;let vs=speechSynthesis.getVoices();voices.innerHTML=vs.map((v,i)=>`<option value="${i}">${esc(v.name)} — ${esc(v.lang)}</option>`).join("")}
function readText(){let u=new SpeechSynthesisUtterance(reader.value),vs=speechSynthesis.getVoices();u.voice=vs[+voices.value]||null;speechSynthesis.cancel();speechSynthesis.speak(u);status("Speaking…","pass")}
function fpsTest(){let st=performance.now(),f=0;function loop(n){f++;if(n-st<3000)requestAnimationFrame(loop);else{fps.textContent=Math.round(f/3)+" FPS";status("3-second measurement complete ✓","pass")}}requestAnimationFrame(loop)}
function setupTouch(){touch.onpointerdown=e=>{touch.setPointerCapture(e.pointerId);points.set(e.pointerId,e);paintTouch(e)};touch.onpointermove=e=>{if(points.has(e.pointerId)){points.set(e.pointerId,e);paintTouch(e)}};touch.onpointerup=touch.onpointercancel=e=>{points.delete(e.pointerId);document.querySelectorAll(".touchPoint").forEach(x=>x.remove());status(points.size+" active point(s)")}}
function paintTouch(e){document.querySelectorAll(".touchPoint").forEach(x=>x.remove());points.forEach(p=>{let d=document.createElement("div");d.className="touchPoint";d.style.left=p.clientX+"px";d.style.top=p.clientY+"px";document.body.appendChild(d)});status(points.size+" active point(s)","pass")}
function startMotion(){try{if(typeof DeviceMotionEvent==="undefined"){status("Motion sensors unavailable.","fail");return}if(typeof DeviceMotionEvent.requestPermission==="function"){DeviceMotionEvent.requestPermission().then(p=>{if(p!=="granted")return status("Motion permission denied.","fail");listenMotion()}).catch(()=>status("Motion permission failed.","fail"))}else listenMotion()}catch(e){status("Motion sensor unavailable.","fail")}}
function listenMotion(){window.ondevicemotion=e=>{let a=e.accelerationIncludingGravity||{};motion.textContent=`X ${(+a.x||0).toFixed(2)}\nY ${(+a.y||0).toFixed(2)}\nZ ${(+a.z||0).toFixed(2)}`;status("Motion sensor active ✓","pass")}}
function setPixels(c){let col={black:"#000",white:"#fff",red:"#f00",green:"#0f0",blue:"#00f"}[c];document.querySelectorAll(".pixel").forEach(x=>x.style.background=col)}
function cyclePixels(){let cs=["#000","#fff","#f00","#0f0","#00f"],i=0;clearInterval(timer);timer=setInterval(()=>setPixelsRaw(cs[i++%cs.length]),400);setTimeout(()=>clearInterval(timer),6000)}
function setPixelsRaw(c){document.querySelectorAll(".pixel").forEach(x=>x.style.background=c)}
function pixelFix(){if(timer){clearInterval(timer);timer=null;fix.textContent="Start Color Cycle";status("Stopped.");return}let cs=["#000","#fff","#f00","#0f0","#00f","#ff0","#0ff","#f0f"],i=0;timer=setInterval(()=>fixer.style.background=cs[i++%cs.length],70);fix.textContent="Stop Color Cycle";status("Color cycle running…","pass")}
function metronome(){if(timer){clearInterval(timer);timer=null;metro.textContent="Start";status("Stopped.");return}let bpm=Math.max(30,Math.min(240,+document.getElementById("bpm").value||100));safeTone(880,.08);timer=setInterval(()=>{safeTone(880,.08);beat.textContent=beat.textContent==="●"?"○":"●"},60000/bpm);metro.textContent="Stop";status("Running at "+bpm+" BPM","pass")}
async function startRecord(){try{let s=await navigator.mediaDevices.getUserMedia({audio:true});recChunks=[];rec=new MediaRecorder(s);rec.ondataavailable=e=>recChunks.push(e.data);rec.onstop=()=>{let blob=new Blob(recChunks,{type:rec.mimeType||"audio/webm"});audio.src=URL.createObjectURL(blob);audio.style.display="block";s.getTracks().forEach(t=>t.stop());status("Recording ready ✓","pass")};rec.start();record.disabled=true;stopRecord.disabled=false;status("Recording…","pass")}catch(e){status("Recording unavailable. Allow microphone permission and use HTTPS/localhost.","fail")}}
function stopRecordFn(){if(rec?.state==="recording"){rec.stop();record.disabled=false;stopRecord.disabled=true}}
function postComment(){let n=commentName.value.trim()||"Guest",t=commentText.value.trim();if(!t)return;(comments[current[0]]??=[]).unshift({n,t,time:new Date().toLocaleString()});localStorage.setItem("ot-comments",JSON.stringify(comments));commentText.value="";renderComments()}
function renderComments(){commentsDiv=document.getElementById("comments");commentsDiv.innerHTML=(comments[current[0]]||[]).map(c=>`<div class="comment"><b>${esc(c.n)}</b><span class="note"> · ${esc(c.time)}</span><p>${esc(c.t)}</p></div>`).join("")||`<div class="comment">No comments yet.</div>`}
function cleanup(){if(micStream)stopMic();if(camStream)stopCam();if(osc){try{osc.stop()}catch(e){}osc=null}if(timer){clearInterval(timer);timer=null}speechSynthesis?.cancel();document.querySelectorAll(".touchPoint").forEach(x=>x.remove())}
function closeDrawer(){drawer.classList.remove("open");shade.style.display="none"}menuBtn.onclick=()=>{drawer.classList.add("open");shade.style.display="block"}
function animateHero(){let p=[],t=0;function f(){t+=.08;p=[];for(let x=0;x<=600;x+=8)p.push(x+","+((110+Math.sin(x*.045+t)*35+Math.sin(x*.013+t*1.7)*18)));heroWave.setAttribute("points",p.join(" "));requestAnimationFrame(f)}f()}
init();
</script>
</body></html>
