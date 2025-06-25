# rafitype1812.github.io
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Toko Aluminium & Baut Mur</title>
  <link rel="stylesheet" href="toko2.css" />
</head>
    <style>
    .logo a {
      text-decoration: none;
      color: inherit;
      font-weight: bold;
      transition: transform 0.3s ease, color 0.3s ease;
    }
    .logo a:hover {
      transform: scale(1.1);
      color: orange;
    }
  </style>
<body>
  <header>
    <div class="logo"><a href="toko2.html">🔩 Barakah Aluminium</a></div>
    <nav>
      <a href="toko2.html">Beranda</a>
      <a href="#produk">Produk</a>
      <a href="#tentang">Tentang Kami</a>
      <a href="#kontak">Kontak</a>
    </nav>
  </header>

  <section class="hero">
  <div class="hero-slider">
    <div class="slide active" style="background-image: url('tukang.png');"></div>
    <div class="slide" style="background-image: url('baut.jpg');"></div>
    <div class="slide" style="background-image: url('alumunium.png');"></div>

    <!-- Tombol manual -->
    <button class="slide-btn prev">&#10094;</button>
    <button class="slide-btn next">&#10095;</button>
  </div>
  <div class="hero-content">
    <h1>Solusi Kuat untuk Konstruksi Anda</h1>
    <div class="buttons">
      <a href="#produk" class="btn btn-orange">Lihat Produk</a>
      <a href="#" class="btn btn-outline" id="katalogBtn">Katalog PDF</a>
    </div>
  </div>
</section>

  <section id="produk" class="produk">
  <h2>Kategori Produk</h2>
  <div class="produk-grid">
    
    <div class="card">
      <a href="alumunium.html">
        <img src="alumunium.png" alt="Aluminium Lembaran">
        <p>Alumunium</p>
      </a>
    </div>

    <div class="card">
      <a href="kaca.html">
        <img src="kaca.avif" alt="Kaca">
        <p>Kaca</p>
      </a>
    </div>

    <div class="card">
      <a href="bautmur.html">
        <img src="baut.png" alt="Baut">
        <p>Baut Mur & Ring</p>
      </a>
    </div>

    <div class="card">
      <a href="jasa.html">
        <img src="tukang.png" alt="Jasa Pembuatan">
        <p>Jasa Pembuatan</p>
      </a>
    </div>

  </div>
</section>


  <section id="katalog" class="keunggulan">
    <h2>Keunggulan Kami</h2>
    <div class="keunggulan-grid">
      <div class="item">📦 Stok Lengkap</div>
      <div class="item">🚚 Pengiriman Cepat</div>
      <div class="item">🛡️ Kualitas Terjamin</div>
      <div class="item">📞 Konsultasi Gratis</div>
    </div>
  </section>

  <section id="tentang" class="testimoni">
    <h2>Testimoni Pelanggan</h2>
    <div class="testi-grid">
      <blockquote>
        <p>Produk sangat berkualitas dan pengirimannya cepat!</p>
        <cite>– Budi, Kontraktor</cite>
      </blockquote>
      <blockquote>
        <p>Langganan di sini karena lengkap dan responsif CS-nya.</p>
        <cite>– Sari, Bengkel Teknik</cite>
      </blockquote>
    </div>
  </section>

  <section id="kontak" class="kontak">
    <h2>Hubungi Kami</h2>
    <form id="kontakForm">
      <input type="text" id="nama" placeholder="Nama Lengkap" required>
      <input type="email" id="email" placeholder="Email" required>
      <textarea id="pesan" placeholder="Pesan Anda" rows="5" required></textarea>
      <button type="submit">Kirim Pesan</button>
    </form>
  </section>

  <footer>
    <div class="footer-grid">
      <div>
        <h3>Toko Konstruksi</h3>
        <p>Menjual berbagai kebutuhan aluminium dan fastener <br> terbaik untuk industri dan konstruksi.</p>
      </div>
      <div>
        <h4>Kontak</h4>
        <p>Email: barokahalumunium@gmail.com</p>
        <p>Telp: 0831-0781-9553</p>
        <p>Alamat: Barokah Alumunium Sukorejo, W27J+WJC, <br> Beteng, Tamping Winarno, Kec. Sukorejo,<br> Kabupaten Kendal, Jawa Tengah 51363</p>
      </div>
      <div>
        <h4>Ikuti Kami</h4>
        <p>Instagram <br> Facebook <br> WhatsApp</p>
      </div>
    </div>
    <p class="copyright">© 2025 Toko Konstruksi. Semua hak dilindungi.</p>
  </footer>

  <script>
  // Jalankan semua JS setelah halaman siap
  document.addEventListener("DOMContentLoaded", function () {
    // === SLIDER ===
    let currentSlide = 0;
    const slides = document.querySelectorAll('.slide');
    const totalSlides = slides.length;

    function showSlide(index) {
      slides.forEach((slide, i) => {
        slide.classList.toggle('active', i === index);
      });
    }

    function nextSlide() {
      currentSlide = (currentSlide + 1) % totalSlides;
      showSlide(currentSlide);
    }

    function prevSlide() {
      currentSlide = (currentSlide - 1 + totalSlides) % totalSlides;
      showSlide(currentSlide);
    }

    document.querySelector('.slide-btn.next').addEventListener('click', nextSlide);
    document.querySelector('.slide-btn.prev').addEventListener('click', prevSlide);
    setInterval(nextSlide, 5000);

    // === SMOOTH SCROLL ===
    document.querySelectorAll('nav a[href^="#"]').forEach(anchor => {
      anchor.addEventListener("click", function(e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute("href"));
        target.scrollIntoView({ behavior: "smooth" });
      });
    });

    // === FORM VALIDATION ===
    document.getElementById("kontakForm").addEventListener("submit", function(e) {
      e.preventDefault();
      
      const nama = document.getElementById("nama").value.trim();
      const email = document.getElementById("email").value.trim();
      const pesan = document.getElementById("pesan").value.trim();

      if (!nama || !email || !pesan) {
        alert("Semua kolom wajib diisi!");
        return;
      }

      const emailPattern = /^[^\\s@]+@[^\\s@]+\\.[^\\s@]+$/;
      if (!emailPattern.test(email)) {
        alert("Format email tidak valid!");
        return;
      }

      alert("Pesan berhasil dikirim!\n\nNama: " + nama + "\nEmail: " + email + "\nPesan: " + pesan);
      document.getElementById("kontakForm").reset();
    });

    // === TOMBOL KATALOG ===
    document.getElementById("katalogBtn").addEventListener("click", function(e) {
      e.preventDefault();
      window.open("katalog-produk.pdf", "_blank");
    });
  });
</script>

  </script>
</body>
</html>
