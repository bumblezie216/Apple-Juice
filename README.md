<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Lola ♡</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Georgia, "Times New Roman", serif;
    color: #edf8ff;
    min-height: 100vh;
    overflow-x: hidden;
    background:
        radial-gradient(circle at 15% 10%, rgba(78, 164, 255, 0.24), transparent 28%),
        radial-gradient(circle at 85% 25%, rgba(116, 89, 255, 0.20), transparent 30%),
        radial-gradient(circle at 45% 75%, rgba(53, 187, 255, 0.16), transparent 32%),
        linear-gradient(180deg, #01030d 0%, #05091d 38%, #07132c 70%, #020510 100%);
    position: relative;
}

body::before {
    content: "";
    position: fixed;
    inset: 0;
    pointer-events: none;
    z-index: -10;
    background-image:
        radial-gradient(circle, rgba(255,255,255,.95) 1px, transparent 1.5px),
        radial-gradient(circle, rgba(160,215,255,.8) 1px, transparent 1.5px),
        radial-gradient(circle, rgba(255,255,255,.65) 1px, transparent 1.5px);
    background-size: 85px 85px, 135px 135px, 210px 210px;
    background-position: 10px 20px, 50px 80px, 120px 40px;
    animation: starsMove 40s linear infinite;
    opacity: .55;
}

@keyframes starsMove {
    from {
        transform: translateY(0);
    }
    to {
        transform: translateY(85px);
    }
}

.galaxy-cloud {
    position: fixed;
    width: 500px;
    height: 500px;
    border-radius: 50%;
    filter: blur(80px);
    opacity: .13;
    pointer-events: none;
    z-index: -8;
}

.cloud-one {
    background: #42a5ff;
    top: -220px;
    left: -170px;
}

.cloud-two {
    background: #8a63ff;
    top: 35%;
    right: -240px;
}

.cloud-three {
    background: #36cfff;
    bottom: -280px;
    left: 20%;
}

.shooting-star {
    position: fixed;
    width: 140px;
    height: 2px;
    background: linear-gradient(90deg, transparent, #bfeaff, white);
    transform: rotate(-35deg);
    opacity: 0;
    pointer-events: none;
    z-index: -4;
    animation: shooting 9s linear infinite;
}

.shooting-star.one {
    top: 14%;
    left: -160px;
    animation-delay: 2s;
}

.shooting-star.two {
    top: 52%;
    left: -160px;
    animation-delay: 6s;
}

@keyframes shooting {
    0% {
        transform: translate(-100px, -50px) rotate(-35deg);
        opacity: 0;
    }
    8% {
        opacity: 1;
    }
    25% {
        transform: translate(100vw, 40vh) rotate(-35deg);
        opacity: 0;
    }
    100% {
        opacity: 0;
    }
}

/* STINGRAYS */

.stingray {
    position: fixed;
    width: 100px;
    height: 55px;
    z-index: -3;
    opacity: .28;
    pointer-events: none;
    animation: swimAcross 25s linear infinite;
}

.stingray::before {
    content: "";
    position: absolute;
    width: 48px;
    height: 30px;
    left: 27px;
    top: 9px;
    background: linear-gradient(135deg, #79d4f5, #386d99);
    border-radius: 70% 30% 70% 30%;
    transform: rotate(-10deg);
    box-shadow: 0 0 25px rgba(110,210,255,.3);
}

.stingray::after {
    content: "";
    position: absolute;
    width: 85px;
    height: 38px;
    left: 7px;
    top: 3px;
    border-radius: 50%;
    background: linear-gradient(
        140deg,
        transparent 20%,
        rgba(105,195,235,.7) 45%,
        transparent 47%
    );
}

.stingray .tail {
    position: absolute;
    width: 55px;
    height: 2px;
    background: #70c9ed;
    left: 66px;
    top: 34px;
    transform: rotate(18deg);
}

.stingray-one {
    top: 17%;
    left: -150px;
    animation-delay: 0s;
}

.stingray-two {
    top: 43%;
    left: -180px;
    animation-delay: 9s;
    transform: scale(.7);
}

.stingray-three {
    top: 72%;
    left: -150px;
    animation-delay: 16s;
    transform: scale(1.15);
}

@keyframes swimAcross {
    0% {
        left: -160px;
        transform: translateY(0) rotate(0deg);
    }

    25% {
        transform: translateY(-30px) rotate(4deg);
    }

    50% {
        transform: translateY(20px) rotate(-4deg);
    }

    75% {
        transform: translateY(-20px) rotate(4deg);
    }

    100% {
        left: 110vw;
        transform: translateY(0) rotate(0deg);
    }
}

.container {
    width: min(900px, 92%);
    margin: auto;
    position: relative;
    z-index: 2;
}

section {
    padding: 95px 0;
}

.hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
}

.hero-inner {
    max-width: 760px;
}

.small-title {
    color: #9ddcff;
    letter-spacing: 4px;
    text-transform: uppercase;
    font-size: .75rem;
    margin-bottom: 25px;
}

h1 {
    font-size: clamp(4rem, 15vw, 8rem);
    color: #c8edff;
    text-shadow:
        0 0 10px rgba(140,215,255,.5),
        0 0 35px rgba(100,180,255,.4),
        0 0 70px rgba(90,160,255,.25);
    margin-bottom: 20px;
    animation: glow 4s ease-in-out infinite;
}

@keyframes glow {
    0%, 100% {
        text-shadow:
            0 0 10px rgba(140,215,255,.5),
            0 0 35px rgba(100,180,255,.4);
    }

    50% {
        text-shadow:
            0 0 20px rgba(180,230,255,.8),
            0 0 60px rgba(100,180,255,.7);
    }
}

h2 {
    font-size: clamp(2rem, 7vw, 3.6rem);
    color: #bde9ff;
    margin-bottom: 25px;
}

h3 {
    color: #c9edff;
    margin-bottom: 12px;
}

p {
    line-height: 1.9;
    color: #dcefff;
}

.hero p {
    font-size: 1.15rem;
    max-width: 650px;
    margin: auto;
}

.button {
    display: inline-block;
    margin-top: 35px;
    padding: 15px 28px;
    border: 1px solid rgba(180,225,255,.55);
    border-radius: 50px;
    color: #effaff;
    text-decoration: none;
    background: rgba(110,190,255,.08);
    transition: .3s;
    cursor: pointer;
    font-family: inherit;
    font-size: 1rem;
    box-shadow: 0 0 20px rgba(80,170,255,.08);
}

.button:hover {
    background: rgba(150,220,255,.2);
    transform: translateY(-4px);
    box-shadow: 0 0 35px rgba(130,210,255,.25);
}

.card {
    background: rgba(255,255,255,.055);
    border: 1px solid rgba(180,220,255,.16);
    border-radius: 28px;
    padding: 35px;
    margin: 25px 0;
    backdrop-filter: blur(15px);
    box-shadow: 0 20px 60px rgba(0,0,0,.25);
}

.center {
    text-align: center;
}

.intro {
    font-size: 1.15rem;
    max-width: 720px;
    margin: auto;
}

/* HEART */

.tap-heart {
    width: 105px;
    height: 105px;
    margin: 35px auto;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 3.2rem;
    cursor: pointer;
    background: rgba(130,210,255,.08);
    border: 1px solid rgba(170,220,255,.3);
    box-shadow: 0 0 35px rgba(100,190,255,.15);
    transition: .4s;
    animation: heartPulse 2.5s ease-in-out infinite;
}

.tap-heart:hover {
    transform: scale(1.12);
}

@keyframes heartPulse {
    0%, 100% {
        box-shadow: 0 0 20px rgba(100,190,255,.12);
    }

    50% {
        box-shadow: 0 0 45px rgba(100,210,255,.3);
    }
}

.heart-message {
    max-height: 0;
    overflow: hidden;
    opacity: 0;
    transition: max-height 1s ease, opacity 1s ease;
}

.heart-message.show {
    max-height: 500px;
    opacity: 1;
}

/* REASONS */

.reasons {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
    gap: 15px;
    margin-top: 35px;
}

.reason {
    border: 1px solid rgba(180,220,255,.14);
    border-radius: 20px;
    padding: 22px;
    background: rgba(255,255,255,.045);
    cursor: pointer;
    transition: .35s;
}

.reason:hover {
    transform: translateY(-5px);
    background: rgba(130,210,255,.1);
}

.reason-number {
    color: #83d2ff;
    font-size: .8rem;
    margin-bottom: 8px;
}

.reason .secret {
    display: block;
    margin-top: 12px;
    color: #bce8ff;
    opacity: 0;
    max-height: 0;
    overflow: hidden;
    transition: .5s;
}

.reason.revealed .secret {
    opacity: 1;
    max-height: 150px;
}

/* STORY */

.timeline {
    margin-top: 40px;
}

.timeline-item {
    padding: 28px;
    margin: 20px 0;
    border-left: 2px solid #83caff;
    background: rgba(255,255,255,.04);
    border-radius: 0 20px 20px 0;
    transition: .3s;
}

.timeline-item:hover {
    transform: translateX(5px);
    background: rgba(120,200,255,.07);
}

/* FAVOURITES */

.favourites {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(170px, 1fr));
    gap: 15px;
    margin-top: 30px;
}

.favourite {
    text-align: center;
    padding: 28px 15px;
    border-radius: 22px;
    background: rgba(255,255,255,.05);
    border: 1px solid rgba(180,220,255,.12);
    transition: .35s;
}

.favourite:hover {
    transform: translateY(-6px);
    box-shadow: 0 10px 35px rgba(100,190,255,.1);
}

.favourite-icon {
    font-size: 2.3rem;
    margin-bottom: 12px;
}

/* CONSTELLATION */

.constellation {
    position: relative;
    height: 280px;
    margin-top: 30px;
    border-radius: 25px;
    background:
        radial-gradient(circle at center, rgba(100,180,255,.08), transparent 65%);
    overflow: hidden;
    border: 1px solid rgba(160,220,255,.12);
}

.constellation::before {
    content: "";
    position: absolute;
    width: 65%;
    height: 1px;
    background: rgba(170,220,255,.25);
    top: 43%;
    left: 18%;
    transform: rotate(10deg);
}

.constellation::after {
    content: "";
    position: absolute;
    width: 55%;
    height: 1px;
    background: rgba(170,220,255,.2);
    top: 48%;
    left: 25%;
    transform: rotate(-18deg);
}

.star {
    position: absolute;
    width: 15px;
    height: 15px;
    border-radius: 50%;
    background: white;
    box-shadow: 0 0 18px #a9ddff;
    cursor: pointer;
    transition: .3s;
    z-index: 2;
}

.star:hover {
    transform: scale(1.8);
}

.star.one {
    left: 20%;
    top: 35%;
}

.star.two {
    left: 40%;
    top: 20%;
}

.star.three {
    left: 60%;
    top: 40%;
}

.star.four {
    left: 75%;
    top: 25%;
}

.star.five {
    left: 50%;
    top: 70%;
}

.constellation-message {
    text-align: center;
    padding-top: 25px;
    color: #aee3ff;
    min-height: 60px;
}

/* OPEN WHEN */

.open-when {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 15px;
    margin-top: 30px;
}

.open-button {
    padding: 27px 15px;
    border: 1px solid rgba(180,220,255,.2);
    border-radius: 22px;
    background: rgba(255,255,255,.045);
    color: #dff5ff;
    font-family: inherit;
    font-size: 1rem;
    cursor: pointer;
    transition: .35s;
}

.open-button:hover {
    background: rgba(150,210,255,.12);
    transform: translateY(-5px);
}

/* FUTURE */

.future-list {
    list-style: none;
    margin-top: 30px;
}

.future-list li {
    padding: 20px;
    margin: 12px 0;
    border-radius: 18px;
    background: rgba(255,255,255,.045);
    border: 1px solid rgba(180,220,255,.1);
    transition: .3s;
}

.future-list li:hover {
    transform: translateX(8px);
}

.future-list li::before {
    content: "✦ ";
    color: #83caff;
}

/* LOVE LETTER */

.letter {
    max-height: 0;
    overflow: hidden;
    opacity: 0;
    transition: max-height 1.5s ease, opacity 1s ease;
}

.letter.open {
    max-height: 1200px;
    opacity: 1;
}

.letter p {
    margin-bottom: 20px;
}

/* FINAL */

.final-card {
    text-align: center;
    padding: 55px 30px;
    background:
        radial-gradient(circle at center, rgba(120,200,255,.13), transparent 65%),
        rgba(255,255,255,.04);
}

.hidden-message {
    display: none;
    margin-top: 30px;
    font-size: 1.2rem;
    line-height: 2;
    color: #dff5ff;
}

/* FOOTER */

footer {
    text-align: center;
    padding: 45px 20px;
    color: #7fa8c4;
    font-size: .9rem;
}

/* MOBILE */

@media (max-width: 600px) {

    section {
        padding: 70px 0;
    }

    .card {
        padding: 24px;
    }

    .stingray {
        opacity: .16;
    }

    .constellation {
        height: 230px;
    }
}
</style>
</head>

<body>

<div class="galaxy-cloud cloud-one"></div>
<div class="galaxy-cloud cloud-two"></div>
<div class="galaxy-cloud cloud-three"></div>

<div class="shooting-star one"></div>
<div class="shooting-star two"></div>

<div class="stingray stingray-one">
    <div class="tail"></div>
</div>

<div class="stingray stingray-two">
    <div class="tail"></div>
</div>

<div class="stingray stingray-three">
    <div class="tail"></div>
</div>


<script>

const birthday = {

    name: "Lola",

    age: 27,

    from: "Bree / Putiputi",

    birthdayMessage:
        "Today isn't just about another year passing. It's about celebrating the person who makes my world softer simply by existing in it.",

    intro:
        "So I made you a tiny universe. Every little corner is here because it reminds me of you.",

    finalMessage:
        "If I could give you anything for your birthday, it would be the ability to see yourself through my eyes. Maybe then you'd finally understand why I love you so much. Happy 27th birthday, my love. 🩵"

};

const reasons = [

    "Your hazel eyes.",
    "Your voice.",
    "The way you make me feel at home.",
    "Your little laugh.",
    "Your beautiful heart.",
    "Your softness.",
    "Your strength.",
    "Your love for otters.",
    "Your baby blue world.",
    "Your black coffee.",
    "The way you make me smile.",
    "The way you listen.",
    "Your little habits.",
    "Your beautiful soul.",
    "The way you calm me.",
    "The way you make ordinary moments special.",
    "Your kindness.",
    "Your patience.",
    "Your silly side.",
    "Your beautiful mind.",
    "The way you make distance feel smaller.",
    "The way you became my home.",
    "The way you make me feel understood.",
    "Your dreams.",
    "Your courage.",
    "The person you are becoming.",
    "Simply because you're Lola."

];

const secretReasons = [

    "You make the world feel a little less lonely.",
    "Even your silence feels comforting to me.",
    "I could listen to your voice for hours.",
    "You have a softness I never want the world to take from you.",
    "You make ordinary days feel like memories worth keeping.",
    "I love the person you are when nobody else is watching.",
    "Somehow, my heart recognised yours."

];

const favourites = [

    ["🩵", "Baby blue"],
    ["🦦", "Otters"],
    ["☕", "Black coffee"],
    ["🍣", "Sushi"],
    ["🌊", "The ocean"],
    ["⭐", "Stars"],
    ["🤎", "Hazel eyes"],
    ["🎂", "Twenty-seven"]

];

const openWhen = {

    miss:
        "If you miss me, look at the sky. Somewhere beneath that same sky is a girl who is missing you too. Distance doesn't change where my heart belongs. 🩵",

    sad:
        "If you're sad, you don't have to pretend to be okay. Come exactly as you are. You can be messy, tired, quiet or broken. I'll still love you through every version of you.",

    sleep:
        "If you can't sleep, imagine me beside you. No distance. No screens. Just quiet, warm and safe. Close your eyes and imagine my hand in yours.",

    loved:
        "If you need to feel loved, remember this: you are loved beyond the kilometres between us, beyond the days we spend apart and beyond anything words could ever properly explain."

};

const future = [

    "The day I finally get to hold you.",
    "Seeing the ocean together.",
    "A sunrise where neither of us has to say goodbye afterwards.",
    "Exploring somewhere neither of us has ever been.",
    "A little place that feels like ours.",
    "Looking at the stars beside you instead of through a screen.",
    "Growing older together."

];

</script>


<section class="hero">

<div class="container hero-inner">

<div class="small-title">
A little universe made for
</div>

<h1 id="heroName"></h1>

<p>
Twenty-seven years of you.
</p>

<p style="margin-top:20px;">
And somehow, in all the billions of people in this world,
I got lucky enough to find you.
</p>

<a href="#birthday" class="button">
Enter my little universe ↓
</a>

</div>

</section>


<section id="birthday">

<div class="container">

<div class="card center">

<div class="small-title">
For the girl who became my universe
</div>

<h2 id="birthdayTitle"></h2>

<p class="intro" id="birthdayMessage"></p>

<p class="intro" style="margin-top:20px;" id="birthdayIntro"></p>

<div class="tap-heart" onclick="revealHeart()">
♡
</div>

<div class="heart-message" id="heartMessage">

<p>
Tap the heart whenever you want a little piece of my heart.
</p>

<p style="margin-top:15px;">
Because if I could put every reason I love you into the stars,
there still wouldn't be enough of them.
</p>

</div>

</div>

</div>

</section>


<section>

<div class="container">

<div class="center">

<div class="small-title">
Twenty-seven little reasons
</div>

<h2>
Why I love you
</h2>

<p>
Tap each one. Some of them are hiding something.
</p>

</div>

<div class="reasons" id="reasons"></div>

</div>

</section>


<section>

<div class="container">

<div class="center">

<div class="small-title">
Our little story
</div>

<h2>
Then, now, always.
</h2>

</div>

<div class="timeline">

<div class="timeline-item">

<h3>
Then there was you.
</h3>

<p>
Somewhere among all the people in this enormous world,
our paths crossed.

And somehow, I found my way to you.
</p>

</div>


<div class="timeline-item">

<h3>
The distance.
</h3>

<p>
Different countries.
Different skies.
Different time zones.

And somehow you still became one of the closest people to my heart.
</p>

</div>


<div class="timeline-item">

<h3>
All the little things.
</h3>

<p>
The conversations.
The laughter.
The sleepy nights.
The storms.
The moments when your voice made everything feel okay.
</p>

</div>


<div class="timeline-item">

<h3>
And now you're 27.
</h3>

<p>
Another year of you existing,
growing,
dreaming,
laughing,
loving,
and becoming more completely yourself.
</p>

</div>

</div>

</div>

</section>


<section>

<div class="container">

<div class="center">

<div class="small-title">
Things that remind me of you
</div>

<h2>
Your little universe
</h2>

</div>

<div class="favourites" id="favourites"></div>

</div>

</section>


<section>

<div class="container">

<div class="card center">

<div class="small-title">
A constellation for you
</div>

<h2>
Find the stars ♡
</h2>

<p>
Tap the stars.
Something is waiting underneath them.
</p>

<div class="constellation">

<div class="star one" onclick="starMessage(1)"></div>

<div class="star two" onclick="starMessage(2)"></div>

<div class="star three" onclick="starMessage(3)"></div>

<div class="star four" onclick="starMessage(4)"></div>

<div class="star five" onclick="starMessage(5)"></div>

</div>

<div class="constellation-message" id="starMessage">
Tap a star above ✦
</div>

</div>

</div>

</section>


<section>

<div class="container">

<div class="center">

<div class="small-title">
For whenever you need me
</div>

<h2>
Open when...
</h2>

<p>
Some words from me for the moments when you need them most.
</p>

</div>

<div class="open-when">

<button class="open-button" onclick="showMessage('miss')">
💌
<br><br>
You miss me
</button>

<button class="open-button" onclick="showMessage('sad')">
🩵
<br><br>
You're sad
</button>

<button class="open-button" onclick="showMessage('sleep')">
🌙
<br><br>
You can't sleep
</button>

<button class="open-button" onclick="showMessage('loved')">
⭐
<br><br>
You need to feel loved
</button>

</div>

</div>

</section>


<section>

<div class="container">

<div class="center">

<div class="small-title">
Things I want with you
</div>

<h2>
Our someday
</h2>

<p>
These are little places I hope life takes us.
</p>

</div>

<ul class="future-list" id="future"></ul>

</div>

</section>


<section>

<div class="container">

<div class="card center">

<div class="small-title">
A letter from me to you
</div>

<h2>
Read this when you're ready ♡
</h2>

<button class="button" onclick="openLetter()">
Open my heart
</button>

<div class="letter" id="letter">

<br>

<p>
My love,
</p>

<p>
I wish I could be there beside you today.

I wish I could watch your face when you wake up,
give you something wrapped in far too much ribbon,
and steal the first birthday hug before anyone else could.
</p>

<p>
But even though there are kilometres between us,
there is something distance has never managed to touch.

The way I love you.
</p>

<p>
You became home to me in a way I never expected.

Not because of a place.

Not because of a house.

But because somehow,
when I'm talking to you,
the world becomes a little quieter.
</p>

<p>
So on your twenty-seventh birthday,
I hope you remember something.

You are so deeply loved.

Not because you're perfect.

Not because you always have everything figured out.

But because you're you.
</p>

<p>
And if I had to find you again
through every lifetime,
every universe,
every galaxy,
every version of this world...

I'd still look for you.
</p>

<p>
Happy birthday, my love.
</p>

<p>
I'll find you beneath every sky.

<br><br>

Bree / Putiputi ♡
</p>

</div>

</div>

</div>

</section>


<section>

<div class="container">

<div class="card final-card">

<div class="small-title">
One last thing
</div>

<h2>
Until I can give you these things in person...
</h2>

<p>
let this little universe hold them for me.
</p>

<p style="margin-top:25px;">
Love always,
<br>
<strong>Bree / Putiputi</strong>
♡
</p>

<button class="button" onclick="revealFinal()">
One last thing... 🩵
</button>

<div class="hidden-message" id="finalMessage"></div>

</div>

</div>

</section>


<footer>

Made with an unreasonable amount of love for Lola ♡

<br><br>

🌌 🩵 🦦 🌊 ⭐

</footer>


<script>

document.getElementById("heroName").textContent =
    birthday.name + " ♡";

document.getElementById("birthdayTitle").textContent =
    "Happy " + birthday.age + "th Birthday, my love.";

document.getElementById("birthdayMessage").textContent =
    birthday.birthdayMessage;

document.getElementById("birthdayIntro").textContent =
    birthday.intro;


function revealHeart() {

    document
        .getElementById("heartMessage")
        .classList.toggle("show");

}


const reasonsContainer =
    document.getElementById("reasons");

reasons.forEach((reason, index) => {

    const div =
        document.createElement("div");

    div.className =
        "reason";

    const secret =
        secretReasons[index % secretReasons.length];

    div.innerHTML = `

        <div class="reason-number">
            ${index + 1} / 27
        </div>

        <p>
            ${reason}
        </p>

        <span class="secret">
            ✦ ${secret}
        </span>

    `;

    div.onclick = function() {

        div.classList.toggle("revealed");

    };

    reasonsContainer.appendChild(div);

});


const favouritesContainer =
    document.getElementById("favourites");

favourites.forEach(item => {

    const div =
        document.createElement("div");

    div.className =
        "favourite";

    div.innerHTML = `

        <div class="favourite-icon">
            ${item[0]}
        </div>

        <p>
            ${item[1]}
        </p>

    `;

    favouritesContainer.appendChild(div);

});


const futureContainer =
    document.getElementById("future");

future.forEach(item => {

    const li =
        document.createElement("li");

    li.textContent =
        item;

    futureContainer.appendChild(li);

});


function showMessage(type) {

    alert(openWhen[type]);

}


const starMessages = {

    1:
        "You are the star I would choose in every universe. 🩵",

    2:
        "Somewhere between all these stars, I found you.",

    3:
        "Distance is only geography. My heart has never been far from yours.",

    4:
        "If the universe had a favourite love story, I hope it would be ours.",

    5:
        "Look up at the night sky. Somewhere beneath it, I'm loving you too."

};


function starMessage(number) {

    document
        .getElementById("starMessage")
        .textContent =
            starMessages[number];

}


function openLetter() {

    document
        .getElementById("letter")
        .classList.add("open");

}


function revealFinal() {

    const message =
        document.getElementById("finalMessage");

    message.innerHTML = `

        If I could give you anything for your birthday,
        it would be the ability to see yourself through my eyes.

        <br><br>

        Maybe then you'd finally understand
        why I love you so much.

        <br><br>

        You are my favourite person,
        my soft place to land,
        my little piece of home.

        <br><br>

        Happy 27th birthday, my love.

        <br><br>

        I love you across every kilometre,
        every timezone,
        every ocean,
        every sky
        and every universe.

        <br><br>

        🩵 🌌 🦦 ⭐

    `;

    message.style.display =
        "block";

}

</script>

</body>
</html>
