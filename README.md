<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AI Lawyer - Legal AI Assistant</title>

<style>
/* =========================
   GLOBAL STYLES
========================= */
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family: Arial, Helvetica, sans-serif;
}

body{
    background:#f4f6f9;
    color:#333;
    line-height:1.6;
}

a{
    text-decoration:none;
}

.container{
    width:90%;
    max-width:1200px;
    margin:auto;
}

/* =========================
   HEADER
========================= */
header{
    background:#111827;
    color:white;
    padding:20px 0;
}

header .container{
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.logo{
    font-size:24px;
    font-weight:bold;
}

nav ul{
    display:flex;
    list-style:none;
    gap:20px;
}

nav a{
    color:white;
    font-weight:500;
}

.menu-toggle{
    display:none;
    font-size:28px;
    cursor:pointer;
}

/* =========================
   HERO SECTION
========================= */
.hero{
    background:linear-gradient(to right,#2563eb,#1e3a8a);
    color:white;
    padding:80px 20px;
    text-align:center;
}

.hero h1{
    font-size:40px;
    margin-bottom:20px;
}

.hero p{
    font-size:18px;
    margin-bottom:30px;
}

.btn{
    background:#fff;
    color:#2563eb;
    padding:12px 25px;
    border-radius:30px;
    font-weight:bold;
    transition:0.3s;
}

.btn:hover{
    background:#ddd;
}

/* =========================
   FEATURES
========================= */
.features{
    padding:60px 0;
}

.features h2{
    text-align:center;
    margin-bottom:40px;
}

.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:20px;
}

.card{
    background:white;
    padding:25px;
    border-radius:10px;
    box-shadow:0 5px 15px rgba(0,0,0,0.1);
    transition:0.3s;
}

.card:hover{
    transform:translateY(-5px);
}

.card h3{
    margin-bottom:15px;
    color:#2563eb;
}

/* =========================
   USERS SECTION
========================= */
.users{
    background:#e5e7eb;
    padding:60px 0;
    text-align:center;
}

.users h2{
    margin-bottom:30px;
}

.user-box{
    background:white;
    padding:20px;
    border-radius:8px;
    margin:10px;
    display:inline-block;
    width:220px;
}

/* =========================
   PROGRESS SECTION
========================= */
.progress-section{
    padding:60px 0;
    text-align:center;
}

.progress-bar{
    background:#ddd;
    border-radius:20px;
    overflow:hidden;
    margin:20px auto;
    width:70%;
}

.progress-fill{
    background:#2563eb;
    height:25px;
    width:0%;
    text-align:right;
    padding-right:10px;
    color:white;
    font-weight:bold;
    transition:width 2s ease;
}

/* =========================
   FAQ SECTION
========================= */
.faq{
    background:white;
    padding:60px 0;
}

.faq-item{
    margin-bottom:15px;
}

.faq-question{
    background:#2563eb;
    color:white;
    padding:15px;
    cursor:pointer;
    border-radius:5px;
}

.faq-answer{
    display:none;
    padding:15px;
    background:#f3f4f6;
}

/* =========================
   FOOTER
========================= */
footer{
    background:#111827;
    color:white;
    padding:30px;
    text-align:center;
}

/* =========================
   MOBILE RESPONSIVE
========================= */
@media(max-width:768px){
    nav ul{
        flex-direction:column;
        display:none;
        background:#111827;
        position:absolute;
        top:70px;
        right:0;
        width:200px;
        padding:20px;
    }

    nav ul.show{
        display:block;
    }

    .menu-toggle{
        display:block;
    }
}
</style>
</head>

<body>

<header>
    <div class="container">
        <div class="logo">⚖ AI Lawyer</div>
        <div class="menu-toggle" onclick="toggleMenu()">☰</div>
        <nav>
            <ul id="nav-menu">
                <li><a href="#features">Features</a></li>
                <li><a href="#users">Users</a></li>
                <li><a href="#faq">FAQ</a></li>
                <li><a href="#">Login</a></li>
            </ul>
        </nav>
    </div>
</header>

<section class="hero">
    <h1>Your AI-Powered Legal Assistant</h1>
    <p>Research laws, draft documents, analyze contracts and save 75% time instantly.</p>
    <a href="#" class="btn">Try for Free</a>
</section>

<section class="features" id="features">
    <div class="container">
        <h2>Legal AI Features</h2>
        <div class="grid">
            <div class="card">
                <h3>📄 Document Automation</h3>
                <p>Generate contracts, demand letters, and agreements in seconds.</p>
            </div>
            <div class="card">
                <h3>🔎 AI Legal Research</h3>
                <p>Find case laws and legal insights instantly using AI research tools.</p>
            </div>
            <div class="card">
                <h3>🌐 Multi Platform</h3>
                <p>Access on Web, iOS and Android anytime, anywhere.</p>
            </div>
            <div class="card">
                <h3>🔒 Private & Secure</h3>
                <p>Encrypted conversations and secure document storage.</p>
            </div>
        </div>
    </div>
</section>

<section class="users" id="users">
    <h2>Who is AI Lawyer For?</h2>
    <div class="user-box">Legal Consumers</div>
    <div class="user-box">Lawyers</div>
    <div class="user-box">Law Firms</div>
    <div class="user-box">Law Students</div>
</section>

<section class="progress-section">
    <h2>Why Choose AI Lawyer?</h2>
    <p>75% Time Saved on routine legal tasks</p>
    <div class="progress-bar">
        <div class="progress-fill" id="progress">75%</div>
    </div>
</section>

<section class="faq" id="faq">
    <div class="container">
        <h2>Frequently Asked Questions</h2>

        <div class="faq-item">
            <div class="faq-question" onclick="toggleFAQ(this)">What is AI Lawyer?</div>
            <div class="faq-answer">AI Lawyer is an AI-powered assistant that helps draft documents, research laws, and automate legal work.</div>
        </div>

        <div class="faq-item">
            <div class="faq-question" onclick="toggleFAQ(this)">Will AI replace lawyers?</div>
            <div class="faq-answer">No. AI assists lawyers by improving efficiency but does not replace professional legal advice.</div>
        </div>

        <div class="faq-item">
            <div class="faq-question" onclick="toggleFAQ(this)">Can I cancel anytime?</div>
            <div class="faq-answer">Yes. You can cancel your subscription anytime.</div>
        </div>

    </div>
</section>

<footer>
    <p>© 2026 AI Lawyer. All Rights Reserved.</p>
</footer>

<script>
// Mobile Menu Toggle
function toggleMenu(){
    document.getElementById("nav-menu").classList.toggle("show");
}

// FAQ Toggle
function toggleFAQ(element){
    let answer = element.nextElementSibling;
    answer.style.display = answer.style.display === "block" ? "none" : "block";
}

// Animate Progress Bar on Load
window.onload = function(){
    document.getElementById("progress").style.width = "75%";
}

// Smooth Scroll
document.querySelectorAll('a[href^="#"]').forEach(anchor=>{
    anchor.addEventListener("click", function(e){
        e.preventDefault();
        document.querySelector(this.getAttribute("href")).scrollIntoView({
            behavior:"smooth"
        });
    });
});
</script>

</body>
</html># ai-legal-boat
