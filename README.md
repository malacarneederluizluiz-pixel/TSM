# TSM
Nossa empresa esta disposta a levar a sua a sucesso, confira nossas mensalidades ! 
<!--
  Site de Amor - arquivo HTML completo
  Instruções: abra este arquivo no navegador (salve como "amor.html").
  Personalize: procure no código por: {{NOME}} , {{NOME_DESTINATARIO}}, {{MENSAGEM}}, e troque por nomes e texto próprios.
  Para adicionar música: substitua o atributo src do elemento <audio> por um arquivo .mp3 local ou URL.
-->

<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Uma Página Para Você 💌</title>
  <meta name="description" content="Uma página criada com carinho para demonstrar amor.">
  <style>
    :root{
      --bg:#0f1724; --card:#0b1220; --accent:#ff6b81; --muted:#9aa4b2; --glass: rgba(255,255,255,0.04);
      --maxw:980px; --radius:18px;
      --g: linear-gradient(135deg,#ff6b81 0%, #ff9a66 50%, #ffd36e 100%);
      --font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family:var(--font-family); background:radial-gradient(circle at 10% 10%, rgba(255,107,129,0.06), transparent 10%), var(--bg); color:#e6eef6; -webkit-font-smoothing:antialiased; padding:40px 16px;
      display:flex; align-items:center; justify-content:center;
    }
    .wrap{width:100%; max-width:var(--maxw); background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); border-radius:20px; padding:28px; box-shadow: 0 10px 30px rgba(2,6,23,0.7); border:1px solid rgba(255,255,255,0.03)}

    header{display:flex; gap:16px; align-items:center}
    .logo{width:84px; height:84px; border-radius:16px; display:flex; align-items:center; justify-content:center; background:var(--g); color:#111; font-weight:700; font-size:22px}
    .title h1{margin:0; font-size:22px}
    .title p{margin:4px 0 0; color:var(--muted); font-size:14px}

    main{display:grid; grid-template-columns:1fr 360px; gap:20px; margin-top:20px}
    @media (max-width:920px){ main{grid-template-columns:1fr} .side{order:2} }

    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); padding:20px; border-radius:var(--radius); border:1px solid rgba(255,255,255,0.03)}

    .hero{min-height:320px; display:flex; flex-direction:column; gap:18px}
    .heart{align-self:center; width:170px; height:170px; border-radius:50%; background:var(--glass); display:flex; align-items:center; justify-content:center; position:relative;}
    .heart:after{content:''; position:absolute; width:120px; height:120px; background:var(--g); clip-path: path('M10 30 C 10 15, 25 0, 50 20 C 75 0, 90 15, 90 30 C 90 70, 50 95, 50 95 C 50 95, 10 70, 10 30 Z'); opacity:0.95; border-radius:50%; transform:scale(1) rotate(-10deg);}
    .hero h2{margin:0; text-align:center; font-size:24px}
    .hero p{margin:0; text-align:center; color:var(--muted)}

    .letter{margin-top:6px; line-height:1.6; font-size:16px}

    .actions{display:flex; gap:8px; align-items:center; justify-content:center; margin-top:12px}
    .btn{padding:10px 14px; border-radius:12px; border:none; cursor:pointer; background:transparent; color:inherit; border:1px solid rgba(255,255,255,0.06)}
    .btn.primary{background:var(--g); color:#111; font-weight:600; box-shadow:0 6px 18px rgba(255,107,129,0.12)}
    .btn.ghost{background:transparent}

    .side{display:flex; flex-direction:column; gap:14px}
    .small{font-size:13px; color:var(--muted)}

    .poem{white-space:pre-wrap; font-style:italic; font-size:15px}

    .gallery{display:grid; grid-template-columns:repeat(2,1fr); gap:8px}
    .thumb{height:90px; border-radius:12px; background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); display:flex; align-items:center; justify-content:center; color:var(--muted); font-weight:600}

    footer{margin-top:18px; display:flex; gap:8px; align-items:center; justify-content:space-between; color:var(--muted); font-size:13px}

    /* Timeline */
    .timeline{display:flex; flex-direction:column; gap:12px}
    .event{display:flex; gap:12px; align-items:flex-start}
    .event .dot{width:12px; height:12px; border-radius:50%; background:var(--accent); margin-top:6px}
    .event .meta{font-size:14px}

    /* Modal */
    .modal{position:fixed; inset:0; display:none; align-items:center; justify-content:center; z-index:40}
    .modal.show{display:flex}
    .modal .panel{width:90%; max-width:720px; background:#071021; padding:22px; border-radius:14px; border:1px solid rgba(255,255,255,0.03)}

    /* confetti */
    .confetti{position:fixed; inset:0; pointer-events:none; z-index:30}

    /* small form */
    .form-row{display:flex; gap:8px}
    input[type=text], textarea{width:100%; padding:10px; border-radius:10px; background:transparent; border:1px solid rgba(255,255,255,0.04); color:inherit}

    .credit{font-size:12px; color:var(--muted)}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="logo">💖</div>
      <div class="title">
        <h1>Uma Página Especial</h1>
        <p>Feita com carinho para alguém importante — personalize como quiser.</p>
      </div>
    </header>

    <main>
      <section class="card">
        <div class="hero">
          <div class="heart" aria-hidden></div>
          <h2>Para {{NOME_DESTINATARIO}}</h2>
          <p class="small">De: <strong>{{Luiz Eduardo TSM}}</strong> • <span class="small">Data: <span id="today"></span></span></p>

          <div class="letter">
            <p id="letterText">{{Voce é minha inspiração}}
            </p>
          </div>

          <div class="actions">
            <button class="btn primary" id="openLove">Ler Carta Completa</button>
            <button class="btn ghost" id="togglePoem">Ver Poema</button>
            <button class="btn" id="surprise">Surpresa</button>
          </div>
        </div>

        <div class="timeline card" style="margin-top:16px">
          <div class="small">Nossa história</div>
          <div class="event"><div class="dot"></div><div class="meta"><strong>O dia em que nos conhecemos</strong><div class="small">Um momento que mudou tudo.</div></div></div>
          <div class="event"><div class="dot"></div><div class="meta"><strong>Primeira conversa</strong><div class="small">Rimos do mesmo meme.</div></div></div>
          <div class="event"><div class="dot"></div><div class="meta"><strong>Hoje</strong><div class="small">Ainda me encanta pensar em você.</div></div></div>
        </div>

      </section>

      <aside class="side">
        <div class="card">
          <div class="small">Poema</div>
          <div class="poem" id="poemBlock">Eu te vejo nas pequenas coisas —
no café da manhã, no pôr do sol, no silêncio que fala entre nós.

Você é calma e tempestade, lar e viagem. 
Eu sou grato por cada segundo.</div>
          <div style="margin-top:12px; display:flex; gap:8px">
            <button class="btn" id="copyPoem">Copiar Poema</button>
            <button class="btn" id="downloadNote">Baixar Nota</button>
          </div>
        </div>

        <div class="card">
          <div class="small">Galeria</div>
          <div class="gallery" id="gallery">
            <div class="thumb">Foto 1</div>
            <div class="thumb">Foto 2</div>
            <div class="thumb">Foto 3</div>
            <div class="thumb">Foto 4</div>
          </div>
          <p class="small" style="margin-top:8px">Dica: substitua as "thumbs" por imagens suas (use <code>&lt;img src="seuarquivo.jpg"&gt;</code>).</p>
        </div>

        <div class="card">
          <div class="small">Escreva algo para ela/ele</div>
          <div style="margin-top:8px">
            <div class="form-row"><input id="senderName" type="text" placeholder="Seu nome"></div>
            <div style="margin-top:8px"><textarea id="quickMsg" rows="3" placeholder="Escreva uma mensagem rápida..."></textarea></div>
            <div style="margin-top:8px; display:flex; gap:8px"><button class="btn primary" id="sendMail">Enviar por E-mail</button><button class="btn" id="showModal">Mostrar com Confete</button></div>
          </div>
        </div>

      </aside>

    </main>

    <footer>
      <div class="credit">Criei esta página especialmente — personalize o texto e as imagens.</div>
      <div class="small">Made with ❤️</div>
    </footer>
  </div>

  <!-- Modal -->
  <div class="modal" id="modal">
    <div class="panel">
      <h3>Carta</h3>
      <p id="modalText"></p>
      <div style="margin-top:12px; display:flex; gap:8px; justify-content:flex-end"><button class="btn" id="closeModal">Fechar</button></div>
    </div>
  </div>

  <canvas class="confetti" id="confetti"></canvas>

  <!-- Optional audio: troque o src por uma música sua (mp3). -->
  <audio id="song" src="" preload="none"></audio>

  <script>
    // --- Personalize facilmente: altere estas variáveis ---
    const NOME_DESTINATARIO = 'Amor';
    const SEU_NOME = 'Seu Nome';
    const MENSAGEM = `Meu amor,

Cada dia ao seu lado me lembra porque meu coração escolheu você. 

Com carinho,
${SEU_NOME}`;
    // ----------------------------------------------------

    document.getElementById('today').textContent = new Date().toLocaleDateString('pt-BR');
    document.querySelector('h2').textContent = `Para ${NOME_DESTINATARIO}`;
    document.querySelector('.title h1').textContent = `Uma Página Para ${NOME_DESTINATARIO}`;
    document.querySelector('.title p').textContent = `Feita com carinho por ${SEU_NOME}`;
    document.getElementById('letterText').textContent = MENSAGEM;

    // Modal
    const modal = document.getElementById('modal');
    document.getElementById('openLove').addEventListener('click', ()=>{
      document.getElementById('modalText').textContent = MENSAGEM + '\n\nSempre seu.';
      modal.classList.add('show');
      fireConfetti();
    });
    document.getElementById('closeModal').addEventListener('click', ()=> modal.classList.remove('show'));

    // Poem toggle
    const poem = document.getElementById('poemBlock');
    document.getElementById('togglePoem').addEventListener('click', ()=>{
      poem.style.display = poem.style.display==='none'? 'block':'none';
    });

    // Copy poem
    document.getElementById('copyPoem').addEventListener('click', async ()=>{
      try{ await navigator.clipboard.writeText(poem.textContent); alert('Poema copiado!'); }
      catch(e){ alert('Não foi possível copiar.'); }
    });

    // Quick message -> mailto
    document.getElementById('sendMail').addEventListener('click', ()=>{
      const nome = document.getElementById('senderName').value || SEU_NOME;
      const body = document.getElementById('quickMsg').value || 'Pensei em você.';
      const subject = encodeURIComponent(`Uma mensagem de ${nome}`);
      const mailto = `mailto:?subject=${subject}&body=${encodeURIComponent(body)}`;
      window.location.href = mailto;
    });

    // Download a small note (text file)
    document.getElementById('downloadNote').addEventListener('click', ()=>{
      const blob = new Blob([MENSAGEM], {type:'text/plain'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a'); a.href = url; a.download = 'nota-de-amor.txt'; a.click(); URL.revokeObjectURL(url);
    });

    // Surprise button
    document.getElementById('surprise').addEventListener('click', ()=>{
      document.getElementById('modalText').textContent = 'Você me faz querer ser melhor todos os dias.';
      modal.classList.add('show'); fireConfetti();
    });

    // Show modal with confetti
    document.getElementById('showModal').addEventListener('click', ()=>{ document.getElementById('modalText').textContent = document.getElementById('quickMsg').value || 'Um pequeno gesto...'; modal.classList.add('show'); fireConfetti(); });

    // Confetti simple
    function fireConfetti(){
      const c = document.getElementById('confetti');
      const ctx = c.getContext('2d');
      c.width = innerWidth; c.height = innerHeight;
      const pieces = [];
      for(let i=0;i<160;i++){ pieces.push({x:Math.random()*c.width, y:Math.random()*-c.height, r:Math.random()*6+4, s:Math.random()*3+1, rot:Math.random()*360}); }
      let t=0;
      function draw(){ ctx.clearRect(0,0,c.width,c.height); t+=1; for(const p of pieces){ p.y += p.s; p.x += Math.sin((t+p.r)/10); ctx.save(); ctx.translate(p.x,p.y); ctx.rotate(p.rot*Math.PI/180); ctx.fillStyle = `hsl(${(p.r*40)%360} 80% 60%)`; ctx.fillRect(-p.r/2, -p.r/2, p.r, p.r*1.8); ctx.restore(); }
        if(t<220) requestAnimationFrame(draw); else ctx.clearRect(0,0,c.width,c.height);
      }
      draw();
    }

    // Copy and Download helper for the whole page
    document.getElementById('copyPoem').addEventListener('dblclick', ()=>{
      navigator.clipboard.writeText(MENSAGEM).then(()=>alert('Mensagem copiada!'))
    });

    // Accessibility: close modal on ESC
    document.addEventListener('keydown', e=>{ if(e.key==='Escape') modal.classList.remove('show'); });

  </script>
</body>
</html>
