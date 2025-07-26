<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Evolua no Futebol</title>
  <style>
    :root {
      --roxo-escuro: #2a003f;
      --roxo-principal: #4a148c;
      --roxo-hover: #6c28a6;
      --roxo-claro: #e1b0ff;
      --fundo-card: #1a012a;
      --branco: #fff;
      --cinza: #bbb;
    }
    * { box-sizing: border-box; }
    body {
      font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
      background: var(--roxo-escuro);
      color: var(--branco);
      margin: 0;
      padding: 0;
      line-height: 1.8;
      min-height: 100vh;
      transition: background 0.3s;
    }
    header {
      background: var(--roxo-principal);
      padding: 40px 20px 25px 20px;
      text-align: center;
      font-size: 2.2em;
      font-weight: 600;
      letter-spacing: 1.5px;
      color: var(--branco);
      text-transform: uppercase;
      box-shadow: 0 4px 18px rgba(0,0,0,0.6);
    }
    nav {
      display: flex;
      justify-content: center;
      gap: 22px;
      background: var(--roxo-escuro);
      padding: 10px;
      flex-wrap: wrap;
      border-bottom: 1px solid #311252;
      position: sticky;
      top: 0;
      z-index: 10;
    }
    nav a {
      color: var(--roxo-claro);
      text-decoration: none;
      font-weight: 500;
      font-size: 1em;
      padding: 8px 14px;
      border-radius: 18px;
      transition: 
        color 0.25s,
        background 0.25s,
        transform 0.2s;
      position: relative;
    }
    nav a.active, nav a:hover, nav a:focus {
      color: var(--branco);
      background: var(--roxo-hover);
      transform: scale(1.07);
    }
    main {
      display: flex;
      flex-direction: column;
      gap: 32px;
      max-width: 930px;
      margin: 36px auto 18px auto;
      padding: 0 12px;
    }
    section {
      background: var(--fundo-card);
      border-radius: 14px;
      padding: 34px 18px 22px 18px;
      box-shadow: 0 2px 12px rgba(40,8,60,0.18);
      border: 1.5px solid #311252;
      margin-bottom: 0;
      opacity: 0;
      transform: translateY(60px) scale(0.98);
      transition: opacity 0.6s, transform 0.6s;
    }
    section.visible {
      opacity: 1;
      transform: translateY(0) scale(1);
    }
    h2 {
      color: var(--roxo-claro);
      font-weight: 600;
      margin-bottom: 18px;
      font-size: 1.3em;
      text-transform: uppercase;
      letter-spacing: 1px;
      display: flex;
      align-items: center;
      gap: 8px;
    }
    p {
      font-weight: 300;
      color: #ede7f6;
      font-size: 1.04em;
      margin-bottom: 0.6em;
    }
    ul {
      margin-top: 14px;
      padding-left: 22px;
      color: #e0d7f7;
      font-size: 1em;
      list-style: disc inside;
    }
    ul li {
      margin-bottom: 7px;
      transition: color 0.25s;
    }
    .highlight {
      background: var(--roxo-principal);
      padding: 10px 16px;
      border-radius: 8px;
      margin-top: 15px;
      box-shadow: 0 4px 18px rgba(0,0,0,0.24);
      font-size: 0.97em;
      color: #ffe7ff;
      display: flex;
      align-items: center;
      gap: 12px;
      transition: background 0.2s;
    }
    .highlight:hover {
      background: var(--roxo-hover);
    }
    .btn-topo {
      position: fixed;
      right: 16px;
      bottom: 28px;
      background: var(--roxo-principal);
      color: var(--branco);
      border: none;
      border-radius: 50%;
      width: 48px;
      height: 48px;
      font-size: 1.7em;
      cursor: pointer;
      box-shadow: 0 2px 10px rgba(60,0,60,0.14);
      display: flex;
      align-items: center;
      justify-content: center;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.3s, background 0.2s;
      z-index: 15;
    }
    .btn-topo.show {
      opacity: 1;
      pointer-events: auto;
    }
    footer {
      text-align: center;
      padding: 30px 12px 28px 12px;
      font-size: 0.97em;
      color: var(--cinza);
      letter-spacing: 0.4px;
      background: transparent;
      margin-top: 18px;
    }
    /* Animação do menu minimalista */
    nav a::after {
      content: '';
      display: block;
      height: 2px;
      width: 0;
      background: var(--roxo-claro);
      border-radius: 2px;
      transition: width 0.3s;
      margin: 0 auto 0 auto;
    }
    nav a.active::after, nav a:hover::after {
      width: 60%;
    }
    @media (max-width: 700px) {
      header {font-size: 1.3em; padding: 25px 8px 16px 8px;}
      main {padding: 0 4px;}
      section {padding: 20px 7px 13px 7px;}
      .btn-topo {right: 9px; bottom: 14px;}
    }
  </style>
</head>
<body>
  <header>𝙴𝚟𝚘𝚕𝚞𝚊 𝚗𝚘 𝙵𝚞𝚝𝚎𝚋𝚘𝚕</header>
  <nav id="nav">
    <a href="#alimentacao">Alimentação</a>
    <a href="#fisico">Físico</a>
    <a href="#tecnico">Técnico</a>
    <a href="#mental">Mental</a>
    <a href="#criativo">Criativo</a>
    <a href="https://instagram.com/seu_usuario" target="_blank" title="Instagram">Instagram</a>
  </nav>
  <main>
    <section id="alimentacao">
      <h2>🍎 Boa Alimentação</h2>
      <p>Uma nutrição correta garante mais energia, menos lesões e maior rendimento. Jogadores como Cristiano Ronaldo, Messi e Lewandowski seguem planos alimentares rígidos.</p>
      <ul>
        <li><strong>Cristiano Ronaldo:</strong> frango grelhado, saladas variadas e muita água durante o dia.</li>
        <li><strong>Lewandowski:</strong> evita alimentos processados e prioriza proteínas de alta qualidade.</li>
        <li><strong>Messi:</strong> usa shakes naturais no pós-treino para acelerar a recuperação.</li>
      </ul>
      <div class="highlight">
        💡 <strong>Dica:</strong> Prepare refeições simples em casa, como omelete com legumes e arroz integral. Hidrate-se sempre!
      </div>
    </section>
    <section id="fisico">
      <h2>💪 Treino Físico</h2>
      <p>O preparo físico transforma um bom jogador em um craque. Mbappé investe em velocidade e resistência, enquanto Haaland foca na força e impulsão.</p>
      <ul>
        <li><strong>Mbappé:</strong> séries de tiros curtos e escadas de agilidade.</li>
        <li><strong>Haaland:</strong> treinos de salto, agachamentos e pliometria.</li>
        <li><strong>Kevin De Bruyne:</strong> treino funcional com cordas e pesos.</li>
      </ul>
      <div class="highlight">
        💡 <strong>Dica sem equipamento:</strong> Use a rua ou o quintal para correr e fazer polichinelos, flexões e abdominais.
      </div>
    </section>
    <section id="tecnico">
      <h2>⚽ Treino Técnico</h2>
      <p>A técnica é a linguagem do futebol. Neymar e Modrić dedicam horas a controles e dribles.</p>
      <ul>
        <li><strong>Neymar:</strong> dribles em espaço reduzido para criar agilidade.</li>
        <li><strong>Modrić:</strong> prática diária de passes curtos e longos com ambos os pés.</li>
        <li><strong>Pedri:</strong> treinos de recepção rápida sob pressão.</li>
      </ul>
      <div class="highlight">
        💡 <strong>Dica:</strong> Treine passes contra a parede, controle e domínio com qualquer bola disponível.
      </div>
    </section>
    <section id="mental">
      <h2>🧠 Treino Mental</h2>
      <p>A força mental decide jogos. Casemiro e Iniesta mantêm o foco com meditação e análise de jogos.</p>
      <ul>
        <li><strong>Casemiro:</strong> meditação antes dos treinos para clarear a mente.</li>
        <li><strong>Iniesta:</strong> revisa vídeos para melhorar tomada de decisão.</li>
        <li><strong>Kroos:</strong> mantém um diário de progresso pessoal.</li>
      </ul>
      <div class="highlight">
        💡 <strong>Dica:</strong> Antes de treinar, respire fundo por 2 minutos e visualize suas jogadas ideais.
      </div>
    </section>
    <section id="criativo">
      <h2>🎨 Treino Criativo</h2>
      <p>Criar o inesperado é o segredo de craques como Ronaldinho e Vinícius Jr.</p>
      <ul>
        <li><strong>Ronaldinho:</strong> inventava dribles em treinos recreativos.</li>
        <li><strong>Vinícius Jr:</strong> treina mudanças rápidas de direção.</li>
        <li><strong>Foden:</strong> utiliza cones para criar trajetórias novas.</li>
      </ul>
      <div class="highlight">
        💡 <strong>Dica:</strong> Treine com amigos desafios criativos, como driblar em espaços reduzidos ou criar jogadas diferentes.
      </div>
    </section>
  </main>
  <button class="btn-topo" aria-label="Voltar ao topo" id="btnTop" title="Voltar ao topo">↑</button>
  <footer>
    <p>© 2025 Evolua no Futebol — Mais Dicas, Mais Performance</p>
  </footer>
  <script>
    // Scroll reveal minimalista
    function revealSections() {
      const sections = document.querySelectorAll('section');
      const windowHeight = window.innerHeight;
      sections.forEach(section => {
        const sectionTop = section.getBoundingClientRect().top;
        if (sectionTop < windowHeight - 90) {
          section.classList.add('visible');
        }
      });
    }
    window.addEventListener('scroll', revealSections);
    window.addEventListener('DOMContentLoaded', revealSections);

    // Menu ativo ao rolar/interagir
    const navLinks = document.querySelectorAll('nav a[href^="#"]');
    function setActiveMenu() {
      let scrollPos = window.scrollY + 120;
      navLinks.forEach(link => {
        let refSection = document.querySelector(link.getAttribute('href'));
        if (
          refSection &&
          refSection.offsetTop <= scrollPos &&
          refSection.offsetTop + refSection.offsetHeight > scrollPos
        ) {
          link.classList.add('active');
        } else {
          link.classList.remove('active');
        }
      });
    }
    window.addEventListener('scroll', setActiveMenu);
    window.addEventListener('DOMContentLoaded', setActiveMenu);

    // Navegação suave
    navLinks.forEach(link => {
      link.addEventListener('click', function(e) {
        if (this.hash) {
          e.preventDefault();
          document.querySelector(this.hash).scrollIntoView({behavior: 'smooth'});
        }
      });
    });

    // Botão de voltar ao topo
    const btnTop = document.getElementById('btnTop');
    window.addEventListener('scroll', () => {
      if (window.scrollY > 300) {
        btnTop.classList.add('show');
      } else {
        btnTop.classList.remove('show');
      }
    });
    btnTop.addEventListener('click', () => {
      window.scrollTo({top: 0, behavior: 'smooth'});
    });

    // Interação nas dicas (highlight)
    document.querySelectorAll('.highlight').forEach(el => {
      el.setAttribute('tabindex', '0');
      el.addEventListener('focus', function() {
        this.style.background = '#6c28a6';
      });
      el.addEventListener('blur', function() {
        this.style.background = '';
      });
      el.addEventListener('keydown', function(e){
        if(e.key==='Enter'||e.key===' '){
          this.classList.toggle('highlight--active');
        }
      });
    });
  </script>
</body>
</html>
