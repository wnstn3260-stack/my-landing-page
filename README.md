<!doctype html>
<html lang="ko">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>MONEY PICKS | 간편 상담</title>
  <style>
    :root{
      --blue:#0b5bd3;
      --blue2:#0a4fb9;
      --bg:#f6f8fc;
      --text:#0f172a;
      --muted:#64748b;
      --card:#ffffff;
      --line:#e2e8f0;
      --yellow:#ffd400;
      --shadow: 0 10px 30px rgba(2, 6, 23, .10);
      --radius: 18px;
      --max: 1100px;
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, "Noto Sans KR", "Apple SD Gothic Neo", Arial, sans-serif;
      color:var(--text);
      background:var(--bg);
      line-height:1.55;
    }
    a{color:inherit; text-decoration:none}
    .wrap{max-width:var(--max); margin:0 auto; padding:0 18px;}
    /* topbar */
    header{
      position:sticky; top:0; z-index:50;
      background:rgba(255,255,255,.92);
      backdrop-filter:saturate(180%) blur(10px);
      border-bottom:1px solid var(--line);
    }
    .nav{
      display:flex; align-items:center; justify-content:space-between;
      padding:14px 0;
    }
    .brand{
      display:flex; align-items:center; gap:10px; font-weight:800; letter-spacing:.2px;
    }
    .logo{
      width:38px; height:38px; border-radius:12px;
      background:linear-gradient(135deg, var(--blue), #2dd4bf);
      box-shadow: var(--shadow);
    }
    .menu{
      display:flex; gap:18px; color:var(--muted); font-weight:600; font-size:14px;
    }
    .menu a:hover{color:var(--text)}
    .cta{
      display:flex; gap:10px; align-items:center;
    }
    .btn{
      border:1px solid var(--line);
      background:#fff;
      padding:10px 12px;
      border-radius:12px;
      font-weight:700;
      font-size:14px;
      cursor:pointer;
    }
    .btn.primary{
      background:var(--blue);
      border-color:var(--blue);
      color:#fff;
      box-shadow: 0 10px 20px rgba(11,91,211,.25);
    }
    /* hero */
    .hero{
      padding:38px 0 26px;
      background:linear-gradient(180deg, #ffffff 0%, var(--bg) 70%);
    }
    .hero-grid{
      display:grid;
      grid-template-columns: 1.1fr .9fr;
      gap:26px;
      align-items:center;
    }
    .badge{
      display:inline-flex; align-items:center; gap:8px;
      background:#eef6ff;
      color:var(--blue2);
      border:1px solid #dbeafe;
      padding:8px 10px;
      border-radius:999px;
      font-weight:800;
      font-size:13px;
    }
    h1{
      margin:14px 0 10px;
      font-size:40px;
      line-height:1.15;
      letter-spacing:-.6px;
    }
    .sub{
      margin:0 0 18px;
      color:var(--muted);
      font-size:16px;
    }
    .hero-actions{display:flex; gap:10px; flex-wrap:wrap;}
    .note{
      margin-top:14px;
      font-size:13px;
      color:var(--muted);
    }
    /* phone mock */
    .phone{
      width:100%;
      max-width:420px;
      margin-left:auto;
      border-radius:28px;
      background:linear-gradient(180deg, #0b5bd3, #0a3f96);
      padding:18px;
      box-shadow: var(--shadow);
      position:relative;
    }
    .phone-inner{
      background:#fff;
      border-radius:22px;
      padding:18px;
      min-height:360px;
      display:flex;
      align-items:center;
      justify-content:center;
      text-align:center;
      position:relative;
      overflow:hidden;
    }
    .check{
      width:52px; height:52px; border-radius:999px;
      background:#22c55e;
      color:#fff;
      display:grid; place-items:center;
      font-weight:900;
      font-size:26px;
      margin:0 auto 12px;
      box-shadow: 0 10px 20px rgba(34,197,94,.25);
    }
    /* sections */
    section{padding:30px 0;}
    .section-title{
      font-size:22px;
      font-weight:900;
      margin:0 0 12px;
      letter-spacing:-.3px;
    }
    .section-sub{margin:0 0 18px; color:var(--muted); font-size:14px;}
    .grid-4{
      display:grid;
      grid-template-columns: repeat(4, 1fr);
      gap:14px;
    }
    .card{
      background:var(--card);
      border:1px solid var(--line);
      border-radius:var(--radius);
      padding:16px;
      box-shadow: 0 6px 18px rgba(2,6,23,.06);
    }
    .icon{
      width:44px; height:44px; border-radius:14px;
      display:grid; place-items:center;
      background:#f1f5f9;
      font-weight:900;
    }
    .card h3{margin:10px 0 6px; font-size:15px;}
    .card p{margin:0; color:var(--muted); font-size:13px;}
    .pill{
      display:inline-block;
      margin-top:10px;
      padding:6px 10px;
      border-radius:999px;
      background:#f8fafc;
      border:1px solid var(--line);
      font-size:12px;
      color:var(--muted);
      font-weight:700;
    }
    /* live status */
    .blue-band{
      background:linear-gradient(180deg, var(--blue), #083b86);
      color:#fff;
      border-radius:24px;
      padding:22px;
      box-shadow: var(--shadow);
    }
    table{
      width:100%;
      border-collapse:separate;
      border-spacing:0;
      overflow:hidden;
      background:rgba(255,255,255,.06);
      border:1px solid rgba(255,255,255,.18);
      border-radius:18px;
    }
    th, td{
      padding:12px 14px;
      font-size:13px;
      text-align:left;
      border-bottom:1px solid rgba(255,255,255,.12);
      color:#eaf2ff;
    }
    th{color:#ffffff; opacity:.9; font-size:12px; letter-spacing:.2px;}
    tr:last-child td{border-bottom:none;}
    .status{
      display:inline-flex; align-items:center; gap:8px;
      padding:7px 10px;
      border-radius:999px;
      background:rgba(255,255,255,.16);
      border:1px solid rgba(255,255,255,.22);
      font-weight:800;
      color:#fff;
      font-size:12px;
    }
    .dot{
      width:8px; height:8px; border-radius:999px;
      background:#22c55e;
      box-shadow: 0 0 0 4px rgba(34,197,94,.18);
    }
    /* reviews */
    .grid-2{display:grid; grid-template-columns:repeat(2, 1fr); gap:14px;}
    .avatar{
      width:34px; height:34px; border-radius:999px;
      background:#e2e8f0;
      display:grid; place-items:center;
      font-weight:900;
      margin-right:10px;
    }
    .review-head{display:flex; align-items:center; margin-bottom:8px;}
    .who{font-weight:900; font-size:14px;}
    .meta{color:var(--muted); font-size:12px; margin-left:8px;}
    .review-text{color:#334155; font-size:13px; margin:0;}
    /* faq */
    details{
      background:#fff;
      border:1px solid var(--line);
      border-radius:16px;
      padding:12px 14px;
    }
    details + details{margin-top:10px;}
    summary{
      cursor:pointer;
      font-weight:900;
      list-style:none;
    }
    summary::-webkit-details-marker{display:none;}
    .faq-a{margin:8px 0 0; color:var(--muted); font-size:13px;}
    /* footer + sticky */
    footer{
      padding:26px 0 76px;
      color:var(--muted);
      font-size:12px;
    }
    .sticky{
      position:fixed; left:0; right:0; bottom:0; z-index:60;
      background:#0b1220;
      color:#fff;
      padding:10px 12px;
      display:flex;
      gap:10px;
      align-items:center;
      justify-content:center;
      border-top:1px solid rgba(255,255,255,.12);
    }
    .sticky .sbtn{
      flex:1;
      max-width:520px;
      display:flex;
      gap:10px;
      justify-content:space-between;
      align-items:center;
      padding:12px 14px;
      border-radius:14px;
      background:rgba(255,255,255,.08);
      border:1px solid rgba(255,255,255,.16);
      font-weight:900;
    }
    .sticky .kakao{
      background:var(--yellow);
      color:#0b1220;
      border-color:rgba(0,0,0,.06);
    }
    .sticky small{font-weight:700; opacity:.85}
    /* responsive */
    @media (max-width: 920px){
      .hero-grid{grid-template-columns:1fr; }
      .phone{margin: 10px auto 0;}
      h1{font-size:34px;}
      .grid-4{grid-template-columns:repeat(2, 1fr);}
      .grid-2{grid-template-columns:1fr;}
      .menu{display:none;}
    }
    @media (max-width: 420px){
      h1{font-size:30px;}
      .grid-4{grid-template-columns:1fr;}
    }
  </style>
</head>
<body>
<header>
  <div class="wrap">
    <div class="nav">
      <div class="brand">
        <div class="logo" aria-hidden="true"></div>
        <div>MONEY PICKS</div>
      </div>

      <nav class="menu" aria-label="메인 메뉴">
        <a href="#about">서비스소개</a>
        <a href="#products">상품</a>
        <a href="#how">신청방법</a>
        <a href="#faq">FAQ</a>
      </nav>

      <div class="cta">
        <button class="btn" onclick="scrollToId('products')">상품 보기</button>
        <button class="btn primary" onclick="openKakao()">카톡 상담</button>
      </div>
    </div>
  </div>
</header>

<main>
  <div class="hero" id="about">
    <div class="wrap">
      <div class="hero-grid">
        <div>
          <div class="badge">✅ 24시간 상담 · 간편 진행</div>
          <h1>급한 돈 필요하다면<br/>지금 즉시 상담 가능</h1>
          <p class="sub">
            복잡한 서류 준비 없이, 카톡 상담으로 빠르게 진행하세요.<br/>
            상황에 맞는 옵션을 안내해드립니다.
          </p>

          <div class="hero-actions">
            <button class="btn primary" onclick="openKakao()">카톡으로 바로 상담</button>
            <button class="btn" onclick="scrollToId('how')">진행 방법 보기</button>
          </div>

          <div class="note">
            ※ 안내 내용은 예시이며, 실제 조건(한도/금리/기간)은 개인 신용 및 금융사 심사에 따라 달라질 수 있습니다.
          </div>
        </div>

        <div class="phone" aria-label="휴대폰 예시">
          <div class="phone-inner">
            <div>
              <div class="check">✓</div>
              <div style="font-weight:900; font-size:16px; margin-bottom:6px;">상담 접수가 완료되었습니다</div>
              <div style="color:#64748b; font-size:13px;">
                담당자가 확인 후 빠르게 안내드릴게요.<br/>
                (평균 응답 5~10분)
              </div>
              <div style="margin-top:14px; display:flex; gap:10px; justify-content:center; flex-wrap:wrap;">
                <span class="pill">간편 상담</span>
                <span class="pill">맞춤 안내</span>
                <span class="pill">빠른 진행</span>
              </div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </div>

  <section id="products">
    <div class="wrap">
      <div class="section-title">상품 안내</div>
      <p class="section-sub">상황에 맞는 옵션을 빠르게 안내합니다.</p>

      <div class="grid-4">
        <div class="card">
          <div class="icon">📱</div>
          <h3>휴대폰 한도대출</h3>
          <p>소액부터 빠르게 진행 가능한 옵션을 안내합니다.</p>
          <span class="pill">상담 후 가능여부 확인</span>
        </div>
        <div class="card">
          <div class="icon">💳</div>
          <h3>신용카드 한도대출</h3>
          <p>카드 이용내역 기반으로 맞춤 안내를 제공합니다.</p>
          <span class="pill">간단 확인</span>
        </div>
        <div class="card">
          <div class="icon">🎁</div>
          <h3>각종 상품권 매입</h3>
          <p>보유 상품권 종류에 따라 진행 가능 여부를 안내합니다.</p>
          <span class="pill">종류별 상이</span>
        </div>
        <div class="card">
          <div class="icon">➕</div>
          <h3>추가 신용 상담</h3>
          <p>신용점수가 낮아도 가능한 대안을 함께 검토합니다.</p>
          <span class="pill">맞춤형 대안</span>
        </div>
      </div>
    </div>
  </section>

  <section id="how">
    <div class="wrap">
      <div class="section-title">신청 방법</div>
      <p class="section-sub">3단계로 간단하게 진행됩니다.</p>

      <div class="grid-4">
        <div class="card">
          <div class="icon">1</div>
          <h3>카톡 상담 접수</h3>
          <p>필요 금액/상황을 알려주면 됩니다.</p>
        </div>
        <div class="card">
          <div class="icon">2</div>
          <h3>가능 옵션 안내</h3>
          <p>조건에 맞는 상품/절차를 안내합니다.</p>
        </div>
        <div class="card">
          <div class="icon">3</div>
          <h3>진행 및 확인</h3>
          <p>필요 서류/절차를 최소화해 진행합니다.</p>
        </div>
        <div class="card">
          <div class="icon">⏱</div>
          <h3>빠른 응답</h3>
          <p>평균 응답 5~10분 (시간대에 따라 변동)</p>
        </div>
      </div>
    </div>
  </section>

  <section>
    <div class="wrap">
      <div class="blue-band">
        <div style="font-weight:900; font-size:18px; margin-bottom:6px;">실시간 진행현황</div>
        <div style="opacity:.9; font-size:13px; margin-bottom:14px;">
          금일 문의 및 진행 예시(샘플)입니다. 실제 개인정보는 노출하지 않습니다.
        </div>

        <table aria-label="진행 현황 테이블">
          <thead>
            <tr>
              <th>이름</th>
              <th>문의금액</th>
              <th>신청일</th>
              <th>소요시간</th>
              <th>진행상태</th>
            </tr>
          </thead>
          <tbody id="liveRows">
            <tr>
              <td>김**</td><td>800,000원</td><td>2026-01-20</td><td>09분</td>
              <td><span class="status"><span class="dot"></span>진행중</span></td>
            </tr>
            <tr>
              <td>이**</td><td>2,000,000원</td><td>2026-01-20</td><td>06분</td>
              <td><span class="status"><span class="dot"></span>진행중</span></td>
            </tr>
            <tr>
              <td>박**</td><td>500,000원</td><td>2026-01-20</td><td>08분</td>
              <td><span class="status"><span class="dot"></span>진행중</span></td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </section>

  <section>
    <div class="wrap">
      <div class="section-title">이용고객 후기</div>
      <p class="section-sub">실제 고객 후기를 바탕으로 구성(예시 텍스트)</p>

      <div class="grid-2">
        <div class="card">
          <div class="review-head">
            <div class="avatar">🧑</div>
            <div>
              <div><span class="who">이**</span><span class="meta">/ 21</span></div>
              <div class="meta">카톡 상담</div>
            </div>
          </div>
          <p class="review-text">처음엔 걱정했는데 안내가 친절해서 진행이 편했습니다. 질문에도 빠르게 답해주셨어요.</p>
        </div>
        <div class="card">
          <div class="review-head">
            <div class="avatar">👩</div>
            <div>
              <div><span class="who">정**</span><span class="meta">/ 24</span></div>
              <div class="meta">비상금 상담</div>
            </div>
          </div>
          <p class="review-text">조건 설명을 깔끔하게 해줘서 이해가 쉬웠고, 필요한 것만 안내해줘서 좋았습니다.</p>
        </div>
        <div class="card">
          <div class="review-head">
            <div class="avatar">🧔</div>
            <div>
              <div><span class="who">강**</span><span class="meta">/ 26</span></div>
              <div class="meta">상품권 상담</div>
            </div>
          </div>
          <p class="review-text">진행 절차가 생각보다 간단했습니다. 응답도 빨라서 급할 때 도움 됐어요.</p>
        </div>
        <div class="card">
          <div class="review-head">
            <div class="avatar">🧑‍🦱</div>
            <div>
              <div><span class="who">황**</span><span class="meta">/ 19</span></div>
              <div class="meta">추가 신용</div>
            </div>
          </div>
          <p class="review-text">대안까지 같이 비교해줘서 선택하기 편했어요. 부담 없이 상담받을 수 있었습니다.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="faq">
    <div class="wrap">
      <div class="section-title">FAQ</div>
      <p class="section-sub">자주 묻는 질문</p>

      <details>
        <summary>상담은 무료인가요?</summary>
        <p class="faq-a">네, 상담은 무료입니다. 진행 여부는 안내 후 고객님이 결정하시면 됩니다.</p>
      </details>
      <details>
        <summary>당일 진행이 가능한가요?</summary>
        <p class="faq-a">상황/시간대/금융사 심사에 따라 달라질 수 있으나, 가능한 빠르게 안내드립니다.</p>
      </details>
      <details>
        <summary>신용점수가 낮아도 가능한가요?</summary>
        <p class="faq-a">개인 상황에 따라 대안 옵션이 있을 수 있어요. 정확한 건 상담으로 확인이 필요합니다.</p>
      </details>
      <details>
        <summary>개인정보는 안전한가요?</summary>
        <p class="faq-a">필수 정보만 요청하며, 안내 목적 외 사용하지 않도록 운영 정책을 명확히 고지하세요.</p>
      </details>
    </div>
  </section>

  <footer>
    <div class="wrap">
      <div style="font-weight:900; margin-bottom:6px;">고지</div>
      <div>본 페이지는 상담 안내용 예시 템플릿입니다. 실제 대출 상품 안내 시 관련 법령/광고 심의/고지 의무를 준수해야 합니다.</div>
      <div style="margin-top:10px;">
        상호: (회사명) · 대표: (대표자) · 사업자번호: (000-00-00000)<br/>
        주소: (주소) · 문의: <a href="tel:01000000000">010-0000-0000</a> · 카카오톡: (채널명)
      </div>
    </div>
  </footer>
</main>

<div class="sticky">
  <a class="sbtn" href="tel:01000000000">
    <span>📞 전화 상담</span>
    <small>010-0000-0000</small>
  </a>
  <button class="sbtn kakao" onclick="openKakao()">
    <span>💬 카톡 상담</span>
    <small>바로 연결</small>
  </button>
</div>

<script>
  function scrollToId(id){
    const el = document.getElementById(id);
    if(!el) return;
    el.scrollIntoView({behavior:'smooth', block:'start'});
  }
  // TODO: 여기 카카오 채널 링크로 변경하세요.
  function openKakao(){
    // 예시: 카카오 채널/오픈채팅 링크로 변경
    window.open("https://open.kakao.com/o/xxxxxxxx", "_blank");
  }

  // "실시간 진행현황" 느낌 내기용(샘플 row 자동 추가)
  const names = ["최**","윤**","송**","한**","오**","신**"];
  const amounts = ["300,000원","700,000원","1,200,000원","1,500,000원","2,500,000원"];
  function addRow(){
    const tbody = document.getElementById("liveRows");
    const n = names[Math.floor(Math.random()*names.length)];
    const a = amounts[Math.floor(Math.random()*amounts.length)];
    const d = new Date();
    const yyyy = d.getFullYear();
    const mm = String(d.getMonth()+1).padStart(2,"0");
    const dd = String(d.getDate()).padStart(2,"0");
    const mins = String(4 + Math.floor(Math.random()*8)).padStart(2,"0");

    const tr = document.createElement("tr");
    tr.innerHTML = `
      <td>${n}</td><td>${a}</td><td>${yyyy}-${mm}-${dd}</td><td>${mins}분</td>
      <td><span class="status"><span class="dot"></span>진행중</span></td>
    `;
    tbody.prepend(tr);
    // 너무 많아지면 삭제
    while(tbody.children.length > 6) tbody.removeChild(tbody.lastElementChild);
  }
  setInterval(addRow, 6000);
</script>
</body>
</html>
