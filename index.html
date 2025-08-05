<!DOCTYPE html><html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Aplikasi Jadwal & PR</title>
  <style>
    body {
      font-family: sans-serif;
      margin: 0;
      padding: 0;
    }
    header {
      text-align: center;
      padding: 20px;
      background-color: #4CAF50;
      color: white;
    }
    .container {
      padding: 20px;
    }
    input, select, button {
      margin: 5px 0;
      padding: 5px;
      width: 100%;
    }
    .item {
      border: 1px solid #ccc;
      padding: 10px;
      margin: 5px 0;
      border-radius: 5px;
    }
    .item small {
      color: gray;
    }
    nav {
      position: fixed;
      bottom: 0;
      width: 100%;
      display: flex;
      background-color: #eee;
      border-top: 1px solid #ccc;
    }
    nav button {
      flex: 1;
      padding: 15px;
      border: none;
      background: none;
      font-size: 16px;
    }
    nav button.active {
      background-color: #ddd;
      font-weight: bold;
    }
    section {
      display: none;
    }
    section.active {
      display: block;
    }
    #login {
      max-width: 400px;
      margin: 100px auto;
      padding: 20px;
      border: 1px solid #ccc;
      border-radius: 10px;
    }
  </style>
</head>
<body>
  <div id="login">
    <h2>Login</h2>
    <input type="text" id="username" placeholder="Username">
    <input type="password" id="password" placeholder="Password">
    <button onclick="login()">Login</button>
    <p id="login-error" style="color:red;"></p>
  </div>  <div id="app" style="display:none;">
    <header>
      <h1>Aplikasi Jadwal & PR</h1>
    </header><div class="container">
  <section id="menu-input" class="active">
    <h2>Tambah Jadwal Pelajaran</h2>
    <input id="jadwal-hari" placeholder="Hari (contoh: Senin)">
    <input id="jadwal-mapel" placeholder="Mata Pelajaran">
    <button onclick="tambahJadwal()">Tambah Jadwal</button>

    <h2>Tambah PR</h2>
    <input id="pr-mapel" placeholder="Mata Pelajaran">
    <input id="pr-tugas" placeholder="Tugas">
    <input id="pr-tanggal" type="date">
    <button onclick="tambahPR()">Tambah PR</button>
  </section>

  <section id="menu-jadwal">
    <h2>Jadwal Pelajaran</h2>
    <div id="jadwal-list"></div>
  </section>

  <section id="menu-pr">
    <h2>Daftar PR</h2>
    <div id="pr-list"></div>
  </section>
</div>

<nav>
  <button onclick="tampilkanMenu('menu-input')" class="active">Input</button>
  <button onclick="tampilkanMenu('menu-jadwal')">Jadwal</button>
  <button onclick="tampilkanMenu('menu-pr')">PR</button>
</nav>

  </div>  <script>
    const USERNAME = "Rafkha";
    const PASSWORD = "Rafkha40";

    function login() {
      const user = document.getElementById("username").value;
      const pass = document.getElementById("password").value;
      if (user === USERNAME && pass === PASSWORD) {
        document.getElementById("login").style.display = "none";
        document.getElementById("app").style.display = "block";
        tampilkanJadwal();
        tampilkanPR();
      } else {
        document.getElementById("login-error").innerText = "Username atau password salah!";
      }
    }

    let jadwal = JSON.parse(localStorage.getItem('jadwal')) || [];
    let prList = JSON.parse(localStorage.getItem('prList')) || [];

    function simpanData() {
      localStorage.setItem('jadwal', JSON.stringify(jadwal));
      localStorage.setItem('prList', JSON.stringify(prList));
    }

    function tampilkanMenu(id) {
      document.querySelectorAll('section').forEach(s => s.classList.remove('active'));
      document.getElementById(id).classList.add('active');
      document.querySelectorAll('nav button').forEach(b => b.classList.remove('active'));
      event.target.classList.add('active');
      if (id === 'menu-jadwal') tampilkanJadwal();
      if (id === 'menu-pr') tampilkanPR();
    }

    function tampilkanJadwal() {
      const list = document.getElementById("jadwal-list");
      list.innerHTML = "";
      jadwal.forEach((j, i) => {
        list.innerHTML += `<div class='item'>${j.hari} - ${j.mapel} 
          <button onclick='editJadwal(${i})'>Edit</button> 
          <button onclick='hapusJadwal(${i})'>Hapus</button></div>`;
      });
    }

    function tampilkanPR() {
      const list = document.getElementById("pr-list");
      list.innerHTML = "";
      const today = new Date().toISOString().split("T")[0];
      const sorted = prList
        .filter(p => p.tanggal >= today)
        .sort((a, b) => new Date(a.tanggal) - new Date(b.tanggal));
      sorted.forEach((p, i) => {
        const status = p.selesai ? "<strong>(Sudah dikerjakan)</strong>" : "";
        list.innerHTML += `<div class='item'>${p.mapel}: ${p.tugas} ${status}<br><small>Deadline: ${p.tanggal}</small> 
          <button onclick='centangPR(${i})'>✓</button>
          <button onclick='hapusPR(${i})'>Hapus</button></div>`;
      });
    }

    function tambahJadwal() {
      const hari = document.getElementById("jadwal-hari").value;
      const mapel = document.getElementById("jadwal-mapel").value;
      if (hari && mapel) {
        jadwal.push({ hari, mapel });
        simpanData();
        document.getElementById("jadwal-hari").value = "";
        document.getElementById("jadwal-mapel").value = "";
      }
    }

    function hapusJadwal(index) {
      jadwal.splice(index, 1);
      simpanData();
      tampilkanJadwal();
    }

    function editJadwal(index) {
      const j = jadwal[index];
      const newHari = prompt("Ubah Hari:", j.hari);
      const newMapel = prompt("Ubah Mapel:", j.mapel);
      if (newHari && newMapel) {
        jadwal[index] = { hari: newHari, mapel: newMapel };
        simpanData();
        tampilkanJadwal();
      }
    }

    function tambahPR() {
      const mapel = document.getElementById("pr-mapel").value;
      const tugas = document.getElementById("pr-tugas").value;
      const tanggal = document.getElementById("pr-tanggal").value;
      if (mapel && tugas && tanggal) {
        prList.push({ mapel, tugas, tanggal, selesai: false });
        simpanData();
        document.getElementById("pr-mapel").value = "";
        document.getElementById("pr-tugas").value = "";
        document.getElementById("pr-tanggal").value = "";
      }
    }

    function hapusPR(index) {
      prList.splice(index, 1);
      simpanData();
      tampilkanPR();
    }

    function centangPR(index) {
      prList[index].selesai = true;
      simpanData();
      tampilkanPR();
    }
  </script></body>
</html>
