<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <title>Drake Denklemi Simülatörü</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #000;
      background-image: url('https://upload.wikimedia.org/wikipedia/commons/thumb/2/28/Observable_universe_logarithmic_illustration.png/1920px-Observable_universe_logarithmic_illustration.png');
      background-size: cover;
      background-attachment: fixed;
      background-position: center;
      color: #fff;
      text-shadow: 1px 1px 3px #000;
      padding: 40px;
    }
    label, input {
      display: block;
      margin-top: 10px;
    }
    input {
      padding: 5px;
    }
    button {
      margin-top: 20px;
      padding: 10px 20px;
      font-weight: bold;
      border-radius: 8px;
      background: #2ecc71;
      color: white;
      border: none;
      cursor: pointer;
    }
    #result {
      margin-top: 20px;
      font-size: 18px;
      background: rgba(0,0,0,0.6);
      padding: 10px;
      border-radius: 8px;
    }
  </style>
</head>
<body>
  <h1>🌌 Drake Denklemi Simülatörü</h1>

  <label>Yılda oluşan yıldız sayısı (R*): <input type="number" id="r" value="1.5"></label>
  <label>Gezegenli yıldız oranı (fp): <input type="number" id="fp" value="0.5"></label>
  <label>Yaşanabilir gezegen sayısı (ne): <input type="number" id="ne" value="2"></label>
  <label>Yaşam gelişme olasılığı (fl): <input type="number" id="fl" value="0.33"></label>
  <label>Zeki yaşam gelişme olasılığı (fi): <input type="number" id="fi" value="0.01"></label>
  <label>İletişim kurabilecek olasılık (fc): <input type="number" id="fc" value="0.1"></label>
  <label>Uygarlığın iletişim süresi (L): <input type="number" id="l" value="10000"></label>

  <button onclick="hesapla()">Hesapla</button>
  <div id="result"></div>

  <script>
    function hesapla() {
      const R = parseFloat(document.getElementById('r').value);
      const fp = parseFloat(document.getElementById('fp').value);
      const ne = parseFloat(document.getElementById('ne').value);
      const fl = parseFloat(document.getElementById('fl').value);
      const fi = parseFloat(document.getElementById('fi').value);
      const fc = parseFloat(document.getElementById('fc').value);
      const L = parseFloat(document.getElementById('l').value);
      const N = R * fp * ne * fl * fi * fc * L;
      document.getElementById('result').innerHTML = `🌠 Galaksimizde tahmini medeniyet sayısı: <strong>${N.toFixed(2)}</strong>`;
    }
  </script>
</body>
</html>
