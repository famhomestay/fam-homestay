<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Fam Homestay • Raja Ampat</title>
  <meta name="description" content="Homestay nyaman di Fam, Raja Ampat. Booking mudah, lihat foto, dan tinggalkan komentar." />

  <!-- Font & icon (opsional) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">

  <style>
    :root{
      --primary:#0a7cc4;
      --primary-d:#06649e;
      --bg:#f7fbff;
      --text:#1b1e24;
      --muted:#6b7280;
      --card:#ffffff;
      --ring:rgba(10,124,196,.25);
      --radius:18px;
    }
    *{box-sizing:border-box}
    html,body{margin:0;padding:0;font-family:Inter,system-ui,Segoe UI,Arial,sans-serif;color:var(--text);background:var(--bg)}
    a{color:var(--primary);text-decoration:none}
    a:hover{text-decoration:underline}
    .container{width:min(1100px,90vw);margin-inline:auto}
    header{
      position:sticky;top:0;z-index:20;background:rgba(255,255,255,.9);backdrop-filter:saturate(180%) blur(8px);
      border-bottom:1px solid #eef2f7;
    }
    .nav{display:flex;align-items:center;justify-content:space-between;padding:12px 0}
    .brand{display:flex;gap:.6rem;align-items:center;font-weight:800;letter-spacing:.2px}
    .brand .logo{width:36px;height:36px;border-radius:10px;background:var(--primary);display:grid;place-items:center;color:#fff;font-weight:700}
    .menu{display:flex;gap:18px;font-weight:600}
    .btn{display:inline-flex;align-items:center;gap:8px;border:none;background:var(--primary);color:#fff;padding:12px 16px;border-radius:12px;cursor:pointer;font-weight:700}
    .btn:hover{background:var(--primary-d)}
    .btn-outline{background:#fff;color:var(--primary);border:1px solid var(--primary);}
    .hero{display:grid;grid-template-columns:1.2fr .8fr;gap:28px;padding:36px 0 10px}
    .card{background:var(--card);border:1px solid #e9eef4;border-radius:var(--radius);box-shadow:0 10px 30px rgba(0,0,0,.04)}
    .hero-img{min-height:260px;background:url('images/1.jpg') center/cover no-repeat;border-radius:var(--radius)}
    .hero-copy{padding:26px}
    h1{margin:0 0 10px;font-size:clamp(26px,4vw,40px);line-height:1.1}
    .muted{color:var(--muted)}
    .badges{display:flex;flex-wrap:wrap;gap:10px;margin-top:14px}
    .badge{background:#eef7ff;border:1px solid #d8ecff;color:#0b5e93;padding:6px 10px;border-radius:999px;font-size:.9rem;font-weight:600}

    section{padding:28px 0}
    .section-title{font-size:1.6rem;margin:0 0 14px}
    .grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
    .grid-2{display:grid;grid-template-columns:repeat(2,1fr);gap:18px}
    .feature{padding:16px}
    .feature h3{margin:.2rem 0 .2rem}
    .feature p{margin:.2rem 0;color:var(--muted)}

    /* Gallery */
    .gallery{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}
    .gallery img{width:100%;height:180px;object-fit:cover;border-radius:14px;cursor:zoom-in;border:1px solid #e9eef4}
    @media (max-width:900px){.hero{grid-template-columns:1fr}.grid-3{grid-template-columns:1fr 1fr}.gallery{grid-template-columns:1fr 1fr}}
    @media (max-width:640px){.grid-2{grid-template-columns:1fr}.gallery{grid-template-columns:1fr}}

    /* Booking form */
    form{display:grid;gap:10px}
    label{font-weight:600}
    input,textarea,select{
      border:1px solid #d8e1ec;border-radius:12px;padding:12px;outline:none;background:#fff
    }
    input:focus,textarea:focus,select:focus{border-color:var(--primary);box-shadow:0 0 0 4px var(--ring)}
    .two{display:grid;grid-template-columns:1fr 1fr;gap:10px}
    @media (max-width:640px){.two{grid-template-columns:1fr}}

    /* Lightbox modal */
    .lightbox{position:fixed;inset:0;background:rgba(0,0,0,.8);display:none;align-items:center;justify-content:center;z-index:50}
    .lightbox img{max-width:92vw;max-height:86vh;border-radius:12px;box-shadow:0 10px 40px rgba(0,0,0,.6)}
    .lightbox.active{display:flex}
    .close{position:fixed;top:18px;right:18px;background:#fff;border:none;border-radius:999px;padding:10px 12px;cursor:pointer;font-weight:800}

    footer{padding:28px 0;color:var(--muted)}
    .wa{
      position:fixed;right:16px;bottom:16px;background:#25D366;color:#fff;border:none;
      border-radius:999px;padding:12px 14px;font-weight:800;box-shadow:0 8px 18px rgba(37,211,102,.4);z-index:30
    }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <div class="brand">
        <div class="logo">FH</div>
        <div>Fam Homestay • Raja Ampat</div>
      </div>
      <nav class="menu">
        <a href="#tentang">Tentang</a>
        <a href="#galeri">Galeri</a>
        <a href="#booking">Booking</a>
        <a href="#komentar">Komentar</a>
      </nav>
      <a class="btn" href="#booking">Booking Sekarang</a>
    </div>
  </header>

  <main class="container">

    <!-- HERO -->
    <section class="hero">
      <div class="hero-img card" aria-label="Foto hero homestay"></div>
      <div class="hero-copy card">
        <h1>Nyaman, Bersih, & Ramah — di Fam, Raja Ampat</h1>
        <p class="muted">Nikmati ketenangan kepulauan Fam. Sarapan lokal, tur snorkling, dan pemandangan laut biru menunggu Anda.</p>
        <div class="badges">
          <span class="badge">Dekat spot snorkeling</span>
          <span class="badge">Free kopi/teh</span>
          <span class="badge">Antar-jemput boat*</span>
        </div>
        <div style="margin-top:16px;display:flex;gap:10px">
          <a class="btn" href="#booking">Cek Ketersediaan</a>
          <a class="btn btn-outline" href="#galeri">Lihat Foto</a>
        </div>
      </div>
    </section>

    <!-- FASILITAS -->
    <section id="tentang">
      <h2 class="section-title">Fasilitas & Layanan</h2>
      <div class="grid-3">
        <div class="card feature">
          <h3>Kamar Bersih</h3>
          <p>Tempat tidur nyaman, kipas/AC (opsional), handuk & linen bersih.</p>
        </div>
        <div class="card feature">
          <h3>Makan Pagi</h3>
          <p>Sarapan sederhana khas kampung pesisir, kopi/teh sepanjang hari.</p>
        </div>
        <div class="card feature">
          <h3>Tur Lokal</h3>
          <p>Atur trip Piaynemo, snorkeling, memancing, dan jelajah pulau.</p>
        </div>
      </div>
    </section>

    <!-- GALERI -->
    <section id="galeri">
      <h2 class="section-title">Galeri Foto</h2>
      <div class="gallery">
        <!-- Ganti sumber gambar di bawah sesuai file dalam folder /images -->
        <img src="images/1.jpg" alt="Kamar tidur" />
        <img src="images/2.jpg" alt="Ruang makan" />
        <img src="images/3.jpg" alt="Pemandangan depan homestay" />
        <img src="images/4.jpg" alt="Dermaga dan laut" />
        <img src="images/5.jpg" alt="Kamar mandi" />
        <img src="images/6.jpg" alt="Perahu untuk tur" />
      </div>
    </section>

    <!-- BOOKING -->
    <section id="booking">
      <h2 class="section-title">Booking / Cek Ketersediaan</h2>
      <div class="card" style="padding:16px">
        <!-- ACTION: Ganti email di bawah menjadi email Anda -->
        <form action="https://formsubmit.co/your@email.com" method="POST">
          <!-- Pengaturan FormSubmit -->
          <input type="hidden" name="_subject" value="Booking Baru - Fam Homestay">
          <input type="hidden" name="_captcha" value="false">
          <input type="hidden" name="_template" value="table">
          <!-- URL setelah sukses -->
          <input type="hidden" name="_next" value="https://famhomestay.github.io/fam-homestay/#terima-kasih">

          <div class="two">
            <div>
              <label>Nama Lengkap</label>
              <input type="text" name="nama" required>
            </div>
            <div>
              <label>Email</label>
              <input type="email" name="email" required>
            </div>
          </div>

          <div class="two">
            <div>
              <label>No. Whatsapp</label>
              <input type="tel" name="whatsapp" placeholder="+628xxxxxxxxxx" required>
            </div>
            <div>
              <label>Jumlah Tamu</label>
              <input type="number" name="tamu" min="1" value="2" required>
            </div>
          </div>

          <div class="two">
            <div>
              <label>Check-in</label>
              <input type="date" name="checkin" required>
            </div>
            <div>
              <label>Check-out</label>
              <input type="date" name="checkout" required>
            </div>
          </div>

          <div>
            <label>Paket / Catatan</label>
            <textarea name="catatan" rows="4" placeholder="Contoh: butuh antar-jemput boat, sewa snorkel, dll."></textarea>
          </div>

          <button type="submit" class="btn">Kirim Permintaan Booking</button>
          <p class="muted" style="margin:8px 0 0">Kami akan membalas via WhatsApp/Email dalam waktu singkat.</p>
        </form>
      </div>
    </section>

    <section id="terima-kasih" style="display:none">
      <h2>Terima kasih!</h2>
      <p>Permintaan booking Anda sudah terkirim. Kami akan menghubungi Anda segera.</p>
    </section>

    <!-- KOMENTAR -->
    <section id="komentar">
      <h2 class="section-title">Komentar & Testimoni</h2>
      <div class="card" style="padding:8px">
        <!-- Utterances: komentar berbasis GitHub Issues.
             1) Pastikan repo punya "Issues" aktif.
             2) Ubah repo di bawah jika perlu. -->
        <script src="https://utteranc.es/client.js"
          repo="famhomestay/fam-homestay"
          issue-term="url"
          label="komentar"
          theme="github-light"
          crossorigin="anonymous"
          async>
        </script>
        <p class="muted" style="padding:12px">
          *Untuk berkomentar, pengguna perlu login GitHub. Jika ingin komentar tanpa GitHub, nanti bisa diganti ke layanan lain.
        </p>
      </div>
    </section>

  </main>

  <footer class="container">
    <hr style="border:none;border-top:1px solid #e9eef4;margin:0 0 14px">
    <div class="grid-2">
      <div>
        <strong>Fam Homestay</strong><br>
        Kampung Fam, Raja Ampat, Papua Barat Daya<br>
        WhatsApp: <a href="https://wa.me/6281234567890" target="_blank">+62 812-3456-7890</a><br>
        Email: <a href="mailto:info@famhomestay.id">info@famhomestay.id</a>
      </div>
      <div class="muted" style="text-align:right">
        © <span id="y"></span> Fam Homestay. All rights reserved.
      </div>
    </div>
  </footer>

  <!-- Tombol WhatsApp melayang -->
  <a class="wa" href="https://wa.me/6281234567890?text=Halo%20Fam%20Homestay%2C%20saya%20ingin%20tanya%20ketersediaan." target="_blank">Chat WhatsApp</a>

  <!-- LIGHTBOX (untuk galeri) -->
  <div class="lightbox" id="lightbox">
    <button class="close" aria-label="Tutup" onclick="hideLightbox()">✕</button>
    <img id="lightboxImg" alt="">
  </div>

  <script>
    // tahun footer
    document.getElementById('y').textContent = new Date().getFullYear();

    // lightbox galeri
    const lb = document.getElementById('lightbox');
    const lbImg = document.getElementById('lightboxImg');
    document.querySelectorAll('.gallery img').forEach(img=>{
      img.addEventListener('click', ()=>{
        lbImg.src = img.src;
        lb.classList.add('active');
      });
    });
    function hideLightbox(){ lb.classList.remove('active'); lbImg.src=''; }
    lb.addEventListener('click', (e)=>{ if(e.target===lb) hideLightbox(); });

    // tampilkan pesan terima kasih setelah redirect FormSubmit
    if(location.hash==="#terima-kasih"){
      document.getElementById('terima-kasih').style.display='block';
      window.scrollTo({top:document.getElementById('terima-kasih').offsetTop-60,behavior:'smooth'});
    }
  </script>
</body>
</html>