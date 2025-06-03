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
      そういえば...今週末は鎌倉に行ってきたよー！<br>
      キレイな鯉を見つけたから<br><br>
      写真をUPするね～✨
    </p>

    <!-- 新しい鯉の写真 -->
   <img src="https://hikari-hikaru.github.io/dairy4/image0.jpeg" alt="きれいな鯉" width="300">
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
