<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>NEON DRIVE // ARRIVAL</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700;900&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
<style>
  :root{
    --void: #030308;
    --cyan: #00f0ff;
    --magenta: #ff2bd6;
    --amber: #ffb000;
    --grid: #0a2a33;
    --glass: rgba(10, 16, 22, 0.35);
  }
  *{ box-sizing:border-box; }
  html,body{
    margin:0; width:100%; height:100%; overflow:hidden;
    background:var(--void);
    font-family:'Space Mono', monospace;
  }
  canvas{ display:block; position:fixed; inset:0; }

  /* ---------- ENTRY SCREEN ---------- */
  #entry{
    position:fixed; inset:0; z-index:50;
    display:flex; align-items:center; justify-content:center;
    background:radial-gradient(ellipse at 50% 50%, #050a10 0%, #010103 70%);
    transition:opacity 1.1s ease;
  }
  #entry::before{
    content:''; position:absolute; inset:0;
    background-image:
      linear-gradient(rgba(0,240,255,0.035) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,240,255,0.035) 1px, transparent 1px);
    background-size:44px 44px;
    mask-image:radial-gradient(ellipse at 50% 50%, black 0%, transparent 72%);
  }
  #entry.hidden{ opacity:0; pointer-events:none; }

  .eyebrow{
    position:absolute; top:14%; left:50%; transform:translateX(-50%);
    color:var(--cyan); font-size:11px; letter-spacing:6px;
    opacity:0.55; text-transform:uppercase;
  }

  #enterBtn{
    position:relative;
    padding:22px 58px;
    font-family:'Orbitron', sans-serif;
    font-weight:700; font-size:15px; letter-spacing:6px;
    color:#dffdff;
    background:var(--glass);
    border:1px solid rgba(0,240,255,0.35);
    border-radius:2px;
    backdrop-filter:blur(10px) saturate(140%);
    cursor:pointer;
    transition:transform .15s ease, box-shadow .25s ease, border-color .25s ease;
    box-shadow:
      0 0 0px rgba(0,240,255,0),
      inset 0 0 20px rgba(0,240,255,0.05);
    will-change:transform;
    overflow:hidden;
  }
  #enterBtn::before{
    content:''; position:absolute; inset:0;
    background:linear-gradient(120deg, transparent 30%, rgba(0,240,255,0.18) 50%, transparent 70%);
    transform:translateX(-120%);
    transition:transform .8s ease;
  }
  #enterBtn:hover::before{ transform:translateX(120%); }
  #enterBtn:hover{
    border-color:rgba(0,240,255,0.85);
    box-shadow:
      0 0 35px rgba(0,240,255,0.45),
      0 0 80px rgba(255,43,214,0.15),
      inset 0 0 24px rgba(0,240,255,0.12);
  }
  #enterBtn:active{ transform:scale(0.96) !important; }
  #enterBtn span{ position:relative; z-index:1; }

  .sub{
    position:absolute; bottom:14%; left:50%; transform:translateX(-50%);
    color:rgba(190,240,245,0.35); font-size:10px; letter-spacing:3px;
  }

  /* ---------- BOOT SEQUENCE ---------- */
  #boot{
    position:fixed; inset:0; z-index:60;
    background:#000;
    color:var(--cyan);
    font-size:12px; letter-spacing:2px; line-height:1.9;
    padding:8vh 8vw;
    opacity:0; pointer-events:none;
    transition:opacity .4s ease;
  }
  #boot.active{ opacity:1; }
  #boot.glitch{ animation:glitchFlicker .5s steps(2, end) 3; }
  #boot .line{ opacity:0; text-shadow:0 0 6px rgba(0,240,255,0.6); }
  #boot .cursor{ display:inline-block; width:7px; height:12px; background:var(--cyan); margin-left:4px; animation:blink 0.9s steps(1) infinite; vertical-align:-1px;}
  @keyframes blink{ 50%{ opacity:0; } }
  @keyframes glitchFlicker{
    0%{ filter:none; transform:translate(0,0); }
    20%{ filter:invert(1); transform:translate(-2px,1px); }
    40%{ filter:none; transform:translate(2px,-1px); }
    60%{ filter:hue-rotate(90deg); transform:translate(-1px,0); }
    80%{ filter:none; transform:translate(1px,1px); }
    100%{ filter:none; transform:translate(0,0); }
  }
  #bootFlash{
    position:fixed; inset:0; z-index:61; background:#eafeff;
    opacity:0; pointer-events:none;
  }

  /* ---------- HUD ---------- */
  #hud{
    position:fixed; inset:0; z-index:20; pointer-events:none;
    opacity:0; transition:opacity 1.4s ease;
    font-family:'Space Mono', monospace;
  }
  #hud.visible{ opacity:1; }
  #hud .corner{
    position:absolute; color:rgba(180,245,250,0.75); font-size:10px; letter-spacing:3px;
  }
  #hud .tl{ top:26px; left:28px; }
  #hud .tl b{ display:block; font-family:'Orbitron', sans-serif; font-size:15px; letter-spacing:5px; color:#eafeff; text-shadow:0 0 12px rgba(0,240,255,0.7); margin-bottom:4px; }
  #hud .tr{ top:26px; right:28px; text-align:right; }
  #hud .bl{ bottom:26px; left:28px; }
  #hud .br{ bottom:26px; right:28px; text-align:right; }
  #hud .dim{ opacity:0.45; }
  #hud .speedval{ font-family:'Orbitron', sans-serif; font-size:34px; color:var(--cyan); text-shadow:0 0 16px rgba(0,240,255,0.6); }
  #hud .bar{ width:120px; height:2px; background:rgba(0,240,255,0.15); margin-top:6px; position:relative; overflow:hidden;}
  #hud .bar i{ position:absolute; left:0; top:0; height:100%; background:var(--cyan); box-shadow:0 0 8px var(--cyan); }
  #vignetteEdge{
    position:fixed; inset:0; z-index:19; pointer-events:none;
    background:radial-gradient(ellipse at 50% 50%, transparent 55%, rgba(0,0,0,0.55) 100%);
    opacity:0; transition:opacity 1.6s ease;
  }
  #vignetteEdge.visible{ opacity:1; }
</style>
</head>
<body>

  <div id="entry">
    <div class="eyebrow">SYSTEM // DORMANT</div>
    <button id="enterBtn"><span>ENTER THE DRIVE</span></button>
    <div class="sub">NEON DRIVE — CONCEPT ARC-9 · IGNITION SEQUENCE</div>
  </div>

  <div id="boot">
    <div class="line" id="l1">&gt; POWER GRID ............... <span class="ok">ONLINE</span></div>
    <div class="line" id="l2">&gt; NEURAL SUSPENSION ......... <span class="ok">CALIBRATED</span></div>
    <div class="line" id="l3">&gt; PHOTON EMITTERS ........... <span class="ok">ARMED</span></div>
    <div class="line" id="l4">&gt; CHASSIS ARC-9 ............. <span class="ok">SYNCED</span></div>
    <div class="line" id="l5">&gt; ROUTE ..................... <span class="ok">UNKNOWN — GENERATING</span></div>
    <div class="line" id="l6">&gt; INITIATING DRIVE<span class="cursor"></span></div>
  </div>
  <div id="bootFlash"></div>

  <div id="hud">
    <div class="corner tl"><b>NEON DRIVE</b><span class="dim">ARC-9 / AUTONOMOUS SHOWCASE</span></div>
    <div class="corner tr">SECTOR 07 — NULL DISTRICT<br><span class="dim">FOG DENSITY NOMINAL</span></div>
    <div class="corner bl">
      <div class="speedval" id="speedNum">000</div>
      <div class="dim">KM/H · SYNTH DRIVE</div>
    </div>
    <div class="corner br">
      OUTPUT <span id="pwrNum">0</span>%
      <div class="bar"><i id="pwrBar" style="width:0%"></i></div>
    </div>
  </div>
  <div id="vignetteEdge"></div>

<script type="importmap">
{
  "imports": {
    "three": "https://cdn.jsdelivr.net/npm/three@0.160.0/build/three.module.js",
    "three/addons/": "https://cdn.jsdelivr.net/npm/three@0.160.0/examples/jsm/"
  }
}
</script>
<script type="module">
import * as THREE from "three";
import { EffectComposer } from "three/addons/postprocessing/EffectComposer.js";
import { RenderPass } from "three/addons/postprocessing/RenderPass.js";
import { UnrealBloomPass } from "three/addons/postprocessing/UnrealBloomPass.js";
import { ShaderPass } from "three/addons/postprocessing/ShaderPass.js";

/* ============================================================
   0. ENTRY / MAGNETIC BUTTON
   ============================================================ */
const entry = document.getElementById("entry");
const enterBtn = document.getElementById("enterBtn");

window.addEventListener("mousemove", (e) => {
  const r = enterBtn.getBoundingClientRect();
  const cx = r.left + r.width / 2, cy = r.top + r.height / 2;
  const dx = e.clientX - cx, dy = e.clientY - cy;
  const dist = Math.hypot(dx, dy);
  const radius = 160;
  if (dist < radius) {
    const pull = (1 - dist / radius) * 14;
    enterBtn.style.transform = `translate(${(dx / dist) * pull || 0}px, ${(dy / dist) * pull || 0}px)`;
  } else {
    enterBtn.style.transform = "translate(0,0)";
  }
});

enterBtn.addEventListener("click", () => {
  enterBtn.disabled = true;
  entry.classList.add("hidden");
  setTimeout(runBootSequence, 500);
});

/* ============================================================
   1. BOOT SEQUENCE (typewriter + glitch flash)
   ============================================================ */
const boot = document.getElementById("boot");
const bootFlash = document.getElementById("bootFlash");
const lines = ["l1","l2","l3","l4","l5","l6"].map(id => document.getElementById(id));

function runBootSequence(){
  boot.classList.add("active");
  let i = 0;
  const revealNext = () => {
    if (i < lines.length){
      lines[i].style.opacity = "1";
      i++;
      setTimeout(revealNext, 260 + Math.random()*180);
    } else {
      setTimeout(triggerGlitchAndReveal, 500);
    }
  };
  setTimeout(revealNext, 250);
}

function triggerGlitchAndReveal(){
  boot.classList.add("glitch");
  setTimeout(() => {
    bootFlash.style.transition = "opacity 0.06s linear";
    bootFlash.style.opacity = "1";
    setTimeout(() => {
      bootFlash.style.opacity = "0";
      boot.style.transition = "opacity .5s ease";
      boot.style.opacity = "0";
      boot.style.pointerEvents = "none";
      startExperience();
    }, 70);
  }, 620);
}

/* ============================================================
   2. THREE.JS SCENE SETUP
   ============================================================ */
const scene = new THREE.Scene();
scene.fog = new THREE.FogExp2(0x030308, 0.028);

const camera = new THREE.PerspectiveCamera(50, innerWidth/innerHeight, 0.1, 300);
camera.position.set(0, 14, 30);

const renderer = new THREE.WebGLRenderer({ antialias:true, powerPreference:"high-performance" });
renderer.setSize(innerWidth, innerHeight);
renderer.setPixelRatio(Math.min(devicePixelRatio, 2));
renderer.toneMapping = THREE.ACESFilmicToneMapping;
renderer.toneMappingExposure = 1.35;
renderer.outputColorSpace = THREE.SRGBColorSpace;
document.body.appendChild(renderer.domElement);

/* ---- Post-processing: bloom + grade pass (vignette / chromatic aberration / grain) ---- */
const composer = new EffectComposer(renderer);
composer.addPass(new RenderPass(scene, camera));

const bloomPass = new UnrealBloomPass(new THREE.Vector2(innerWidth, innerHeight), 1.15, 0.75, 0.15);
composer.addPass(bloomPass);

const gradeShader = {
  uniforms:{ tDiffuse:{ value:null }, time:{ value:0 } },
  vertexShader:`
    varying vec2 vUv;
    void main(){ vUv = uv; gl_Position = projectionMatrix * modelViewMatrix * vec4(position,1.0); }
  `,
  fragmentShader:`
    uniform sampler2D tDiffuse; uniform float time; varying vec2 vUv;
    void main(){
      vec2 uv = vUv;
      vec2 ca = vec2(0.0016, 0.0);
      float r = texture2D(tDiffuse, uv + ca).r;
      float g = texture2D(tDiffuse, uv).g;
      float b = texture2D(tDiffuse, uv - ca).b;
      vec3 col = vec3(r,g,b);
      float d = distance(uv, vec2(0.5));
      float vig = smoothstep(0.95, 0.32, d);
      col *= mix(0.55, 1.0, vig);
      float grain = (fract(sin(dot(uv*time*60.0, vec2(12.9898,78.233))) * 43758.5453) - 0.5) * 0.035;
      col += grain;
      gl_FragColor = vec4(col, 1.0);
    }
  `
};
const gradePass = new ShaderPass(gradeShader);
composer.addPass(gradePass);

/* ============================================================
   3. LIGHTING
   ============================================================ */
scene.add(new THREE.AmbientLight(0x0a1420, 0.6));
const moon = new THREE.DirectionalLight(0x6fd6ff, 0.35);
moon.position.set(-10, 20, -10);
scene.add(moon);

const cyanPulse = new THREE.PointLight(0x00f0ff, 30, 40);
const magentaPulse = new THREE.PointLight(0xff2bd6, 26, 40);
scene.add(cyanPulse, magentaPulse);

/* ============================================================
   4. ENVIRONMENT — synthwave grid highway
   ============================================================ */
const gridMat = new THREE.ShaderMaterial({
  transparent:true,
  blending:THREE.AdditiveBlending,
  depthWrite:false,
  uniforms:{ time:{ value:0 } },
  vertexShader:`varying vec2 vUv; void main(){ vUv = uv; gl_Position = projectionMatrix * modelViewMatrix * vec4(position,1.0);}`,
  fragmentShader:`
    uniform float time; varying vec2 vUv;
    void main(){
      vec2 uv = vUv * 90.0;
      uv.y += time * 9.0;
      vec2 g = abs(fract(uv - 0.5) - 0.5) / fwidth(uv);
      float line = min(g.x, g.y);
      float glow = 1.0 - min(line, 1.0);
      vec3 col = mix(vec3(0.0,0.05,0.08), vec3(0.0,0.95,1.0), glow);
      float d = length(vUv - vec2(0.5, 0.15));
      float fade = smoothstep(0.95, 0.05, d);
      gl_FragColor = vec4(col * fade, glow * fade);
    }
  `
});
const grid = new THREE.Mesh(new THREE.PlaneGeometry(240, 240, 1, 1), gridMat);
grid.rotation.x = -Math.PI/2;
grid.position.y = 0.02;
scene.add(grid);

// glossy base plane beneath grid for subtle reflection feel
const base = new THREE.Mesh(
  new THREE.PlaneGeometry(240, 240),
  new THREE.MeshStandardMaterial({ color:0x000103, metalness:0.9, roughness:0.25 })
);
base.rotation.x = -Math.PI/2;
scene.add(base);

/* ---- Neon buildings (instanced, two rows receding into fog) ---- */
const buildingGeo = new THREE.BoxGeometry(1, 1, 1);
const buildingMat = new THREE.MeshStandardMaterial({
  color:0x02040a, metalness:0.6, roughness:0.4,
  emissive:0x00f0ff, emissiveIntensity:0.5
});
const BUILDING_COUNT = 140;
const buildings = new THREE.InstancedMesh(buildingGeo, buildingMat, BUILDING_COUNT);
const dummy = new THREE.Object3D();
const buildingColors = [0x00f0ff, 0xff2bd6, 0x7d5bff];
const colorArray = new Float32Array(BUILDING_COUNT * 3);
for (let i=0; i<BUILDING_COUNT; i++){
  const side = i % 2 === 0 ? -1 : 1;
  const z = -(Math.floor(i/2)) * 6 - 8 - Math.random()*3;
  const x = side * (14 + Math.random()*10);
  const h = 6 + Math.random()*26;
  const w = 2.2 + Math.random()*2.4;
  dummy.position.set(x, h/2, z);
  dummy.scale.set(w, h, w);
  dummy.rotation.y = (Math.random()-0.5) * 0.05;
  dummy.updateMatrix();
  buildings.setMatrixAt(i, dummy.matrix);
  const c = new THREE.Color(buildingColors[i % buildingColors.length]);
  colorArray[i*3] = c.r; colorArray[i*3+1] = c.g; colorArray[i*3+2] = c.b;
}
buildings.instanceColor = new THREE.InstancedBufferAttribute(colorArray, 3);
buildingMat.emissive = new THREE.Color(0xffffff);
buildingMat.emissiveIntensity = 0.35;
scene.add(buildings);

/* ---- Floating light beams among buildings ---- */
const beamGeo = new THREE.PlaneGeometry(0.15, 30, 1, 1);
const beamMat = new THREE.MeshBasicMaterial({ color:0x00f0ff, transparent:true, opacity:0.22, blending:THREE.AdditiveBlending, side:THREE.DoubleSide });
const beams = [];
for (let i=0; i<18; i++){
  const beam = new THREE.Mesh(beamGeo, beamMat.clone());
  beam.position.set((Math.random()-0.5)*40, 15, -Math.random()*90);
  beam.rotation.y = Math.random()*Math.PI;
  beam.userData.speed = 4 + Math.random()*6;
  scene.add(beam);
  beams.push(beam);
}

/* ---- Atmospheric particle field ---- */
const PARTICLE_COUNT = 2200;
const pGeo = new THREE.BufferGeometry();
const pPos = new Float32Array(PARTICLE_COUNT * 3);
const pCol = new Float32Array(PARTICLE_COUNT * 3);
const palette = [new THREE.Color(0x00f0ff), new THREE.Color(0xff2bd6), new THREE.Color(0x8a6bff)];
for (let i=0; i<PARTICLE_COUNT; i++){
  pPos[i*3]   = (Math.random()-0.5) * 90;
  pPos[i*3+1] = Math.random() * 26;
  pPos[i*3+2] = -Math.random() * 130 + 20;
  const c = palette[i % palette.length];
  pCol[i*3] = c.r; pCol[i*3+1] = c.g; pCol[i*3+2] = c.b;
}
pGeo.setAttribute("position", new THREE.BufferAttribute(pPos, 3));
pGeo.setAttribute("color", new THREE.BufferAttribute(pCol, 3));
const pMat = new THREE.PointsMaterial({
  size:0.12, vertexColors:true, transparent:true, opacity:0.75,
  blending:THREE.AdditiveBlending, depthWrite:false
});
const particles = new THREE.Points(pGeo, pMat);
scene.add(particles);

/* ============================================================
   5. THE HYPERCAR — procedural, upgraded
   ============================================================ */
const car = new THREE.Group();
scene.add(car);

const paintMat = new THREE.MeshStandardMaterial({
  color:0x0a0a0d, emissive:0x00d9ff, emissiveIntensity:0.55,
  metalness:0.95, roughness:0.18
});
const darkTrim = new THREE.MeshStandardMaterial({ color:0x050505, metalness:0.8, roughness:0.5 });
const glowCyan = new THREE.MeshStandardMaterial({ color:0x000000, emissive:0x00ffff, emissiveIntensity:3.2, roughness:1 });
const glowMagenta = new THREE.MeshStandardMaterial({ color:0x000000, emissive:0xff2bd6, emissiveIntensity:3.2, roughness:1 });
const glowAmber = new THREE.MeshStandardMaterial({ color:0x000000, emissive:0xff5500, emissiveIntensity:3.4, roughness:1 });
const glassMat = new THREE.MeshStandardMaterial({
  color:0x0b0e12, emissive:0x00303a, emissiveIntensity:0.8,
  metalness:0.9, roughness:0.05, transparent:true, opacity:0.85
});

// body shell (lower + cabin wedge for hypercar silhouette)
const lowerBody = new THREE.Mesh(new THREE.BoxGeometry(3.4, 0.5, 1.5), paintMat);
lowerBody.position.y = 0.95;
car.add(lowerBody);

const cabinShape = new THREE.Mesh(new THREE.BoxGeometry(1.5, 0.5, 1.2), paintMat);
cabinShape.position.set(-0.1, 1.42, 0);
cabinShape.rotation.z = -0.03;
car.add(cabinShape);

const nose = new THREE.Mesh(new THREE.ConeGeometry(0.75, 1.3, 4), paintMat);
nose.rotation.z = -Math.PI/2;
nose.rotation.y = Math.PI/4;
nose.scale.set(1, 1, 0.62);
nose.position.set(1.95, 0.95, 0);
car.add(nose);

const windshield = new THREE.Mesh(new THREE.BoxGeometry(1.1, 0.4, 1.1), glassMat);
windshield.position.set(-0.1, 1.55, 0);
car.add(windshield);

// mirrors
[1, -1].forEach(side => {
  const mirror = new THREE.Mesh(new THREE.BoxGeometry(0.25, 0.12, 0.1), darkTrim);
  mirror.position.set(0.55, 1.35, side * 0.85);
  car.add(mirror);
});

// spoiler + struts
const spoiler = new THREE.Mesh(new THREE.BoxGeometry(0.6, 0.07, 1.35), glowMagenta);
spoiler.position.set(-1.65, 1.55, 0);
car.add(spoiler);
[0.55, -0.55].forEach(z => {
  const strut = new THREE.Mesh(new THREE.BoxGeometry(0.08, 0.4, 0.08), darkTrim);
  strut.position.set(-1.65, 1.28, z);
  car.add(strut);
});

// headlights & taillights
const headLightGeo = new THREE.BoxGeometry(0.1, 0.12, 0.35);
[0.42, -0.42].forEach(z => {
  const hl = new THREE.Mesh(headLightGeo, glowCyan);
  hl.position.set(2.55, 0.95, z);
  car.add(hl);
});
[0.5, -0.5].forEach(z => {
  const tl = new THREE.Mesh(new THREE.BoxGeometry(0.08, 0.16, 0.3), glowMagenta);
  tl.position.set(-1.72, 0.95, z);
  car.add(tl);
});

// exhaust glow
const exhaustGlow = new THREE.Mesh(new THREE.CylinderGeometry(0.09, 0.09, 0.2, 12), glowAmber);
exhaustGlow.rotation.z = Math.PI/2;
exhaustGlow.position.set(-1.78, 0.75, 0);
car.add(exhaustGlow);

// wheels: tyre + glowing rim + brake disc
const wheelPositions = [
  [-1.05, 0.6, 0.82], [1.05, 0.6, 0.82],
  [-1.05, 0.6, -0.82], [1.05, 0.6, -0.82]
];
const tyreGeo = new THREE.CylinderGeometry(0.38, 0.38, 0.26, 24);
const rimGeo = new THREE.TorusGeometry(0.2, 0.045, 10, 20);
const discGeo = new THREE.CylinderGeometry(0.24, 0.24, 0.04, 20);
const discMat = new THREE.MeshStandardMaterial({ color:0x999999, metalness:0.9, roughness:0.3 });
const wheels = [];
wheelPositions.forEach(([x,y,z]) => {
  const tyre = new THREE.Mesh(tyreGeo, darkTrim);
  tyre.rotation.z = Math.PI/2;
  tyre.position.set(x,y,z);
  car.add(tyre);

  const disc = new THREE.Mesh(discGeo, discMat);
  disc.rotation.z = Math.PI/2;
  disc.position.set(x,y,z);
  car.add(disc);

  const rim = new THREE.Mesh(rimGeo, glowCyan.clone());
  rim.rotation.y = Math.PI/2;
  rim.position.set(x,y,z);
  car.add(rim);

  wheels.push({ tyre, rim });
});

// underglow
const underGlow = new THREE.Mesh(
  new THREE.BoxGeometry(3.0, 0.03, 1.3),
  new THREE.MeshBasicMaterial({ color:0x00ffff, transparent:true, opacity:0.25, blending:THREE.AdditiveBlending })
);
underGlow.position.set(0, 0.65, 0);
car.add(underGlow);

// dynamic headlight point-lights
const headL = new THREE.PointLight(0x00ffff, 6, 10);
headL.position.set(2.6, 0.95, 0.42);
car.add(headL);
const headR = new THREE.PointLight(0x00ffff, 6, 10);
headR.position.set(2.6, 0.95, -0.42);
car.add(headR);
const tailGlowLight = new THREE.PointLight(0xff2bd6, 4, 6);
tailGlowLight.position.set(-1.7, 0.9, 0);
car.add(tailGlowLight);

// speed trail streaks
const trailGeo = new THREE.BufferGeometry();
const trailPts = [];
for (let i=0; i<120; i++) trailPts.push(new THREE.Vector3(-i * 0.22, 0.5, (i%2===0?0.5:-0.5)));
trailGeo.setFromPoints(trailPts);
const trail = new THREE.Line(trailGeo, new THREE.LineBasicMaterial({ color:0x00f7ff, transparent:true, opacity:0.28 }));
scene.add(trail);

/* ============================================================
   6. CINEMATIC CAMERA DIRECTOR
   ============================================================ */
const clock = new THREE.Clock();
let mode = "intro"; // intro -> cinematic
let introT = 0;

// keyframes: {pos, look, dur}
const introKeyframes = [
  { pos:new THREE.Vector3(0, 3, 46),  look:new THREE.Vector3(0, 1, 0), dur:2.4 },
  { pos:new THREE.Vector3(6, 1.4, 9), look:new THREE.Vector3(0, 1, 0), dur:2.2 },
  { pos:new THREE.Vector3(-4, 2.2, 4),look:new THREE.Vector3(1, 1, 0), dur:2.0 },
  { pos:new THREE.Vector3(2.6, 5.5, 7.5), look:new THREE.Vector3(0, 1, 0), dur:2.0 },
];
let kfIndex = 0;
let kfT = 0;
const tmpCamPos = new THREE.Vector3();
const tmpLook = new THREE.Vector3();
let prevPos = new THREE.Vector3(0, 8, 60);
let prevLook = new THREE.Vector3(0, 1, 0);

function easeInOut(t){ return t<0.5 ? 2*t*t : 1-Math.pow(-2*t+2,2)/2; }

function updateIntroCamera(dt){
  const kf = introKeyframes[kfIndex];
  kfT += dt;
  const t = Math.min(kfT / kf.dur, 1);
  const e = easeInOut(t);
  tmpCamPos.lerpVectors(prevPos, kf.pos, e);
  tmpLook.lerpVectors(prevLook, kf.look, e);
  camera.position.copy(tmpCamPos);
  camera.lookAt(tmpLook);
  if (t >= 1){
    prevPos = kf.pos.clone();
    prevLook = kf.look.clone();
    kfIndex++;
    kfT = 0;
    if (kfIndex >= introKeyframes.length){
      mode = "cinematic";
      hud.classList.add("visible");
      vignetteEdge.classList.add("visible");
    }
  }
}

// cinematic (post-intro) roaming camera: orbit + periodic hero close-ups
let cineT = 0;
const orbitRadius = 8.5;
function updateCinematicCamera(dt, driveT){
  cineT += dt;
  const shake = Math.sin(driveT*14) * 0.02;
  const angle = cineT * 0.18;
  const heroPulse = (Math.sin(cineT * 0.25) + 1) / 2; // 0..1 slow breathing between wide + close
  const radius = orbitRadius - heroPulse * 4.2;
  const height = 2.6 + heroPulse * 3.2;
  camera.position.set(
    car.position.x + Math.sin(angle) * radius,
    height + shake,
    car.position.z + Math.cos(angle) * radius
  );
  camera.lookAt(car.position.x, 1.1, car.position.z);
}

/* ============================================================
   7. HUD refs + animate loop
   ============================================================ */
const hud = document.getElementById("hud");
const vignetteEdge = document.getElementById("vignetteEdge");
const speedNum = document.getElementById("speedNum");
const pwrNum = document.getElementById("pwrNum");
const pwrBar = document.getElementById("pwrBar");

let driveT = 0;
let started = false;

function startExperience(){
  started = true;
  clock.start();
}

function animate(){
  requestAnimationFrame(animate);
  const dt = Math.min(clock.getDelta(), 0.05);
  if (!started){ renderer.render(scene, camera); return; }

  driveT += dt * 0.9;

  // car path
  car.position.x = Math.sin(driveT * 0.6) * 2.6;
  car.position.z = 0;
  car.position.y = 0.05 + Math.sin(driveT * 2.4) * 0.025;
  car.rotation.y = -Math.sin(driveT * 0.6) * 0.22;
  wheels.forEach(w => { w.tyre.rotation.x -= 0.3; w.rim.rotation.x -= 0.3; });

  // environment motion
  gridMat.uniforms.time.value = driveT;
  gradePass.uniforms.time.value += dt;
  particles.rotation.y += dt * 0.01;
  const pos = pGeo.attributes.position;
  for (let i=0; i<PARTICLE_COUNT; i++){
    let z = pos.getZ(i) + dt * 6;
    if (z > 30) z = -130;
    pos.setZ(i, z);
  }
  pos.needsUpdate = true;

  beams.forEach(b => {
    b.position.z += dt * b.userData.speed;
    if (b.position.z > 20) b.position.z = -110;
  });

  buildingMat.emissiveIntensity = 0.3 + Math.sin(driveT * 2) * 0.08;

  cyanPulse.position.set(6 + Math.sin(driveT)*3, 6 + Math.cos(driveT*0.7)*2, car.position.z + 6);
  magentaPulse.position.set(-6 + Math.cos(driveT*0.8)*3, 4 + Math.sin(driveT*1.1)*2, car.position.z + 4);

  // camera direction
  if (mode === "intro"){
    updateIntroCamera(dt);
  } else {
    updateCinematicCamera(dt, driveT);
    // HUD telemetry
    const speed = 180 + Math.sin(driveT*0.5) * 60;
    speedNum.textContent = Math.round(Math.abs(speed)).toString().padStart(3,"0");
    const pwr = 60 + Math.sin(driveT*0.4)*35;
    pwrNum.textContent = Math.round(Math.abs(pwr));
    pwrBar.style.width = Math.abs(pwr) + "%";
  }

  composer.render();
}
animate();

addEventListener("resize", () => {
  camera.aspect = innerWidth/innerHeight;
  camera.updateProjectionMatrix();
  renderer.setSize(innerWidth, innerHeight);
  composer.setSize(innerWidth, innerHeight);
});
</script>
</body>
</html>
