[index.html](https://github.com/user-attachments/files/30213054/index.html)
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>지선아 생일 축하해</title>

  <!-- confetti library -->
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.9.3/dist/confetti.browser.min.js"></script>

  <style>
    @import url('https://fonts.googleapis.com/css2?family=Gowun+Batang:wght@400;700&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;700&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Yeon+Sung&display=swap');

    body {
      background-color: #8ec6f5; 
      font-family: 'Gowun Batang', serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 20px 15px;
      margin: 0;
      color: #1e293b;
    }
    .card {
      background-color: #ffffff;
      padding: 30px 20px;
      border-radius: 24px;
      box-shadow: 0 10px 30px rgba(14, 165, 233, 0.15);
      width: 100%;
      max-width: 450px;
      box-sizing: border-box;
      text-align: center;
    }
    
    .countdown-box {
      background-color: #0ea5e9;
      color: white;
      padding: 12px;
      border-radius: 16px;
      font-size: 15px;
      font-weight: bold;
      margin-bottom: 20px;
      box-shadow: 0 4px 10px rgba(14, 165, 233, 0.3);
      font-family: 'Gowun Batang', serif;
    }
    .concept-tag {
      display: inline-block;
      background-color: #e0f2fe;
      color: #0369a1;
      font-size: 13px;
      font-weight: bold;
      padding: 6px 14px;
      border-radius: 50px;
      margin-bottom: 5px;
    }

    .info-section {
      background-color: #f0f9ff; 
      border: 1.5px dashed #38bdf8; 
      padding: 18px 20px;
      border-radius: 20px;
      margin-bottom: 25px;
      text-align: left; 
      font-family: 'Gowun Batang', serif;
    }
    .info-title {
      font-weight: bold;
      font-size: 15px;
      color: #0284c7;
      margin-bottom: 12px;
      text-align: center;
      border-bottom: 1.5px dashed #bae6fd;
      padding-bottom: 8px;
    }
    .info-content p {
      margin: 8px 0;
      font-size: 10px;
      line-height: 1.6;
      color: #334155;
    }
    .info-content strong {
      color: #0ea5e9; 
    }
    .info-sub-title {
      font-weight: bold;
      color: #0369a1;
      font-size: 15px;
      margin-top: 18px;
      margin-bottom: 5px;
      border-left: 3px solid #0ea5e9;
      padding-left: 8px;
    }
    .timetable-list {
      padding-left: 0;
      list-style: none;
      font-size: 10px;
      color: #475569;
      line-height: 1.6;
      margin: 8px 0;
    }
    .timetable-list li {
      margin-bottom: 6px;
      border-bottom: 1px dotted #cbd5e1;
      padding-bottom: 4px;
    }

    .vote-section {
      background-color: #f8fafc;
      padding: 20px 15px;
      border-radius: 20px;
      margin-bottom: 25px;
      border: 1.5px solid #e2e8f0;
      font-family: 'Gowun Batang', serif;
    }
    .vote-title {
      font-size: 12px;
      font-weight: bold;
      color: #0369a1;
      margin-bottom: 15px;
    }
    .vote-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 10px;
      margin-bottom: 5px;
    }
    .vote-btn {
      background-color: #ffffff;
      border: 1.5px solid #e2e8f0;
      padding: 12px;
      border-radius: 14px;
      font-size: 10px;
      font-family: 'Gowun Batang', serif;
      font-weight: bold;
      cursor: pointer;
      transition: all 0.2s ease;
      display: flex;
      flex-direction: column;
      align-items: center;
      color: #1e293b;
    }
    .vote-btn:hover {
      border-color: #0ea5e9;
      background-color: #f0f9ff;
      transform: translateY(-2px);
    }
    .vote-emoji {
      font-size: 24px;
      margin-bottom: 5px;
    }
    .vote-count {
      font-size: 10px;
      color: #0ea5e9;
      margin-top: 5px;
    }
    input, textarea {
      width: 100%;
      padding: 16px;
      margin-bottom: 15px;
      border: 1.5px solid #e2e8f0;
      border-radius: 16px;
      box-sizing: border-box;
      outline: none;
      background-color: #f8fafc;
      transition: all 0.3s ease;
      font-family: 'Gowun Batang', sans-serif;
      font-size: 11px;
    }
    input:focus, textarea:focus {
      border: 1.5px solid #0ea5e9;
      background-color: #ffffff;	
      box-shadow: 0 0 8px rgba(14, 165, 233, 0.2);
    }
    textarea {
      height: 120px;
      resize: none;
      font-family: 'Gowun Batang', sans-serif;
      font-size: 11px;
    }
    button.submit-btn {
      width: 100%;
      padding: 16px;
      background-color: #0ea5e9;
      color: white;
      border: none;
      border-radius: 16px;
      font-size: 15px;
      font-weight: bold;
      cursor: pointer;
      transition: background 0.3s;
    }
    button.submit-btn:hover {
      background-color: #0284c7;
    }

    hr {
      border: 0;
      height: 1px;
      background: #e2e8f0;
      margin: 30px 0;
    }

    h1 {
      font-size: 20px;
      color: #0ea5e9;
      margin-bottom: 20px;
    }

    h2 {
      font-size: 16px;
      color: #334155;
      margin-bottom: 20px;
    }
    .comment-item {
      background-color: #f0fdf4;
      border-left: 4px solid #38bdf8;
      padding: 15px;
      border-radius: 16px;
      margin-bottom: 15px;
      text-align: left;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.02);
    }
    .comment-name {
      font-weight: bold;
      color: #0284c7;
      font-size: 12px;
      margin-bottom: 5px;
    }
    .comment-text {
      margin: 0;
      font-size: 11px;
      line-height: 1.5;
    }

    .modal-overlay {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background-color: rgba(15, 23, 42, 0.6);
      z-index: 99999;
      justify-content: center;
      align-items: center;
      padding: 20px;
      box-sizing: border-box;
    }

    .modal-content {
      background-color: white;
      padding: 30px 20px;
      border-radius: 24px;
      text-align: center;
      width: 100%;
      max-width: 350px;
      box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
      animation: popUp 0.3s ease;
    }
    @keyframes popUp {
      from { transform: scale(0.8); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }
    .modal-content h3 {
      color: #0284c7;
      margin-top: 0;
      font-size: 20px;
    }
    .modal-content p {
      font-size: 15px;
      color: #475569;
      line-height: 1.6;
      margin-bottom: 25px;
    }
    .modal-close-btn {
      background-color: #0ea5e9;
      color: white;
      border: none;
      padding: 12px 30px;
      border-radius: 12px;
      font-size: 15px;
      font-weight: bold;
      cursor: pointer;
      font-family: 'Gowun Batang', serif;
    }
  </style>
</head>
<body>

  <div class="card">
    <div id="dday-timer" class="countdown-box">남은 시간 계산</div>
    <div class="concept-tag">🎂 지서니 서른두돌잔치 🎂</div>
     
    <h1>하나둘셋! 지선아 생일 축하해</h1>
    <p class="subtitle">
      인생 첫 돌잡이를 하는 지선이를 위해 <br>
      축하의 한 마디를 남겨주세요 >.<
    </p>

    <div class="info-section">
      <div class="info-title">✨ 생일 포트럭 파티 초대장 ✨</div>
      <div class="info-content">
        <p style="text-align: center; font-weight: bold; margin-bottom: 20px; color: #0284c7;">
          음식, 술, 그리고 레즈비언 필승룩을 장착하고 만나는<br>
          지선이의 생일 포트럭 파티에 여러분을 초대합니다 >.<
        </p>
        
        <div class="info-sub-title">📍 일시 및 장소</div>
        <p><strong>일시:</strong> 2026년 8월 1일(토) 12:00 PM</p>
        <p><strong>장소:</strong> 스피크이지 <br>
         &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(서울 서대문구 연세로7안길 10-5 지하1층)
         </p>
        
        <iframe 
          src="https://maps.google.com/maps?q=%EC%84%9C%EC%9A%B8%20%EC%84%9C%EB%8C%80%EB%AC%B8%EA%B5%AC%20%EC%97%B0%EC%84%B8%EB%A1%9C7%EC%95%88%EA%B8%B8%2010-5&t=&z=17&ie=UTF8&iwloc=&output=embed" 
          width="100%" 
          height="220" 
          style="border:0; border-radius: 14px; margin-top: 10px; box-shadow: 0 4px 10px rgba(0,0,0,0.05);" 
          allowfullscreen="" 
          loading="lazy">
        </iframe>

        <div style="text-align: right; margin-top: 12px; margin-bottom: 12px;">
          <a href="https://naver.me/GntmbOm7" 
             target="_blank" 
             style="display: inline-block; background-color: #e0f2fe; color: #0369a1; border: 1.5px solid #bae6fd; padding: 8px 16px; border-radius: 50px; text-decoration: none; font-weight: bold; font-size: 10px; transition: all 0.2s ease; box-shadow: 0 2px 6px rgba(14, 165, 233, 0.08);"
             onmouseover="this.style.backgroundColor='#bae6fd'" 
             onmouseout="this.style.backgroundColor='#e0f2fe'">
            📍 네이버 지도에서 위치 보기
          </a>
        </div>

        <div class="info-sub-title">👗 드레스코드: 과한 레즈비언</div>
        <p>가장 레즈비언스러운 <strong>'필승룩'</strong>을 입고 입장해 주세요.<br>
        투표를 통해 선정된 '베스트 드레서'에게는 특별한 선물이 증정됩니다!</p>

        <div class="info-sub-title">🥪 준비물 & 제공 안내</div>
        <p><strong>챙겨올 것(필수):</strong> 포트럭 파티를 위한 1~2인분의 음식</p>
        <p><strong>챙겨올 것(선택):</strong> 사회생활력, 생일 선물(2만원 이하)</p>
        <p><strong>제공되는 것:</strong> 간단한 안주류, 나영 Pick 술, 플레이리스트</p>
        <p style="text-align: center; font-size: 10px; color: #64748b; background: #e0f2fe; padding: 10px; border-radius: 10px; margin-top: 10px;">
          전자레인지, 인덕션, 에어프라이어 구비<br>
          데워 먹어야 하는 요리도 괜찮습니다!
        </p>

        <div class="info-sub-title">⏳ 파티 타임테이블</div>
        <ul class="timetable-list">
          <li><strong>12:00 ~ 12:30</strong> | 탑엘식 자기소개 & 필승룩 소개</li>
          <li><strong>12:30 ~ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</strong> | 가져온 음식 소개, 포트럭 파티 시작</li>
          <li><strong>15:30 ~ 16:00</strong> | 서른두돌잡이, 선물 언박싱</li>
          <li><strong>16:00 ~ 17:00</strong> | 베스트 드레서 시상, 정리정돈</li>
        </ul>

        <p style="text-align: center; font-size: 11.5px; font-weight: bold; color: #0284c7; margin-top: 20px; border-top: 1px dashed #bae6fd; padding-top: 15px;">
          파티 끝나고 아쉬운 사람 계신가요?<br>
          원하시는 분들은 함께 2차에 가요...^_^ <br>
          <span style="font-size: 10px; color: #64748b;">(호스트가 지치지 않을 수 있을지...)</span>
        </p>
      </div>
    </div>

    <form id="comment-form">
      <input type="text" id="nickname" placeholder="이름 또는 닉네임" required>
      <textarea id="message" placeholder="축하의 마음을 담아 메시지를 작성해 주세요!" required></textarea>
      <button type="submit" class="submit-btn">마음 보내기</button>
    </form>
    
    <hr>
    
    <div class="vote-section">
      <div class="vote-title">서른두돌잡이, 지선이가 잡을 물건에 투표해 주세요!</div>
      <div class="vote-grid">
        <button type="button" class="vote-btn" data-option="cash">
          <span class="vote-emoji">💵</span>
          <span>평생 돈 걱정 없을 정도의 재물</span>
          <span class="vote-count" id="count-cash">0표</span>
        </button>
        <button type="button" class="vote-btn" data-option="beer">
          <span class="vote-emoji">💐</span>
          <span>멋진 배우자와의 결혼</span>
          <span class="vote-count" id="count-beer">0표</span>
        </button>
        <button type="button" class="vote-btn" data-option="pills">
          <span class="vote-emoji">🎓</span>
          <span>패티쉬 셀프 실현을 위한 대학원</span>
          <span class="vote-count" id="count-pills">0표</span>
        </button>
        <button type="button" class="vote-btn" data-option="mouse">
          <span class="vote-emoji">💻</span>
          <span>일복...</span>
          <span class="vote-count" id="count-mouse">0표</span>
        </button>
      </div>
    </div>
    
    <hr>
    
    <h2>💌</h2>
    <div id="comments-list"></div>
  </div>

  <div id="success-modal" class="modal-overlay">
    <div class="modal-content">
      <h3>마음 전달 완료 💙</h3>
      <p>
        소중한 마음이 잘 도착했어요. <br>
        축하해 주셔서 감사합니다.
      </p>
      <button id="close-modal-btn" class="modal-close-btn">확인</button>
    </div>
  </div>

  <script type="module">
    import { initializeApp } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-app.js";
    import { getFirestore, collection, addDoc, onSnapshot, query, orderBy, setDoc, doc, increment } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-firestore.js";

    // 콘솔 메시지 
console.log(
  '%c애인이 짠 코드 뜯어보는 거 아니지? 생일 축하해! 사랑해 >.<',
  'font-size: 15px; font-weight: bold; color: #0369a1; background: #e0f2fe; padding: 6px 12px; border-radius: 8px; font-family: sans-serif; display: inline-block; margin-top: 6px;'
);


    const firebaseConfig = {
      apiKey: "AIzaSyAgnyTQJHhZfnMnmG6ViXOuW7ahv9TVFCg",
      authDomain: "happy-js-s-birthday.firebaseapp.com",
      projectId: "happy-js-s-birthday",
      storageBucket: "happy-js-s-birthday.firebasestorage.app",
      messagingSenderId: "303535194011",
      appId: "1:303535194011:web:8dbb7ef66528336b7beb3e"
    };

    const app = initializeApp(firebaseConfig);
    const db = getFirestore(app);
    const modal = document.getElementById('success-modal');

    // 폭죽 효과
    const triggerConfetti = () => {
      confetti({
        particleCount: 120,
        spread: 75,
        origin: { y: 0.6 },
        colors: ['#0ea5e9', '#38bdf8', '#bae6fd', '#ffffff', '#e0f2fe']
      });
    };

    const openModal = () => { 
      modal.style.display = 'flex'; 
      triggerConfetti(); 
    };
    
    const closeModal = () => { 
      modal.style.display = 'none'; 
    };
    
    document.getElementById('close-modal-btn').addEventListener('click', closeModal);

    // 디데이 타이머
    const startCountdown = () => {
      const targetDate = new Date("2026-08-01T00:00:00").getTime();
      const timerElement = document.getElementById('dday-timer');

      const updateTimer = () => {
        const now = new Date().getTime();
        const difference = targetDate - now;

        if (difference < 0) {
          timerElement.innerText = "🎉 지서나 생일 축하해 🎉";
          return;
        }

        const days = Math.floor(difference / (1000 * 60 * 60 * 24));
        const hours = Math.floor((difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((difference % (1000 * 60)) / 1000);

        timerElement.innerText = `생일까지 D-${days}일 ${hours}시간 ${minutes}분 ${seconds}초`;
      };

      updateTimer();
      setInterval(updateTimer, 1000);
    };
    startCountdown();

    // 돌잡이 투표 처리
    const handleVote = async (option) => {
      if (localStorage.getItem('hasVoted')) {
        alert("이미 투표에 참여하셨습니다!");
        return;
      }

      try {
        const voteRef = doc(db, "votes", "doljabi");
        await setDoc(voteRef, { [option]: increment(1) }, { merge: true });
        
        localStorage.setItem('hasVoted', 'true');
        triggerConfetti();
        alert("투표가 성공적으로 반영되었습니다! 🎉");
      } catch (error) {
        console.error("투표 오류: ", error);
      }
    };

    document.querySelectorAll('.vote-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        if (localStorage.getItem('hasVoted')) {
          alert("이미 투표에 참여하셨습니다!");
          return;
        }
        const option = btn.getAttribute('data-option');
        handleVote(option);
      });
    });

    // 실시간 득표 갱신
    onSnapshot(doc(db, "votes", "doljabi"), (docSnap) => {
      if (docSnap.exists()) {
        const data = docSnap.data();
        document.getElementById('count-cash').innerText = `${data.cash || 0}표`;
        document.getElementById('count-beer').innerText = `${data.beer || 0}표`;
        document.getElementById('count-pills').innerText = `${data.pills || 0}표`;
        document.getElementById('count-mouse').innerText = `${data.mouse || 0}표`;
      }
    });

    // 방명록 등록
    document.getElementById('comment-form').addEventListener('submit', async (e) => {
      e.preventDefault();
      const name = document.getElementById('nickname').value;
      const text = document.getElementById('message').value;

      try {
        await addDoc(collection(db, "letters"), {
          name: name,
          text: text,
          timestamp: new Date()
        });
        document.getElementById('message').value = ''; 
        openModal(); 
      } catch (error) {
        console.error("저장 실패: ", error);
      }
    });

    // 실시간 방명록 목록
    const q = query(collection(db, "letters"), orderBy("timestamp", "desc"));
    onSnapshot(q, (snapshot) => {
      const container = document.getElementById('comments-list');
      container.innerHTML = '';
      snapshot.forEach((doc) => {
        const data = doc.data();
        
        // 날짜 포맷 (YYYY-MM-DD HH:mm:ss)
        let timeStr = "";
        if (data.timestamp) {
          const date = data.timestamp.toDate ? data.timestamp.toDate() : new Date(data.timestamp);
          const yyyy = date.getFullYear();
          const mm = String(date.getMonth() + 1).padStart(2, '0');
          const dd = String(date.getDate()).padStart(2, '0');
          const hh = String(date.getHours()).padStart(2, '0');
          const min = String(date.getMinutes()).padStart(2, '0');
          const ss = String(date.getSeconds()).padStart(2, '0');
          timeStr = `${yyyy}-${mm}-${dd} ${hh}:${min}:${ss}`;
        }

        container.innerHTML += `
          <div class="comment-item">
            <div class="comment-name" style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 8px;">
              <span>✨ ${data.name}</span>
              <span style="font-size: 11px; color: #94a3b8; font-weight: normal;">${timeStr}</span>
            </div>
            <div class="comment-text">${data.text}</div>
          </div>
        `;
      });
    });
  </script>
</body>
</html>
</html>
