<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />

  <title>Fam Homestay • Raja Ampat</title>
  <meta name="description" content="Fam Homestay di Waigeo Barat Kepulauan, Raja Ampat. Booking mudah, lihat foto, dan baca ulasan tamu.">

  <!-- Open Graph / Social -->
  <meta property="og:title" content="Fam Homestay • Raja Ampat">
  <meta property="og:description" content="Nginep nyaman, bersih, ramah. Booking mudah via WhatsApp.">
  <meta property="og:type" content="website">
  <meta property="og:image" content="images/1.jpg"> <!-- TODO: ganti -->

  <!-- Favicons (optional) -->
  <link rel="icon" href="favicon.ico">

  <style>
    :root{
      --primary:#0077b6; --primary2:#0096c7; --dark:#023e8a;
      --bg:#f5fbff; --card:#ffffff; --text:#102a43; --muted:#6b7280;
      --radius:18px; --ring: 0 0 0 4px rgba(0,150,199,.18);
    }
    *{box-sizing:border-box}
    html,body{margin:0;padding:0;font-family:system-ui,Segoe UI,Roboto,Arial,sans-serif;background:var(--bg);color:var(--text)}
    img{max-width:100%;display:block}
    a{color:var(--primary2);text-decoration:none}
    a:hover{text-decoration:underline}
    .container{width:min(1100px,92vw);margin-inline:auto}
    header{position:sticky;top:0;z-index:40;background:#ffffffcc;backdrop-filter:saturate(180%) blur(8px);border-bottom:1px solid #e7eef6}
    .nav{display:flex;align-items:center;justify-content:space-between;padding:12px 0}
    .brand{display:flex;align-items:center;gap:.6rem;font-weight:800}
    .logo{width:36px;height:36px;border-radius:10px;background:linear-gradient(135deg,var(--primary),var(--primary2));display:grid;place-items:center;color:#fff}
    .menu{display:flex;gap:18px;font-weight:700}
    .btn{display:inline-flex;align-items:center;gap:8px;border:none;background:var(--primary);color:#fff;padding:12px 16px;border-radius:12px;cursor:pointer;font-weight:800}
    .btn:hover{background:var(--dark)}
    .btn-outline{background:#fff;border:1px solid var(--primary);color:var(--primary)}
    .btn-ghost{background:transparent;border:1px dashed #cfeaff;color:var(--dark)}
    .card{background:var(--card);border:1px solid #e6edf5;border-radius:var(--radius);box-shadow:0 10px 30px rgba(0,0,0,.04)}
    section{padding:28px 0}
    h1{margin:.2rem 0 .6rem;font-size:clamp(26px,4vw,40px);line-height:1.15}
    h2{margin:0 0 .6rem}
    .muted{color:var(--muted)}

    /* Hero */
    .hero{display:grid;grid-template-columns:1.15fr .85fr;gap:22px;padding:26px 0 8px}
    .hero-img{min-height:280px;background:url('images/1.jpg') center/cover no-repeat;border-radius:var(--radius)} /* TODO: ganti gambar */
    .hero-copy{padding:20px}
    .badges{display:flex;flex-wrap:wrap;gap:10px;margin-top:10px}
    .badge{background:#eaf6ff;border:1px solid #cfeaff;color:#0b5e93;padding:6px 10px;border-radius:999px;font-weight:700;font-size:.9rem}

    /* Grids */
    .grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
    .grid-2{display:grid;grid-template-columns:repeat(2,1fr);gap:18px}
    .feature{padding:16px}
    .feature h3{margin:.2rem 0 .2rem}
    .feature p{margin:.2rem 0;color:var(--muted)}

    /* Gallery + lightbox */
    .gallery{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}
    .gallery img{width:100%;height:180px;object-fit:cover;border-radius:14px;cursor:zoom-in;border:1px solid #e6edf5}
    .lightbox{position:fixed;inset:0;background:rgba(0,0,0,.88);display:none;align-items:center;justify-content:center;z-index:60}
    .lightbox.active{display:flex}
    .lightbox img{max-width:92vw;max-height:86vh;border-radius:12px;box-shadow:0 10px 40px rgba(0,0,0,.6)}
    .lb-nav{position:fixed;inset-inline:0;top:50%;display:flex;justify-content:space-between;align-items:center;color:#fff;font-size:36px;padding:0 14px;user-select:none}
    .close{position:fixed;top:18px;right:18px;background:#fff;border:none;border-radius:999px;padding:10px 12px;cursor:pointer;font-weight:800}

    /* Form */
    form{display:grid;gap:10px}
    label{font-weight:700}
    input,textarea,select{border:1px solid #d8e1ec;border-radius:12px;padding:12px;outline:none;background:#fff}
    input:focus,textarea:focus,select:focus{border-color:var(--primary2);box-shadow:var(--ring)}
    .two{display:grid;grid-template-columns:1fr 1fr;gap:10px}
    .hint{font-size:.9rem;color:var(--muted)}
    .note{background:#f8fbff;border:1px solid #e3f0ff;padding:12px;border-radius:12px}

    /* Stars */
    .stars{display:inline-flex;gap:6px;font-size:24px;cursor:pointer}
    .stars span{filter:grayscale(1);opacity:.6}
    .stars .active{filter:none;opacity:1;color:#f59e0b}

    footer{padding:28px 0;color:var(--muted)}
    .wa{position:fixed;right:16px;bottom:16px;background:#25D366;color:#fff;border:none;border-radius:999px;padding:12px 14px;font-weight:800;box-shadow:0 8px 18px rgba(37,211,102,.4);z-index:50}

    @media (max-width:900px){.hero{grid-template-columns:1fr}.grid-3{grid-template-columns:1fr 1fr}.gallery{grid-template-columns:1fr 1fr}}
    @media (max-width:640px){.grid-2{grid-template-columns:1fr}.gallery{grid-template-columns:1fr}}
  </style>

  <!-- Schema.org for rich results -->
  <script type="application/ld+json">
  {
    "@context":"https://schema.org",
    "@type":"LodgingBusiness",
    "name":"Fam Homestay",
    "address":{"@type":"PostalAddress","addressLocality":"Waigeo Barat Kepulauan","addressRegion":"Papua Barat Daya","addressCountry":"ID"},
    "telephone":"+62 853-9630-6439",
    "priceRange":"IDR 450k - 600k",
    "url":"https://example.com"  /* TODO: ganti domain jika ada */
  }
  </script>
</head>
<body>
  <header aria-label="Navigasi utama">
    <div class="container nav">
      <div class="brand">
        <div class="logo" aria-hidden="true">FH</div>
        <div>Fam Homestay • Raja Ampat</div>
      </div>
      <nav class="menu">
        <a href="#profil">Profil</a>
        <a href="#galeri">Galeri</a>
        <a href="#booking">Booking</a>
        <a href="#ulasan">Ulasan</a>
      </nav>
      <a class="btn" href="#booking">Booking Sekarang</a>
    </div>
  </header>

  <main class="container">

    <!-- HERO -->
    <section class="hero" id="profil">
      <div class="hero-img" role="img" aria-label="Foto homestay"></div>
      <div class="hero-copy card">
        <h1>Fam Homestay – Nyaman, Bersih, Ramah</h1>
        <p class="muted">Waigeo Barat Kepulauan, Kabupaten Raja Ampat, Papua Barat Daya.</p>
        <div class="badges" aria-label="Keunggulan">
          <span class="badge">Dekat spot snorkeling</span>
          <span class="badge">Antar-jemput boat*</span>
          <span class="badge">Kopi & teh free</span>
        </div>
        <div style="margin-top:14px;display:flex;gap:10px;flex-wrap:wrap">
          <a class="btn" href="#booking">Cek Ketersediaan</a>
          <a class="btn btn-outline" href="#galeri">Lihat Foto</a>
        </div>
      </div>
    </section>

    <!-- FASILITAS & HARGA -->
    <section aria-labelledby="fasilitasTitle">
      <h2 id="fasilitasTitle">Fasilitas & Harga</h2>
      <div class="grid-3">
        <div class="card feature">
          <h3>Kamar Biasa</h3>
          <p>Rp 450.000 / malam</p>
          <p class="hint">Kipas angin, kasur double, sarapan.</p>
        </div>
        <div class="card feature">
          <h3>Kamar VIP</h3>
          <p>Rp 600.000 / malam</p>
          <p class="hint">Kamar lebih luas, view laut.</p>
        </div>
        <div class="card feature">
          <h3>Layanan Tambahan</h3>
          <p>Trip Piaynemo, snorkeling, memancing, & antar-jemput bandara/pelabuhan.</p>
        </div>
      </div>
    </section>

    <!-- GALERI -->
    <section id="galeri" aria-labelledby="galeriTitle">
      <h2 id="galeriTitle">Galeri Foto</h2>
      <div class="card" style="padding:14px">
        <div class="gallery" role="list">
          <!-- TODO: ganti src sesuai file di /images -->
          <img src="images/1.jpg" alt="Kamar" loading="lazy" role="listitem"/>
          <img src="images/2.jpg" alt="Pemandangan" loading="lazy" role="listitem"/>
          <img src="images/3.jpg" alt="Ruang makan" loading="lazy" role="listitem"/>
          <img src="images/4.jpg" alt="Dermaga" loading="lazy" role="listitem"/>
          <img src="images/5.jpg" alt="Kamar mandi" loading="lazy" role="listitem"/>
          <img src="images/6.jpg" alt="Perahu tur" loading="lazy" role="listitem"/>
        </div>
      </div>
    </section>

    <!-- BOOKING -->
    <section id="booking" aria-labelledby="bookingTitle">
      <h2 id="bookingTitle">Booking / Cek Ketersediaan</h2>
      <div class="card" style="padding:16px">
        <form id="bookingForm" novalidate>
          <div class="two">
            <div>
              <label for="nama">Nama Lengkap</label>
              <input type="text" id="nama" name="nama" autocomplete="name" required>
            </div>
            <div>
              <label for="wa">No. WhatsApp</label>
              <input type="tel" id="wa" name="wa" placeholder="+62…" autocomplete="tel" required>
            </div>
          </div>

          <div class="two">
            <div>
              <label for="roomType">Tipe Kamar</label>
              <select name="kamar" id="roomType" required>
                <option value="biasa" data-harga="450000">Kamar Biasa (Rp 450.000)</option>
                <option value="vip" data-harga="600000">Kamar VIP (Rp 600.000)</option>
              </select>
            </div>
            <div>
              <label for="tamu">Jumlah Tamu</label>
              <input type="number" id="tamu" name="tamu" min="1" value="2" required>
            </div>
          </div>

          <div class="two">
            <div>
              <label for="checkin">Check-in</label>
              <input type="date" name="checkin" id="checkin" required>
            </div>
            <div>
              <label for="checkout">Check-out</label>
              <input type="date" name="checkout" id="checkout" required>
            </div>
          </div>

          <div>
            <label for="catatan">Catatan</label>
            <textarea id="catatan" name="catatan" rows="3" placeholder="Contoh: minta antar-jemput boat, sewa snorkel, dll."></textarea>
          </div>

          <div class="note">
            <strong>Ringkasan:</strong>
            <div id="summary" class="muted">Pilih tanggal & tipe kamar untuk melihat total.</div>
            <div class="hint">Harga dapat berubah saat high season. Kami akan konfirmasi via WhatsApp.</div>
          </div>

          <div style="display:flex;gap:10px;flex-wrap:wrap;margin-top:8px">
            <button type="submit" class="btn">Kirim via WhatsApp</button>
            <a id="quickWA" class="btn btn-outline" target="_blank" href="#">Chat Tanya Harga</a>
          </div>
          <p class="muted" style="margin:6px 0 0">Kami akan balas secepatnya via WhatsApp.</p>
        </form>
      </div>
    </section>

    <!-- ULASAN -->
    <section id="ulasan" aria-labelledby="ulasanTitle">
      <h2 id="ulasanTitle">Komentar & Rating Tamu</h2>
      <div class="card" style="padding:16px">
        <div style="margin-bottom:10px">
          <div class="stars" id="starsInput" aria-label="Pilih rating" role="radiogroup">
            <span data-v="1" role="radio" aria-label="1 bintang">★</span>
            <span data-v="2" role="radio" aria-label="2 bintang">★</span>
            <span data-v="3" role="radio" aria-label="3 bintang">★</span>
            <span data-v="4" role="radio" aria-label="4 bintang">★</span>
            <span data-v="5" role="radio" aria-label="5 bintang">★</span>
          </div>
          <small class="muted" id="rateHint">Pilih bintang (opsional)</small>
        </div>
        <form id="reviewForm">
          <div class="two">
            <input type="text" id="rvName" placeholder="Nama (opsional)" aria-label="Nama">
            <input type="text" id="rvOrigin" placeholder="Asal kota/negara (opsional)" aria-label="Asal">
          </div>
          <textarea id="rvText" rows="3" placeholder="Tulis pengalaman menginap..." required aria-label="Ulasan"></textarea>
          <div style="display:flex;gap:10px;margin-top:8px">
            <button class="btn" type="submit">Kirim Ulasan</button>
            <button class="btn btn-ghost" type="button" id="clearReviews">Hapus Ulasan (perangkat ini)</button>
          </div>
          <p class="muted" style="margin:6px 0 0">Catatan: ulasan disimpan di perangkat pengunjung (sementara).</p>
        </form>
        <hr style="margin:16px 0;border:none;border-top:1px solid #edf2f7">
        <div id="reviewsList" aria-live="polite"></div>
      </div>
    </section>

  </main>

  <footer class="container">
    <hr style="border:none;border-top:1px solid #e7eef6;margin:0 0 14px">
    <div class="grid-2">
      <div>
        <strong>Fam Homestay</strong><br>
        Waigeo Barat Kepulauan, Kab. Raja Ampat, Papua Barat Daya<br>
        WA: <a id="waFooter" href="https://wa.me/6285396306439" target="_blank" rel="noopener">+62 853-9630-6439</a><br>
        Email: <a href="mailto:info@famhomestay.id">info@famhomestay.id</a> <!-- TODO: ganti -->
      </div>
      <div class="muted" style="text-align:right">
        © <span id="year"></span> Fam Homestay. All rights reserved.
      </div>
    </div>
  </footer>

  <!-- Tombol WhatsApp melayang -->
  <a class="wa" id="waFloat" href="https://wa.me/6285396306439?text=Halo%20Fam%20Homestay%2C%20saya%20ingin%20tanya%20ketersediaan." target="_blank" rel="noopener" aria-label="Chat WhatsApp">Chat WhatsApp</a>

  <!-- LIGHTBOX -->
  <div class="lightbox" id="lightbox" aria-modal="true" role="dialog" aria-label="Gambar diperbesar">
    <button class="close" aria-label="Tutup" onclick="hideLightbox()">✕</button>
    <div class="lb-nav">
      <button class="btn btn-outline" id="prevImg" aria-label="Sebelumnya">‹</button>
      <button class="btn btn-outline" id="nextImg" aria-label="Berikutnya">›</button>
    </div>
    <img id="lightboxImg" alt="">
  </div>

  <script>
    // ----------------- KONFIG -----------------
    const WA_NUMBER = "6285396306439"; // TODO: ganti nomor WA
    const PRICE = { biasa: 450000, vip: 600000 }; // TODO: ganti harga

    // ----------------- UTIL -----------------
    const fmtIDR = n => new Intl.NumberFormat('id-ID',{style:'currency',currency:'IDR',maximumFractionDigits:0}).format(n);
    const toISO = d => d.toISOString().split('T')[0];
    const today = new Date(); today.setHours(0,0,0,0);
    document.getElementById('year').textContent = new Date().getFullYear();

    // ----------------- GALLERY LIGHTBOX ----------
    const lb = document.getElementById('lightbox');
    const lbImg = document.getElementById('lightboxImg');
    const galleryImgs = Array.from(document.querySelectorAll('.gallery img'));
    let currentIndex = -1;

    function showLightboxAt(i){
      currentIndex = (i + galleryImgs.length) % galleryImgs.length;
      lbImg.src = galleryImgs[currentIndex].src;
      lb.classList.add('active');
    }
    function hideLightbox(){ lb.classList.remove('active'); lbImg.src=''; currentIndex=-1; }
    document.querySelectorAll('.gallery img').forEach((img, i)=>{
      img.addEventListener('click', ()=> showLightboxAt(i));
    });
    lb.addEventListener('click',(e)=>{ if(e.target===lb) hideLightbox(); });
    document.getElementById('prevImg').addEventListener('click', (e)=>{ e.stopPropagation(); showLightboxAt(currentIndex-1); });
    document.getElementById('nextImg').addEventListener('click', (e)=>{ e.stopPropagation(); showLightboxAt(currentIndex+1); });
    document.addEventListener('keydown', (e)=>{
      if(!lb.classList.contains('active')) return;
      if(e.key==='Escape') hideLightbox();
      if(e.key==='ArrowLeft') showLightboxAt(currentIndex-1);
      if(e.key==='ArrowRight') showLightboxAt(currentIndex+1);
    });

    // ----------------- BOOKING FORM ----------
    const checkin = document.getElementById('checkin');
    const checkout = document.getElementById('checkout');
    const roomType = document.getElementById('roomType');
    const summary = document.getElementById('summary');
    const quickWA = document.getElementById('quickWA');

    checkin.min = toISO(today);
    checkout.min = toISO(today);

    checkin.addEventListener('change', ()=>{
      const ci = new Date(checkin.value);
      if(checkout.value){
        const co = new Date(checkout.value);
        if(co<=ci){ co.setDate(ci.getDate()+1); checkout.value = toISO(co); }
      } else {
        const co = new Date(ci); co.setDate(ci.getDate()+1); checkout.value = toISO(co);
      }
      updateSummary();
    });
    checkout.addEventListener('change', updateSummary);
    roomType.addEventListener('change', updateSummary);
    document.querySelectorAll('#bookingForm input, #bookingForm textarea').forEach(el=>{
      el.addEventListener('input', updateSummary);
    });

    function nights(ci, co){
      const t = (new Date(co) - new Date(ci)) / (1000*60*60*24);
      return Math.max(0, Math.round(t));
    }

    function updateSummary(){
      const ci = checkin.value, co = checkout.value, rt = roomType.value;
      if(!ci || !co){ summary.textContent = "Pilih tanggal & tipe kamar untuk melihat total."; return; }
      const malam = nights(ci, co);
      const perMalam = PRICE[rt] || 0;
      if(malam<=0){ summary.textContent = "Tanggal tidak valid. Pastikan check-out setelah check-in."; return; }
      const total = malam * perMalam;
      summary.innerHTML = `Menginap <strong>${malam} malam</strong> — ${rt ? rt.toUpperCase() : '—'} @ ${perMalam?fmtIDR(perMalam):'-'}/malam<br>Total perkiraan: <strong>${fmtIDR(total)}</strong>`;
      // quick WA link (tanpa isi data tamu)
      const txt = encodeURIComponent(`Halo Fam Homestay, saya ingin tanya ketersediaan.\nTipe: ${rt?.toUpperCase()||'-'}\nCheck-in: ${ci}\nCheck-out: ${co}\nPerkiraan total: ${fmtIDR(total)}\nTerima kasih.`);
      quickWA.href = `https://wa.me/${WA_NUMBER}?text=${txt}`;
    }
    updateSummary();

    // Submit ke WhatsApp dengan data lengkap
    document.getElementById('bookingForm').addEventListener('submit', (e)=>{
      e.preventDefault();
      const f = new FormData(e.target);
      const ci = f.get('checkin'), co = f.get('checkout');
      const tipe = f.get('kamar');
      const malam = nights(ci, co);
      if(!ci || !co || !tipe){ alert('Lengkapi tanggal & tipe kamar.'); return; }
      const total = malam * (PRICE[tipe]||0);
      const msg = `Halo Fam Homestay, saya ingin booking:\n`+
        `Nama: ${f.get('nama')}\n`+
        `WA: ${f.get('wa')}\n`+
        `Tipe kamar: ${tipe.toUpperCase()}\n`+
        `Tamu: ${f.get('tamu')}\n`+
        `Check-in: ${ci}\n`+
        `Check-out: ${co}\n`+
        `Perkiraan total: ${fmtIDR(total)}\n`+
        `Catatan: ${f.get('catatan')||'-'}\n`+
        `Dikirim dari website.`;
      const url = `https://wa.me/${WA_NUMBER}?text=${encodeURIComponent(msg)}`;
      window.open(url,'_blank','noopener');
    });

    // ----------------- REVIEWS (LocalStorage) ----------
    const starsInput = document.getElementById('starsInput');
    let currentStar = 0;
    const rateHint = document.getElementById('rateHint');
    starsInput.querySelectorAll('span').forEach(s=>{
      s.addEventListener('mouseenter',()=>paintStars(s.dataset.v));
      s.addEventListener('click',()=>{ currentStar = +s.dataset.v; paintStars(currentStar); rateHint.textContent = `Rating: ${currentStar} bintang`; });
    });
    starsInput.addEventListener('mouseleave',()=>paintStars(currentStar));
    function paintStars(n){ starsInput.querySelectorAll('span').forEach(x=>x.classList.toggle('active', +x.dataset.v <= n)); }

    const listEl = document.getElementById('reviewsList');
    const STORAGE_KEY = 'fam_reviews_v1';

    function escapeHTML(s){ return s.replace(/[&<>"']/g,m=>({ '&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;' }[m])); }

    function loadReviews(){
      const arr = JSON.parse(localStorage.getItem(STORAGE_KEY)||'[]');
      renderReviews(arr);
    }
    function renderReviews(arr){
      if(!arr.length){ listEl.innerHTML = '<p class="muted">Belum ada ulasan. Jadilah yang pertama!</p>'; return; }
      listEl.innerHTML = arr.map(r=>`
        <div class="card" style="padding:12px; margin-bottom:10px">
          <div style="display:flex;justify-content:space-between;align-items:center">
            <strong>${escapeHTML(r.name||'Tamu')}</strong>
            <div class="stars" aria-hidden="true">${[1,2,3,4,5].map(i=>`<span class="${i<=r.star?'active':''}">★</span>`).join('')}</div>
          </div>
          <small class="muted">${r.origin?escapeHTML(r.origin)+' • ':''}${new Date(r.ts).toLocaleDateString('id-ID')}</small>
          <p style="margin:.4rem 0 0">${escapeHTML(r.text)}</p>
        </div>
      `).join('');
    }

    document.getElementById('reviewForm').addEventListener('submit',(e)=>{
      e.preventDefault();
      const name = document.getElementById('rvName').value.trim();
      const origin = document.getElementById('rvOrigin').value.trim();
      const text = document.getElementById('rvText').value.trim();
      if(!text){ alert('Tulis ulasan dulu ya.'); return; }
      const arr = JSON.parse(localStorage.getItem(STORAGE_KEY)||'[]');
      arr.unshift({ name, origin, text, star: currentStar||5, ts: Date.now() });
      localStorage.setItem(STORAGE_KEY, JSON.stringify(arr));
      document.getElementById('rvText').value = ''; currentStar=0; paintStars(0); rateHint.textContent='Pilih bintang (opsional)';
      renderReviews(arr);
      alert('Terima kasih! Ulasan tersimpan di perangkat ini.');
    });

    document.getElementById('clearReviews').addEventListener('click', ()=>{
      if(confirm('Hapus semua ulasan tersimpan di perangkat ini?')){ localStorage.removeItem(STORAGE_KEY); loadReviews(); }
    });

    loadReviews();
  </script>
</body>
</html>