<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>100 Razones Para Amarte ❤️</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Caveat:wght@600;700&family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #ff758c 0%, #ff7eb3 50%, #fecfef 100%);
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
      overflow-x: hidden;
      position: relative;
    }

    /* Floating Hearts Container */
    .hearts-bg {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 1;
      overflow: hidden;
    }

    .heart-particle {
      position: absolute;
      bottom: -50px;
      color: rgba(255, 255, 255, 0.7);
      animation: floatUp linear infinite;
      user-select: none;
    }

    @keyframes floatUp {
      0% {
        transform: translateY(0) rotate(0deg) scale(0.8);
        opacity: 1;
      }
      100% {
        transform: translateY(-115vh) rotate(360deg) scale(1.3);
        opacity: 0;
      }
    }

    /* Music Control Button */
    .music-btn {
      position: fixed;
      top: 20px;
      right: 20px;
      z-index: 100;
      background: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(5px);
      border: 2px solid #ff4b72;
      color: #ff4b72;
      width: 50px;
      height: 50px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.3rem;
      cursor: pointer;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.15);
      transition: all 0.3s ease;
    }

    .music-btn:hover {
      transform: scale(1.1);
      background: #ff4b72;
      color: white;
    }

    /* Main Card Container */
    .card {
      background: rgba(255, 255, 255, 0.95);
      backdrop-filter: blur(10px);
      padding: 30px 25px;
      border-radius: 25px;
      box-shadow: 0 15px 35px rgba(230, 57, 70, 0.25);
      max-width: 600px;
      width: 100%;
      text-align: center;
      position: relative;
      z-index: 10;
      border: 2px solid rgba(255, 255, 255, 0.8);
      animation: fadeIn 0.8s ease-out;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h1 {
      font-family: 'Caveat', cursive;
      color: #e63946;
      font-size: 2.6rem;
      margin-bottom: 10px;
      text-shadow: 1px 1px 2px rgba(0,0,0,0.05);
    }

    h2 {
      font-family: 'Caveat', cursive;
      color: #e63946;
      font-size: 2.3rem;
      margin-bottom: 15px;
    }

    .photo-preview-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 10px;
      margin-bottom: 20px;
    }

    .photo-preview-grid img {
      width: 100%;
      height: 110px;
      object-fit: cover;
      border-radius: 12px;
      border: 2px solid #ffccd5;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      transition: transform 0.3s ease;
    }

    .photo-preview-grid img:hover {
      transform: scale(1.05) rotate(1deg);
    }

    .interm-message {
      color: #d62828;
      font-size: 1.1rem;
      font-weight: 600;
      margin-bottom: 15px;
      background: #ffe6e6;
      padding: 12px 15px;
      border-radius: 15px;
      border-left: 5px solid #ff4b72;
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.02); }
    }

    .reasons-list {
      max-height: 320px;
      overflow-y: auto;
      text-align: left;
      padding: 15px 20px 15px 40px;
      margin-bottom: 20px;
      border: 1px solid #ffccd5;
      border-radius: 15px;
      background: #fff;
      box-shadow: inset 0 2px 6px rgba(0, 0, 0, 0.03);
      scroll-behavior: smooth;
    }

    .reasons-list::-webkit-scrollbar {
      width: 8px;
    }
    .reasons-list::-webkit-scrollbar-track {
      background: #fff0f3;
      border-radius: 10px;
    }
    .reasons-list::-webkit-scrollbar-thumb {
      background: #ffb3c1;
      border-radius: 10px;
    }

    .reasons-list li {
      margin-bottom: 10px;
      color: #4a4a4a;
      line-height: 1.4;
      font-size: 0.95rem;
    }

    button.primary-btn {
      background: linear-gradient(45deg, #ff4b72, #ff758c);
      color: white;
      border: none;
      padding: 14px 36px;
      font-size: 1.15rem;
      border-radius: 30px;
      cursor: pointer;
      transition: all 0.3s ease;
      font-weight: 600;
      box-shadow: 0 6px 20px rgba(255, 75, 114, 0.4);
    }

    button.primary-btn:hover {
      background: linear-gradient(45deg, #e63946, #ff4b72);
      transform: translateY(-3px) scale(1.03);
      box-shadow: 0 8px 25px rgba(255, 75, 114, 0.6);
    }

    .screen {
      display: block;
    }

    .hidden {
      display: none;
    }

    /* Proposal Arena */
    .proposal-container {
      position: relative;
      min-height: 280px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }

    .buttons-wrapper {
      margin-top: 25px;
      display: flex;
      justify-content: center;
      align-items: center;
      width: 100%;
      height: 120px;
      position: relative;
    }

    #btnYes {
      position: relative;
      z-index: 10;
      font-size: 1.3rem;
      padding: 16px 42px;
    }

    #btnNo {
      position: absolute;
      background: #8d99ae;
      color: white;
      border: none;
      padding: 12px 28px;
      font-size: 1.1rem;
      border-radius: 30px;
      cursor: pointer;
      font-weight: 600;
      transition: all 0.15s ease-out;
      box-shadow: 0 4px 12px rgba(0,0,0,0.15);
    }

    /* Final Screen Celebration */
    .final-photo-container {
      position: relative;
      margin: 15px auto;
      max-width: 380px;
      border-radius: 20px;
      overflow: hidden;
      box-shadow: 0 10px 25px rgba(230, 57, 70, 0.3);
      border: 4px solid #fff;
    }

    .final-photo-container img {
      width: 100%;
      height: auto;
      display: block;
    }

    .celebration-icon {
      font-size: 3rem;
      margin-bottom: 10px;
      animation: heartBeat 1.2s infinite;
    }

    @keyframes heartBeat {
      0% { transform: scale(1); }
      14% { transform: scale(1.2); }
      28% { transform: scale(1); }
      42% { transform: scale(1.2); }
      70% { transform: scale(1); }
    }
  </style>
</head>
<body>

  <!-- Floating Hearts Background -->
  <div class="hearts-bg" id="heartsBg"></div>

  <!-- Music Toggle Button -->
  <button class="music-btn" id="musicBtn" onclick="toggleMusic()" title="Reproducir / Pausar Música">🎵</button>

  <audio id="bgMusic" loop preload="auto">
    <source src="https://cdn.pixabay.com/download/audio/2022/05/27/audio_1808fbf07a.mp3?filename=romantic-piano-112199.mp3" type="audio/mpeg">
  </audio>

  <div class="card">
    
    <!-- PANTALLA 1: Primeras 50 razones -->
    <div id="screen1" class="screen">
      <h1>100 Razones para amarte ❤️</h1>
      <div class="photo-preview-grid">
        <img src="foto2.jpg" alt="Nuestro recuerdo 1">
        <img src="foto3.jpg" alt="Nuestro recuerdo 2">
        <img src="foto4.jpg" alt="Nuestro recuerdo 3">
      </div>
      <ol class="reasons-list" start="1">
        <li>Tu energía positiva</li>
        <li>Tu forma de amar</li>
        <li>Tus metas claras</li>
        <li>Tus valores firmes</li>
        <li>Tu manera de enfrentar retos</li>
        <li>Tu manera de superar miedos</li>
        <li>Tu sensibilidad</li>
        <li>Tu conexión conmigo</li>
        <li>Tu forma de consolarme</li>
        <li>Tus ganas de vivir</li>
        <li>Tus sueños compartidos</li>
        <li>Tus bromas espontáneas</li>
        <li>Tus pequeños detalles</li>
        <li>Tu sonrisa al despertar</li>
        <li>Tus caricias en silencio</li>
        <li>Tu compañía en la adversidad</li>
        <li>Tu luz en mi vida</li>
        <li>Tu fe en nosotros</li>
        <li>Tu habilidad para perdonar</li>
        <li>Tu compromiso con tus sueños</li>
        <li>Tus ideas únicas</li>
        <li>Tus acciones desinteresadas</li>
        <li>Tus palabras de aliento</li>
        <li>Tu humildad</li>
        <li>Tus ganas de aprender</li>
        <li>Tu esfuerzo diario</li>
        <li>Tus abrazos inesperados</li>
        <li>Tus besos sinceros</li>
        <li>Tus risas contagiosas</li>
        <li>Tu amabilidad con todos</li>
        <li>Tu apoyo incondicional</li>
        <li>Tu mirada que lo dice todo</li>
        <li>Tu capacidad de transformar un mal día</li>
        <li>Tu valentía para ser tú misma</li>
        <li>Tu forma de enfrentar la vida</li>
        <li>Tus manos que me reconfortan</li>
        <li>Tu paciencia infinita</li>
        <li>Tu espíritu libre</li>
        <li>Tus palabras que sanan</li>
        <li>Tu fidelidad inquebrantable</li>
        <li>Tu risa que ilumina el día</li>
        <li>Tu habilidad de hacerme sentir amado</li>
        <li>Tu amor por la naturaleza</li>
        <li>Tu forma de cuidar de mí</li>
        <li>Tu capacidad de sorprenderme</li>
        <li>Tus detalles inesperados</li>
        <li>Tus ideas locas pero geniales</li>
        <li>Tu forma de escucharme</li>
        <li>Tus historias que me atrapan</li>
        <li>Tus consejos llenos de sabiduría</li>
      </ol>
      <button class="primary-btn" onclick="goToScreen2()">Siguiente ❤️</button>
    </div>

    <!-- PANTALLA 2: Segundas 50 razones -->
    <div id="screen2" class="screen hidden">
      <div class="interm-message">
        50 razones son muy pocas así que ten 50 razones más 💕
      </div>
      <ol class="reasons-list" start="51">
        <li>Tu dedicación a lo que amas</li>
        <li>Tu manera de ver lo positivo</li>
        <li>Tus gustos que compartimos</li>
        <li>Tus palabras que inspiran</li>
        <li>Tus manías que adoro</li>
        <li>Tus errores que te hacen humana</li>
        <li>Tu constancia en todo</li>
        <li>Tu habilidad de ser única</li>
        <li>Tu esencia que no se compara</li>
        <li>Tu calidez que me envuelve</li>
        <li>Tu sentido de la justicia</li>
        <li>Tu amor por la vida</li>
        <li>Tus sueños que me motivan</li>
        <li>Tus metas que me inspiran</li>
        <li>Tu curiosidad insaciable</li>
        <li>Tu deseo de mejorar</li>
        <li>Tu honestidad con los demás</li>
        <li>Tu orgullo por lo que haces</li>
        <li>Tu fortaleza en los momentos difíciles</li>
        <li>Tu conexión con el mundo</li>
        <li>Tu fe en el amor</li>
        <li>Tus pequeñas locuras</li>
        <li>Tu amor por los detalles</li>
        <li>Tu risa cuando estamos solos</li>
        <li>Tu forma de hacerme sentir especial</li>
        <li>Tu manera de iluminar cualquier lugar</li>
        <li>Tu sinceridad en todo momento</li>
        <li>Tus palabras cuando más las necesito</li>
        <li>Tu silencio que me comprende</li>
        <li>Tu amor por las pequeñas cosas</li>
        <li>Tu felicidad que compartes conmigo</li>
        <li>Tu forma de enseñarme cosas nuevas</li>
        <li>Tus ganas de explorar el mundo</li>
        <li>Tus emociones que compartes</li>
        <li>Tus logros que celebro contigo</li>
        <li>Tu habilidad de adaptarte</li>
        <li>Tu fortaleza para seguir adelante</li>
        <li>Tu capacidad de sorprenderme cada día</li>
        <li>Tu forma de demostrarme tu amor</li>
        <li>Tus promesas que siempre cumples</li>
        <li>Tu manera de hacerme sentir en casa</li>
        <li>Tus pequeñas locuras que adoro</li>
        <li>Tu valentía para enfrentar tus miedos</li>
        <li>Tu dedicación a lo que amas</li>
        <li>Tus valores que guían tu vida</li>
        <li>Tu compasión por los demás</li>
        <li>Tu habilidad de convertir lo ordinario en especial</li>
        <li>Tu pasión por lo que haces</li>
        <li>Tu amor que no tiene límites</li>
        <li>Tu manera de apoyarme sin juzgar</li>
      </ol>
      <button class="primary-btn" onclick="goToProposal()">Siguiente ❤️</button>
    </div>

    <!-- PANTALLA 3: La Pregunta -->
    <div id="screen3" class="screen hidden">
      <div class="proposal-container" id="proposalArea">
        <h2>¿Quieres ser mi novia? 🌹</h2>
        <p style="color: #666; margin-bottom: 10px;">Prometo quererte y cuidarte cada día...</p>
        <div class="buttons-wrapper" id="buttonArea">
          <button id="btnYes" class="primary-btn" onclick="acceptProposal()">¡SÍ! 💕</button>
          <button id="btnNo">No 😜</button>
        </div>
      </div>
    </div>

    <!-- PANTALLA 4: Respuesta Final con la foto especial elegida -->
    <div id="screen4" class="screen hidden">
      <div class="celebration-icon">💖🎉✨</div>
      <h2>¡Sabía que dirías que sí! 🥰✨</h2>
      
      <div class="final-photo-container">
        <img src="foto1.jpg" alt="Foto especial al decir SÍ">
      </div>

      <p style="font-size: 1.1rem; color: #4a4a4a; margin-top: 15px; line-height: 1.5;">
        Prometo hacerte la persona más feliz del mundo y celebrar cada día a tu lado. ❤️
      </p>
    </div>

  </div>

  <script>
    // Generador de corazones flotantes
    const heartsBg = document.getElementById('heartsBg');
    const heartSymbols = ['❤️', '💖', '💗', '💕', '🌸', '✨'];

    function createHeart() {
      const heart = document.createElement('div');
      heart.classList.add('heart-particle');
      heart.innerHTML = heartSymbols[Math.floor(Math.random() * heartSymbols.length)];
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (Math.random() * 3 + 4) + 's';
      heart.style.fontSize = (Math.random() * 15 + 15) + 'px';
      heartsBg.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 7000);
    }
    setInterval(createHeart, 350);

    // Reproductor de música
    const bgMusic = document.getElementById('bgMusic');
    const musicBtn = document.getElementById('musicBtn');
    let isPlaying = false;

    function toggleMusic() {
      if (isPlaying) {
        bgMusic.pause();
        musicBtn.innerHTML = '🎵';
        isPlaying = false;
      } else {
        bgMusic.play().then(() => {
          musicBtn.innerHTML = '🎶';
          isPlaying = true;
        }).catch(() => {
          alert('Por favor interactúa con la página para reproducir la música.');
        });
      }
    }

    document.body.addEventListener('click', function startAudioOnFirstClick() {
      if (!isPlaying) {
        bgMusic.play().then(() => {
          musicBtn.innerHTML = '🎶';
          isPlaying = true;
        }).catch(() => {});
      }
      document.body.removeEventListener('click', startAudioOnFirstClick);
    });

    // Navegación
    function goToScreen2() {
      switchScreen('screen1', 'screen2');
    }

    function goToProposal() {
      switchScreen('screen2', 'screen3');
      setTimeout(positionNoButtonInitial, 50);
    }

    function acceptProposal() {
      switchScreen('screen3', 'screen4');
      for (let i = 0; i < 40; i++) {
        setTimeout(createHeart, i * 50);
      }
    }

    function switchScreen(fromId, toId) {
      const fromScreen = document.getElementById(fromId);
      const toScreen = document.getElementById(toId);
      
      fromScreen.classList.add('hidden');
      toScreen.classList.remove('hidden');
      toScreen.parentElement.style.animation = 'none';
      void toScreen.parentElement.offsetWidth;
      toScreen.parentElement.style.animation = 'fadeIn 0.6s ease-out';
    }

    // Botón NO evasivo
    const btnNo = document.getElementById('btnNo');
    const buttonArea = document.getElementById('buttonArea');

    function positionNoButtonInitial() {
      btnNo.style.left = '65%';
      btnNo.style.top = '35px';
    }

    function moveNoButton() {
      const containerRect = buttonArea.getBoundingClientRect();
      const btnRect = btnNo.getBoundingClientRect();

      const maxX = containerRect.width - btnRect.width;
      const maxY = containerRect.height - btnRect.height;

      const randomX = Math.floor(Math.random() * Math.max(0, maxX));
      const randomY = Math.floor(Math.random() * Math.max(0, maxY));

      btnNo.style.left = `${randomX}px`;
      btnNo.style.top = `${randomY}px`;
    }

    btnNo.addEventListener('mouseover', moveNoButton);
    btnNo.addEventListener('touchstart', function(e) {
      e.preventDefault();
      moveNoButton();
    });
  </script>
</body>
</html>
