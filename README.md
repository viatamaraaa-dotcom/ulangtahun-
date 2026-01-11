#   
export const name = "Ren Sayang ❤️";  
  
export const wishes = [  
  "Selamat ulang tahun ya, Ren Sayang 🎂🥳",  
  "Semoga semua doa baik kamu dikabulkan ✨",  
  "Terima kasih udah hadir dan bikin hidup aku lebih berwarna 💕",  
  "Aku harap aku masih bisa nemenin kamu di banyak ulang tahun berikutnya 🥹",  
  "Intinya satu… aku sayang kamu 😳❤️"  
];  
import { useState } from "react";  
import { name, wishes } from "./data";  
import "./styles.css";  
  
function App() {  
  const [index, setIndex] = useState(0);  
  
  const playMusic = () => {  
    const music = document.getElementById("bg-music");  
    if (music && music.paused) {  
      music.play();  
    }  
  };  
  
  const nextWish = () => {  
    playMusic();  
    if (index < wishes.length - 1) {  
      setIndex(index + 1);  
    }  
  };  
  
  return (  
    <div className="container">  
      <audio id="bg-music" src="/music.mp3" loop />  
  
      <div className="card">  
        <h1>Hai {name} 👀</h1>  
  
        <p className="wish">  
          {wishes[index]}  
        </p>  
  
        {index < wishes.length - 1 && (  
          <button onClick={nextWish}>  
            Klik aku 🎁  
          </button>  
        )}  
  
        {index === wishes.length - 1 && (  
          <p className="ending">  
            🎉🎈💖  
          </p>  
        )}  
      </div>  
    </div>  
  );  
}  
  
export default App;  
.container {  
  height: 100vh;  
  background: linear-gradient(135deg, #ff758c, #ff7eb3);  
  display: flex;  
  justify-content: center;  
  align-items: center;  
  font-family: "Segoe UI", sans-serif;  
}  
  
.card {  
  background: rgba(255, 255, 255, 0.25);  
  padding: 30px;  
  border-radius: 22px;  
  text-align: center;  
  width: 90%;  
  max-width: 420px;  
  box-shadow: 0 20px 40px rgba(0,0,0,0.3);  
  color: white;  
  animation: fadeIn 1.2s ease;  
}  
  
h1 {  
  font-size: 2.2em;  
}  
  
.wish {  
  font-size: 1.15em;  
  min-height: 90px;  
}  
  
button {  
  margin-top: 20px;  
  padding: 14px 28px;  
  border: none;  
  border-radius: 30px;  
  background: white;  
  color: #ff4d6d;  
  font-weight: bold;  
  cursor: pointer;  
}  
  
button:hover {  
  transform: scale(1.05);  
}  
  
.ending {  
  font-size: 2em;  
}  
  
@keyframes fadeIn {  
  from {  
    opacity: 0;  
    transform: scale(0.85);  
  }  
  to {  
    opacity: 1;  
    transform: scale(1);  
  }  
}  
