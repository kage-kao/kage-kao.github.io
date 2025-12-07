<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Verdana&weight=900&size=30&pause=1000&color=000000&background=FFDD00&center=true&vCenter=true&width=500&lines=КУПЛЮ+ГАРАЖ;ПРОДАМ+ЗИМНЮЮ+РЕЗИНУ;СДАМ+КОМНАТУ;ОТДАМ+КОТА" alt="Trash" />
</div>
~~💾~~
![alt text](https://pomf2.lain.la/f/39sg6aqv.png)
end.
<svg width="800" height="200" viewBox="0 0 800 200" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Эффект "шума" для стекла -->
    <filter id="glass-distortion">
      <feTurbulence type="fractalNoise" baseFrequency="0.05" numOctaves="3" result="noise" />
      <feDisplacementMap in="SourceGraphic" in2="noise" scale="5" />
    </filter>
  </defs>

  <style>
    /* Настройки фона и текста */
    .bg { fill: #000; }
    
    .text {
      font-family: 'Verdana', sans-serif;
      font-weight: 900;
      font-size: 80px;
      fill: #ff0000; /* Цвет ника красный */
      text-anchor: middle;
      opacity: 0; /* Скрыт в начале */
      animation: reveal-text 0.1s linear forwards 1.3s, flicker 3s infinite 2s;
    }

    /* Дульный выстрел / вспышка */
    .muzzle-flash {
      fill: #fff;
      opacity: 0;
      transform-origin: center;
      animation: shoot-flash 0.15s linear forwards 1.0s;
    }

    /* Пулевое отверстие */
    .bullet-hole {
      fill: #111;
      stroke: #333;
      stroke-width: 2;
      r: 0;
      opacity: 0.9;
      animation: hole-appear 0.05s linear forwards 1.1s;
    }

    /* Трещины */
    .cracks {
      fill: none;
      stroke: #ffffff;
      stroke-width: 2;
      stroke-linecap: round;
      stroke-linejoin: round;
      opacity: 0;
      filter: url(#glass-distortion);
      animation: crack-appear 0.05s linear forwards 1.1s;
    }

    /* Весь экран трясется при выстреле */
    .container {
      animation: shake 0.2s cubic-bezier(.36,.07,.19,.97) both 1.0s;
    }

    /* ------ АНИМАЦИИ ------ */
    
    /* Тряска экрана */
    @keyframes shake {
      10%, 90% { transform: translate3d(-2px, -1px, 0); }
      20%, 80% { transform: translate3d(4px, 2px, 0); }
      30%, 50%, 70% { transform: translate3d(-8px, -4px, 0); }
      40%, 60% { transform: translate3d(8px, 4px, 0); }
    }

    /* Вспышка выстрела */
    @keyframes shoot-flash {
      0% { opacity: 0; r: 0; }
      50% { opacity: 1; r: 300; }
      100% { opacity: 0; r: 600; }
    }

    /* Появление дырки */
    @keyframes hole-appear {
      0% { r: 0; }
      100% { r: 15; }
    }

    /* Появление трещин */
    @keyframes crack-appear {
      0% { opacity: 0; stroke-dasharray: 0 500; }
      100% { opacity: 0.8; stroke-dasharray: 500 0; }
    }

    /* Появление текста (резко) */
    @keyframes reveal-text {
      0% { opacity: 0; transform: scale(0.9); }
      100% { opacity: 1; transform: scale(1); }
    }
    
    /* Мерцание текста как сломанная вывеска */
    @keyframes flicker {
      0%, 19%, 21%, 23%, 25%, 54%, 56%, 100% { opacity: 1; }
      20%, 24%, 55% { opacity: 0.4; }
    }
  </style>

  <!-- ГРУППА АНИМАЦИИ -->
  <g class="container">
    <!-- Черный фон -->
    <rect width="100%" height="100%" class="bg" />

    <!-- НИКНЕЙМ (появляется после выстрела) -->
    <text x="50%" y="65%" class="text">kage-kao</text>

    <!-- Вспышка от выстрела -->
    <circle cx="400" cy="100" r="0" class="muzzle-flash" />

    <!-- Трещины (рисунок паутины) -->
    <path d="M400,100 L320,20 M400,100 L450,10 M400,100 L550,60 M400,100 L500,180 M400,100 L350,190 M400,100 L250,120 M400,100 L280,60 
             M350,50 L320,20 M450,50 L480,20 M500,100 L560,90" class="cracks" />
    <path d="M400,100 m-40,-20 l80,-10 l10,60 l-60,10 z" class="cracks" style="opacity:0.3; stroke-width:1" />

    <!-- Дырка от пули -->
    <circle cx="400" cy="100" class="bullet-hole" />
  </g>
</svg>
