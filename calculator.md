# 義大利人事成本試算器

> 在義大利聘用一位員工要花多少：稅前薪資、雇主保費、INAIL 與離職金提撥，以兩份協約為例，並說明大區與市級稅如何影響實領。


<section> <span class="eyebrow">成本試算器</span> <h1 id="what-an-employee-in-italy-really-costs">在義大利聘一位員工的真實成本</h1> <p class="lede">您支付員工的實際人事成本，加上我們的月費。以下以兩份協約為例，拆解人事成本的組成。</p> </section> <section> <div class="grid"> <form class="panel" id="calc" style="display:grid;gap:16px"> <label for="ral">稅前年薪 RAL（歐元）<input id="ral" type="number" min="15000" step="1000" value="50000"></label> <label for="ccnl">集體協約（CCNL）<select id="ccnl"><option value="commercio">商業服務業（CCNL Terziario, Distribuzione e Servizi）</option><option value="metalmeccanico">工程與製造業（CCNL Metalmeccanico Industria）</option></select></label> <label style="display:flex;gap:10px;align-items:center;font-weight:400"><input id="prorata" type="checkbox" checked style="width:auto">第 13、14 個月按月分攤至每期薪資</label> <label style="display:flex;gap:10px;align-items:center;font-weight:400"><input id="tfrfund" type="checkbox" checked style="width:auto">TFR 每月提撥至員工選擇的基金</label> <label for="fx">每歐元兌美元匯率<input id="fx" type="number" step="0.01" value="1.08"></label> <p id="ccnlnote" style="margin:0;color:var(--muted);font-size:14px"></p> </form> <div class="panel" style="min-width:0"> <div class="tbl"><table id="out"> <thead><tr><th>項目</th><th class="num">每月（平均）</th><th class="num">每年</th></tr></thead> <tbody></tbody> </table></div> <p id="inst" style="font-size:14px;color:var(--muted);margin-bottom:0"></p> </div> </div> <p style="font-size:14px;color:var(--muted)">範例數字，費率更新於 2026-10-26。保費與保險費率為參考值 <span class="tag">估算</span>，實際依產業、公司規模與職務風險等級而定，我們會在報價中確認。帳單可改以新台幣或港幣開立，依同一歐元參考匯率換算。</p> </section> <section> <h2 id="your-monthly-invoices-over-a-year">一年 12 期帳單</h2> <p class="prose" style="margin:0">全年成本不變，選項只改變付款時點：兩個選項都勾選時，每月金額相同，不會在年底或離職時累積一大筆。</p> <div class="tbl"><table id="sched"><thead><tr><th>月份</th><th class="num">薪資</th><th class="num">INPS + INAIL</th><th class="num">TFR</th><th class="num">服務費</th><th class="num">帳單</th></tr></thead><tbody></tbody></table></div> <p id="schednote" style="font-size:14px;color:var(--muted);margin:0"></p>  </section> <section class="prose"> <h2 id="what-the-employment-cost-is-made-of">人事成本的組成</h2> <div class="fact"><b>RAL</b><span><strong>稅前年薪。</strong>錄取通知上的數字。依協約分 13 或 14 期發放：多出的是第 13 個月（12 月），商業服務業另有第 14 個月（7 月）。</span></div> <div class="fact"><b>INPS</b><span><strong>雇主社會保險費。</strong>退休金、失業、疾病與生育基金，約稅前薪資的 29–32%。員工另從自己的稅前薪資負擔約 9%，這部分不是您的額外成本。</span></div> <div class="fact"><b>INAIL</b><span><strong>職災保險。</strong>強制投保。辦公室職務很低（遠低於 1%），技術與生產職務較高。</span></div> <div class="fact"><b>TFR</b><span><strong>離職金提撥。</strong>每年提撥稅前薪資的 6.91%，僱傭關係結束時不論原因都發給員工（民法第 2120 條）。</span></div> <div class="fact"><b>服務費</b><span><strong>我們的 EOR 服務費。</strong>每位員工每月 €250。</span></div> </section> <section class="prose"> <h2 id="billed-on-actuals-month-by-month">每月依實際金額計費</h2> <p>上表是估算。每個月我們執行實際薪資並依實際成本開立帳單：加班、獎金、無薪假、部分由 INPS 給付的病假、調薪與協約調整，都會反映在當月數字。每張帳單附薪資摘要，每一行都可核對。</p> <p>付款條件：開始時收取一個月預估成本作為可退還押金，加上第一個月預付；之後每月依估算預付，並在下一期帳單依實際薪資調整。</p> </section> <section class="prose"> <h2 id="two-collective-agreements-compared">兩份協約比較</h2> <p>同樣 €50,000 的 RAL，金屬機械業協約下的工程職位，雇主每年成本比商業服務業協約下的辦公室職位約多 €1,500–2,000：社會保險費率約高 2–3 個百分點，技術職務的職災保險也較高。商業服務業協約分 14 期發放，每期薪資較少，但全年仍是同一個 RAL。</p> <p>適用哪份協約不能自由選擇，而是依職務與工作所屬產業決定。我們在擬約時選定並說明理由。</p> </section> <section class="prose"> <h2 id="why-the-city-changes-net-pay-not-your-cost">城市影響的是實領，不是您的成本</h2> <p>除了全國所得稅（IRPEF），每位員工還要繳<strong>大區</strong>附加稅（依大區與所得級距，約應稅所得的 1.23% 至 3.33%）與<strong>市級</strong>附加稅（通常 0–0.8%；羅馬 0.9%、拿坡里 1%、杜林最高 1.2%；許多城市對低所得免徵）。兩者都從員工的稅前薪資中預扣。</p> <p>它們不改變您的支出，只改變員工的實領：以 €50,000 RAL 計算，最便宜與最貴的大區與城市組合，每年實領差距約 €1,000–1,500。比較不同城市候選人的錄取條件時值得留意。</p>  </section> <div class="cta"><a class="btn" href="contact.html">取得精確報價</a><a class="btn ghost" href="net-pay-calculator.html">看員工實領</a></div> <script>(function(){const P = {"_note":"Parametri del calcolatore con fonte e stato. 'indicative' = da sostituire con data/params/2026.yaml verificato.","updated":"2026-10-26","ccnl":{"commercio":{"label":"商業服務業（CCNL Terziario, Distribuzione e Servizi）","installments":14,"employer_social_rate":0.29,"inail_rate":0.004,"status":"indicative","note":"常見於辦公室、資訊服務、顧問與業務職位。有第 13 與第 14 個月。"},"metalmeccanico":{"label":"工程與製造業（CCNL Metalmeccanico Industria）","installments":13,"employer_social_rate":0.315,"inail_rate":0.012,"status":"indicative","note":"常見於工程、生產與技術職位。有第 13 個月。"}},"tfr_rate":{"value":0.0691,"status":"verified","source":"Civil Code art. 2120: gross pay / 13.5, less 0.5% to the INPS fund"},"employee_social_rate":{"value":0.0919,"status":"indicative","source":"INPS employee share, private sector"},"regional_surcharge":{"min":0.0123,"max":0.0333,"status":"indicative","source":"MEF, addizionale regionale IRPEF"},"municipal_surcharge":{"min":0,"max":0.009,"status":"indicative","source":"MEF, addizionale comunale IRPEF (0.8% general cap; Rome 0.9%)"},"eor_fee_eur":{"value":250,"status":"list price"},"usd_per_eur":{"value":1.08,"status":"indicative","source":"Replace with ECB daily reference rate at build time"},"net":{"status":"secondary","source":"data/params/2026.yaml (irpef, inps, addizionali); TUIR art. 11 and 13; L. 207/2024; L. 199/2025","employee_inps":0.0919,"extra_1pct_above":56224,"irpef":[[28000,0.23],[50000,0.33],[null,0.43]],"cities":{"Milan":{"region":"Lombardy","regional":[[null,0.0123]],"municipal":0.008,"exempt":23000},"Rome":{"region":"Lazio","regional":[[28000,0.0173],[null,0.0333]],"municipal":0.009,"exempt":14000},"Turin":{"region":"Piedmont","regional":[[null,0.0162]],"municipal":0.008,"municipal_note":"0.8% to 1.2% by band; 0.8% used","exempt":11790},"Bologna":{"region":"Emilia-Romagna","regional":[[null,0.0133]],"municipal":0.008,"exempt":15000},"Naples":{"region":"Campania","regional":[[null,0.0173]],"municipal":0.01,"exempt":12000}}}};

const eur = n => '€' + Math.round(n).toLocaleString('en-US');
const usd = n => '$' + Math.round(n).toLocaleString('en-US');
function calc(){
  const ral = +document.getElementById('ral').value || 0;
  const fx = +document.getElementById('fx').value || 0;
  const c = P.ccnl[document.getElementById('ccnl').value];
  const items = [
    ['稅前薪資（RAL）', ral],
    ['雇主社會保險費（INPS）', ral * c.employer_social_rate],
    ['職災保險（INAIL）', ral * c.inail_rate],
    ['離職金提撥（TFR）', ral * P.tfr_rate.value],
    ['義大利僱傭 EOR 服務費', P.eor_fee_eur.value * 12],
  ];
  const tot = items.reduce((s, x) => s + x[1], 0);
  document.querySelector('#out tbody').innerHTML = items.map(([k, v]) => `<tr><td>${k}</td><td class="num">${eur(v/12)}</td><td class="num">${eur(v)}</td></tr>`).join('')
    + `<tr><td><b>總成本</b></td><td class="num"><b>${eur(tot/12)}</b></td><td class="num"><b>${eur(tot)}</b></td></tr>`
    + `<tr><td>美元合計</td><td class="num">${usd(tot/12*fx)}</td><td class="num">${usd(tot*fx)}</td></tr>`;
  document.getElementById('inst').textContent = `薪資分 ${c.installments} 期發放，每期稅前 ${eur(ral / c.installments)}。總成本比 RAL 高 ${(tot / ral * 100 - 100).toFixed(0)}%。`;
  document.getElementById('ccnlnote').textContent = c.note;
  const pr = document.getElementById('prorata').checked, tf = document.getElementById('tfrfund').checked;
  const inst = ral / c.installments, extra = c.installments - 12;
  const months = ['1月','2月','3月','4月','5月','6月','7月','8月','9月','10月','11月','12月'];
  const rate = c.employer_social_rate + c.inail_rate, fee = P.eor_fee_eur.value;
  let rows = '', sum = 0;
  months.forEach((m, i) => {
    let sal = pr ? ral / 12 : inst + (i === 11 ? inst : 0) + (extra === 2 && i === 6 ? inst : 0);
    const tfr = tf ? ral * P.tfr_rate.value / 12 : 0;
    const inv = sal * (1 + rate) + tfr + fee; sum += inv;
    rows += `<tr><td>${m}</td><td class="num">${eur(sal)}</td><td class="num">${eur(sal*rate)}</td><td class="num">${eur(tfr)}</td><td class="num">${eur(fee)}</td><td class="num"><b>${eur(inv)}</b></td></tr>`;
  });
  rows += `<tr><td><b>全年</b></td><td></td><td></td><td></td><td></td><td class="num"><b>${eur(sum)}</b></td></tr>`;
  document.querySelector('#sched tbody').innerHTML = rows;
  document.getElementById('schednote').textContent = tf ? 'TFR 每月提撥，不會累積離職金負債。' : `每年累積 ${eur(ral * P.tfr_rate.value)} 的 TFR，於離職時發給；由押金擔保。`;
}
document.getElementById('calc').addEventListener('input', calc);
document.getElementById('calc').addEventListener('submit', e => e.preventDefault());
calc();
})();</script>


---
Source: https://yidaliguyong.com/calculator.html
