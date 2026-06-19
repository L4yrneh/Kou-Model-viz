<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kou 双指数跳跃扩散模型 · 可视化</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.16.9/katex.min.css">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,440;9..144,600;9..144,680&family=Inter:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#0B0F14;
    --panel:#121922;
    --panel-2:#1A232E;
    --text:#E7ECF2;
    --text-dim:#8C99AA;
    --rule:#26313D;
    --up:#F2A33D;
    --down:#7C8BFF;
    --diffusion:#C9D2DC;
    --spark:#49D3E8;
    --bs:#7C8898;
    --maxw:1080px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--ink);
    color:var(--text);
    font-family:'Inter',system-ui,sans-serif;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  .bg-grid{
    position:fixed; inset:0; z-index:-1;
    background-image:
      linear-gradient(rgba(255,255,255,0.025) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255,255,255,0.025) 1px, transparent 1px);
    background-size: 44px 44px;
    mask-image: radial-gradient(ellipse 80% 60% at 50% 0%, black 30%, transparent 75%);
  }
  h1,h2,h3{ font-family:'Fraunces', serif; font-weight:600; letter-spacing:-0.01em; margin:0; }
  .mono{ font-family:'IBM Plex Mono', monospace; }
  a{ color:var(--spark); }

  .eyebrow{
    font-family:'IBM Plex Mono', monospace;
    font-size:0.78rem;
    letter-spacing:0.08em;
    color:var(--text-dim);
    text-transform:none;
    margin:0 0 0.6rem 0;
  }

  /* ---------- HERO ---------- */
  .hero{
    min-height: 92vh;
    display:flex;
    align-items:center;
    padding: 6vh 1.5rem 4vh;
    border-bottom:1px solid var(--rule);
  }
  .hero-inner{ max-width: var(--maxw); margin:0 auto; width:100%; }
  .hero h1{ font-size: clamp(2.1rem, 5.2vw, 3.4rem); line-height:1.18; margin-bottom:1.1rem; }
  .hero h1 .accent{ color:var(--spark); display:block; font-size: 0.62em; margin-top:0.35em; font-weight:600;}
  .hero .lede{ max-width:560px; color:var(--text-dim); font-size:1.05rem; margin-bottom:2.2rem;}
  .hero-canvas{
    width:100%; height:160px; display:block;
    background:var(--panel);
    border:1px solid var(--rule);
    border-radius:6px;
    margin-bottom:2rem;
  }
  .hero-cta{
    display:inline-flex; align-items:center; gap:0.4rem;
    font-family:'IBM Plex Mono', monospace; font-size:0.85rem;
    color:var(--text); text-decoration:none;
    border:1px solid var(--rule); padding:0.6rem 1rem; border-radius:5px;
    transition: border-color .2s, color .2s;
  }
  .hero-cta:hover{ border-color:var(--spark); color:var(--spark); }

  /* ---------- SECTIONS ---------- */
  main{ max-width: var(--maxw); margin:0 auto; padding:0 1.5rem; }
  .section{ padding: 5.5rem 0; border-bottom:1px solid var(--rule); }
  .section:last-child{ border-bottom:none; }
  .section h2{ font-size: clamp(1.5rem, 3vw, 2rem); margin-bottom:0.9rem; }
  .section > p.intro{ color:var(--text-dim); max-width:640px; margin-bottom:2.2rem; }

  .formula-card{
    background:var(--panel);
    border:1px solid var(--rule);
    border-radius:8px;
    padding:1.6rem 1.8rem;
    margin-bottom:1.2rem;
    overflow-x:auto;
  }
  .formula-card .formula-caption{
    font-family:'IBM Plex Mono', monospace;
    font-size:0.78rem; color:var(--text-dim);
    margin-top:0.5rem;
  }
  .formula-row{ margin-bottom:1.4rem; }
  .formula-row:last-child{ margin-bottom:0; }

  .panel-grid{
    display:grid;
    grid-template-columns: 280px 1fr;
    gap:1.6rem;
    align-items:start;
  }
  @media (max-width: 760px){
    .panel-grid{ grid-template-columns: 1fr; }
  }

  .controls{
    background:var(--panel);
    border:1px solid var(--rule);
    border-radius:8px;
    padding:1.4rem;
    position:sticky;
    top:1rem;
  }
  @media (max-width: 760px){ .controls{ position:static; } }

  .control{ margin-bottom:1.3rem; }
  .control:last-child{ margin-bottom:0; }
  .control-label{
    display:flex; justify-content:space-between; align-items:baseline;
    font-size:0.84rem; color:var(--text-dim); margin-bottom:0.45rem;
  }
  .control-value{ font-family:'IBM Plex Mono', monospace; color:var(--text); }
  input[type=range]{
    width:100%; -webkit-appearance:none; appearance:none;
    height:3px; background:var(--rule); border-radius:2px; outline:none;
  }
  input[type=range]::-webkit-slider-thumb{
    -webkit-appearance:none; appearance:none;
    width:14px; height:14px; border-radius:50%;
    background:var(--spark); cursor:pointer;
    border:2px solid var(--ink);
  }
  input[type=range]::-moz-range-thumb{
    width:14px; height:14px; border-radius:50%;
    background:var(--spark); cursor:pointer; border:2px solid var(--ink);
  }

  .btn{
    width:100%; padding:0.7rem 1rem; margin-top:0.4rem;
    background:var(--spark); color:#06151A; border:none; border-radius:5px;
    font-family:'IBM Plex Mono', monospace; font-size:0.82rem; font-weight:500;
    cursor:pointer; transition:opacity .2s;
  }
  .btn:hover{ opacity:0.85; }
  .status{ font-size:0.76rem; color:var(--text-dim); margin-top:0.6rem; min-height:1em; font-family:'IBM Plex Mono', monospace;}

  .chart-stack{ display:flex; flex-direction:column; gap:1.2rem; }
  .chart-card{
    background:var(--panel);
    border:1px solid var(--rule);
    border-radius:8px;
    padding:1.1rem 1.2rem 0.8rem;
  }
  .chart-card h4{
    font-family:'Inter', sans-serif; font-weight:600; font-size:0.86rem;
    color:var(--text); margin:0 0 0.7rem 0;
  }
  .chart-card .canvas-wrap{ height:280px; position:relative; }
  .chart-card canvas{ width:100% !important; height:100% !important; }

  .legend-row{
    display:flex; gap:1.2rem; flex-wrap:wrap;
    font-size:0.78rem; color:var(--text-dim);
    margin-top:0.5rem; font-family:'IBM Plex Mono', monospace;
  }
  .legend-row span{ display:inline-flex; align-items:center; gap:0.4rem; }
  .dot{ width:9px; height:9px; border-radius:50%; display:inline-block; }

  footer{
    max-width:var(--maxw); margin:0 auto; padding:3rem 1.5rem 5rem;
    color:var(--text-dim); font-size:0.85rem;
  }
  footer a{ color:var(--text-dim); text-decoration:underline; }
  footer .rule{ border-top:1px solid var(--rule); margin-bottom:2rem; }

  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
  }
</style>
</head>
<body>

<div class="bg-grid"></div>

<header class="hero">
  <div class="hero-inner">
    <p class="eyebrow">毕业设计 · 数理金融可视化</p>
    <h1>当价格不再连续行走<span class="accent">Kou 双指数跳跃扩散模型</span></h1>
    <p class="lede">布朗运动负责"漫步"，泊松过程负责"惊吓"。这个页面把 Kou (2002) 模型拆开看：跳跃从哪来、长什么样、如何重塑资产路径，以及它为什么能解释期权市场里的波动率微笑。</p>
    <canvas id="heroCanvas" class="hero-canvas"></canvas>
    <a href="#model" class="hero-cta">开始探索 ↓</a>
  </div>
</header>

<main>

  <section id="model" class="section">
    <p class="eyebrow">§1 模型</p>
    <h2>扩散 + 跳跃</h2>
    <p class="intro">在 Kou 模型中，资产的对数价格由两部分驱动：一个连续的布朗扩散，叠加一个由泊松过程计数、跳跃幅度服从非对称双指数分布的复合跳跃过程。</p>

    <div class="formula-card">
      <div class="formula-row" id="f-sde"></div>
      <div class="formula-row" id="f-jump-count"></div>
      <p class="formula-caption">μ 为漂移，σ 为扩散波动率，N_t 为强度 λ 的泊松过程，Y_i 为第 i 次跳跃的对数跳幅。</p>
    </div>

    <div class="formula-card">
      <div class="formula-row" id="f-density"></div>
      <p class="formula-caption">p 为向上跳跃概率；η₁、η₂ 分别控制向上 / 向下跳跃的衰减速度（越大，跳幅越集中在小幅区间）。η₁ &gt; 1 保证矩存在。</p>
    </div>
  </section>

  <section id="jump" class="section">
    <p class="eyebrow">§2 跳跃剖析</p>
    <h2>非对称双指数密度</h2>
    <p class="intro">拖动滑块，观察 p、η₁、η₂ 如何决定跳跃方向的概率与幅度——这正是 Kou 模型相比对称跳跃模型（如 Merton）多出的"不对称"自由度。</p>

    <div class="panel-grid">
      <div class="controls">
        <div class="control">
          <div class="control-label"><span>p（向上跳跃概率）</span><span class="control-value mono" id="jd-p-val"></span></div>
          <input type="range" id="jd-p" min="0" max="1" step="0.01" value="0.35">
        </div>
        <div class="control">
          <div class="control-label"><span>η₁（上跳衰减速度）</span><span class="control-value mono" id="jd-eta1-val"></span></div>
          <input type="range" id="jd-eta1" min="2" max="50" step="0.5" value="25">
        </div>
        <div class="control">
          <div class="control-label"><span>η₂（下跳衰减速度）</span><span class="control-value mono" id="jd-eta2-val"></span></div>
          <input type="range" id="jd-eta2" min="2" max="50" step="0.5" value="15">
        </div>
      </div>
      <div class="chart-card">
        <h4>跳跃幅度密度 f_Y(y)</h4>
        <div class="canvas-wrap"><canvas id="jumpChart"></canvas></div>
        <div class="legend-row">
          <span><span class="dot" style="background:var(--up)"></span>向上跳跃 y ≥ 0</span>
          <span><span class="dot" style="background:var(--down)"></span>向下跳跃 y &lt; 0</span>
        </div>
      </div>
    </div>
  </section>

  <section id="paths" class="section">
    <p class="eyebrow">§3 模拟路径</p>
    <h2>资产价格的样本轨道</h2>
    <p class="intro">每条灰色细线是一次蒙特卡洛模拟出的价格路径，彩色圆点标记跳跃发生的时刻与方向。右下方对比了模拟得到的终值对数收益分布与"纯扩散假设下"的理论正态密度——差距就是跳跃的贡献。</p>

    <div class="panel-grid">
      <div class="controls">
        <div class="control">
          <div class="control-label"><span>μ（年化漂移）</span><span class="control-value mono" id="path-mu-val"></span></div>
          <input type="range" id="path-mu" min="-0.1" max="0.3" step="0.01" value="0.06">
        </div>
        <div class="control">
          <div class="control-label"><span>σ（扩散波动率）</span><span class="control-value mono" id="path-sigma-val"></span></div>
          <input type="range" id="path-sigma" min="0.05" max="0.6" step="0.01" value="0.2">
        </div>
        <div class="control">
          <div class="control-label"><span>λ（年化跳跃强度）</span><span class="control-value mono" id="path-lambda-val"></span></div>
          <input type="range" id="path-lambda" min="0" max="8" step="0.1" value="1.5">
        </div>
        <div class="control">
          <div class="control-label"><span>p（向上跳跃概率）</span><span class="control-value mono" id="path-p-val"></span></div>
          <input type="range" id="path-p" min="0" max="1" step="0.01" value="0.35">
        </div>
        <div class="control">
          <div class="control-label"><span>η₁ / η₂</span><span class="control-value mono" id="path-eta-val"></span></div>
          <input type="range" id="path-eta1" min="2" max="50" step="0.5" value="25">
          <input type="range" id="path-eta2" min="2" max="50" step="0.5" value="15" style="margin-top:0.5rem;">
        </div>
        <div class="control">
          <div class="control-label"><span>T（年）</span><span class="control-value mono" id="path-T-val"></span></div>
          <input type="range" id="path-T" min="0.5" max="5" step="0.1" value="2">
        </div>
      </div>
      <div class="chart-stack">
        <div class="chart-card">
          <h4>样本价格路径（S₀ = 100）</h4>
          <div class="canvas-wrap"><canvas id="pathChart"></canvas></div>
        </div>
        <div class="chart-card">
          <h4>终值对数收益分布：模拟 vs 纯扩散理论</h4>
          <div class="canvas-wrap"><canvas id="histChart"></canvas></div>
          <div class="legend-row">
            <span><span class="dot" style="background:var(--spark)"></span>Kou 模拟（含跳跃）</span>
            <span><span class="dot" style="background:var(--bs)"></span>纯扩散理论密度（无跳跃）</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="pricing" class="section">
    <p class="eyebrow">§4 期权定价与波动率微笑</p>
    <h2>跳跃如何制造"微笑"</h2>
    <p class="intro">在风险中性测度下，漂移被修正为 μ_ℚ = r − λζ − σ²/2（ζ = E[e^Y − 1]），保证折现价格过程是鞅。用蒙特卡洛对欧式看涨期权定价，并与同一 σ 下的 Black–Scholes 价格对比，再反推隐含波动率——厚尾与偏度会立刻显形为一条微笑曲线。</p>

    <div class="formula-card">
      <div class="formula-row" id="f-rn"></div>
      <div class="formula-row" id="f-price"></div>
    </div>

    <div class="panel-grid">
      <div class="controls">
        <div class="control">
          <div class="control-label"><span>r（无风险利率）</span><span class="control-value mono" id="price-r-val"></span></div>
          <input type="range" id="price-r" min="0" max="0.1" step="0.005" value="0.03">
        </div>
        <div class="control">
          <div class="control-label"><span>σ（扩散波动率）</span><span class="control-value mono" id="price-sigma-val"></span></div>
          <input type="range" id="price-sigma" min="0.05" max="0.5" step="0.01" value="0.2">
        </div>
        <div class="control">
          <div class="control-label"><span>T（到期年限）</span><span class="control-value mono" id="price-T-val"></span></div>
          <input type="range" id="price-T" min="0.1" max="3" step="0.1" value="1">
        </div>
        <div class="control">
          <div class="control-label"><span>λ（跳跃强度）</span><span class="control-value mono" id="price-lambda-val"></span></div>
          <input type="range" id="price-lambda" min="0" max="5" step="0.1" value="1.5">
        </div>
        <div class="control">
          <div class="control-label"><span>p（向上跳跃概率）</span><span class="control-value mono" id="price-p-val"></span></div>
          <input type="range" id="price-p" min="0" max="1" step="0.01" value="0.35">
        </div>
        <div class="control">
          <div class="control-label"><span>η₁ / η₂</span><span class="control-value mono" id="price-eta-val"></span></div>
          <input type="range" id="price-eta1" min="2" max="50" step="0.5" value="25">
          <input type="range" id="price-eta2" min="2" max="50" step="0.5" value="15" style="margin-top:0.5rem;">
        </div>
        <button class="btn" id="price-recompute">重新计算（20,000 次模拟 / 行权价）</button>
        <div class="status" id="price-status"></div>
      </div>
      <div class="chart-stack">
        <div class="chart-card">
          <h4>欧式看涨期权价格 vs 行权价</h4>
          <div class="canvas-wrap"><canvas id="priceChart"></canvas></div>
          <div class="legend-row">
            <span><span class="dot" style="background:var(--spark)"></span>Kou（蒙特卡洛）</span>
            <span><span class="dot" style="background:var(--bs)"></span>Black–Scholes（解析解）</span>
          </div>
        </div>
        <div class="chart-card">
          <h4>隐含波动率微笑</h4>
          <div class="canvas-wrap"><canvas id="smileChart"></canvas></div>
          <div class="legend-row">
            <span><span class="dot" style="background:var(--spark)"></span>由 Kou 价格反推的隐含波动率</span>
            <span><span class="dot" style="background:var(--bs)"></span>输入的 σ（常数基准线）</span>
          </div>
        </div>
      </div>
    </div>
  </section>

</main>

<footer>
  <div class="rule"></div>
  <p>所有模拟均在浏览器本地用 JavaScript 完成，不依赖后端，可直接部署在 GitHub Pages 上。模型与公式参考 Kou, S. G. (2002), <em>A Jump-Diffusion Model for Option Pricing</em>, Management Science。</p>
</footer>

<script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.16.9/katex.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.min.js"></script>
<script>
/* ========================= 随机数与模型核心函数 ========================= */

function randNormal(){
  let u=0,v=0;
  while(u===0) u=Math.random();
  while(v===0) v=Math.random();
  return Math.sqrt(-2*Math.log(u))*Math.cos(2*Math.PI*v);
}
function randExp(rate){ return -Math.log(Math.random())/rate; }
function randPoisson(mean){
  if(mean<=0) return 0;
  if(mean<30){
    const L=Math.exp(-mean);
    let k=0,p=1;
    do{ k++; p*=Math.random(); } while(p>L);
    return k-1;
  }
  return Math.max(0, Math.round(mean+Math.sqrt(mean)*randNormal()));
}
function randKouJump(p,eta1,eta2){
  return Math.random()<p ? randExp(eta1) : -randExp(eta2);
}
function kouDensity(y,p,eta1,eta2){
  return y>=0 ? p*eta1*Math.exp(-eta1*y) : (1-p)*eta2*Math.exp(eta2*y);
}
function kouZeta(p,eta1,eta2){
  return p*eta1/(eta1-1) + (1-p)*eta2/(eta2+1) - 1;
}
function erf(x){
  const sign = x<0?-1:1; x=Math.abs(x);
  const a1=0.254829592,a2=-0.284496736,a3=1.421413741,a4=-1.453152027,a5=1.061405429,pp=0.3275911;
  const t=1/(1+pp*x);
  const y=1-(((((a5*t+a4)*t)+a3)*t+a2)*t+a1)*t*Math.exp(-x*x);
  return sign*y;
}
function normCdf(x){ return 0.5*(1+erf(x/Math.sqrt(2))); }
function normPdf(x){ return Math.exp(-x*x/2)/Math.sqrt(2*Math.PI); }
function bsCall(S,K,r,sigma,T){
  if(T<=0||sigma<=0) return Math.max(S-K,0);
  const d1=(Math.log(S/K)+(r+0.5*sigma*sigma)*T)/(sigma*Math.sqrt(T));
  const d2=d1-sigma*Math.sqrt(T);
  return S*normCdf(d1)-K*Math.exp(-r*T)*normCdf(d2);
}
function impliedVol(price,S,K,r,T){
  let lo=0.001, hi=3.0;
  for(let i=0;i<60;i++){
    const mid=(lo+hi)/2;
    if(bsCall(S,K,r,mid,T)>price) hi=mid; else lo=mid;
  }
  return (lo+hi)/2;
}

/* ========================= 工具：滑块绑定 ========================= */
function bindSlider(id, fmt, onInput, onChange){
  const el=document.getElementById(id);
  const valEl=document.getElementById(id+'-val');
  const update=()=>{ if(valEl) valEl.textContent=fmt(parseFloat(el.value)); };
  update();
  el.addEventListener('input', ()=>{ update(); onInput && onInput(); });
  el.addEventListener('change', ()=>{ onChange && onChange(); });
  return el;
}
const f2=v=>v.toFixed(2);
const f3=v=>v.toFixed(3);
const fPct=v=>(v*100).toFixed(1)+'%';

/* ========================= KaTeX 公式渲染 ========================= */
katex.render(String.raw`d\ln S_t=\Big(\mu-\frac{\sigma^2}{2}\Big)dt+\sigma\,dW_t+dJ_t,\qquad J_t=\sum_{i=1}^{N_t}Y_i`, document.getElementById('f-sde'), {displayMode:true});
katex.render(String.raw`N_t\sim\text{Poisson}(\lambda t)`, document.getElementById('f-jump-count'), {displayMode:true});
katex.render(String.raw`f_Y(y)=p\,\eta_1e^{-\eta_1y}\mathbf{1}_{\{y\ge0\}}+(1-p)\,\eta_2e^{\eta_2y}\mathbf{1}_{\{y<0\}}`, document.getElementById('f-density'), {displayMode:true});
katex.render(String.raw`\zeta=\mathbb{E}[e^{Y}-1]=\frac{p\,\eta_1}{\eta_1-1}+\frac{(1-p)\,\eta_2}{\eta_2+1}-1,\qquad \mu_{\mathbb{Q}}=r-\lambda\zeta-\frac{\sigma^2}{2}`, document.getElementById('f-rn'), {displayMode:true});
katex.render(String.raw`C(K,T)=e^{-rT}\,\mathbb{E}^{\mathbb{Q}}\big[(S_T-K)^+\big]`, document.getElementById('f-price'), {displayMode:true});

/* ========================= Chart.js 全局风格 ========================= */
Chart.defaults.color = '#8C99AA';
Chart.defaults.font.family = "'Inter', sans-serif";
Chart.defaults.font.size = 12;
const gridStyle = { color:'rgba(255,255,255,0.06)' };

/* ========================= §2 跳跃密度图 ========================= */
const jumpChart = new Chart(document.getElementById('jumpChart'), {
  type:'line',
  data:{ datasets:[
    {label:'向上', data:[], borderColor:'#F2A33D', backgroundColor:'rgba(242,163,61,0.18)', fill:true, pointRadius:0, borderWidth:2, tension:0},
    {label:'向下', data:[], borderColor:'#7C8BFF', backgroundColor:'rgba(124,139,255,0.18)', fill:true, pointRadius:0, borderWidth:2, tension:0}
  ]},
  options:{
    responsive:true, maintainAspectRatio:false, animation:{duration:200},
    plugins:{ legend:{display:false} },
    scales:{
      x:{ type:'linear', title:{display:true,text:'对数跳幅 y'}, grid:gridStyle },
      y:{ title:{display:true,text:'密度 f_Y(y)'}, grid:gridStyle, beginAtZero:true }
    }
  }
});
function updateJumpChart(){
  const p=parseFloat(document.getElementById('jd-p').value);
  const eta1=parseFloat(document.getElementById('jd-eta1').value);
  const eta2=parseFloat(document.getElementById('jd-eta2').value);
  const up=[], down=[];
  for(let y=0; y<=0.6; y+=0.005) up.push({x:y, y:kouDensity(y,p,eta1,eta2)});
  for(let y=-0.6; y<=0; y+=0.005) down.push({x:y, y:kouDensity(y,p,eta1,eta2)});
  jumpChart.data.datasets[0].data = up;
  jumpChart.data.datasets[1].data = down;
  jumpChart.update();
}
bindSlider('jd-p', v=>v.toFixed(2), updateJumpChart);
bindSlider('jd-eta1', v=>v.toFixed(1), updateJumpChart);
bindSlider('jd-eta2', v=>v.toFixed(1), updateJumpChart);
updateJumpChart();

/* ========================= §3 路径模拟 ========================= */
const pathChart = new Chart(document.getElementById('pathChart'), {
  type:'line',
  data:{ datasets:[] },
  options:{
    responsive:true, maintainAspectRatio:false, animation:{duration:0},
    plugins:{ legend:{display:false}, tooltip:{enabled:false} },
    elements:{ point:{ } },
    scales:{
      x:{ type:'linear', title:{display:true,text:'时间（年）'}, grid:gridStyle },
      y:{ title:{display:true,text:'价格 S_t'}, grid:gridStyle }
    }
  }
});
const histChart = new Chart(document.getElementById('histChart'), {
  type:'bar',
  data:{ datasets:[
    { type:'bar', label:'Kou 模拟', data:[], backgroundColor:'rgba(73,211,232,0.55)', borderWidth:0, order:2 },
    { type:'line', label:'纯扩散理论密度', data:[], borderColor:'#7C8898', borderDash:[5,4], pointRadius:0, borderWidth:1.6, fill:false, order:1 }
  ]},
  options:{
    responsive:true, maintainAspectRatio:false, animation:{duration:0},
    plugins:{ legend:{display:false} },
    scales:{
      x:{ type:'linear', title:{display:true,text:'终值对数收益'}, grid:gridStyle },
      y:{ title:{display:true,text:'概率密度'}, grid:gridStyle, beginAtZero:true }
    }
  }
});

function simulatePath(mu,sigma,lambda,p,eta1,eta2,T,nSteps){
  const dt=T/nSteps;
  let logS=Math.log(100);
  const driftPerStep=(mu-0.5*sigma*sigma)*dt;
  const pts=[{x:0,y:100}]; const jumpsUp=[]; const jumpsDown=[];
  for(let i=1;i<=nSteps;i++){
    const t=i*dt;
    const diffusion=sigma*Math.sqrt(dt)*randNormal();
    const nJ=randPoisson(lambda*dt);
    let jumpSum=0;
    for(let j=0;j<nJ;j++){
      const y=randKouJump(p,eta1,eta2);
      jumpSum+=y;
    }
    logS+=driftPerStep+diffusion+jumpSum;
    const price=Math.exp(logS);
    pts.push({x:t,y:price});
    if(nJ>0){
      const lastJumpUp = jumpSum>=0;
      (lastJumpUp?jumpsUp:jumpsDown).push({x:t,y:price});
    }
  }
  return {pts, jumpsUp, jumpsDown};
}

function updatePathSection(){
  const mu=parseFloat(document.getElementById('path-mu').value);
  const sigma=parseFloat(document.getElementById('path-sigma').value);
  const lambda=parseFloat(document.getElementById('path-lambda').value);
  const p=parseFloat(document.getElementById('path-p').value);
  const eta1=parseFloat(document.getElementById('path-eta1').value);
  const eta2=parseFloat(document.getElementById('path-eta2').value);
  const T=parseFloat(document.getElementById('path-T').value);
  document.getElementById('path-eta-val').textContent = eta1.toFixed(1)+' / '+eta2.toFixed(1);

  const nSteps=Math.round(252*T);
  const nPaths=6;
  const datasets=[];
  const allUp=[], allDown=[];
  for(let i=0;i<nPaths;i++){
    const {pts,jumpsUp,jumpsDown}=simulatePath(mu,sigma,lambda,p,eta1,eta2,T,nSteps);
    datasets.push({
      data:pts, borderColor:'rgba(201,210,220,'+(0.85-i*0.08)+')',
      borderWidth:1.3, pointRadius:0, tension:0, fill:false
    });
    allUp.push(...jumpsUp); allDown.push(...jumpsDown);
  }
  datasets.push({ data:allUp, type:'scatter', showLine:false, pointBackgroundColor:'#F2A33D', pointBorderWidth:0, pointRadius:4, borderColor:'#F2A33D' });
  datasets.push({ data:allDown, type:'scatter', showLine:false, pointBackgroundColor:'#7C8BFF', pointBorderWidth:0, pointRadius:4, borderColor:'#7C8BFF' });
  pathChart.data.datasets = datasets;
  pathChart.update();

  // 终值分布
  const nSims=4000;
  const zeta=kouZeta(p,eta1,eta2);
  const logReturns=[];
  for(let i=0;i<nSims;i++){
    const diffusion=sigma*Math.sqrt(T)*randNormal();
    const nJ=randPoisson(lambda*T);
    let jumpSum=0;
    for(let j=0;j<nJ;j++) jumpSum+=randKouJump(p,eta1,eta2);
    logReturns.push((mu-0.5*sigma*sigma)*T+diffusion+jumpSum);
  }
  const minR=Math.min(...logReturns), maxR=Math.max(...logReturns);
  const nBins=28;
  const binWidth=(maxR-minR)/nBins || 1;
  const bins=new Array(nBins).fill(0);
  logReturns.forEach(r=>{
    let idx=Math.floor((r-minR)/binWidth);
    if(idx>=nBins) idx=nBins-1; if(idx<0) idx=0;
    bins[idx]++;
  });
  const barData=bins.map((c,i)=>({x:minR+(i+0.5)*binWidth, y:c/(nSims*binWidth)}));

  const theoMean=(mu-0.5*sigma*sigma)*T;
  const theoSd=sigma*Math.sqrt(T);
  const curve=[];
  for(let x=minR; x<=maxR; x+=(maxR-minR)/80){
    curve.push({x, y: normPdf((x-theoMean)/theoSd)/theoSd });
  }
  histChart.data.datasets[0].data = barData;
  histChart.data.datasets[0].barThickness = Math.max(2, 260/nBins);
  histChart.data.datasets[1].data = curve;
  histChart.update();
}
['path-mu','path-sigma','path-lambda','path-p','path-eta1','path-eta2','path-T'].forEach(id=>{
  bindSlider(id, v=>v.toFixed(2), updatePathSection);
});
updatePathSection();

/* ========================= §4 期权定价 ========================= */
const priceChart = new Chart(document.getElementById('priceChart'), {
  type:'line',
  data:{ datasets:[
    { label:'Kou (MC)', data:[], borderColor:'#49D3E8', backgroundColor:'transparent', pointRadius:2.5, pointBackgroundColor:'#49D3E8', borderWidth:2, tension:0.15 },
    { label:'Black-Scholes', data:[], borderColor:'#7C8898', backgroundColor:'transparent', pointRadius:0, borderDash:[5,4], borderWidth:1.8, tension:0.15 }
  ]},
  options:{
    responsive:true, maintainAspectRatio:false,
    plugins:{ legend:{display:false} },
    scales:{
      x:{ type:'linear', title:{display:true,text:'行权价 K'}, grid:gridStyle },
      y:{ title:{display:true,text:'期权价格'}, grid:gridStyle }
    }
  }
});
const smileChart = new Chart(document.getElementById('smileChart'), {
  type:'line',
  data:{ datasets:[
    { label:'隐含波动率', data:[], borderColor:'#49D3E8', backgroundColor:'transparent', pointRadius:2.5, pointBackgroundColor:'#49D3E8', borderWidth:2, tension:0.15 },
    { label:'基准 σ', data:[], borderColor:'#7C8898', backgroundColor:'transparent', pointRadius:0, borderDash:[5,4], borderWidth:1.6 }
  ]},
  options:{
    responsive:true, maintainAspectRatio:false,
    plugins:{ legend:{display:false} },
    scales:{
      x:{ type:'linear', title:{display:true,text:'行权价 K'}, grid:gridStyle },
      y:{ title:{display:true,text:'隐含波动率'}, grid:gridStyle, ticks:{ callback:v=>(v*100).toFixed(0)+'%' } }
    }
  }
});

function runPricing(){
  const statusEl=document.getElementById('price-status');
  statusEl.textContent='计算中…';
  const S0=100;
  const r=parseFloat(document.getElementById('price-r').value);
  const sigma=parseFloat(document.getElementById('price-sigma').value);
  const T=parseFloat(document.getElementById('price-T').value);
  const lambda=parseFloat(document.getElementById('price-lambda').value);
  const p=parseFloat(document.getElementById('price-p').value);
  const eta1=parseFloat(document.getElementById('price-eta1').value);
  const eta2=parseFloat(document.getElementById('price-eta2').value);
  document.getElementById('price-eta-val').textContent = eta1.toFixed(1)+' / '+eta2.toFixed(1);

  const zeta=kouZeta(p,eta1,eta2);
  const muQ=r-lambda*zeta-0.5*sigma*sigma;
  const nSims=20000;
  const strikes=[];
  for(let k=0.6; k<=1.5001; k+=0.06) strikes.push(Math.round(S0*k));

  const kouPrices=[], bsPrices=[], impliedVols=[], flatVol=[];
  strikes.forEach(K=>{
    let payoffSum=0;
    for(let i=0;i<nSims;i++){
      const diffusion=sigma*Math.sqrt(T)*randNormal();
      const nJ=randPoisson(lambda*T);
      let jumpSum=0;
      for(let j=0;j<nJ;j++) jumpSum+=randKouJump(p,eta1,eta2);
      const ST=S0*Math.exp(muQ*T+diffusion+jumpSum);
      payoffSum+=Math.max(ST-K,0);
    }
    const kouPrice=Math.exp(-r*T)*payoffSum/nSims;
    const bsPrice=bsCall(S0,K,r,sigma,T);
    kouPrices.push({x:K,y:kouPrice});
    bsPrices.push({x:K,y:bsPrice});
    const iv = impliedVol(Math.max(kouPrice,1e-6),S0,K,r,T);
    impliedVols.push({x:K,y:iv});
    flatVol.push({x:K,y:sigma});
  });

  priceChart.data.datasets[0].data=kouPrices;
  priceChart.data.datasets[1].data=bsPrices;
  priceChart.update();
  smileChart.data.datasets[0].data=impliedVols;
  smileChart.data.datasets[1].data=flatVol;
  smileChart.update();
  statusEl.textContent='已更新 · ζ = '+zeta.toFixed(4)+'，风险中性漂移 μ_ℚ = '+muQ.toFixed(4);
}
['price-r','price-sigma','price-T','price-lambda','price-p','price-eta1','price-eta2'].forEach(id=>{
  bindSlider(id, v=>v.toFixed(3));
});
document.getElementById('price-recompute').addEventListener('click', runPricing);
['price-r','price-sigma','price-T','price-lambda','price-p','price-eta1','price-eta2'].forEach(id=>{
  document.getElementById(id).addEventListener('change', runPricing);
});
runPricing();

/* ========================= Hero 动画 ========================= */
(function(){
  const canvas=document.getElementById('heroCanvas');
  const ctx=canvas.getContext('2d');
  const reduceMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  let dpr=window.devicePixelRatio||1;
  function resize(){
    const rect=canvas.getBoundingClientRect();
    canvas.width=Math.max(1,rect.width*dpr);
    canvas.height=Math.max(1,rect.height*dpr);
    ctx.setTransform(dpr,0,0,dpr,0,0);
  }
  function genPath(){
    const steps=420, dt=1/steps, lambda=2.4, p=0.35, eta1=22, eta2=14, sigma=0.55;
    let logS=0; const pts=[0]; const jumps=[];
    for(let i=1;i<=steps;i++){
      const diffusion=sigma*Math.sqrt(dt)*randNormal();
      const nJ=randPoisson(lambda*dt);
      let js=0;
      for(let j=0;j<nJ;j++){ const y=randKouJump(p,eta1,eta2); js+=y; jumps.push({i, dir:y>=0?'up':'down'}); }
      logS+=-0.5*sigma*sigma*dt+diffusion+js;
      pts.push(logS);
    }
    return {pts, jumps};
  }
  function draw(data){
    resize();
    const w=canvas.width/dpr, h=canvas.height/dpr;
    ctx.clearRect(0,0,w,h);
    const pts=data.pts;
    const maxAbs=Math.max(...pts.map(Math.abs), 0.25);
    ctx.beginPath();
    pts.forEach((v,i)=>{
      const x=(i/(pts.length-1))*w;
      const y=h/2-(v/maxAbs)*(h*0.42);
      if(i===0) ctx.moveTo(x,y); else ctx.lineTo(x,y);
    });
    ctx.strokeStyle='rgba(201,210,220,0.85)';
    ctx.lineWidth=1.5;
    ctx.stroke();
    data.jumps.forEach(j=>{
      const x=(j.i/(pts.length-1))*w;
      const y=h/2-(pts[j.i]/maxAbs)*(h*0.42);
      ctx.beginPath(); ctx.arc(x,y,3,0,Math.PI*2);
      ctx.fillStyle=j.dir==='up'?'#F2A33D':'#7C8BFF';
      ctx.fill();
    });
  }
  let current=genPath();
  draw(current);
  window.addEventListener('resize', ()=>draw(current));
  if(!reduceMotion){
    setInterval(()=>{ current=genPath(); draw(current); }, 4200);
  }
})();
</script>
</body>
</html>
