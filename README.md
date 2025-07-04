# Cricket-Based-Website
Aim : To Design and Develop a websites centered around cricket.

Goal : Build an interactive cricket website using only frontend technologies.

✅ Approach (in Simple Words):

1. Picking up Idea that : 
 i have choosen some option to be aviailable on website will be — like showing live scores board, cricket news, or a quiz.

2. Make the Web Pages (HTML + CSS) : 
 using HTML to build the structure (headings, buttons, sections).
 using CSS to make it look nice (colors, fonts, layout, border, styles, adding navbar, flexbox or Grid for layout).

3. Add Functions with JavaScript :
 using JavaScript to: Show scores or news
 Add button actions(to function like updating scores) or animations
 Fetch data from a cricket API if needed

4. Use a Cricket API (Optional) :
 If you want live scores or player info, you can connect your website to a free cricket API using JavaScript. This will show real data.

5. Test and Improve :
 Checking that how my website looks on mobile and desktop. Fix any bugs or layout issues.

6. Publish It Online :
 Uploading project to GitHub Pages or Netlify so others can see it.


🧰 Tools You Will Use :
 HTML – for content
 CSS – for design
 JavaScript – for making it interactive

GitHub Pages or Netlify – to put your website online

code for this project :-

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Cricket Live Score</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <h1>🏏 Cricket Live Scores</h1>
    <nav>
      <a href="#">Home</a>
      <a href="#">Matches</a>
      <a href="#">Players</a>
      <a href="#">About</a>
    </nav>
  </header>

  <main>
    <section class="scores">
      <h2>Live Match</h2>
      <div id="scoreboard">
        <!-- Score will appear here -->
      </div>
    </section>
  </main>

  <footer>
    <p>© 2025 Cricket Website. Built with HTML, CSS & JS.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>



body {
  font-family: Arial, sans-serif;
  margin: 0;
  background-color: #f2f2f2;
}

header {
  background-color: #007b3d;
  color: white;
  padding: 20px;
  text-align: center;
}

nav a {
  margin: 0 15px;
  color: white;
  text-decoration: none;
}

.scores {
  padding: 20px;
  text-align: center;
}

#scoreboard {
  background-color: white;
  padding: 20px;
  margin: auto;
  max-width: 400px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
  border-radius: 8px;
}

footer {
  background-color: #222;
  color: #ccc;
  text-align: center;
  padding: 10px;
  position: fixed;
  bottom: 0;
  width: 100%;
}



// Mock cricket match data
const matchData = {
  team1: "India",
  team2: "Australia",
  score: "India 210/3 (35 overs)",
  status: "India needs 90 runs in 15 overs"
};

const scoreboard = document.getElementById("scoreboard");

function displayScore(data) {
  scoreboard.innerHTML = `
    <h3>${data.team1} vs ${data.team2}</h3>
    <p><strong>Score:</strong> ${data.score}</p>
    <p><strong>Status:</strong> ${data.status}</p>
  `;
}

displayScore(matchData);
