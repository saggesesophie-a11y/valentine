# valentine
<!DOCTYPE html>
<html lang="it">
<head>
<meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MY BABY</title>
<style>
 body {
  margin: 0;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #f3c1d9;
  font-family: Arial, sans-serif;
}

.container {
  text-align: center;
}

h1 {
  color: darkred;
  margin-bottom: 20px;
}

.buttons button {
  padding: 12px 25px;
  margin: 0 10px;
  font-size: 16px;
  border-radius: 8px;
  border: none;
  cursor: pointer;
}

.yes {
  background-color: #ff4d6d;
  color: white;
}

.no {
  background-color: #999;
  color: white;
}

/* Pulsante Yes iniziale */
#yesBtn {
    font-size: 16px;
    padding: 10px 20px;
}

/* Contenitore fullscreen invisibile all’inizio */
#fullscreenContainer {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: pink;
    justify-content: center;
    align-items: center;
    z-index: 9999;
}

/* Immagine fullscreen */
#fullscreenContainer img {
    max-width: 100%;
    max-height: 100%;
    object-fit: contain;
}

</style>
</head>
<style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center; /* centro orizzontale */
      align-items: center;     /* centro verticale */
      background-color: pink;
    }

    h1 {
      color: #B22222;
    }
  </style>
<body>
<!-- Pulsanti -->
<div class="container">
  <h1>Michele, Will You Be My Valentine? ❤️</h1>
  <div class="buttons">
<button id="yesBtn" onclick="mostraFullscreen()">Yes</button>
<button onclick="ingrandisciYes()">No</button>
  </div>
<!-- Contenitore fullscreen -->
<div id="fullscreenContainer" onclick="chiudiFullscreen()">
    <img src="gatto.jpg" alt="Fullscreen">
</div>

<script>
let size = 16;

// Funzione Yes → mostra fullscreen
function mostraFullscreen() {
    document.getElementById("fullscreenContainer").style.display = "flex";
}

// Funzione No → ingrandisce Yes
function ingrandisciYes() {
    size += 4;
    document.getElementById("yesBtn").style.fontSize = size + "px";
}

// Click sullo sfondo fullscreen chiude l’immagine
function chiudiFullscreen() {
    document.getElementById("fullscreenContainer").style.display = "none";
}
</script>

</body>
</html>
