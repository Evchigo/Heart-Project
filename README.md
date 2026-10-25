# Heart-Project
Heart Jar
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Heart Jar</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      background: linear-gradient(180deg, #fff8fb 0%, #fce8f0 100%);
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      color: #6f4354;
      touch-action: manipulation;
      overflow: hidden;
    }

    .app {
      width: 100%;
      max-width: 430px;
      min-height: 100vh;
      padding: 42px 20px 28px;
      text-align: center;
      position: relative;
    }

    h1 {
      margin: 0;
      font-size: 32px;
      font-weight: 750;
      letter-spacing: -0.5px;
    }

    .message {
      margin: 8px 0 22px;
      font-size: 16px;
      color: #9a6d7e;
    }

    .heart-source {
      width: 78px;
      height: 72px;
      margin: 0 auto 12px;
      display: grid;
      place-items: center;
      font-size: 64px;
      line-height: 1;
      color: #ed6688;
      cursor: grab;
      user-select: none;
      -webkit-user-select: none;
      touch-action: none;
      filter: drop-shadow(0 6px 5px rgba(135, 65, 88, 0.18));
      transition: transform 0.18s ease;
    }

    .heart-source:active {
      cursor: grabbing;
      transform: scale(1.08);
    }

    .hint {
      margin: 0 0 18px;
      font-size: 14px;
      color: #aa7b8c;
    }

    .jar-area {
      width: 280px;
      height: 310px;
      margin: 0 auto;
      position: relative;
    }

    .jar-neck {
      width: 170px;
      height: 30px;
      position: absolute;
      top: 0;
      left: 55px;
      z-index: 4;
      border: 7px solid rgba(128, 156, 172, 0.65);
      border-radius: 13px;
      background: rgba(255, 255, 255, 0.35);
      box-shadow:
        inset 0 0 0 3px rgba(255, 255, 255, 0.7),
        0 3px 6px rgba(97, 121, 137, 0.12);
    }

    .jar {
      width: 240px;
      height: 270px;
      position: absolute;
      left: 20px;
      bottom: 0;
      overflow: hidden;
      border: 7px solid rgba(128, 156, 172, 0.55);
      border-top-width: 5px;
      border-radius: 35px 35px 70px 70px;
      background:
        linear-gradient(
          105deg,
          rgba(255, 255, 255, 0.62) 0%,
          rgba(255, 255, 255, 0.18) 30%,
          rgba(181, 222, 235, 0.15) 65%,
          rgba(255, 255, 255, 0.5) 100%
        );
      box-shadow:
        inset 12px 0 18px rgba(255, 255, 255, 0.7),
        inset -8px 0 14px rgba(125, 180, 198, 0.12),
        0 15px 25px rgba(112, 73, 87, 0.14);
    }

    .jar-highlight {
      width: 17px;
      height: 145px;
      position: absolute;
      top: 48px;
      left: 24px;
      z-index: 5;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.67);
      transform: rotate(3deg);
      pointer-events: none;
    }

    .jar-label {
      position: absolute;
      left: 50%;
      top: 95px;
      z-index: 6;
      transform: translateX(-50%) rotate(-2deg);
      width: 130px;
      padding: 9px 8px;
      border-radius: 8px;
      background: rgba(255, 248, 239, 0.82);
      border: 2px solid rgba(186, 144, 126, 0.32);
      color: #a16074;
      font-family: Georgia, serif;
      font-size: 18px;
      font-weight: bold;
      box-shadow: 0 3px 6px rgba(92, 57, 70, 0.08);
      pointer-events: none;
    }

    .counter {
      margin-top: 18px;
      font-size: 22px;
      font-weight: 700;
      color: #79485b;
    }
  </style>
</head>

<body>
  <main class="app">
    <h1>My Heart Jar</h1>
    <p class="message">A little place for all of your wins.</p>

    <div class="heart-source" aria-label="Heart">♥</div>
    <p class="hint">Tap or drag the heart into the jar</p>

    <div class="jar-area">
      <div class="jar-neck"></div>

      <div class="jar">
        <div class="jar-highlight"></div>
        <div class="jar-label">Good Things</div>
      </div>
    </div>

    <div class="counter">0 Hearts</div>
  </main>
</body>
</html>
