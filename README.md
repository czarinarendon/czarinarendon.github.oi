<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Czarina | IT Portfolio</title>

<style>
:root {
    --dark: #20000b;
    --maroon: #4b0018;
    --accent: #85002d;
    --pink: #f0b5c8;
    --light: #fff5f8;
    --text: #f8eaf0;
    --muted: #c9a9b5;
}

* { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }

body {
    font-family: Arial, sans-serif;
    background: var(--dark);
    color: var(--text);
    min-height: 100vh;
}

button, input { font: inherit; }

.topbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    padding: 20px 6%;
    background: #170008;
    border-bottom: 1px solid #542033;
    position: sticky;
    top: 0;
    z-index: 10;
}

.logo { font-size: 21px; font-weight: bold; letter-spacing: 1px; white-space: nowrap; }
.logo span { color: var(--pink); }

nav { display: flex; flex-wrap: wrap; justify-content: flex-end; gap: 8px; }

nav button {
    background: transparent;
    color: var(--muted);
    border: 1px solid transparent;
    border-radius: 20px;
    padding: 10px 14px;
    cursor: pointer;
    transition: 0.2s;
}

nav button:hover, nav button.active {
    background: var(--accent);
    border-color: var(--pink);
    color: white;
}

main { max-width: 1200px; margin: auto; padding: 35px 6%; }
.page { display: none; animation: appear 0.3s ease; }
.page.active { display: block; }

@keyframes appear {
    from { opacity: 0; transform: translateY(8px); }
    to { opacity: 1; transform: translateY(0); }
}

.hero {
    min-height: 65vh;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 35px;
}

.hero-text { max-width: 650px; }

.eyebrow {
    color: var(--pink);
    letter-spacing: 3px;
    font-size: 12px;
    font-weight: bold;
    margin-bottom: 20px;
}

h1 { font-size: clamp(35px, 6vw, 65px); line-height: 1.1; margin-bottom: 18px; }
h1 span { color: var(--pink); }
h2 { font-size: 32px; margin-bottom: 12px; }
h3 { color: var(--pink); margin-bottom: 12px; }

p { line-height: 1.8; color: var(--muted); margin-bottom: 14px; }
.hero h3 { color: #e6b1c3; font-size: 19px; }

.buttons { display: flex; flex-wrap: wrap; gap: 12px; margin-top: 25px; }

.action {
    padding: 12px 20px;
    border: 1px solid var(--pink);
    border-radius: 6px;
    background: var(--accent);
    color: white;
    cursor: pointer;
    transition: 0.2s;
}

.action:hover { background: #a8003b; transform: translateY(-2px); }
.action.secondary { background: transparent; color: var(--pink); }

.profile-placeholder {
    width: 240px;
    height: 290px;
    flex-shrink: 0;
    border: 2px dashed #a64a6b;
    border-radius: 16px;
    background: linear-gradient(145deg, #430018, #24000d);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 12px;
    color: var(--pink);
    text-align: center;
    overflow: hidden;
}

.profile-placeholder img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
    border-radius: 14px;
}

.profile-placeholder span { font-size: 42px; }
.section-heading { margin-bottom: 25px; }

.cards {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 18px;
    margin-top: 25px;
}

.card {
    padding: 24px;
    background: #300011;
    border: 1px solid #612039;
    border-radius: 12px;
    transition: 0.2s;
}

.card:hover { border-color: var(--pink); transform: translateY(-4px); }
.card h3 { font-size: 19px; }

.tag {
    display: inline-block;
    padding: 6px 10px;
    margin: 3px;
    border-radius: 20px;
    background: #4b1028;
    color: var(--pink);
    font-size: 12px;
}

.education-list {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    align-items: stretch;
    gap: 15px;
    margin-top: 25px;
}

.education-item {
    min-width: 0;
    padding: 18px;
    border-top: 4px solid var(--pink);
    background: #300011;
    border-radius: 10px;
}

.education-item h3 { margin-bottom: 8px; }

.family-photo {
    height: 190px;
    margin-bottom: 18px;
    border: 1px dashed #a64a6b;
    border-radius: 8px;
    background: #24000d;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--pink);
    text-align: center;
    overflow: hidden;
}

.family-photo img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
    border-radius: 8px;
}

/* SECRET CHALLENGE */
.secret-card { max-width: 650px; margin: 25px auto; text-align: center; }

.cipher {
    margin: 22px 0;
    padding: 20px 10px;
    background: #fff0f5;
    color: #650d25;
    border: 2px dashed var(--pink);
    border-radius: 10px;
    font-size: clamp(25px, 5vw, 38px);
    font-weight: bold;
    letter-spacing: 4px;
}

.secret-card label {
    display: block;
    text-align: left;
    color: var(--pink);
    margin-bottom: 8px;
}

.secret-card input {
    width: 100%;
    padding: 13px;
    margin-bottom: 14px;
    border: 1px solid #a64a6b;
    border-radius: 6px;
    background: #20000b;
    color: white;
    font-size: 16px;
}

#secretFeedback { margin-top: 15px; font-weight: bold; }

#surprise {
    margin-top: 25px;
    padding: 25px;
    background: #fff0f5;
    color: #650d25;
    border: 2px solid var(--pink);
    border-radius: 15px;
    text-align: center;
    animation: surprisePop 0.6s ease;
}

#surprise h1 {
    color: #85002d;
    font-size: clamp(32px, 7vw, 48px);
    animation: surpriseGlow 1s infinite alternate;
}

#surprise h2 { color: #a8003b; }
#surprise p { color: #650d25; }

@keyframes surprisePop {
    from { transform: scale(0.2); opacity: 0; }
    to { transform: scale(1); opacity: 1; }
}

@keyframes surpriseGlow {
    from { text-shadow: 0 0 3px #f0b5c8; }
    to { text-shadow: 0 0 18px #f080a8; }
}

.confetti {
    position: fixed;
    top: -20px;
    z-index: 9999;
    width: 10px;
    height: 15px;
    pointer-events: none;
    animation: fall 3s linear forwards;
}

@keyframes fall {
    to { transform: translateY(110vh) rotate(720deg); opacity: 0; }
}

footer {
    text-align: center;
    padding: 25px;
    border-top: 1px solid #542033;
    color: var(--muted);
    font-size: 12px;
}

@media (max-width: 750px) {
    .topbar { align-items: flex-start; flex-direction: column; padding: 16px 5%; }
    nav { justify-content: flex-start; }
    nav button { padding: 8px 11px; font-size: 12px; }
    main { padding: 25px 5%; }
    .hero {
        min-height: auto;
        padding: 35px 0;
        flex-direction: column-reverse;
        align-items: flex-start;
    }
    .profile-placeholder { width: 150px; height: 170px; }
    .cards { grid-template-columns: 1fr; }
    h2 { font-size: 27px; }
}

@media (prefers-reduced-motion: reduce) {
    *, *::before, *::after {
        animation-duration: 0.01ms !important;
        scroll-behavior: auto !important;
    }
}


/* ONE-SCREEN LAYOUT: keep portfolio information from scrolling */
html, body {
    height: 100%;
    overflow: hidden;
}
body {
    height: 100vh;
    display: flex;
    flex-direction: column;
}
.topbar {
    flex: 0 0 auto;
}
main {
    flex: 1 1 auto;
    min-height: 0;
    height: 0;
    overflow: hidden;
    padding-top: clamp(12px, 2.5vh, 28px);
    padding-bottom: clamp(12px, 2.5vh, 28px);
}
.page {
    height: 100%;
    overflow: hidden;
}
.hero {
    min-height: 0;
    height: 100%;
}
.section-heading {
    margin-bottom: clamp(10px, 2vh, 22px);
}
.cards {
    margin-top: clamp(10px, 2vh, 22px);
    gap: clamp(10px, 1.5vw, 18px);
}
.card {
    padding: clamp(12px, 1.8vw, 24px);
}
.education-list {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: clamp(8px, 1vw, 12px);
    width: 100%;
    margin-top: clamp(10px, 2vh, 18px);
    align-items: stretch;
}
.education-item {
    min-width: 0;
    padding: clamp(10px, 1vw, 12px);
    border: 1px solid #612039;
    border-top: 3px solid var(--pink);
    border-radius: 10px;
    background: #300011;
    overflow-wrap: anywhere;
}
.education-item h3 {
    font-size: clamp(11px, 1.1vw, 15px);
    line-height: 1.3;
    margin-bottom: 8px;
}
.education-item p {
    font-size: clamp(10px, 0.9vw, 12px);
    line-height: 1.4;
    margin: 5px 0;
}
.family-photo {
    height: clamp(100px, 20vh, 190px);
}
footer {
    flex: 0 0 auto;
    padding: 12px;
}
@media (max-width: 750px) {
    main { padding: 12px 5%; }
    .topbar { gap: 8px; }
    nav { gap: 3px; }
    nav button { padding: 6px 8px; font-size: 11px; }
    .hero { gap: 12px; }
    .cards { grid-template-columns: repeat(3, minmax(0, 1fr)); }
    .education-list { grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 8px; }
    .education-item { padding: 10px; }
    .card { padding: 10px; }
    p { line-height: 1.35; margin-bottom: 7px; font-size: 12px; }
    h2 { font-size: 22px; }
    .card h3, h3 { font-size: 14px; }
    .family-photo { height: 95px; }
    .profile-placeholder { width: 125px; height: 145px; }
}

</style>
</head>

<body>

<div class="topbar">
    <div class="logo">MA. CZARINA<span>.</span></div>

    <nav aria-label="Main navigation">
        <button class="active" data-page="home">Home</button>
        <button data-page="about">About Me</button>
        <button data-page="education">Education</button>
        <button data-page="achievements">Achievements</button>
        <button data-page="family">Family</button>
        <button data-page="secret">🔐 Secret</button>
    </nav>
</div>

<main>
    <!-- HOME -->
    <section class="page active" id="home">
        <div class="hero">
            <div class="hero-text">
                <div class="eyebrow">WELCOME TO MY PORTFOLIO</div>
                <h1>Hello, I'm <span>Ma. Czarina T. Rendon</span></h1>
                <h3>BS Information Technology Student</h3>
                <p>
                    Welcome to my personal portfolio. I am an IT student
                    interested in web design, programming, and technology.
                    This website shares my background, education,
                    achievements, and the family who supports me.
                </p>

                <div class="buttons">
                    <button class="action" data-page="about">Discover About Me</button>
                    <button class="action secondary" data-page="family">Meet My Family</button>
                </div>
            </div>

            <!-- PROFILE PHOTO: Put profile.jpg beside index.html -->
            <div class="profile-placeholder">
                <img src="profile.jpg" alt="Czarina's Profile Photo">
            </div>
        </div>
    </section>

    <!-- ABOUT -->
    <section class="page" id="about">
        <div class="section-heading">
            <div class="eyebrow">GET TO KNOW ME</div>
            <h2>About Me</h2>
            <p>A little introduction about who I am and what I want to achieve.</p>
        </div>

        <div class="cards">
            <div class="card">
                <h3>Who Am I?</h3>
                <p>
                    I am Ma. Czarina T. Rendon, a Bachelor of Science
                    in Information Technology student.
                </p>
            </div>

            <div class="card">
                <h3>My Interests</h3>
                <p>
                    I am interested in computers, web design, programming,
                    and discovering how technology works.
                </p>
                <span class="tag">Web Design</span>
                <span class="tag">Programming</span>
                <span class="tag">Technology</span>
            </div>

            <div class="card">
                <h3>My Goals</h3>
                <p>
                    I want to develop my technical skills, gain experience,
                    and become a successful IT professional.
                </p>
            </div>
        </div>
    </section>

    <!-- EDUCATION -->
    <section class="page" id="education">
        <div class="section-heading">
            <div class="eyebrow">MY LEARNING JOURNEY</div>
            <h2>My Education</h2>
            <p>My academic background and educational journey.</p>
        </div>

        <div class="education-list">
            <div class="education-item">
                <h3>Tertiary Education</h3>
                <p>Course: BS Information Technology</p>
                <p>School: University of the Cordilleras</p>
                <p>Year: Currently studying</p>
            </div>

            <div class="education-item">
                <h3>Senior High School</h3>
                <p>School: Alaminos City National High School</p>
                <p>Strand: Science, Technology, Engineering, and Mathematics (STEM)</p>
                <p>Graduation year: To be added</p>
            </div>

            <div class="education-item">
                <h3>Secondary Education</h3>
                <p>School: Alaminos City National High School</p>
                <p>Graduation year: To be added</p>
            </div>

            <div class="education-item">
                <h3>Primary Education</h3>
                <p>School: Colegio San Jose de Alaminos</p>
                <p>Graduation year: To be added</p>
            </div>
        </div>
    </section>

    <!-- ACHIEVEMENTS -->
    <section class="page" id="achievements">
        <div class="section-heading">
            <div class="eyebrow">MILESTONES AND GROWTH</div>
            <h2>My Achievements</h2>
            <p>Update these sections with your actual awards, activities, and skills.</p>
        </div>

        <div class="cards">
            <div class="card">
                <h3>Academic Awards</h3>
                <p>Add your academic awards, honors, and recognitions here.</p>
            </div>

            <div class="card">
                <h3>School Activities</h3>
                <p>Add school events, seminars, organizations, or activities you joined.</p>
            </div>

            <div class="card">
                <h3>Skills and Certificates</h3>
                <p>Add your IT skills, completed training, and certificates here.</p>
            </div>
        </div>
    </section>

    <!-- FAMILY -->
    <section class="page" id="family">
        <div class="section-heading">
            <div class="eyebrow">THE PEOPLE WHO SUPPORT ME</div>
            <h2>My Family</h2>
            <p>My family is an important part of my life and my journey.</p>
        </div>

        <div class="cards">
            <div class="card">
                <div class="family-photo">
                    <img src="mother.jpg" alt="My Mother">
                </div>
                <h3>My Mother</h3>
                <p>Cecilia T. Rendon</p>
                <p>Thank you for your love, care, and support.</p>
            </div>

            <div class="card">
                <div class="family-photo">
                    <img src="father.jpg" alt="My Father">
                </div>
                <h3>My Father</h3>
                <p>Armando T. Rendon</p>
                <p>Thank you for your guidance and support.</p>
            </div>

            <div class="card">
                <div class="family-photo">
                    <img src="brother.jpg" alt="My Brother">
                </div>
                <h3>My Brother</h3>
                <p>Your Brother's Name</p>
                <p>An important member of our family.</p>
            </div>
        </div>
    </section>

    <!-- SECRET CHALLENGE -->
    <section class="page" id="secret">
        <div class="section-heading">
            <div class="eyebrow">✦ A LITTLE SURPRISE ✦</div>
            <h2>🔐 Secret Challenge</h2>
            <p>Decode the message to unlock a special surprise!</p>
        </div>

        <div class="card secret-card">
            <h3>Can You Crack the Code?</h3>
            <p>Each letter has been shifted forward by 3 places. Shift every letter backward by 3 to decode it.</p>

            <div class="cipher">BRX FDQ GR LW!</div>

            <label for="answer">Enter the decoded message:</label>
            <input id="answer" type="text" placeholder="Type your answer here..." autocomplete="off">

            <button class="action" onclick="checkAnswer()">Unlock Surprise 💌</button>
            <p id="secretFeedback" aria-live="polite"></p>

            <div id="surprise" hidden>
                <h1>🎉 BOOOOOOM! 💥</h1>
                <h2>YOU CAN DO IT!</h2>
                <p>🎊 You cracked the code! 🎊</p>
                <p>Believe in yourself, keep learning, and never give up on your dreams. Your future is bright! 💗</p>
            </div>
        </div>
    </section>
</main>

<footer>
    © 2026 Ma. Czarina T. Rendon | IT Personal Portfolio
</footer>

<script>
const titles = {
    home: "Home",
    about: "About Me",
    education: "Education",
    achievements: "Achievements",
    family: "Family",
    secret: "Secret Challenge"
};

function showPage(pageName) {
    const selectedPage = document.getElementById(pageName);
    if (!selectedPage) return;

    document.querySelectorAll(".page").forEach(page => {
        page.classList.remove("active");
    });
    selectedPage.classList.add("active");

    document.querySelectorAll("nav button").forEach(button => {
        const isActive = button.dataset.page === pageName;
        button.classList.toggle("active", isActive);

        if (isActive) button.setAttribute("aria-current", "page");
        else button.removeAttribute("aria-current");
    });

    document.title = titles[pageName] + " | Czarina's IT Portfolio";
    window.scrollTo({ top: 0, behavior: "smooth" });
}

document.querySelectorAll("[data-page]").forEach(button => {
    button.addEventListener("click", () => showPage(button.dataset.page));
});

function checkAnswer() {
    const answer = document.getElementById("answer").value
        .trim().toUpperCase()
        .replace(/[.!]/g, "")
        .replace(/\s+/g, " ");

    const surprise = document.getElementById("surprise");
    const feedback = document.getElementById("secretFeedback");

    if (answer === "YOU CAN DO IT") {
        surprise.hidden = false;
        feedback.textContent = "Correct! You unlocked the surprise!";
        launchConfetti();
    } else {
        surprise.hidden = true;
        feedback.textContent = "Not quite! Shift every letter backward by 3 and try again.";
    }
}

function launchConfetti() {
    const colors = ["#85002d", "#ff8bb5", "#f0b5c8", "#ffd166", "#ffffff"];

    for (let i = 0; i < 70; i++) {
        const piece = document.createElement("div");
        piece.className = "confetti";
        piece.style.left = Math.random() * 100 + "vw";
        piece.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
        piece.style.animationDelay = Math.random() + "s";
        document.body.appendChild(piece);
        piece.addEventListener("animationend", () => piece.remove());
    }
}
</script>

</body>
</html>
