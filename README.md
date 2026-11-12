
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Green Earth | Environmental Awareness</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
    font-family: 'Segoe UI', sans-serif;
}

:root {
    --green: #16834a;
    --light-green: #e5f5e9;
    --dark: #123b2b;
    --white: #ffffff;
    --text: #263b30;
    --background: #f5fff7;
}

body {
    background: var(--background);
    color: var(--text);
    transition: 0.4s;
}

body.dark {
    --background: #101e18;
    --white: #1c3026;
    --text: #e8f5ec;
    --light-green: #263f30;
    --dark: #b8ebc9;
}

header {
    background: var(--white);
    padding: 20px 8%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 3px 15px #0001;
}

.logo {
    color: var(--green);
    font-size: 25px;
    font-weight: bold;
}

nav a {
    text-decoration: none;
    color: var(--text);
    margin: 0 12px;
    font-weight: 600;
    transition: 0.3s;
}

nav a:hover {
    color: var(--green);
}

.toggle {
    background: var(--green);
    color: white;
    border: none;
    padding: 10px 16px;
    border-radius: 25px;
    cursor: pointer;
}

.hero {
    min-height: 85vh;
    background:
    linear-gradient(#082c1c99, #082c1c99),
    url('https://images.unsplash.com/photo-1448375240586-882707db888b?auto=format&fit=crop&w=1600&q=85');
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: center;
    padding: 8%;
    color: white;
}

.hero-content {
    max-width: 650px;
    animation: slideUp 1.2s ease;
}

.hero h1 {
    font-size: 58px;
    line-height: 1.2;
    margin-bottom: 20px;
}

.hero p {
    font-size: 18px;
    margin-bottom: 30px;
    line-height: 1.7;
}

.btn {
    display: inline-block;
    background: #25a65a;
    color: white;
    padding: 14px 28px;
    text-decoration: none;
    border-radius: 30px;
    font-weight: bold;
    transition: 0.3s;
}

.btn:hover {
    background: #126b39;
    transform: translateY(-4px);
}

section {
    padding: 80px 8%;
}

.section-title {
    text-align: center;
    margin-bottom: 45px;
}

.section-title h2 {
    color: var(--green);
    font-size: 35px;
    margin-bottom: 12px;
}

.section-title p {
    font-size: 16px;
}

.about {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 40px;
    align-items: center;
}

.about img {
    width: 100%;
    border-radius: 20px;
    box-shadow: 0 8px 25px #0002;
}

.about-text h2 {
    color: var(--green);
    font-size: 35px;
    margin-bottom: 20px;
}

.about-text p {
    line-height: 1.8;
    margin-bottom: 15px;
}

.cards {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 25px;
}

.card {
    background: var(--white);
    padding: 30px;
    border-radius: 18px;
    text-align: center;
    box-shadow: 0 5px 20px #0001;
    transition: 0.4s;
}

.card:hover {
    transform: translateY(-10px);
    box-shadow: 0 12px 25px #16834a30;
}

.card .icon {
    font-size: 50px;
    margin-bottom: 15px;
}

.card h3 {
    color: var(--green);
    margin-bottom: 12px;
}

.card p {
    line-height: 1.7;
}

.tips {
    background: var(--light-green);
}

.tip-list {
    max-width: 850px;
    margin: auto;
}

.tip {
    background: var(--white);
    margin-bottom: 15px;
    padding: 20px;
    border-radius: 12px;
    display: flex;
    gap: 15px;
    align-items: center;
    transition: 0.3s;
}

.tip:hover {
    transform: translateX(8px);
}

.tip span {
    font-size: 30px;
}

.action {
    text-align: center;
    background: linear-gradient(120deg, #126b39, #27a65d);
    color: white;
    border-radius: 25px;
    padding: 65px 25px;
}

.action h2 {
    font-size: 35px;
    margin-bottom: 15px;
}

.action p {
    margin-bottom: 25px;
    line-height: 1.7;
}

.action .btn {
    background: white;
    color: #16834a;
}

footer {
    background: #102f21;
    color: white;
    text-align: center;
    padding: 30px;
}

footer p {
    margin: 8px;
}

@keyframes slideUp {
    from {
        opacity: 0;
        transform: translateY(40px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@media(max-width: 850px) {
    header {
        flex-wrap: wrap;
        gap: 15px;
    }

    nav {
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        gap: 12px;
    }

    nav a {
        margin: 0;
    }

    .about {
        grid-template-columns: 1fr;
    }

    .cards {
        grid-template-columns: 1fr;
    }

    .hero h1 {
        font-size: 40px;
    }
}
</style>
</head>

<body>

<header>
    <div class="logo">🌿 GREEN EARTH</div>

    <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#importance">Importance</a>
        <a href="#tips">Eco Tips</a>
        <a href="#action">Take Action</a>
    </nav>

    <button class="toggle" onclick="toggleMode()">
        🌙 Dark Mode
    </button>
</header>

<!-- HOME -->
<div class="hero" id="home">
    <div class="hero-content">
        <h1>Protect Nature, Protect Our Future.</h1>
        <p>
            Our planet is our home. Let us work together to protect
            the environment, reduce pollution, conserve resources,
            and create a greener and healthier world.
        </p>
        <a href="#about" class="btn">Explore More 🌱</a>
    </div>
</div>

<!-- ABOUT -->
<section id="about">
    <div class="about">
        <img src="https://images.unsplash.com/photo-1470071459604-3b5ec3a7fe05?auto=format&fit=crop&w=900&q=85"
             alt="Beautiful green forest">

        <div class="about-text">
            <h2>What is Environmental Awareness?</h2>
            <p>
                Environmental awareness means understanding the
                importance of protecting our natural surroundings
                and recognizing how our actions affect the planet.
            </p>
            <p>
                It encourages everyone to make responsible choices
                such as planting trees, reducing waste, recycling,
                saving water, and using energy wisely.
            </p>
            <p>
                Small actions can create a big difference when
                everyone works together.
            </p>
        </div>
    </div>
</section>

<!-- IMPORTANCE -->
<section id="importance">
    <div class="section-title">
        <h2>Why Protect Our Environment?</h2>
        <p>A healthy environment means a better future for everyone.</p>
    </div>

    <div class="cards">
        <div class="card">
            <div class="icon">🌳</div>
            <h3>Plant More Trees</h3>
            <p>
                Trees provide oxygen, absorb carbon dioxide,
                protect wildlife, and help fight climate change.
            </p>
        </div>

        <div class="card">
            <div class="icon">💧</div>
            <h3>Save Water</h3>
            <p>
                Water is essential for life. Avoid wasting it
                and help protect rivers, lakes, and oceans.
            </p>
        </div>

        <div class="card">
            <div class="icon">♻️</div>
            <h3>Reduce Pollution</h3>
            <p>
                Proper waste disposal, recycling, and reducing
                plastic help keep our surroundings clean.
            </p>
        </div>
    </div>
</section>

<!-- ECO TIPS -->
<section class="tips" id="tips">
    <div class="section-title">
        <h2>Simple Ways to Save Earth</h2>
        <p>Start making a difference through your everyday habits.</p>
    </div>

    <div class="tip-list">
        <div class="tip">
            <span>🌱</span>
            <div>
                <h3>Plant Trees</h3>
                <p>Grow plants and help restore green spaces.</p>
            </div>
        </div>

        <div class="tip">
            <span>🚲</span>
            <div>
                <h3>Use Eco-Friendly Transportation</h3>
                <p>Walk, bike, or use public transportation when possible.</p>
            </div>
        </div>

        <div class="tip">
            <span>🛍️</span>
            <div>
                <h3>Avoid Single-Use Plastics</h3>
                <p>Bring reusable bags, bottles, and containers.</p>
            </div>
        </div>

        <div class="tip">
            <span>💡</span>
            <div>
                <h3>Save Electricity</h3>
                <p>Turn off lights and unplug unused appliances.</p>
            </div>
        </div>

        <div class="tip">
            <span>🗑️</span>
            <div>
                <h3>Practice Proper Waste Segregation</h3>
                <p>Separate biodegradable, recyclable, and residual waste.</p>
            </div>
        </div>
    </div>
</section>

<!-- CALL TO ACTION -->
<section id="action">
    <div class="action">
        <h2>Be Part of the Solution! 🌍</h2>
        <p>
            The Earth does not need a few people practicing
            environmental protection perfectly. It needs millions
            of people doing it consistently.
            <br>
            Together, we can build a cleaner, greener, and
            more sustainable future!
        </p>
        <a href="#home" class="btn">Start Today 💚</a>
    </div>
</section>

<!-- FOOTER -->
<footer>
    <h2>🌿 GREEN EARTH</h2>
    <p>Protect the Environment. Preserve Our Future.</p>
    <p>Every Small Action Matters!</p>
    <p>© 2026 Green Earth | Environmental Awareness</p>
</footer>

<script>
function toggleMode() {
    document.body.classList.toggle("dark");

    const button = document.querySelector(".toggle");

    if (document.body.classList.contains("dark")) {
        button.innerHTML = "☀️ Light Mode";
    } else {
        button.innerHTML = "🌙 Dark Mode";
    }
}
</script>

</body>
</html>
