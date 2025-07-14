<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>2025年7月15日 - おさんぽ～♪</title>
  <link rel="stylesheet" href="../style.css">

  <style>
    #blackout {
      display: none;
      position: fixed;
      inset: 0;
      background: black;
      z-index: 9999;
    }

    .protected-photo {
      width: 100%;
      user-select: none;
      -webkit-user-drag: none;
      pointer-events: auto;
      display: block;
    }

    .watermark-container {
      position: relative;
      display: inline-block;
      width: 300px;
      margin-bottom: 16px;
    }

    .watermark {
      position: absolute;
      bottom: 8px;
      right: 12px;
      color: white;
      font-size: 12px;
      opacity: 0.6;
      text-shadow: 1px 1px 2px black;
      pointer-events: none;
    }
  </style>
</head>
<body oncontextmenu="return false;" onselectstart="return false;" ondragstart="return false;">
  <header>
    <h1>HIKARI・HIKARU 日々のブログ</h1>
  </header>

  <main>
    <h2>2025年7月15日 - Koi(beauty fish)！</h2>
    <p>
      そういえば...先々週末だったかなー...?(笑)。鎌倉に行ってきたよー！<br>
      キレイな鯉を見つけたから<br><br>
      写真をUPするね～✨
    </p>

    <div class="watermark-container">
      <img src="https://hikari-hikaru.github.io/dairy4/image0.jpeg" alt="きれいな鯉" class="protected-photo">
      <div class="watermark">© HIKARI-HIKARU 2025</div>
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
      photo.addEventListener('touchend', () => clearTimeout(timer));
      photo.addEventListener('touchcancel', () => clearTimeout(timer));
    });

    blackout.addEventListener('click', () => {
      blackout.style.display = 'none';
    });
  </script>
</body>
</html>
