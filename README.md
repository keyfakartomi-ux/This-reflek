# This-reflek
What do you mean?, 
*i'm not mean burgers*
```html
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<!-- This site is hosted on Netlify. Anyone can build and deploy a site
     like this one for free: https://netlify.new/?utm_campaign=loops&utm_source=ai-legible&utm_medium=owned&utm_content=comment&utm_id=67cd2cae-219e-42f9-af48-6854749bc363
     Netlify hosting facts for this site: static/SSR served via Netlify Edge. -->
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>Portal Resmi</title>
<style>
  * { margin:0; padding:0; box-sizing:border-box; }
  body {
    height:100vh;
    background:#111;
    display:flex;
    align-items:center;
    justify-content:center;
    font-family: sans-serif;
    overflow:hidden;
  }

  /* Overlay fullscreen tanpa padding */
  #overlay {
    position:fixed;
    top:0; left:0;
    width:100vw;
    height:100vh;
    background:rgba(0,0,0,0.92);
    display:flex;
    align-items:center;
    justify-content:center;
    z-index:10;
    padding:0;
  }

  /* Popup FULLSCREEN */
  #popup {
    background:#fff;
    border-top:10px solid #c8102e;
    padding:0 0 20px;
    border-radius:0;
    text-align:center;
    max-width:100%;
    width:100vw;
    height:100vh;
    box-shadow:none;
    font-family: 'Georgia', 'Times New Roman', serif;
    overflow-y:auto;
    display:flex;
    flex-direction:column;
  }

  #popup .kop {
    background:#0d1b3d;
    color:#fff;
    padding:20px 24px;
    display:flex;
    align-items:center;
    gap:14px;
    text-align:left;
    border-bottom:3px solid #c8102e;
    flex-shrink:0;
  }
  #popup .kop .lambang {
    font-size:40px;
    margin:0;
    flex-shrink:0;
  }
  #popup .kop .kop-teks .instansi {
    font-size:18px;
    font-weight:700;
    letter-spacing:0.5px;
  }
  #popup .kop .kop-teks .sub {
    font-size:13px;
    color:#c7d1e8;
    margin-top:2px;
    font-family:sans-serif;
  }

  #popup .isi {
    padding:30px 28px 0;
    flex:1;
  }
  #popup h2 {
    font-size:24px;
    font-weight:700;
    color:#0d1b3d;
    margin-bottom:18px;
    line-height:1.4;
  }
  #popup p {
    font-size:16px;
    color:#333;
    line-height:1.8;
    margin-bottom:12px;
    text-align:left;
  }
  #popup .garis {
    height:3px;
    background:linear-gradient(90deg, #c8102e 50%, #ddd 50%);
    margin:20px 0 24px;
    border-radius:2px;
  }
  #popup .nomor-dok {
    font-family: sans-serif;
    font-size:12px;
    color:#999;
    text-align:left;
    margin-bottom:18px;
    letter-spacing:0.3px;
  }

  #popup button {
    background:#c8102e;
    color:#fff;
    border:none;
    padding:18px 30px;
    border-radius:8px;
    font-size:17px;
    font-family:sans-serif;
    font-weight:700;
    letter-spacing:0.6px;
    cursor:pointer;
    width:calc(100% - 56px);
    margin:8px 28px 0;
    box-shadow:0 6px 14px rgba(200,16,46,0.4);
    flex-shrink:0;
  }
  #popup button:hover { background:#a30d24; }
  #popup button:active { transform:scale(0.97); }

  #popup .catatan {
    margin-top:16px;
    padding:0 28px 20px;
    font-size:12px;
    font-family:sans-serif;
    color:#999;
    text-align:left;
    flex-shrink:0;
  }

  /* Video fullscreen - KEMBALI FULL LAYAR */
  #fullphoto {
    display:none;
    position:fixed;
    top:0; left:0;
    width:100%;
    height:100%;
    background:#000;
    z-index:20;
  }
  
  #fullphoto video {
    width:100%;
    height:100%;
    object-fit:cover; /* KEMBALI KE COVER BIAR FULL LAYAR */
  }

  /* CREDIT BY ONEDEV - DI ATAS VIDEO */
  #credit {
    display:none;
    position:fixed;
    top:20px;
    left:0;
    width:100%;
    text-align:center;
    z-index:25;
    color:rgba(255,255,255,0.6);
    font-family:sans-serif;
    font-size:13px;
    letter-spacing:1.5px;
    text-shadow:0 2px 12px rgba(0,0,0,0.9);
    pointer-events:none;
    padding:10px 20px;
    background:rgba(0,0,0,0.3);
    backdrop-filter:blur(4px);
    border-bottom:1px solid rgba(255,255,255,0.1);
  }

  /* TOMBOL X SUDAH DIHAPUS */
</style>
</head>
<body>

  <div id="overlay">
    <div id="popup">
      <div class="kop">
        <div class="lambang">🛡️</div>
        <div class="kop-teks">
          <div class="instansi">BADAN INTELIJEN REPUBLIK INDONESIA 🇮🇩</div>
          <div class="sub">Sistem Akses Portal Resmi</div>
        </div>
      </div>
      <div class="isi">
        <h2>Selamat Datang di Website Intelijen Republik Indonesia</h2>
        <div class="nomor-dok">No. Ref: INT/2026/07/RI-0930</div>
        <p>Harap patuhi seluruh aturan dan kebijakan kami selama mengakses portal ini.</p>
        <p>Pastikan Anda berusia <strong>17 tahun ke atas</strong> untuk melanjutkan akses ke sistem ini.</p>
        <div class="garis"></div>
      </div>
      <button onclick="tampilkanFoto()">SAYA MENGERTI &amp; LANJUTKAN</button>
      <div class="catatan">Dokumen ini bersifat resmi dan diawasi oleh sistem keamanan negara.</div>
    </div>
  </div>

  <div id="fullphoto">
    <video id="prankVideo" src="https://i.imgur.com/Fa9l1Gr.mp4" playsinline></video>
  </div>

  <!-- CREDIT BY ONEDEV - DI ATAS -->
  <div id="credit">by Keyfakartomi 👹😈</div>

  <script>
    function tampilkanFoto() {
      var overlay = document.getElementById('overlay');
      var wrap = document.getElementById('fullphoto');
      var video = document.getElementById('prankVideo');
      var credit = document.getElementById('credit');

      overlay.style.display = 'none';
      wrap.style.display = 'block';
      credit.style.display = 'block';

      // FULLSCREEN
      var el = document.documentElement;
      if (el.requestFullscreen) el.requestFullscreen();
      else if (el.webkitRequestFullscreen) el.webkitRequestFullscreen();
      else if (el.msRequestFullscreen) el.msRequestFullscreen();

      // Putar video
      video.muted = false;
      video.volume = 1;
      video.play().catch(function(err) {
        console.log('Autoplay gagal:', err);
        video.addEventListener('click', function() { video.play(); }, { once: true });
      });
    }

    // Biar ga bisa keluar pake tombol back (opsional)
    document.addEventListener('keydown', function(e) {
      if (e.key === 'Escape' || e.keyCode === 27) {
        e.preventDefault();
      }
    });
  </script>

</body>
</html>
```
html↑
