# 取得報價

> 申請在義大利聘用員工的報價。三個簡單步驟，一個工作天內回覆。


<section> <span class="eyebrow">取得報價</span> <h1 id="tell-us-who-you-want-to-hire">告訴我們您想聘用誰</h1> <p class="lede">三個簡單步驟。我們在一個工作天內回覆完整成本與契約大綱，並可依您的需求以新台幣、港幣或美元報價。</p> </section> <section> <form id="lead" class="panel" style="display:grid;gap:18px;max-width:640px" novalidate> <p id="stepinfo" class="tag" style="justify-self:start">第 1 步，共 3 步</p> <fieldset data-step="1" style="border:0;padding:0;margin:0;display:grid;gap:14px"> <label for="email">公司電子郵件<input id="email" type="email" autocomplete="email" required></label> <label for="company">公司名稱<input id="company" autocomplete="organization"></label> </fieldset> <fieldset data-step="2" hidden style="border:0;padding:0;margin:0;display:grid;gap:14px"> <label for="service">您需要什麼服務？<select id="service"><option>名義雇主（EOR）</option><option>薪資代辦（已有義大利公司）</option><option>工作簽證／藍卡</option><option>招募</option></select></label> <label for="count">在義大利聘用幾人？<input id="count" type="number" min="1" value="1"></label> <label for="city">城市或地區<input id="city" placeholder="米蘭、杜林、遠距…"></label> <label for="salary">預計稅前年薪（歐元）<input id="salary" type="number" step="1000"></label> </fieldset> <fieldset data-step="3" hidden style="border:0;padding:0;margin:0;display:grid;gap:14px"> <label for="name">您的姓名<input id="name" autocomplete="name"></label> <label for="start">預計到職日<input id="start" type="date"></label> <label for="notes">其他說明<textarea id="notes" rows="4"></textarea></label> <label style="display:flex;gap:10px;align-items:flex-start;font-weight:400"><input id="consent" type="checkbox" style="width:auto;margin-top:5px">我同意義大利僱傭為回覆本次詢問而處理我的資料（隱私權政策）。</label> </fieldset> <p id="msg" role="status" style="margin:0;color:var(--accent)"></p> <div class="cta"><button type="button" class="btn ghost" id="back" hidden>上一步</button><button type="submit" class="btn" id="next">繼續</button></div> </form> </section> <script>
// Il passo 1 salva subito l'email (lead abbandonato recuperabile dal nurturing). Endpoint del worker: /api/lead.
const f = document.getElementById('lead'); let step = 1;
const sets = [...f.querySelectorAll('fieldset')];
const data = () => Object.fromEntries([...f.querySelectorAll('input,select,textarea')].map(e => [e.id, e.type === 'checkbox' ? e.checked : e.value]));
async function save(final){ try { await fetch('/api/lead', {method:'POST', headers:{'Content-Type':'application/json'}, body: JSON.stringify({...data(), step, final, brand:'yidaliguyong'})}); } catch(e){} }
function show(){ sets.forEach(s => s.hidden = +s.dataset.step !== step);
  document.getElementById('stepinfo').textContent = `第 ${step} 步，共 3 步`;
  document.getElementById('back').hidden = step === 1;
  document.getElementById('next').textContent = step === 3 ? '送出' : '繼續'; }
// Ripresa dal link nelle email: ?resume=<token> precompila i campi e salta al passo successivo.
(async () => { const tok = new URLSearchParams(location.search).get('resume'); if (!tok) return;
  try { const r = await fetch('/api/lead/' + encodeURIComponent(tok)); if (!r.ok) return; const d = await r.json();
    for (const [k, v] of Object.entries(d)) { const el = document.getElementById(k); if (el && v != null) el.value = v; }
    step = d.step || 2; show(); } catch(e){} })();
document.getElementById('back').onclick = () => { step--; show(); };
f.addEventListener('submit', e => { e.preventDefault(); const m = document.getElementById('msg'); m.textContent = '';
  if (step === 1 && !document.getElementById('email').checkValidity()) { m.textContent = '請輸入有效的公司電子郵件以繼續。'; return; }
  if (step === 3 && !document.getElementById('consent').checked) { m.textContent = '請勾選同意欄位，我們才能回覆您。'; return; }
  save(step === 3);
  if (step < 3) { step++; show(); } else { f.querySelectorAll('fieldset,.cta').forEach(x => x.hidden = true); m.textContent = '謝謝！我們將在一個工作天內回覆。'; } });
</script>

<script>(function(){var sj=new URLSearchParams(location.search).get('subject');var n=document.getElementById('notes');if(sj&&n&&!n.value)n.value='['+sj.slice(0,40)+'] ';})();</script>


---
Source: https://yidaliguyong.com/contact.html
