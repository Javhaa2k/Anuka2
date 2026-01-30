<!DOCTYPE html>
<html lang="mn">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Чамдаа</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      color: #fff;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .page {
      display: none;
      text-align: center;
      max-width: 600px;
      padding: 30px;
      background: rgba(255, 255, 255, 0.15);
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
    }
    .page.active {
      display: block;
    }
    h1, h2, p {
      margin-bottom: 20px;
    }
    button {
      background: #ff4b5c;
      border: none;
      padding: 12px 25px;
      border-radius: 30px;
      color: #fff;
      font-size: 16px;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #ff2e44;
      transform: scale(1.05);
    }
    input {
      padding: 12px;
      border-radius: 20px;
      border: none;
      width: 80%;
      font-size: 16px;
      text-align: center;
      margin-bottom: 15px;
    }
    .error {
      color: #ffe6e6;
      margin-top: 10px;
    }
    .link {
      margin-top: 8px;
      text-decoration: underline;
      cursor: pointer;
      color: #fff;
    }
  </style>
</head>
<body>

  <!-- Page 1 -->
  <div class="page active" id="page1">
    <h1>Энийг харж буй хөөрхөн танд энэ цагийн мэндийг хүргэе 💖</h1>
    <p>Таны найз залууд танд хэлэх үг байна гэнэ ээ</p>
    <button onclick="goToPage(2)">Цааш үргэлжлүүлэх</button>
  </div>

  <!-- Page 2 -->
  <div class="page" id="page2">
    <h2>Цааш үргэлжлүүлэхийн тулд нууц үг хийнэ үү 🔐</h2>
    <input type="password" id="password" placeholder="Нууц үг" />
    <br />
    <button onclick="checkPassword()">Нэвтрэх</button>
    <div class="error" id="error"></div>
    <div class="link" id="skip" onclick="goToPage(3)" style="display:none;">
      Тоглоомондоо энд дарна уу 😉
    </div>
  </div>

  <!-- Page 3 -->
  <div class="page" id="page3">
    <h2>Сайн уу миний гүнжээ 💕</h2>
    <p>
      Чи минь энийг унших цаг минутын мэндийг хүргэе. <br /><br />
      Хайрийгaa гомдоож уурлуулдагт уучлаарай. <br />
      Хэдий цаг хугацаа, зай биднийг түр холдуулсан ч <br />
      зүрхний цохилт бүр минь чиний төлөө цохилдог юм шүү. <br /><br />
      Чамтай өнгөрүүлэх ирээдүйн өдрүүдийг <br />
      би тэсэн ядан хүлээж байна. <br /><br />
      Чамдаа хязгааргүй их хайртай шүү 💖
    </p>
  </div>

  <script>
    function goToPage(pageNumber) {
      document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
      document.getElementById('page' + pageNumber).classList.add('active');
    }

    function checkPassword() {
      const input = document.getElementById('password').value;
      const error = document.getElementById('error');
      const skip = document.getElementById('skip');

      if (input === 'Anuka247') {
        error.textContent = 'Нууц үг буруу байна 😅';
        skip.style.display = 'block';
      } else {
        error.textContent = 'Нууц үг буруу байна 😅';
        skip.style.display = 'block';
      }
    }
  </script>

</body>
</html>
