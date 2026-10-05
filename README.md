<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Website Destroyer Generator</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
    body {
      background-color: #0f172a;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      padding: 20px;
    }
    .card {
      background: #1e293b;
      padding: 30px;
      border-radius: 16px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.5);
      width: 100%;
      max-width: 450px;
      text-align: center;
      border: 1px solid #334155;
    }
    h1 {
      font-size: 1.8rem;
      margin-bottom: 10px;
      color: #38bdf8;
    }
    p {
      color: #94a3b8;
      font-size: 0.95rem;
      margin-bottom: 25px;
    }
    .input-group {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }
    input {
      width: 100%;
      padding: 14px;
      border-radius: 8px;
      border: 1px solid #475569;
      background: #0f172a;
      color: #fff;
      font-size: 1rem;
      outline: none;
      transition: border-color 0.2s;
    }
    input:focus {
      border-color: #38bdf8;
    }
    button {
      padding: 14px;
      border-radius: 8px;
      border: none;
      background: #ef4444;
      color: #fff;
      font-weight: bold;
      font-size: 1rem;
      cursor: pointer;
      transition: background 0.2s, transform 0.1s;
    }
    button:hover {
      background: #dc2626;
    }
    button:active {
      transform: scale(0.98);
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>💥 Destroy Any Web</h1>
    <p>Masukkan URL website yang mau kamu hancurkan!</p>
    
    <div class="input-group">
      <input type="url" id="targetUrl" placeholder="https://example.com" required>
      <button onclick="destroyWebsite()">START DESTROY 🚀</button>
    </div>
  </div>

  <script>
    function destroyWebsite() {
      let urlInput = document.getElementById('targetUrl').value.trim();
      
      if (!urlInput) {
        alert('Isi URL websitenya dulu bro!');
        return;
      }

      // Otomatis tambah https:// kalau user lupa ketik
      if (!urlInput.startsWith('http://') && !urlInput.startsWith('https://')) {
        urlInput = 'https://' + urlInput;
      }

      // Encode URL agar aman dipakai di query parameter
      const encodedUrl = encodeURIComponent(urlInput);
      const destroyLink = `https://destroy.spritefusion.com/?from=badge&url=${encodedUrl}`;

      // Buka game di tab baru
      window.open(destroyLink, '_blank');
    }
  </script>

</body>
</html>
