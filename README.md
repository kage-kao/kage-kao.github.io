<div align="center">
  <img src="glitch.svg" width="100%" alt="KAGE-KAO ERROR">
</div>

<svg width="100%" height="100%" viewBox="0 0 800 150" preserveAspectRatio="xMidYMid meet" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Эффект помех (Глитч) -->
    <filter id="glitch" x="-20%" y="-20%" width="140%" height="140%">
      <feTurbulence type="fractalNoise" baseFrequency="0.02 0.15" numOctaves="1" result="noise" seed="0">
        <animate attributeName="baseFrequency" values="0.01 0.1;0.5 0.1;0.01 0.5;0.01 0.1" dur="0.2s" repeatCount="indefinite"/>
        <animate attributeName="seed" values="0;10;20;30;0" dur="0.2s" repeatCount="indefinite"/>
      </feTurbulence>
      <feDisplacementMap in="SourceGraphic" in2="noise" scale="10" xChannelSelector="R" yChannelSelector="G"/>
    </filter>

    <!-- Эффект RGB сдвига (хроматическая аберрация) -->
    <filter id="rgb-split">
      <feOffset in="SourceGraphic" dx="-3" dy="0" result="left"/>
      <feOffset in="SourceGraphic" dx="3" dy="0" result="right"/>
      <feMerge>
        <feMergeNode in="left"/>
        <feMergeNode in="right"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>

  <style>
    @import url('https://fonts.googleapis.com/css2?family=Rubik+Glitch&amp;display=swap');
    
    .bg { fill: #050505; }
    
    .text-base {
      font-family: 'Rubik Glitch', 'Courier New', monospace;
      font-size: 80px;
      fill: #ffffff;
      text-anchor: middle;
      dominant-baseline: middle;
      letter-spacing: 5px;
    }
    
    /* Красный призрак текста */
    .text-glitch-1 {
      fill: #ff0000;
      opacity: 0.6;
      mix-blend-mode: overlay;
      animation: shake 0.3s infinite linear alternate-reverse;
    }
    
    /* Циан призрак текста */
    .text-glitch-2 {
      fill: #00ffff;
      opacity: 0.4;
      mix-blend-mode: overlay;
      animation: shake 0.4s infinite linear alternate;
    }

    .overlay {
      fill: none;
      stroke: rgba(255,255,255,0.1);
      stroke-width: 1;
      width: 100%;
      height: 100%;
    }

    /* Анимация хаотичного дерганья */
    @keyframes shake {
      0% { transform: translate(2px, 1px); }
      20% { transform: translate(-3px, 0); }
      40% { transform: translate(1px, -1px); opacity: 0; }
      60% { transform: translate(-1px, 2px); opacity: 0.8; }
      80% { transform: translate(2px, -2px); }
      100% { transform: translate(0, 0); }
    }
    
    /* Строка сканирования (Scanline) */
    .scanline {
      width: 100%;
      height: 100px;
      fill: url(#gradient);
      opacity: 0.1;
      animation: scan 3s linear infinite;
    }

    @keyframes scan {
      0% { transform: translateY(-100%); }
      100% { transform: translateY(200%); }
    }
  </style>

  <!-- Фон -->
  <rect width="100%" height="100%" class="bg" />

  <!-- Группа текстов с фильтрами -->
  <g transform="translate(400, 75)">
    <!-- Скрытые слои для эффекта жирности и дерганья -->
    <text x="-2" y="2" class="text-base text-glitch-1" filter="url(#glitch)">kage-kao</text>
    <text x="2" y="-2" class="text-base text-glitch-2">kage-kao</text>
    
    <!-- Основной белый текст -->
    <text x="0" y="0" class="text-base">kage-kao</text>
  </g>

  <!-- Линии старого монитора -->
  <path d="M0 0 H800 M0 4 H800 M0 8 H800 M0 12 H800 M0 16 H800 M0 20 H800 M0 24 H800 M0 28 H800 M0 32 H800 M0 36 H800 M0 40 H800 M0 44 H800 M0 48 H800 M0 52 H800 M0 56 H800 M0 60 H800 M0 64 H800 M0 68 H800 M0 72 H800 M0 76 H800 M0 80 H800 M0 84 H800 M0 88 H800 M0 92 H800 M0 96 H800 M0 100 H800 M0 104 H800 M0 108 H800 M0 112 H800 M0 116 H800 M0 120 H800 M0 124 H800 M0 128 H800 M0 132 H800 M0 136 H800 M0 140 H800 M0 144 H800 M0 148 H800" class="overlay"/>
</svg>
