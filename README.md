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

      /* iOS保存時に黒くなりやすい処理 */
      mix-blend-mode: multiply;
      filter: brightness(0.3);
      -webkit-mask-image: linear-gradient(black, black);
    }

    .photo-wrapper {
      position: relative;
      display: inline-block;
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
    <h2>2025年7月15日 - Koi(beauty fish)！</h2>
    <p>
      そういえば...今週末は鎌倉に行ってきたよー！<br>
      キレイな鯉を見つけたから<br><br>
      写真をUPするね～✨
    </p>

    <!-- 鯉の写真をラッパーで囲って制御 -->
    <div class="photo-wrapper">
      <img src="https://hikari-hikaru.github.io/dairy4/image0.jpeg" alt="きれいな鯉" class="protected-photo">
    </div>
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
