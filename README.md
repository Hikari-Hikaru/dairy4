# dairy4
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>2025年7月15日 - おさんぽ～♪</title>
  <link rel="stylesheet" href="../style.css"> <!-- 共通CSSの読み込み -->

  <style>
    #blackout {
      display: none;
      position: fixed;
      inset: 0;
      background: black;
      z-index: 9999;
    }

    .protected-photo {
      width: 300px;
      user-select: none;
      -webkit-user-drag: none;
      pointer-events: auto;
      margin-bottom: 16px;
    }
  </style>
</head>
<body
  oncontextmenu="return false;"
  onselectstart="return false;"
  ondragstart="return false;"
>
  <header>
    <h1>HIKARI・HIKARU 日々のブログ</h1>
  </header>

  <main>
    <h2>2025年7月15日 - BeautyFish！</h2>
    <p>
      今日は鎌倉行ってきたよー！<br>
      キレイな鯉を見つけたから<br><br>
      写真をUPするね～✨
    </p>

    <p>※写真を0.5秒以上長押しすると黒画面になります。</p>

    <!-- 新しい鯉の写真 -->
    <img src="images/image0.jpeg" alt="きれいな鯉" class="protected-photo">
  </main>

  <div id="blackout"></div>

  <script>
    const photos = document.querySelectorAll('.protected-photo');
    const blackout = document.getElementById('blackout');

    photos.forEach(photo => {
      let timer;

      photo.addEventListener('touchstart', () => {
        timer = setTimeout(() => {
          blackout.style.display = 'block';
        }, 500);
      });

      photo.addEventListener('touchend', () => {
        clearTimeout(timer);
      });

      photo.addEventListener('touchcancel', () => {
        clearTimeout(timer);
      });
    });

    blackout.addEventListener('click', () => {
      blackout.style.display = 'none';
    });
  </script>
</body>
</html>
