# Happy birthday   
  
<!DOCTYPE html>  
<html lang="id">  
<head>  
<meta charset="UTF-8">  
<title>Selamat Ulang Tahun ❤️</title>  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<style>  
    body {  
        margin: 0;  
        height: 100vh;  
        background: linear-gradient(135deg, #ff9a9e, #fad0c4);  
        overflow: hidden;  
        font-family: 'Segoe UI', sans-serif;  
        display: flex;  
        justify-content: center;  
        align-items: center;  
        color: white;  
        text-align: center;  
    }  
  
    .card {  
        background: rgba(255,255,255,0.15);  
        padding: 30px;  
        border-radius: 20px;  
        box-shadow: 0 10px 30px rgba(0,0,0,0.2);  
        animation: fadeIn 2s ease;  
        z-index: 10;  
    }  
  
    h1 {  
        font-size: 2.5em;  
        margin-bottom: 10px;  
    }  
  
    p {  
        font-size: 1.2em;  
    }  
  
    @keyframes fadeIn {  
        from { opacity: 0; transform: scale(0.8); }  
        to { opacity: 1; transform: scale(1); }  
    }  
  
    /* Balon */  
    .balloon {  
        position: absolute;  
        bottom: -150px;  
        width: 60px;  
        height: 80px;  
        background: red;  
        border-radius: 50%;  
        animation: float 10s linear infinite;  
    }  
  
    .balloon::after {  
        content: '';  
        position: absolute;  
        width: 2px;  
        height: 50px;  
        background: white;  
        left: 50%;  
        top: 80px;  
    }  
  
    @keyframes float {  
        from { transform: translateY(0); }  
        to { transform: translateY(-120vh); }  
    }  
</style>  
</head>  
<body>  
  
<div class="card">  
    <h1>🎂 Selamat Ulang Tahun!</h1>  
    <p><strong>Untuk kamu yang paling spesial ❤️</strong></p>  
    <p>Semoga hari ini penuh senyum, cinta, dan kebahagiaan ✨</p>  
    <p>— Dari aku yang sayang kamu 💕</p>  
</div>  
  
<script>  
    const colors = ["#ff4d6d", "#ffd166", "#06d6a0", "#4cc9f0", "#c77dff"];  
  
    for (let i = 0; i < 20; i++) {  
        const balloon = document.createElement("div");  
        balloon.className = "balloon";  
        balloon.style.left = Math.random() * 100 + "vw";  
        balloon.style.background = colors[Math.floor(Math.random() * colors.length)];  
        balloon.style.animationDuration = (8 + Math.random() * 5) + "s";  
        document.body.appendChild(balloon);  
    }  
</script>  
  
</body>  
</html>  
  
