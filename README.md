<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Fam Homestay • Raja Ampat</title>
  <meta name="description" content="Fam Homestay di Waigeo Barat Kepulauan, Raja Ampat. Booking mudah, lihat foto, dan baca ulasan tamu.">

  <!-- 🌸 CSS -->
  <style>
    :root{
      --primary:#0077b6;
      --primary2:#0096c7;
      --dark:#023e8a;
      --bg:#f5fbff;
      --card:#ffffff;
      --text:#102a43;
      --muted:#6b7280;
      --radius:18px;
    }
    body {
      background: var(--bg);
      color: var(--text);
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }
    header {
      background: var(--primary);
      padding: 1rem;
      color: white;
    }
    .container {
      max-width: 900px;
      margin: auto;
      padding: 1rem;
    }
    nav a {
      color: white;
      margin: 0 0.5rem;
      text-decoration: none;
    }
    .btn {
      background: var(--primary2);
      padding: 0.5rem 1rem;
      border-radius: var(--radius);
      color: white;
      text-decoration: none;
    }
    /* Booking form */
    form {
      background: var(--card);
      padding: 1rem;
      border-radius: var(--radius);
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      margin-top: 1rem;
    }
    input, select {
      padding: 0.5rem;
      width: 100%;
      margin-bottom: 1rem;
    }
    #summary {
      font-weight: bold;
      margin: 0.5rem 0;
    }
    /* Galeri */
    .gallery img {
      width: 150px;
      margin: 5px;
      border-radius: var(--radius);
      cursor: pointer;
    }
    /* Ulasan */
    .review {
      background: var(--card);
      padding: 0.5rem;
      border-radius: var(--radius);
      margin-bottom: 0.5rem;
    }
  </style>
</head>
<body>
  <!-- 🌿 HTML -->
  <header>
    <div class="container nav">
      <div class="brand">
        <div class="logo">FH</div>
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
    <section id="profil">
      <h2>Profil</h2>
      <p>Fam Homestay terletak di Waigeo Barat Kepulauan, Raja Ampat. Nikmati penginapan nyaman, bersih, dan dekat dengan destinasi wisata terbaik.</p>
    </section>

    <section id="galeri">
      <h2>Galeri</h2>
      <div class="gallery">
        <img src="foto1.jpg" alt="Foto 1">
        <img src="foto2.jpg" alt="Foto 2">
        <img src="foto3.jpg" alt="Foto 3">
      </div>
    </section>

    <section id="booking">
      <h2>Form Booking</h2>
      <form id="bookingForm">
        <label>Check-in:</label>
        <input type="date" id="checkin">
        <label>Check-out:</label>
        <input type="date" id="checkout">
        <label>Tipe Kamar:</label>
        <select id="roomType">
          <option value="">--Pilih--</option>
          <option value="biasa">Biasa - Rp 450.000/malam</option>
          <option value="vip">VIP - Rp 600.000/malam</option>
        </select>
        <div id="summary">Pilih tanggal & tipe kamar</div>
        <button type="button" class="btn" id="bookNow">Kirim Booking via WhatsApp</button>
      </form>
    </section>

    <section id="ulasan">
      <h2>Ulasan Tamu</h2>
      <div id="reviewList"></div>
      <form id="reviewForm">
        <input type="text" id="reviewName" placeholder="Nama" required>
        <textarea id="reviewText" placeholder="Tulis ulasan..." required></textarea>
        <button type="submit" class="btn">Kirim Ulasan</button>
      </form>
    </section>
  </main>

  <!-- 🚀 JavaScript -->
  <script>
    const WA_NUMBER = "6285396306439";
    const PRICE = { biasa: 450000, vip: 600000 };

    const checkin = document.getElementById('checkin');
    const checkout = document.getElementById('checkout');
    const roomType = document.getElementById('roomType');
    const summary = document.getElementById('summary');
    const bookNow = document.getElementById('bookNow');

    const fmtIDR = n => new Intl.NumberFormat('id-ID', {
      style: 'currency', currency: 'IDR'
    }).format(n);

    function nights(ci, co) {
      const t = (new Date(co) - new Date(ci)) / (1000*60*60*24);
      return Math.max(0, Math.round(t));
    }

    function updateSummary() {
      const ci = checkin.value, co = checkout.value, rt = roomType.value;
      if (!ci || !co || !rt) {
        summary.textContent = "Pilih tanggal & tipe kamar";
        return;
      }
      const malam = nights(ci, co);
      const total = malam * PRICE[rt];
      summary.textContent = `Total: ${fmtIDR(total)} untuk ${malam} malam`;
    }

    checkin.addEventListener('change', updateSummary);
    checkout.addEventListener('change', updateSummary);
    roomType.addEventListener('change', updateSummary);

    bookNow.addEventListener('click', () => {
      const ci = checkin.value, co = checkout.value, rt = roomType.value;
      if (!ci || !co || !rt) {
        alert("Lengkapi semua data booking!");
        return;
      }
      const malam = nights(ci, co);
      const total = malam * PRICE[rt];
      const msg = `Halo, saya ingin booking di Fam Homestay:%0A- Check-in: ${ci}%0A- Check-out: ${co}%0A- Tipe kamar: ${rt}%0A- Total: ${fmtIDR(total)}`;
      window.open(`https://wa.me/${WA_NUMBER}?text=${msg}`, '_blank');
    });

    // Review
    const reviewList = document.getElementById('reviewList');
    const reviewForm = document.getElementById('reviewForm');
    const reviewName = document.getElementById('reviewName');
    const reviewText = document.getElementById('reviewText');

    function loadReviews() {
      reviewList.innerHTML = '';
      const reviews = JSON.parse(localStorage.getItem('reviews') || '[]');
      reviews.forEach(r => {
        const div = document.createElement('div');
        div.className = 'review';
        div.innerHTML = `<strong>${r.name}</strong><p>${r.text}</p>`;
        reviewList.appendChild(div);
      });
    }

    reviewForm.addEventListener('submit', e => {
      e.preventDefault();
      const reviews = JSON.parse(localStorage.getItem('reviews') || '[]');
      reviews.push({ name: reviewName.value, text: reviewText.value });
      localStorage.setItem('reviews', JSON.stringify(reviews));
      reviewName.value = '';
      reviewText.value = '';
      loadReviews();
    });

    loadReviews();

    // Galeri Lightbox
    document.querySelectorAll('.gallery img').forEach(img => {
      img.addEventListener('click', () => {
        const lightbox = document.createElement('div');
        lightbox.style.position = 'fixed';
        lightbox.style.top = '0';
        lightbox.style.left = '0';
        lightbox.style.width = '100%';
        lightbox.style.height = '100%';
        lightbox.style.background = 'rgba(0,0,0,0.8)';
        lightbox.style.display = 'flex';
        lightbox.style.justifyContent = 'center';
        lightbox.style.alignItems = 'center';
        lightbox.innerHTML = `<img src="${img.src}" style="max-width:90%; max-height:90%; border-radius:var(--radius)">`;
        lightbox.addEventListener('click', () => document.body.removeChild(lightbox));
        document.body.appendChild(lightbox);
      });
    });
  </script>
</body>
</html>