<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ELFE MY - Official</title>

<script src="https://telegram.org/js/telegram-web-app.js"></script>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #071a12;
  color: white;
}

header {
  background: linear-gradient(135deg,#123d28,#071a12);
  padding: 30px 20px;
  text-align: center;
  border-bottom: 2px solid #d9b84f;
}

.logo {
  font-size: 35px;
}

h1 {
  color: #e7c75a;
  margin: 10px 0;
}

header p {
  color: #b8d5c0;
}

.container {
  padding: 20px;
  max-width: 600px;
  margin: auto;
}

.welcome {
  background: #123523;
  border: 1px solid #d9b84f;
  border-radius: 15px;
  padding: 20px;
  margin-bottom: 20px;
}

.welcome h2 {
  color: #e7c75a;
}

.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px;
}

.card {
  background: #153b28;
  border: 1px solid #315b40;
  border-radius: 15px;
  padding: 20px 10px;
  text-align: center;
  color: white;
  cursor: pointer;
}

.card:active {
  background: #245b3c;
}

.icon {
  font-size: 30px;
}

.card h3 {
  color: #e7c75a;
  font-size: 15px;
}

button {
  font-family: inherit;
}

footer {
  text-align: center;
  padding: 30px;
  color: #d9b84f;
  font-size: 12px;
}
</style>
</head>

<body>

<header>
  <div class="logo">👑</div>
  <h1>ELFE MY</h1>
  <p>OFFICIAL TELEGRAM MANAGER</p>
</header>

<div class="container">

  <div class="welcome">
    <h2>Bienvenue sur ELFE MY 💚</h2>
    <p>Votre espace officiel de gestion Telegram.</p>
    <p id="username">Utilisateur : Visiteur</p>
  </div>

  <h2>⚙️ Tableau de bord</h2>

  <div class="grid">

    <button class="card" onclick="show('Gestion des groupes')">
      <div class="icon">👥</div>
      <h3>Groupes</h3>
    </button>

    <button class="card" onclick="show('Modération')">
      <div class="icon">🛡️</div>
      <h3>Modération</h3>
    </button>

    <button class="card" onclick="show('Gestion du staff')">
      <div class="icon">⭐</div>
      <h3>Staff</h3>
    </button>

    <button class="card" onclick="show('Paramètres')">
      <div class="icon">⚙️</div>
      <h3>Paramètres</h3>
    </button>

    <button class="card" onclick="show('Statistiques')">
      <div class="icon">📊</div>
      <h3>Statistiques</h3>
    </button>

    <button class="card" onclick="show('Profil utilisateur')">
      <div class="icon">👤</div>
      <h3>Mon profil</h3>
    </button>

  </div>

</div>

<footer>
  👑 ELFE MY OFFICIAL<br>
  © 2026 - Tous droits réservés
</footer>

<script>
const tg = window.Telegram.WebApp;

tg.ready();
tg.expand();

const user = tg.initDataUnsafe?.user;

if (user) {
  document.getElementById("username").textContent =
    "Utilisateur : " + user.first_name;
}

function show(section) {
  tg.showAlert(
    section + " : Fonctionnalité en préparation."
  );
}
</script>

</body>
</html>
