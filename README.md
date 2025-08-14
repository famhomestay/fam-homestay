
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Fam Homestay Raja Ampat</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Selamat Datang di Fam Homestay Raja Ampat</h1>
  <p>Pesan penginapan Anda sekarang dengan mudah.</p>

  <form action="https://formsubmit.co/EMAIL_KAKA" method="POST">
    <label>Nama:</label>
    <input type="text" name="nama" required>
    
    <label>Email:</label>
    <input type="email" name="email" required>
    
    <label>Tanggal Check-in:</label>
    <input type="date" name="checkin" required>
    
    <label>Tanggal Check-out:</label>
    <input type="date" name="checkout" required>
    
    <label>Jumlah Tamu:</label>
    <input type="number" name="tamu" required>
    
    <button type="submit">Kirim Booking</button>
  </form>
</body>
</html>