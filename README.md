<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>장태근 & 한연수 결혼식 초대</title>

<!-- 폰트 -->
<link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@500;600&display=swap" rel="stylesheet">
<link href="https://webfontworld.github.io/cafe24/Cafe24SsurroundAir.css" rel="stylesheet">

<style>
/* ===== 기본 설정 ===== */
body { margin:0; padding:0; font-family:'Cafe24SsurroundAir', sans-serif; background:#fefaf8; color:#3a3a3a; text-align:center; }
section { margin:60px 0; padding:0 20px; }
h2 { font-size:1.6em; color:#e4b7b7; margin-bottom:20px; font-weight:600; }
.fade-in { opacity:0; transform:translateY(30px); transition: all 1s ease; }
.fade-in.visible { opacity:1; transform:translateY(0); }

/* ===== 하트 애니메이션 ===== */
.heart { position:fixed; color:#EBCFC4; font-size:1.2rem; opacity:0.8; animation: floatUp 6s linear infinite; z-index:0; }
@keyframes floatUp { 0% { transform:translateY(0) scale(1); opacity:1; } 100% { transform:translateY(-100vh) scale(1.5); opacity:0; } }

/* ===== 메인 슬라이드 ===== */
.slider { position:relative; width:100%; height:90vh; overflow:hidden; }
.slider img { width:100%; height:100%; object-fit:cover; position:absolute; top:0; left:0; opacity:0; transition: opacity 1.2s ease; }
.slider img.active { opacity:1; }
.main-text { position:absolute; bottom:10%; width:100%; text-align:center; color:white; font-family:'Dancing Script', cursive; font-size:2.5em; text-shadow:0 2px 10px rgba(0,0,0,0.4); transition:all 1.2s ease; }

/* ===== 중간 사진 & 앨범 ===== */
.middle-photo img, .album img { width:100%; border-radius:12px; max-width:600px; margin:auto; display:block; transition: transform .3s; }
.album { display:grid; grid-template-columns:repeat(2,1fr); gap:8px; padding:10px; }
.album img:hover { transform: scale(1.03); }

/* ===== 달력 ===== */
.calendar { display:grid; grid-template-columns:repeat(7,1fr); max-width:320px; margin:0 auto; gap:8px; justify-items:center; }
.calendar div { padding:10px 0; font-size:15px; color:#444; width:36px; text-align:center; }
.heart-day { position:relative; width:36px; height:32px; }
.heart-day::before { content:"❤"; position:absolute; top:50%; left:50%; transform:translate(-50%,-50%); color:#EBCFC4; font-size:34px; z-index:1; }
.heart-day span { position:absolute; top:50%; left:50%; transform:translate(-50%,-52%); color:#fff; font-weight:600; font-size:14px; z-index:2; }

/* ===== 가족 & 연락 ===== */
.call-btn { color:#EBCFC4; text-decoration:none; font-size:1.1em; }

/* ===== 오시는 길 ===== */
.map { width:100%; max-width:360px; height:260px; margin:1em auto; border-radius:10px; overflow:hidden; }

/* ===== 버튼 ===== */
.btn { background:#EBCFC4; color:#fff; padding:10px 20px; border-radius:25px; text-decoration:none; font-size:0.9em; margin:5px; display:inline-block; cursor:pointer; transition:0.3s; }
.btn:hover { background:#f3dcd4; }

/* ===== 마음 전할 곳 ===== */
#account button { background:#EBCFC4; border:none; color:#fff; padding:10px 16px; border-radius:10px; cursor:pointer; font-size:0.9rem; transition:0.3s; }
#account button:hover { background:#f3dcd4; transform:scale(1.03); }

/* ===== 방명록 ===== */
#guestbookMessages div { background:#fff7f8; padding:14px 16px; border-radius:12px; margin-bottom:10px; box-shadow:0 1px 6px rgba(0,0,0,0.05); }
#guestbookMessages strong { color:#EBCFC4; font-weight:600; display:block; margin-bottom:5px; }

/* ===== BGM 버튼 ===== */
#music-btn { position:fixed; top:16px; right:16px; background:rgba(255,255,255,0.9); border:none; border-radius:50%; width:44px; height:44px; font-size:20px; cursor:pointer; box-shadow:0 2px 8px rgba(0,0,0,0.15); z-index:100; }

/* ===== 반응형 ===== */
@media(max-width:480px){ .main-text{ font-size:9vw; bottom:12%; } .album{ grid-template-columns:1fr 1fr; } }
</style>
</head>
<body>

<!-- 하트 애니메이션 -->
<script>
function createHeart(){
  const heart=document.createElement('div');
  heart.className='heart';
  heart.style.left=Math.random()*100+'vw';
  heart.style.animationDuration=(4+Math.random()*3)+'s';
  heart.innerHTML='💗';
  document.body.appendChild(heart);
  setTimeout(()=>heart.remove(),7000);
}
setInterval(createHeart,800);
</script>

<!-- 메인 슬라이드 -->
<div class="slider fade-in">
  <img src="메인1.jpg" class="active">
  <img src="메인2.jpg">
  <img src="메인3.jpg">
  <div class="main-text" id="mainText">Jan Teageun & Han Yean-su</div>
</div>

<!-- 카운트다운 -->
<section class="fade-in">
  <h2>Wedding Countdown</h2>
  <div id="countdown"></div>
</section>

<!-- 중간 사진 -->
<section class="fade-in middle-photo">
  <img src="커플사진1.jpg">
</section>

<!-- 달력 -->
<section class="fade-in calendar-section">
  <h2>1월</h2>
  <div class="calendar">
    <div>일</div><div>월</div><div>화</div><div>수</div><div>목</div><div>금</div><div>토</div>
    <div></div><div></div><div></div><div></div><div>1</div><div>2</div><div>3</div>
    <div>4</div><div>5</div><div>6</div><div>7</div><div>8</div><div>9</div><div>10</div>
    <div>11</div><div>12</div><div>13</div><div>14</div><div>15</div><div>16</div><div>17</div>
    <div>18</div><div>19</div><div>20</div><div>21</div><div>22</div><div>23</div><div>24</div>
    <div class="heart-day"><span>25</span></div>
    <div>26</div><div>27</div><div>28</div><div>29</div><div>30</div><div>31</div>
  </div>
</section>

<!-- 앨범 -->
<section class="fade-in">
  <h2>Album</h2>
  <div class="album">
  <img src="커플사진2.jpg"><img src="커플사진3.jpg">
    <img src="커플사진4.jpg"><img src="커플사진5.jpg">
    <img src="커플사진6.jpg"><img src="커플사진7.jpg">
  </div>
</section>

<!-- 가족 -->
<section class="fade-in">
  <h2>Our Family</h2>
  <p>장경수 / 신현숙의 아들 <b>태근</b> <a href="tel:010-0000-0000" class="call-btn">📞</a></p>
  <p>한상근 / 이현지의 딸 <b>연수</b> <a href="tel:010-0000-0000" class="call-btn">📞</a></p>
</section>

<!-- 오시는 길 -->
<section class="fade-in">
  <h2 style="color:#EBCFC4;">오시는 길</h2>
  <p>경기 의정부시 시민로 70, 의정부 웨딩팰리스</p>
  <p>문의 031-837-0101</p>
  <iframe class="map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3155.2178040318595!2d127.04028137457112!3d37.73803421427772!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x357cc735a7b9f213%3A0xfd65a43762c6d1fd!2z7Juo65Sp7Yyw66as7Iqk!5e0!3m2!1sko!2skr!4v1762446158857!5m2!1sko!2skr" allowfullscreen="" loading="lazy"></iframe>
  <div style="margin-top:20px; display:flex; justify-content:center; gap:10px;">
    <a href="#" class="btn">카카오맵</a>
    <a href="#" class="btn">T맵</a>
    <a href="#" class="btn">네이버지도</a>
  </div>

<!-- 교통 안내 -->
  <div style="margin-top:35px;">
    <h3 style="color:#EBCFC4; font-size:1.1rem; font-weight:600;">교통 안내</h3>
    <p style="margin-top:12px; line-height:1.6; font-size:0.95rem;">
      🚇 <strong>지하철:</strong> 1호선 의정부역 2번 출구 도보 5분<br>
      🚉 <strong>경전철:</strong> 경전철 의정부역 1번<br>
      🚌 <strong>버스:</strong> 의정부 시청 앞 하차 후 도보 3분
    </p>
  </div>
</section>

<!-- 마음 전할 곳 -->
<section id="account" class="fade-in">
  <h2 style="color:#EBCFC4; font-size:1.6rem; font-weight:600;">마음 전할 곳</h2>
  <p style="color:#777; margin:12px 0 35px; font-size:0.95rem;">두 사람의 새로운 시작을 따뜻한 마음으로 축복해 주세요.</p>

   <div style="display:flex; flex-direction:column; gap:25px; max-width:400px; margin:0 auto;">
    <div>
    <div style="background:#fff; padding:25px; border-radius:18px; box-shadow:0 2px 10px rgba(0,0,0,0.05);">
      <h3 style="color:#EBCFC4;">🤵 신랑측</h3>
      <p>장태근 · 부모님 장경수 · 신현숙</p>
      <button onclick="copyAccount('신한은행 110-123-456789 장태근')">계좌 복사하기</button>
    </div>
<div style="background:#fff; padding:25px; border-radius:18px; box-shadow:0 2px 10px rgba(0,0,0,0.05);">
      <h3 style="color:#EBCFC4;">👰 신부측</h3>
      <p>한연수 · 부모님 한상근 · 이현지</p>
      <button onclick="copyAccount('국민은행 123-456-789012 한연수')">계좌 복사하기</button>
    </div>
  </div>
</section>

<!-- 방명록 -->
<section id="guestbook" class="fade-in">
  <h2 style="color:#EBCFC4;">방명록</h2>
  <p style="color:#777; margin:12px 0 35px;">축하의 한마디를 남겨주세요 ✨</p>

  <form id="guestbookForm" style="max-width:400px; margin:0 auto; display:flex; flex-direction:column; gap:12px;">
    <input type="text" id="name" placeholder="이름" required>
    <textarea id="message" placeholder="축하 메시지를 입력해주세요" required></textarea>
    <button type="submit">남기기</button>
  </form>
  <div id="guestbookMessages" style="margin-top:20px; max-width:400px; margin:auto; text-align:left;"></div>
</section>

<!-- BGM 버튼 -->
<button id="music-btn">🎵</button>
<audio id="bgm" loop preload="auto">
  <source src="C:\Users\USER\OneDrive\바탕 화면\wedding_invite\music.mp3.mp3" type="audio/mpeg">
</audio>

<script>
// ===== 하트 =====
function createHeart(){const heart=document.createElement('div');heart.className='heart';heart.style.left=Math.random()*100+'vw';heart.style.animationDuration=(4+Math.random()*3)+'s';heart.innerHTML='💗';document.body.appendChild(heart);setTimeout(()=>heart.remove(),7000);}
setInterval(createHeart,800);

// ===== DOMContentLoaded =====
document.addEventListener('DOMContentLoaded',()=>{

  // 슬라이드
  const slides=document.querySelectorAll('.slider img');
  const mainText=document.getElementById('mainText');
  let index=0;
  const texts=["Jan Teageun & <br>Han Yean-su","WE ARE GETTING MARRIED","2026.01.25 11:00<br>Wedding Palace"];
  setInterval(()=>{
    slides[index].classList.remove('active');
    index=(index+1)%slides.length;
    slides[index].classList.add('active');
    mainText.innerHTML=texts[index];
  },4000);

  // 카운트다운
  const countdownEl=document.getElementById('countdown');
  const weddingDate=new Date('2026-01-25T11:00:00');
  setInterval(()=>{
    const now=new Date();
    const diff=weddingDate-now;
    if(diff<0){countdownEl.innerHTML="오늘 결혼식!"; return;}
    const d=Math.floor(diff/1000/60/60/24);
    const h=Math.floor(diff/1000/60/60)%24;
    const m=Math.floor(diff/1000/60)%60;
    const s=Math.floor(diff/1000)%60;
    countdownEl.innerHTML=`${d}일 ${h}시간 ${m}분 ${s}초`;
  },1000);

  // fade-in
  const faders=document.querySelectorAll('.fade-in');
  const observer=new IntersectionObserver(entries=>{entries.forEach(entry=>{if(entry.isIntersecting) entry.target.classList.add('visible');});},{threshold:0.2});
  faders.forEach(f=>observer.observe(f));

  // 방명록
  const form=document.getElementById('guestbookForm');
  const messages=document.getElementById('guestbookMessages');
  // 기존 localStorage 불러오기
  let saved=JSON.parse(localStorage.getItem('guestbook'))||[];
  saved.forEach(g=>{const div=document.createElement('div');div.innerHTML=`<strong>${g.name}</strong><p>${g.message}</p>`;messages.prepend(div);});
  form.addEventListener('submit',e=>{
    e.preventDefault();
    const n=document.getElementById('name').value.trim();
    const m=document.getElementById('message').value.trim();
    if(n&&m){
      const div=document.createElement('div'); div.innerHTML=`<strong>${n}</strong><p>${m}</p>`; messages.prepend(div);
      saved.unshift({name:n,message:m}); localStorage.setItem('guestbook',JSON.stringify(saved));
      form.reset(); alert('방명록에 작성되었습니다!');
    }
  });

  // BGM
  const musicBtn=document.getElementById('music-btn');
  const bgm=document.getElementById('bgm');
  let playing=false;
  musicBtn.addEventListener('click',()=>{
    if(!playing){ bgm.play(); musicBtn.textContent="⏸️"; }
    else{ bgm.pause(); musicBtn.textContent="🎵"; }
    playing=!playing;
  });

});

// 계좌 복사
function copyAccount(){
  navigator.clipboard.writeText('123-456-7890').then(()=>{alert('계좌가 복사되었습니다!');});
}
</script>

</body>
</html>
