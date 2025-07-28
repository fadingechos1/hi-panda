# hi-panda
Countdown to Sufi’s Birthday 🎂
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Hi Panda 🐼</title>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&family=EB+Garamond&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="container">
    <h1>Hi Panda 🐼</h1>
    <p class="countdown" id="countdown"></p>

    <div class="message-box morning">
      <h2>🌞 Good Morning</h2>
      <p id="morning-message">You are the sunshine of this world, Sufi.</p>
      <img id="morning-image" src="" alt="morning aesthetic">
    </div>

    <div class="message-box night">
      <h2>🌙 Good Night</h2>
      <p id="night-message">Sleep peacefully like petals in moonlight.</p>
      <img id="night-image" src="" alt="night aesthetic">
    </div>

    <footer>
      Counting down to the day the world got lucky — <b>29th November 🎂</b>
    </footer>
  </div>

  <script src="script.js"></script>
</body>
</html>

body {
  font-family: 'EB Garamond', serif;
  background: #fffafc;
  color: #3d2e2e;
  text-align: center;
  padding: 2rem;
}

h1 {
  font-family: 'Dancing Script', cursive;
  font-size: 2.8rem;
  color: #d291bc;
  margin-bottom: 0.5rem;
}

.countdown {
  font-size: 1.2rem;
  color: #9c5a91;
  margin-bottom: 2rem;
}

.message-box {
  background: #fbe4f0;
  border-radius: 12px;
  padding: 1rem;
  margin: 1.5rem auto;
  max-width: 500px;
  box-shadow: 0 0 12px rgba(0,0,0,0.05);
}

.message-box img {
  width: 100%;
  height: auto;
  border-radius: 8px;
  margin-top: 0.5rem;
}

footer {
  margin-top: 3rem;
  font-size: 0.9rem;
  color: #a68da5;
}


// Countdown to birthday
const birthday = new Date("2025-11-29");
const today = new Date();
const timeDiff = birthday - today;
const daysLeft = Math.ceil(timeDiff / (1000 * 60 * 60 * 24));
document.getElementById("countdown").innerText = `${daysLeft} days left until your birthday!`;

// Message options
const morningMessages = [
  "Good morning, Panda 🌞 You're the first light in every heart.",
  "Hey sleepyhead 🐱 Start this day with a smile!",
  "Another beautiful day with you in the world 💗"
];

const nightMessages = [
  "Sweet dreams, Panda 🌙",
  "Rest well — you're the softest star in the sky.",
  "Sleep like a cozy kitten under moonlight 🐾"
];

// Aesthetic image sets (unsplash.com direct links)
const morningImages = [
  "https://source.unsplash.com/featured/?cute-cat",
  "https://source.unsplash.com/featured/?morning-flowers",
  "https://source.unsplash.com/featured/?pink-sky"
];

const nightImages = [
  "https://source.unsplash.com/featured/?cat,sleep",
  "https://source.unsplash.com/featured/?moon,flowers",
  "https://source.unsplash.com/featured/?night-stars"
];

// Pick one per day
const index = new Date().getDate() % 3;
document.getElementById("morning-message").innerText = morningMessages[index];
document.getElementById("morning-image").src = morningImages[index];
document.getElementById("night-message").innerText = nightMessages[index];
document.getElementById("night-image").src = nightImages[index];