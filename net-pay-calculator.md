# 義大利實領薪資試算器

> 2026 年義大利從稅前到實發：員工社會保險費、含薪資所得減免的所得稅（IRPEF）、大區與市級附加稅，涵蓋米蘭、羅馬、杜林、波隆那與拿坡里。


<section> <span class="eyebrow">實領試算器</span> <h1 id="what-your-employee-takes-home-in-italy">員工在義大利實際拿到多少</h1> <p class="lede">輸入稅前年薪與城市。估算套用 2026 年規則：員工社會保險費、含薪資所得減免的所得稅，以及地方附加稅。</p> </section> <section> <div class="grid"> <form class="panel" id="nf" style="display:grid;gap:16px"> <label for="g">稅前年薪 RAL（歐元）<input id="g" type="number" min="10000" step="1000" value="50000"></label> <label for="city">城市<select id="city"><option value="Milan">米蘭</option><option value="Rome">羅馬</option><option value="Turin">杜林</option><option value="Bologna">波隆那</option><option value="Naples">拿坡里</option></select></label> <label for="inst">發放期數<select id="inst"><option value="13">13 期</option><option value="14">14 期</option><option value="12">12 期（第 13／14 個月按月分攤）</option></select></label> </form> <div class="panel" style="min-width:0"><div class="tbl"><table id="nt"><thead><tr><th>項目</th><th class="num">每年</th></tr></thead><tbody></tbody></table></div> <p id="nm" style="margin-bottom:0;font-weight:600"></p></div> </div>  </section> <section class="prose"> <h2 id="how-the-calculation-works">計算方式</h2> <ol> <li>員工就稅前薪資負擔 9.19% 社會保險費，年薪超過 €56,224 的部分再加 1%。</li> <li>剩餘金額課所得稅（IRPEF）：€28,000 以內 23%，€28,000 至 €50,000 為 33%，以上 43%。</li> <li>薪資所得稅額減免降低稅額，低薪時最大，到 €50,000 歸零。€20,000 至 €40,000 之間另有最高 €1,000 的額外減免。</li> <li>再加上大區與市級附加稅，所得低於該市免稅門檻者免徵市級稅。</li> </ol> <p>以上都不影響雇主的支出，請見<a href="calculator.html">雇主成本試算器</a>。台灣員工習慣看月薪，請注意義大利實領要除以 13 或 14 期。</p> </section> <script>(function(){const N = {"status":"secondary","source":"data/params/2026.yaml (irpef, inps, addizionali); TUIR art. 11 and 13; L. 207/2024; L. 199/2025","employee_inps":0.0919,"extra_1pct_above":56224,"irpef":[[28000,0.23],[50000,0.33],[null,0.43]],"cities":{"Milan":{"region":"倫巴底","regional":[[null,0.0123]],"municipal":0.008,"exempt":23000},"Rome":{"region":"拉齊奧","regional":[[28000,0.0173],[null,0.0333]],"municipal":0.009,"exempt":14000},"Turin":{"region":"皮埃蒙特","regional":[[null,0.0162]],"municipal":0.008,"municipal_note":"0.8% to 1.2% by band; 0.8% used","exempt":11790},"Bologna":{"region":"艾米利亞-羅馬涅","regional":[[null,0.0133]],"municipal":0.008,"exempt":15000},"Naples":{"region":"坎帕尼亞","regional":[[null,0.0173]],"municipal":0.01,"exempt":12000}}};

const eur = n => (n < 0 ? '−€' : '€') + Math.round(Math.abs(n)).toLocaleString('en-US');
function bands(x, b){ let t = 0, lo = 0; for (const [hi, r] of b){ const top = hi ?? Infinity; if (x > lo) t += (Math.min(x, top) - lo) * r; lo = top; } return t; }
function credit(r){ if (r <= 15000) return 1955; if (r <= 28000) return 1910 + 1190 * (28000 - r) / 13000; if (r <= 50000) return 1910 * (50000 - r) / 22000 + (r > 25000 && r <= 35000 ? 65 : 0); return 0; }
function extra(r){ if (r > 20000 && r <= 32000) return 1000; if (r > 32000 && r < 40000) return 1000 * (40000 - r) / 8000; return 0; }
function calc(){
  const g = +document.getElementById('g').value || 0, c = N.cities[document.getElementById('city').value], n = +document.getElementById('inst').value;
  const inps = g * N.employee_inps + Math.max(0, g - N.extra_1pct_above) * 0.01;
  const tx = g - inps;
  const irpef = Math.max(0, bands(tx, N.irpef) - credit(tx) - extra(tx));
  const reg = bands(tx, c.regional), mun = tx > c.exempt ? tx * c.municipal : 0;
  const net = g - inps - irpef - reg - mun;
  const rows = [['稅前薪資', g], ['員工社會保險費', -inps], ['所得稅（IRPEF，扣除減免後）', -irpef], [`大區附加稅（${c.region}）`, -reg], ['市級附加稅', -mun]];
  document.querySelector('#nt tbody').innerHTML = rows.map(([k, v]) => `<tr><td>${k}</td><td class="num">${eur(v)}</td></tr>`).join('') + `<tr><td><b>實領</b></td><td class="num"><b>${eur(net)}</b></td></tr>`;
  document.getElementById('nm').textContent = `每期實領約 ${eur(net / n)}，共 ${n} 期（為稅前的 ${(net / g * 100).toFixed(0)}%）。`;
}
document.getElementById('nf').addEventListener('input', calc); document.getElementById('nf').addEventListener('submit', e => e.preventDefault()); calc();
})();</script>


---
Source: https://yidaliguyong.com/net-pay-calculator.html
