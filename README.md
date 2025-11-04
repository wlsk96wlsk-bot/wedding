<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Taegeun & Yeonsu Wedding Invitation</title>

  <!-- Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Noto+Sans+KR:wght@400;500&display=swap" rel="stylesheet">

  <style>
    body {
      margin: 0;
      background-color: #faf6f3;
      color: #333;
      font-family: 'Noto Sans KR', sans-serif;
      overflow-x: hidden;
    }
    section {
      text-align: center;
      padding: 60px 20px;
    }
    h1, h2, h3 {
      margin: 0 0 20px;
    }

    /* 메인 슬라이드 */
    .slideshow {
      position: relative;
      height: 90vh;
      overflow: hidden;
    }
    .slide {
      position: absolute;
      width: 100%;
      height: 100%;
      opacity: 0;
      transition: opacity 1.5s ease;
      background-size: cover;
      background-position: center;
    }
    .slide.active { opacity: 1; }
    .slide-text {
      position: absolute;
      bottom: 15%;
      width: 100%;
      text-align: center;
      color: white;
      font-family: 'Dancing Script', cursive;
      font-size: 2.3em;
      text-shadow: 0 2px 10px rgba(0,0,0,0.3);
      opacity: 0;
      transform: translateY(20px);
      transition: all 1s ease;
    }
    .slide.active .slide-text {
      opacity: 1;
      transform: translateY(0);
    }

    /* D-day */
    .countdown {
      font-size: 1.3em;
      margin: 10px 0;
      color: #555;
    }
    .time-box {
      display: inline-block;
      margin: 10px;
      font-size: 1.1em;
    }

 /* 인사말 */
    .intro { line-height: 1.8; color: #444; }

    /* 달력 */
    .calendar { display: inline-block; border-collapse: collapse; margin-top: 30px; }
    .calendar th, .calendar td { padding: 10px 12px; text-align: center; }
    .calendar th { color: #ebcfc4; font-weight: 500; }
    .calendar td { color: #333; }
    .highlight { background-color: #ebcfc4; color: white; border-radius: 50%; }

    /* 사진 앨범 */
    .photo-album {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 15px;
      margin-top: 30px;
    }
    .photo-album img {
      width: 100%;
      border-radius: 10px;
      box-shadow: 0 3px 8px rgba(0,0,0,0.2);
    }

    /* 가족 소개 */
    .family p { margin: 10px 0; }
    .phone { cursor: pointer; font-size: 1.1em; color: #ebcfc4; }

    /* 지도 및 오시는 길 */
    iframe {
      border: none;
      width: 100%;
      height: 300px;
      border-radius: 10px;
    }
    .map-buttons {
      margin-top: 20px;
    }
    .map-buttons a {
      display: inline-block;
      background-color: #ebcfc4;
      color: white;
      padding: 8px 14px;
      border-radius: 6px;
      margin: 5px;
      text-decoration: none;
      font-size: 0.9em;
    }

    /* 방명록 */
    .guestbook {
      text-align: left;
      max-width: 400px;
      margin: 0 auto;
    }
    textarea {
      width: 100%;
      height: 80px;
      border: 1px solid #ccc;
      border-radius: 8px;
      padding: 8px;
      margin-bottom: 10px;
      font-family: 'Noto Sans KR', sans-serif;
    }
    .submit-btn {
      background-color: #ebcfc4;
      color: white;
      border: none;
      border-radius: 8px;
      padding: 10px 16px;
      cursor: pointer;
    }

    /* 마음 전할 곳 */
    .accounts {
      display: flex;
      justify-content: center;
      gap: 15px;
      flex-wrap: wrap;
      margin-top: 20px;
    }
    .account {
      background-color: #fff;
      border-radius: 10px;
      padding: 15px 20px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
      min-width: 160px;
    }
    .copy-btn {
      margin-top: 8px;
      padding: 6px 12px;
      background-color: #ebcfc4;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      font-size: 0.9em;
    }

    /* 음악 버튼 */
    .music-btn {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background-color: #ebcfc4;
      color: white;
      border: none;
      border-radius: 50%;
      width: 50px;
      height: 50px;
      font-size: 1.3em;
      cursor: pointer;
      box-shadow: 0 3px 8px rgba(0,0,0,0.2);
    }
  </style>
</head>

<body>

  <!-- 메인 슬라이드 -->
  <div class="slideshow">
  <div class="slide active" style="background-image: url('메인1.jpg');">
    <div class="slide-text">Taegeun & Yeonsu</div>
  </div>
  <div class="slide" style="background-image: url('메인2.jpg');">
    <div class="slide-text">We are getting married</div>
  </div>
  <div class="slide" style="background-image: url('메인3.jpg');">
    <div class="slide-text">2026.01.25 · Uijeongbu Wedding Palace</div>
  </div>
  </div>

  <!-- D-day -->
  <section>
    <h2>태근 • 연수 결혼식</h2>
    <div id="countdown" class="countdown"></div>
  </section>

<!-- 사진 1장 -->
    <div class="countdown-photo">
      <img src="C:\Users\USER\OneDrive\바탕 화면\wedding_invite\커플사진1 (2).jpg" alt="커플사진">
    </div>
 </div>

  <!-- 인사말 -->
  <section>
    <p class="intro">서로의 마음을 하나로 모아<br>평생을 함께하려 합니다.<br>따뜻한 축복으로 저희의 시작을 함께해주세요.</p>
  </section>

  <!-- 달력 -->
  <section>
    <h2 style="color:#ebcfc4;">1월</h2>
    <table class="calendar" id="calendar"></table>
  </section>

<!-- 사진 앨범 6장 -->
    <div class="photo-album">
      <img src="C:\Users\USER\OneDrive\바탕 화면\wedding_invite\커플사진2.jpg" alt="커플사진1">
      <img src="‪C:\Users\USER\OneDrive\바탕 화면\wedding_invite\커플사진3.jpg" alt="커플사진2">
      <img src="C:\Users\USER\OneDrive\바탕 화면\wedding_invite\커플사진4.jpg" alt="커플사진3">
      <img src="C:\Users\USER\OneDrive\바탕 화면\wedding_invite\커플사진5.jpg" alt="커플사진4">
      <img src="C:\Users\USER\OneDrive\바탕 화면\wedding_invite\커플사진6.jpg" alt="커플사진5">
      <img src="‪C:\Users\USER\OneDrive\바탕 화면\wedding_invite\커플사진7.jpg" alt="커플사진6">
    </div>
  </section>

  <!-- 가족 소개 -->
  <section class="family">
    <p><strong>장경수 · 신현숙</strong>의 아들 <span>태근</span> <a href="tel:010-1234-5678" class="phone">📞</a></p>
    <p><strong>한상근 · 이현지</strong>의 딸 <span>연수</span> <a href="tel:010-9876-5432" class="phone">📞</a></p>
  </section>

  <!-- 오시는 길 -->
  <section>
    <h2 style="color:#ebcfc4;">오시는 길</h2>
    <p>경기 의정부시 시민로 70<br>의정부 웨딩팰리스</p>
    <p>문의 : 031-837-0101</p>
    <iframe src="http://www.w3.org/1999/xhtml"></iframe>

    <div class="map-buttons">
      <a href="https://map.naver.com/v5/search/의정부웨딩팰리스" target="_blank">네이버지도</a>
      <a href="https://map.kakao.com/link/search/의정부웨딩팰리스" target="_blank">카카오맵</a>
      <a href="https://tmap.co.kr/tmap/?searchKeyword=의정부웨딩팰리스" target="_blank">T맵</a>
    </div>
  </section>

  <!-- 대중교통 안내 -->
  <section>
    <h2 style="color:#ebcfc4;">대중교통 안내</h2>
    <p><strong>지하철:</strong> 1호선 의정부역 하차 → 2번출구 시청 방면 도보 1분</p>
    <p><strong>시내버스:</strong> 1, 2, 3, 5, 8, 21, 23, 25, 33, 39, 50, 51, 55 </p>
    <p><strong>마을버스:</strong> 201, 202-1, 206-2, 207, 208 </p>
    <p><strong>경전철:</strong> 의정부경전철 의정부역 하차 → 1번 출구 도보 1분 </p>
  </section>

  <!-- 방명록 -->
  <section>
    <h2 style="color:#ebcfc4;">방명록</h2>
    <div class="guestbook">
      <textarea id="guestMsg" placeholder="축하 메시지를 남겨주세요"></textarea>
      <button class="submit-btn" onclick="saveMessage()">남기기</button>
      <div id="guestList"></div>
    </div>
  </section>

  <!-- 마음 전할 곳 -->
  <section>
    <h2 style="color:#ebcfc4;">마음 전할 곳</h2>
    <div class="accounts">
      <div class="account">
        <h4>신랑측</h4>
        <p>국민 123456-78-987654<br>장태근</p>
        <button class="copy-btn" onclick="copyText('국민 123456-78-987654')">계좌 복사</button>
      </div>
      <div class="account">
        <h4>신부측</h4>
        <p>신한 987654-32-123456<br>한연수</p>
        <button class="copy-btn" onclick="copyText('신한 987654-32-123456')">계좌 복사</button>
      </div>
    </div>
  </section>

  <!-- 음악 버튼 -->
  <button class="music-btn" id="musicToggle">🎵</button>
  <audio id="bgMusic" loop>
    <source src="https://files.freemusicarchive.org/storage-freemusicarchive-org/music/no_curator/Kevin_MacLeod/Tenderness/Kevin_MacLeod_-_Tenderness.mp3" type="audio/mpeg">
  </audio>

  <script>
    /* 슬라이드 */
    const slides = document.querySelectorAll('.slide');
    let currentSlide = 0;
    setInterval(() => {
      slides[currentSlide].classList.remove('active');
      currentSlide = (currentSlide + 1) % slides.length;
      slides[currentSlide].classList.add('active');
    }, 4000);

    /* D-day 카운트다운 */
    const targetDate = new Date("2026-01-25T11:00:00");
    const countdown = document.getElementById("countdown");

    function updateCountdown() {
      const now = new Date();
      const diff = targetDate - now;

      if (diff <= 0) {
        countdown.innerHTML = "오늘, 두 사람이 하나됩니다 💕";
        return;
      }

      const days = Math.floor(diff / (1000*60*60*24));
      const hours = Math.floor((diff / (1000*60*60)) % 24);
      const mins = Math.floor((diff / (1000*60)) % 60);
      const secs = Math.floor((diff / 1000) % 60);

      countdown.innerHTML = `
        <div>${days}일 ${hours}시간 ${mins}분 ${secs}초 남았습니다</div>
      `;
    }
    setInterval(updateCountdown, 1000);

    /* 달력 생성 */
    function createCalendar() {
      const calendar = document.getElementById('calendar');
      const weeks = ['일','월','화','수','목','금','토'];
      let html = '<tr>' + weeks.map(w => `<th>${w}</th>`).join('') + '</tr>';
      const year = 2026, month = 0;
      const firstDay = new Date(year, month, 1).getDay();
      const lastDate = new Date(year, month+1, 0).getDate();
      let day = 1;
      for (let i=0; i<6; i++) {
        html += '<tr>';
        for (let j=0; j<7; j++) {
          if (i===0 && j<firstDay || day>lastDate) html += '<td></td>';
          else {
            const highlight = (day===25) ? 'highlight' : '';
            html += `<td class="${highlight}">${day}</td>`;
            day++;
          }
        }
        html += '</tr>';
      }
      calendar.innerHTML = html;
    }
    createCalendar();

    /* 방명록 저장 */
    function saveMessage() {
      const msg = document.getElementById('guestMsg').value.trim();
      if (!msg) return;
      const list = document.getElementById('guestList');
      const div = document.createElement('div');
      div.textContent = msg;
      list.prepend(div);
      document.getElementById('guestMsg').value = '';
    }

    /* 계좌 복사 */
    function copyText(text) {
      navigator.clipboard.writeText(text);
      alert('계좌번호가 복사되었습니다.');
    }

    /* 음악 */
    const music = document.getElementById('bgMusic');
    const btn = document.getElementById('musicToggle');
    let playing = false;
    btn.addEventListener('click', () => {
      if (!playing) { music.play(); playing = true; btn.textContent = '⏸️'; }
      else { music.pause(); playing = false; btn.textContent = '🎵'; }
    });
  </script>

</body>
</html>
