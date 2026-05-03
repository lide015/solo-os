[index.html.html](https://github.com/user-attachments/files/27323541/index.html.html)
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Solo OS — 個人公司作業系統 v1.0 | 90 天從受僱者到 Solo CEO</title>
<meta name="description" content="一套讓你不再「忙得像狗，賺得像鬼」的個人公司作業系統。戰略指南 + 工作模板 + 35 個高轉換 Prompts + 12 月財務模型 + KPI 儀表板。">
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    font-family: -apple-system, BlinkMacSystemFont, "PingFang TC", "Microsoft JhengHei", sans-serif;
    color: #1a202c; line-height: 1.6; background: #fff;
  }
  .container { max-width: 1100px; margin: 0 auto; padding: 0 24px; }
  section { padding: 80px 0; }
  @media (max-width: 768px) { section { padding: 50px 0; } }

  /* Hero */
  .hero {
    background: linear-gradient(135deg, #1a202c 0%, #2d3748 100%);
    color: white; padding: 100px 0 80px;
  }
  .hero .badge {
    display: inline-block; padding: 6px 14px; background: rgba(66,153,225,0.2);
    border: 1px solid rgba(66,153,225,0.4); border-radius: 20px; font-size: 13px;
    color: #90cdf4; margin-bottom: 24px; font-weight: 500;
  }
  .hero h1 {
    font-size: 52px; font-weight: 800; line-height: 1.15; margin-bottom: 24px;
    letter-spacing: -1px;
  }
  .hero h1 .accent { color: #4299e1; }
  .hero .subtitle {
    font-size: 20px; color: #cbd5e0; margin-bottom: 36px; max-width: 720px;
    line-height: 1.5;
  }
  .hero .cta-row { display: flex; gap: 16px; align-items: center; flex-wrap: wrap; }
  .price-tag { color: #90cdf4; font-size: 14px; }
  .price-tag s { color: #718096; margin-right: 8px; }
  .btn {
    display: inline-block; padding: 16px 36px; background: #4299e1; color: white;
    text-decoration: none; border-radius: 8px; font-weight: 700; font-size: 16px;
    transition: all 0.2s; border: none; cursor: pointer;
  }
  .btn:hover { background: #2b6cb0; transform: translateY(-2px); }
  .btn-secondary { background: transparent; border: 1px solid #4a5568; }
  .btn-secondary:hover { background: #4a5568; }

  @media (max-width: 768px) {
    .hero h1 { font-size: 32px; }
    .hero .subtitle { font-size: 16px; }
  }

  /* Pain section */
  .pain { background: #f7fafc; }
  h2 {
    font-size: 36px; font-weight: 800; margin-bottom: 16px; letter-spacing: -0.5px;
    text-align: center;
  }
  .section-sub { font-size: 18px; color: #718096; text-align: center; margin-bottom: 50px; }
  .pain-grid {
    display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px; margin-top: 40px;
  }
  @media (max-width: 768px) { .pain-grid { grid-template-columns: 1fr; } }
  .pain-card {
    background: white; padding: 28px; border-radius: 12px; border: 1px solid #e2e8f0;
  }
  .pain-card .icon { font-size: 28px; margin-bottom: 12px; display: block; }
  .pain-card h3 { font-size: 18px; font-weight: 700; margin-bottom: 8px; }
  .pain-card p { color: #4a5568; font-size: 15px; }

  /* What's inside */
  .deliverables-grid {
    display: grid; grid-template-columns: repeat(2, 1fr); gap: 24px; margin-top: 40px;
  }
  @media (max-width: 768px) { .deliverables-grid { grid-template-columns: 1fr; } }
  .deliverable {
    border: 2px solid #e2e8f0; padding: 28px; border-radius: 12px;
    transition: all 0.2s;
  }
  .deliverable:hover { border-color: #4299e1; box-shadow: 0 4px 20px rgba(66,153,225,0.1); }
  .deliverable .num { font-size: 12px; color: #4299e1; font-weight: 700; letter-spacing: 1px; }
  .deliverable h3 { font-size: 22px; font-weight: 700; margin: 8px 0 12px; }
  .deliverable .desc { color: #4a5568; margin-bottom: 16px; font-size: 15px; }
  .deliverable ul { list-style: none; padding: 0; }
  .deliverable li { font-size: 14px; color: #2d3748; padding: 4px 0 4px 22px; position: relative; }
  .deliverable li::before {
    content: '✓'; position: absolute; left: 0; color: #48bb78; font-weight: 700;
  }

  /* Who is this for */
  .who { background: #1a202c; color: white; }
  .who h2 { color: white; }
  .who-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 32px; margin-top: 40px; }
  @media (max-width: 768px) { .who-grid { grid-template-columns: 1fr; } }
  .who-col { padding: 24px; border-radius: 12px; }
  .who-col.yes { background: rgba(72,187,120,0.1); border: 1px solid rgba(72,187,120,0.3); }
  .who-col.no { background: rgba(245,101,101,0.1); border: 1px solid rgba(245,101,101,0.3); }
  .who-col h3 { font-size: 22px; margin-bottom: 16px; }
  .who-col.yes h3 { color: #68d391; }
  .who-col.no h3 { color: #fc8181; }
  .who-col li { padding: 8px 0 8px 28px; position: relative; color: #cbd5e0; font-size: 15px; }
  .who-col.yes li::before { content: '✓'; position: absolute; left: 0; color: #68d391; font-weight: 700; }
  .who-col.no li::before { content: '✗'; position: absolute; left: 0; color: #fc8181; font-weight: 700; }

  /* Pricing */
  .pricing { text-align: center; }
  .price-card {
    max-width: 480px; margin: 40px auto 0; padding: 40px; border: 2px solid #4299e1;
    border-radius: 16px; background: linear-gradient(135deg, #fff 0%, #f7fafc 100%);
    box-shadow: 0 10px 40px rgba(66,153,225,0.12);
  }
  .price-card .label {
    display: inline-block; padding: 4px 12px; background: #4299e1; color: white;
    border-radius: 4px; font-size: 12px; font-weight: 700; letter-spacing: 1px;
    margin-bottom: 16px;
  }
  .price-original { color: #a0aec0; text-decoration: line-through; font-size: 18px; }
  .price-now { font-size: 56px; font-weight: 800; color: #2d3748; margin: 8px 0; }
  .price-now .currency { font-size: 28px; vertical-align: super; color: #4a5568; }
  .price-once { color: #718096; font-size: 14px; margin-bottom: 24px; }
  .price-card ul { text-align: left; margin: 24px 0; }
  .price-card li { padding: 6px 0 6px 28px; position: relative; font-size: 15px; color: #2d3748; }
  .price-card li::before { content: '✓'; position: absolute; left: 0; color: #48bb78; font-weight: 700; }

  /* FAQ */
  .faq { background: #f7fafc; }
  .faq-list { max-width: 800px; margin: 40px auto 0; }
  .faq-item { background: white; margin-bottom: 12px; border-radius: 8px; border: 1px solid #e2e8f0; overflow: hidden; }
  .faq-q {
    padding: 18px 24px; font-weight: 700; cursor: pointer; display: flex;
    justify-content: space-between; align-items: center; font-size: 16px;
  }
  .faq-q:hover { background: #f7fafc; }
  .faq-a { padding: 0 24px 18px; color: #4a5568; font-size: 15px; display: none; }
  .faq-item.open .faq-a { display: block; }
  .faq-item.open .faq-q::after { content: '−'; }
  .faq-q::after { content: '+'; font-size: 24px; color: #a0aec0; font-weight: 400; }

  /* Final CTA */
  .final-cta {
    background: linear-gradient(135deg, #4299e1 0%, #2b6cb0 100%); color: white;
    text-align: center;
  }
  .final-cta h2 { color: white; margin-bottom: 16px; }
  .final-cta p { color: #cbd5e0; font-size: 18px; margin-bottom: 32px; }
  .final-cta .btn { background: white; color: #2b6cb0; }
  .final-cta .btn:hover { background: #f7fafc; }

  footer {
    background: #1a202c; color: #a0aec0; text-align: center; padding: 24px;
    font-size: 13px;
  }
  footer a { color: #90cdf4; }

  /* Guarantee */
  .guarantee {
    background: #fffaf0; border: 1px solid #f6ad55; padding: 20px; border-radius: 8px;
    margin-top: 24px; max-width: 600px; margin-left: auto; margin-right: auto;
  }
  .guarantee strong { color: #c05621; }
</style>
</head>
<body>

<!-- HERO -->
<section class="hero">
  <div class="container">
    <div class="badge">v1.0 · 適合 30-45 歲想 Solo 的華人專業工作者</div>
    <h1>一套作業系統，<br>讓你<span class="accent">不再「忙得像狗，賺得像鬼」</span></h1>
    <p class="subtitle">
      Solo OS 不是另一本雞湯。是一套 90 天可以執行、跑得動現金流的個人公司作業系統。<br>
      包含 戰略指南 + 工作模板 + 35 個 Prompt + 12 月財務模型 + KPI 儀表板。
    </p>
    <div class="cta-row">
      <a href="#pricing" class="btn">立刻取得 $29</a>
      <a href="#whats-inside" class="btn btn-secondary">先看裡面有什麼</a>
      <span class="price-tag"><s>$49</s> 早鳥優惠 · 限前 100 名</span>
    </div>
  </div>
</section>

<!-- PAIN -->
<section class="pain">
  <div class="container">
    <h2>你正在經歷這些嗎？</h2>
    <p class="section-sub">如果三個有一個——這套系統就是為你做的</p>
    <div class="pain-grid">
      <div class="pain-card">
        <span class="icon">🔥</span>
        <h3>工作 12 小時，一個月卻只有上班時的 70%</h3>
        <p>因為你在賣時間，不是賣結果。你的定價、你的服務、你的客戶選擇，全部沒有系統化。</p>
      </div>
      <div class="pain-card">
        <span class="icon">📉</span>
        <h3>收入像心電圖，這個月很多、下個月歸零</h3>
        <p>你沒有客戶管線。前一個案子結束時，下一個還沒談好。永遠在「青黃不接」中焦慮。</p>
      </div>
      <div class="pain-card">
        <span class="icon">🌀</span>
        <h3>知道該做行銷，但永遠在交付，沒空做</h3>
        <p>你把 100% 時間給客戶，0% 給未來。客戶結束你就裸奔，從零開始找下一個。</p>
      </div>
    </div>
  </div>
</section>

<!-- WHAT'S INSIDE -->
<section id="whats-inside">
  <div class="container">
    <h2>你會收到什麼</h2>
    <p class="section-sub">五個模組，組合成一套完整的個人公司作業系統</p>
    <div class="deliverables-grid">

      <div class="deliverable">
        <span class="num">01 · 戰略指南</span>
        <h3>個人公司化作戰手冊（PDF/MD）</h3>
        <p class="desc">7 章 + 3 個附錄，從心智重設到規模化決策樹的完整地圖。</p>
        <ul>
          <li>定位戰場：利基鎖定的三維公式</li>
          <li>作業系統：5 大模組 + 5/2/1 時間分配</li>
          <li>90 天執行藍圖（週週可對照）</li>
          <li>財務命脈：三個口袋理論 + 安全水位</li>
          <li>客戶引擎：獲客三條腿 + 提案三幕劇</li>
        </ul>
      </div>

      <div class="deliverable">
        <span class="num">02 · 工作模板</span>
        <h3>週作戰系統 + 客戶管線管理</h3>
        <p class="desc">每週 1 小時填，省下 10 小時的「忙了卻不知道在忙什麼」。</p>
        <ul>
          <li>週節奏範本（5/2/1 時間分配）</li>
          <li>三個必勝戰役（Must Win Battles）</li>
          <li>客戶五階段管線追蹤表</li>
          <li>主動聯繫 / 提案三幕劇 / 推薦邀請腳本</li>
          <li>客戶 ABC 分級矩陣</li>
        </ul>
      </div>

      <div class="deliverable">
        <span class="num">03 · Prompts 庫</span>
        <h3>35 個高轉換 Solo CEO Prompts</h3>
        <p class="desc">給 ChatGPT / Claude / Gemini 通用，複製即用。</p>
        <ul>
          <li>定位診斷器 / 競爭對手解剖</li>
          <li>三層定價設計 / 提案三幕劇生成</li>
          <li>機會成本快速分析 / 緊急基金壓力測試</li>
          <li>內容改寫成五個平台 / Hook 公式產生器</li>
          <li>+ 其他 26 個分屬 10 大領域</li>
        </ul>
      </div>

      <div class="deliverable">
        <span class="num">04 · 財務模型</span>
        <h3>12 個月 Solo 財務試算表（Excel）</h3>
        <p class="desc">131 個公式自動驗算，改一個假設，全部數字重跑。</p>
        <ul>
          <li>Assumptions 假設輸入（藍/黃顏色標準）</li>
          <li>12 個月損益 + 現金流預估</li>
          <li>KPI 儀表自動健康判讀</li>
          <li>損益平衡點 + 安全水位計算</li>
          <li>支援保守/基本/樂觀三情境</li>
        </ul>
      </div>

      <div class="deliverable" style="grid-column: 1 / -1; border-color: #4299e1;">
        <span class="num">05 · 互動式儀表板</span>
        <h3>Solo OS Dashboard（HTML，本地端）</h3>
        <p class="desc">下載即用，打開瀏覽器就能填，所有資料儲存於你自己的電腦，不上傳任何雲端。</p>
        <ul>
          <li>四大頂部 KPI（收入 / 現金 / 跑道 / 客戶集中度）</li>
          <li>客戶管線即時追蹤 + 健康讀數</li>
          <li>本週深度工作節奏視覺化</li>
          <li>每週反思引導</li>
          <li>JSON 匯出，可以接到任何工具</li>
        </ul>
      </div>

    </div>
  </div>
</section>

<!-- WHO IS THIS FOR -->
<section class="who">
  <div class="container">
    <h2>誰該買 / 誰不該買</h2>
    <p class="section-sub" style="color:#a0aec0;">說實話，比你預期的更直接</p>
    <div class="who-grid">

      <div class="who-col yes">
        <h3>✓ 這套系統適合你，如果...</h3>
        <ul>
          <li>你是 30-45 歲華人專業工作者</li>
          <li>你有一技之長，但「不會把它變現」</li>
          <li>你已經 Solo 但收入像心電圖</li>
          <li>你還在公司，但每月想著「下一步」</li>
          <li>你願意每週投入 5 小時建立系統</li>
          <li>你受夠了「成功學雞湯」想要實際工具</li>
        </ul>
      </div>

      <div class="who-col no">
        <h3>✗ 這套不適合你，如果...</h3>
        <ul>
          <li>你想要「一夜致富」的捷徑</li>
          <li>你連自己想做什麼都還不知道</li>
          <li>你期待「不用做事就會有客戶」</li>
          <li>你只想看不想做（這是工具書，不是讀物）</li>
          <li>你已經月入 $30,000 USD 以上，這套對你太基礎</li>
          <li>你已經有完整的個人公司系統在跑</li>
        </ul>
      </div>

    </div>
  </div>
</section>

<!-- PRICING -->
<section id="pricing" class="pricing">
  <div class="container">
    <h2>投資自己的時間 = 投資自己的選擇權</h2>
    <p class="section-sub">買一杯咖啡的錢，換 90 天可執行的系統</p>

    <div class="price-card">
      <span class="label">早鳥優惠 · 限前 100 名</span>
      <div class="price-original">$49 USD</div>
      <div class="price-now"><span class="currency">$</span>29</div>
      <div class="price-once">一次付清 · 終身使用 · 含 v1.0 全部 5 個模組 · 後續更新免費</div>

      <ul>
        <li>戰略指南（30+ 頁深度內容）</li>
        <li>2 個工作模板（週節奏 + 客戶管線）</li>
        <li>35 個高轉換 Prompts</li>
        <li>12 月財務模型 Excel</li>
        <li>互動式 KPI Dashboard</li>
        <li>使用說明 + 90 天執行計畫</li>
      </ul>

      <a href="#" class="btn" style="width:100%; padding: 18px;">立刻取得 Solo OS v1.0</a>

      <div class="guarantee">
        <strong>14 天無條件退款保證</strong> — 你買回去用，覺得沒幫助，寄一封 email 全額退費。我不會問你任何理由。
      </div>
    </div>
  </div>
</section>

<!-- FAQ -->
<section class="faq">
  <div class="container">
    <h2>常見問題</h2>
    <div class="faq-list">
      <div class="faq-item">
        <div class="faq-q" onclick="this.parentElement.classList.toggle('open')">這跟其他「自由工作者課程」有什麼不一樣？</div>
        <div class="faq-a">大多數課程是「資訊」——告訴你 Solo 是什麼、為什麼很棒。這套是「系統」——給你模板、表單、公式、決策樹，是工具不是讀物。讀完課程你還是不知道下一步，用完這套你會知道。</div>
      </div>
      <div class="faq-item">
        <div class="faq-q" onclick="this.parentElement.classList.toggle('open')">我是新手 / 我已經 Solo 兩年了，適合嗎？</div>
        <div class="faq-a">新手：適合，因為你會少走 12 個月的彎路。<br>已 Solo 兩年：適合，因為你會發現你「應該系統化」的事，全部沒系統化。</div>
      </div>
      <div class="faq-item">
        <div class="faq-q" onclick="this.parentElement.classList.toggle('open')">我不會用 Excel / 不會寫程式怎麼辦？</div>
        <div class="faq-a">財務模型只需要改藍色和黃色格子，其他自動算。Dashboard 是 HTML 檔，雙擊開瀏覽器就能用，不需任何安裝。</div>
      </div>
      <div class="faq-item">
        <div class="faq-q" onclick="this.parentElement.classList.toggle('open')">內容是中文還是英文？</div>
        <div class="faq-a">主要為繁體中文，介面保留必要英文術語（Lead / Pipeline / KPI 等）。Prompts 提供中英雙版可貼到 ChatGPT。</div>
      </div>
      <div class="faq-item">
        <div class="faq-q" onclick="this.parentElement.classList.toggle('open')">後續會不會有更新？</div>
        <div class="faq-a">v1.0 購買者享有所有 v1.x 免費更新。v2.0（預計加入「產品化轉型模組」）預計 2027 年上半年發布，購買者可享 50% 升級價。</div>
      </div>
      <div class="faq-item">
        <div class="faq-q" onclick="this.parentElement.classList.toggle('open')">退款條件？</div>
        <div class="faq-a">14 天內無條件退款。寄一封 email 我退錢。檔案不需要刪除，但希望你誠實——這是最便宜也最公平的關係。</div>
      </div>
      <div class="faq-item">
        <div class="faq-q" onclick="this.parentElement.classList.toggle('open')">我可以分享給朋友嗎？</div>
        <div class="faq-a">不可以分享原檔。但你可以用裡面的方法、模板（改寫後）服務你自己的客戶。我相信知識傳播，但我也要養活自己。</div>
      </div>
    </div>
  </div>
</section>

<!-- FINAL CTA -->
<section class="final-cta">
  <div class="container">
    <h2>90 天後，你會感謝今天的決定</h2>
    <p>或者繼續用感覺經營，繼續焦慮，繼續從零找下一個客戶。<br>選擇是你的。</p>
    <a href="#pricing" class="btn">立刻取得 Solo OS · $29</a>
  </div>
</section>

<footer>
  © 2026 Solo OS · 14 天退款保證 · 一次付清終身使用<br>
  <a href="#">退款政策</a> · <a href="#">使用條款</a> · <a href="#">聯絡作者</a>
</footer>

</body>
</html>
