
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DIGITAL CHAT | Connect With The World</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700;800&family=Outfit:wght@400;500;600;700;800&display=swap');

:root {
  --primary:#6842e8;
  --secondary:#ff6584;
  --dark:#17152b;
  --muted:#77758b;
  --bg:#f6f5fc;
  --white:#ffffff;
  --green:#18b981;
}

* { box-sizing:border-box; margin:0; padding:0; }

body {
  font-family:'DM Sans',sans-serif;
  background:var(--bg);
  color:var(--dark);
}

a { text-decoration:none; color:inherit; }
button { font-family:inherit; cursor:pointer; border:0; }

.topbar {
  background:#17152b;
  color:white;
  text-align:center;
  padding:10px;
  font-size:13px;
}

.topbar span { color:#ffb7c7; font-weight:700; }

header {
  background:white;
  padding:17px 6%;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:20px;
  box-shadow:0 3px 20px #17152b0a;
  position:sticky;
  top:0;
  z-index:20;
}

.logo {
  font-family:'Outfit',sans-serif;
  font-size:25px;
  font-weight:800;
  letter-spacing:-1px;
}

.logo span { color:var(--primary); }

.nav {
  display:flex;
  align-items:center;
  gap:25px;
  font-size:14px;
  font-weight:600;
}

.nav a:hover { color:var(--primary); }

.btn {
  display:inline-flex;
  align-items:center;
  justify-content:center;
  padding:12px 20px;
  border-radius:12px;
  font-weight:700;
  font-size:14px;
  transition:.2s;
}

.btn:hover { transform:translateY(-2px); }

.btn-primary {
  background:linear-gradient(135deg,#7049f0,#9b57ed);
  color:white;
  box-shadow:0 7px 18px #7049f044;
}

.btn-light { background:#f0edff; color:var(--primary); }
.btn-pink { background:#fff0f4; color:#e64e75; }

.hero {
  padding:65px 6% 55px;
  background:
    radial-gradient(circle at 85% 20%,#ffdce7 0,transparent 30%),
    radial-gradient(circle at 10% 90%,#e4dcff 0,transparent 35%),
    linear-gradient(120deg,#f5f1ff,#fff7fa);
  display:grid;
  grid-template-columns:1.1fr .9fr;
  align-items:center;
  gap:35px;
}

.eyebrow {
  color:var(--primary);
  font-size:13px;
  font-weight:800;
  letter-spacing:1.5px;
  text-transform:uppercase;
  margin-bottom:16px;
}

.hero h1 {
  font-family:'Outfit',sans-serif;
  font-size:clamp(38px,5vw,64px);
  line-height:1.08;
  letter-spacing:-2px;
  margin-bottom:20px;
}

.hero h1 span {
  background:linear-gradient(90deg,#7049f0,#f05c91);
  -webkit-background-clip:text;
  color:transparent;
}

.hero p {
  color:#69677c;
  font-size:16px;
  line-height:1.8;
  max-width:550px;
  margin-bottom:27px;
}

.hero-buttons { display:flex; gap:12px; flex-wrap:wrap; }

.hero-visual {
  position:relative;
  min-height:350px;
  display:flex;
  align-items:center;
  justify-content:center;
}

.hero-photo {
  width:85%;
  max-width:420px;
  height:350px;
  object-fit:cover;
  border-radius:35px;
  box-shadow:0 25px 60px #32215d30;
}

.floating-card {
  position:absolute;
  background:white;
  border-radius:16px;
  padding:13px 16px;
  box-shadow:0 12px 35px #17152b18;
  font-size:13px;
  font-weight:700;
}

.float-one { top:35px; left:0; }
.float-two { bottom:30px; right:0; }

.online-dot {
  display:inline-block;
  width:9px;
  height:9px;
  border-radius:50%;
  background:#18b981;
  margin-right:6px;
}

section { padding:55px 6%; }

.section-heading {
  display:flex;
  justify-content:space-between;
  align-items:end;
  gap:20px;
  margin-bottom:25px;
}

.section-heading h2 {
  font-family:'Outfit',sans-serif;
  font-size:30px;
  letter-spacing:-.7px;
}

.section-heading p {
  color:var(--muted);
  font-size:14px;
  margin-top:7px;
}

.stats {
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:18px;
}

.stat-card {
  background:white;
  padding:23px;
  border-radius:20px;
  box-shadow:0 7px 25px #17152b08;
  border:1px solid #eeeaf8;
}

.stat-top {
  display:flex;
  align-items:center;
  justify-content:space-between;
  margin-bottom:18px;
}

.stat-icon {
  width:43px;
  height:43px;
  display:grid;
  place-items:center;
  border-radius:13px;
  font-size:21px;
  background:#f0edff;
}

.stat-card:nth-child(2) .stat-icon { background:#e8fff6; }
.stat-card:nth-child(3) .stat-icon { background:#fff0f4; }

.stat-card small { color:var(--muted); font-weight:600; }
.stat-card h3 { font-size:27px; margin-top:5px; }
.stat-card .note { color:var(--muted); font-size:12px; margin-top:8px; }

.wallet-actions { display:flex; gap:10px; margin-top:20px; flex-wrap:wrap; }

.filters {
  display:flex;
  gap:10px;
  flex-wrap:wrap;
  margin-bottom:22px;
}

.search {
  flex:1;
  min-width:200px;
  padding:13px 16px;
  border:1px solid #e7e3f0;
  border-radius:12px;
  background:white;
  outline:none;
  font:inherit;
}

.search:focus { border-color:var(--primary); }

.filter-select {
  padding:13px;
  border:1px solid #e7e3f0;
  border-radius:12px;
  background:white;
  font:inherit;
  color:var(--dark);
}

.people-grid {
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:18px;
}

.person-card {
  background:white;
  border-radius:19px;
  overflow:hidden;
  border:1px solid #eeeaf5;
  transition:.25s;
}

.person-card:hover {
  transform:translateY(-5px);
  box-shadow:0 15px 35px #30215b15;
}

.person-image {
  width:100%;
  height:190px;
  object-fit:cover;
  display:block;
}

.person-info { padding:15px; }

.person-name {
  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:5px;
}

.person-name h3 { font-size:16px; }

.status {
  font-size:11px;
  color:#149c70;
  font-weight:700;
}

.country {
  color:var(--muted);
  font-size:12px;
  margin:7px 0;
}

.topic {
  display:inline-block;
  background:#f1eeff;
  color:#7049e8;
  border-radius:20px;
  padding:6px 10px;
  font-size:11px;
  font-weight:700;
  margin:5px 0 13px;
}

.chat-button {
  width:100%;
  background:var(--primary);
  color:white;
  border-radius:10px;
  padding:11px;
  font-weight:700;
}

.chat-button:hover { background:#5230cb; }

.demo-label {
  font-size:10px;
  color:#999;
  margin-top:8px;
  text-align:center;
}

.empty-state {
  display:none;
  text-align:center;
  color:var(--muted);
  padding:35px;
}

.join-banner {
  margin:10px 6% 55px;
  padding:42px;
  border-radius:25px;
  background:linear-gradient(120deg,#6540e6,#a44ee9,#f05c91);
  color:white;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:25px;
}

.join-banner h2 {
  font-family:'Outfit',sans-serif;
  font-size:30px;
  margin-bottom:10px;
}

.join-banner p { color:#f4eaff; line-height:1.6; }

.join-banner .btn {
  background:white;
  color:#7049e8;
  white-space:nowrap;
}

footer {
  background:#17152b;
  color:white;
  padding:45px 6% 20px;
}

.footer-grid {
  display:grid;
  grid-template-columns:2fr 1fr 1fr;
  gap:35px;
  margin-bottom:35px;
}

footer p, footer a {
  color:#bcb9cf;
  font-size:13px;
  line-height:2;
}

footer h3 { margin-bottom:13px; }
footer a:hover { color:white; }

.copyright {
  border-top:1px solid #343149;
  padding-top:20px;
  text-align:center;
  color:#9995ad;
  font-size:12px;
}

.contact-links {
  display:flex;
  gap:10px;
  flex-wrap:wrap;
  margin-top:15px;
}

.contact-links a {
  display:inline-block;
  background:#ffffff13;
  border-radius:9px;
  padding:9px 13px;
  color:white;
}

.modal {
  display:none;
  position:fixed;
  inset:0;
  z-index:100;
  background:#100d20b8;
  align-items:center;
  justify-content:center;
  padding:15px;
}

.modal.show { display:flex; }

.modal-box {
  background:white;
  width:100%;
  max-width:440px;
  border-radius:20px;
  overflow:hidden;
  box-shadow:0 20px 70px #0003;
}

.modal-header {
  padding:17px 20px;
  background:linear-gradient(120deg,#6842e8,#a34de9);
  color:white;
  display:flex;
  justify-content:space-between;
  align-items:center;
}

.close {
  background:#ffffff25;
  color:white;
  font-size:23px;
  width:33px;
  height:33px;
  border-radius:9px;
}

.chat-content { padding:20px; }

.chat-person {
  display:flex;
  gap:12px;
  align-items:center;
  margin-bottom:20px;
}

.chat-person img {
  width:50px;
  height:50px;
  object-fit:cover;
  border-radius:50%;
}

.chat-message {
  background:#f2efff;
  padding:13px;
  border-radius:13px;
  font-size:13px;
  line-height:1.6;
  margin-bottom:15px;
}

.chat-warning {
  font-size:12px;
  color:#777;
  line-height:1.6;
  margin-bottom:15px;
}

.chat-input-row { display:flex; gap:8px; }

.chat-input-row input {
  flex:1;
  min-width:0;
  padding:12px;
  border:1px solid #e6e2ef;
  border-radius:10px;
  outline:none;
}

.chat-input-row button {
  background:var(--primary);
  color:white;
  padding:0 15px;
  border-radius:10px;
}

.toast {
  display:none;
  position:fixed;
  bottom:20px;
  left:50%;
  transform:translateX(-50%);
  background:#17152b;
  color:white;
  padding:13px 20px;
  border-radius:12px;
  z-index:200;
  font-size:13px;
}

@media(max-width:950px) {
  .people-grid { grid-template-columns:repeat(3,1fr); }
}

@media(max-width:700px) {
  header { padding:14px 5%; }
  .nav { display:none; }
  .hero {
    grid-template-columns:1fr;
    padding:45px 6%;
  }
  .hero-visual { min-height:280px; }
  .hero-photo { height:270px; }
  .stats { grid-template-columns:1fr; }
  .people-grid { grid-template-columns:repeat(2,1fr); gap:12px; }
  .person-image { height:150px; }
  .join-banner { margin:5px 5% 40px; padding:27px; flex-direction:column; align-items:flex-start; }
  .join-banner h2 { font-size:25px; }
  .footer-grid { grid-template-columns:1fr; gap:25px; }
  section { padding:40px 5%; }
  .section-heading { align-items:flex-start; flex-direction:column; }
}

@media(max-width:380px) {
  .people-grid { grid-template-columns:1fr; }
  .person-image { height:210px; }
}
</style>
</head>

<body>

<div class="topbar">
  Welcome to <span>DIGITAL CHAT</span> — Connect, communicate and discover new cultures.
</div>

<header>
  <a href="#" class="logo">DIGITAL<span>CHAT.</span></a>

  <nav class="nav">
    <a href="#home">Home</a>
    <a href="#people">People</a>
    <a href="#wallet">Dashboard</a>
    <a href="#contact">Contact</a>
  </nav>

  <a class="btn btn-primary" href="https://moxeraagencies.com/register?ref=JOBSCODE" target="_blank">
    Join Now ↗
  </a>
</header>

<!-- HERO -->
<div class="hero" id="home">
  <div>
    <div class="eyebrow">🌍 A world of conversations</div>
    <h1>Meet People.<br><span>Share Languages.</span><br>Connect Globally.</h1>

    <p>
      Discover people from different countries, make new connections
      and enjoy conversations across cultures. Your next conversation
      could start here.
    </p>

    <div class="hero-buttons">
      <a href="#people" class="btn btn-primary">Explore People →</a>
      <a href="https://moxeraagencies.com/register?ref=JOBSCODE"
         target="_blank" class="btn btn-light">Create Account</a>
    </div>
  </div>

  <div class="hero-visual">
    <img class="hero-photo"
      src="https://images.unsplash.com/photo-1529156069898-49953e39b3ac?w=900"
      alt="People connecting and talking">

    <div class="floating-card float-one">
      🌍 Connect across countries
    </div>

    <div class="floating-card float-two">
      💬 New conversations start here
    </div>
  </div>
</div>

<!-- DASHBOARD -->
<section id="wallet">
  <div class="section-heading">
    <div>
      <h2>Your Dashboard</h2>
      <p>Your account overview will appear here after account integration.</p>
    </div>
  </div>

  <div class="stats">
    <div class="stat-card">
      <div class="stat-top">
        <div>
          <small>NET PROFIT</small>
          <h3>0.00</h3>
        </div>
        <div class="stat-icon">📈</div>
      </div>
      <div class="note">Account earnings information</div>
    </div>

    <div class="stat-card">
      <div class="stat-top">
        <div>
          <small>BALANCE</small>
          <h3>0.00</h3>
        </div>
        <div class="stat-icon">💰</div>
      </div>
      <div class="note">Your available account balance</div>
    </div>

    <div class="stat-card">
      <div class="stat-top">
        <div>
          <small>WITHDRAWAL</small>
          <h3>0.00</h3>
        </div>
        <div class="stat-icon">💳</div>
      </div>
      <div class="note">Withdrawal information</div>
    </div>
  </div>

  <div class="wallet-actions">
    <button class="btn btn-primary" onclick="walletMessage()">Withdraw</button>
    <button class="btn btn-light" onclick="walletMessage()">Transaction History</button>
  </div>
</section>

<!-- PEOPLE -->
<section id="people">
  <div class="section-heading">
    <div>
      <div class="eyebrow">Discover new connections</div>
      <h2>People to Chat With</h2>
      <p>Explore profiles and discover people from around the world.</p>
    </div>
  </div>

  <div class="filters">
    <input class="search" id="searchInput"
      type="search" placeholder="🔍 Search by name or country...">

    <select class="filter-select" id="countryFilter">
      <option value="">All Countries</option>
      <option value="USA">USA</option>
      <option value="UK">United Kingdom</option>
      <option value="Canada">Canada</option>
      <option value="Germany">Germany</option>
      <option value="France">France</option>
      <option value="Australia">Australia</option>
      <option value="Tanzania">Tanzania</option>
      <option value="Italy">Italy</option>
    </select>

    <select class="filter-select" id="topicFilter">
      <option value="">All Topics</option>
      <option value="Language">Language</option>
      <option value="Culture">Culture</option>
      <option value="Travel">Travel</option>
      <option value="Lifestyle">Lifestyle</option>
      <option value="Business">Business</option>
    </select>
  </div>

  <div class="people-grid" id="peopleGrid"></div>

  <div class="empty-state" id="emptyState">
    No matching profiles found. Try another search.
  </div>
</section>

<!-- REGISTRATION -->
<div class="join-banner">
  <div>
    <h2>Ready to Join DIGITAL CHAT?</h2>
    <p>Create your account and discover new opportunities to connect with people.</p>
  </div>

  <a href="https://moxeraagencies.com/register?ref=JOBSCODE"
     target="_blank" class="btn">Register Now ↗</a>
</div>

<!-- FOOTER -->
<footer id="contact">
  <div class="footer-grid">
    <div>
      <div class="logo">DIGITAL<span style="color:#ff789c">CHAT.</span></div>
      <p style="margin-top:15px;max-width:350px">
        A platform concept for connecting people, sharing languages
        and discovering different cultures around the world.
      </p>
    </div>

    <div>
      <h3>Quick Links</h3>
      <p><a href="#home">Home</a></p>
      <p><a href="#people">Explore People</a></p>
      <p><a href="#wallet">Dashboard</a></p>
      <p><a href="https://moxeraagencies.com/register?ref=JOBSCODE" target="_blank">Register</a></p>
    </div>

    <div>
      <h3>Contact Us</h3>
      <p>WhatsApp: 0799223490</p>
      <p>Phone: 0756501819</p>

      <div class="contact-links">
        <a href="https://wa.me/255799223490" target="_blank">WhatsApp Us</a>
        <a href="tel:+255756501819">Call Us</a>
      </div>
    </div>
  </div>

  <div class="copyright">
    © 2026 DIGITAL CHAT. All rights reserved.
  </div>
</footer>

<!-- CHAT MODAL -->
<div class="modal" id="chatModal">
  <div class="modal-box">
    <div class="modal-header">
      <strong>💬 DIGITAL CHAT</strong>
      <button class="close" onclick="closeChat()">×</button>
    </div>

    <div class="chat-content">
      <div class="chat-person">
        <img id="chatImage" src="" alt="Profile">
        <div>
          <strong id="chatName">Profile</strong>
          <div style="font-size:12px;color:#777" id="chatCountry"></div>
        </div>
      </div>

      <div class="chat-message">
        Hello! Welcome to DIGITAL CHAT. 👋
        This is a preview of the conversation interface.
      </div>

      <p class="chat-warning">
        This chat window is currently a front-end preview.
        Real messages between users require a connected chat server
        and registered user accounts.
      </p>

      <div class="chat-input-row">
        <input type="text" id="messageInput"
          placeholder="Type a message..." disabled>
        <button onclick="chatNotice()">Send</button>
      </div>
    </div>
  </div>
</div>

<div class="toast" id="toast"></div>

<script>
const registrationLink = "https://moxeraagencies.com/register?ref=JOBSCODE";

const people = [
  {name:"Emma",country:"USA",topic:"Language",image:"https://images.unsplash.com/photo-1534528741775-53994a69daeb?w=500"},
  {name:"Daniel",country:"UK",topic:"Travel",image:"https://images.unsplash.com/photo-1500648767791-00dcc994a43e?w=500"},
  {name:"Sophia",country:"Canada",topic:"Culture",image:"https://images.unsplash.com/photo-1524504388940-b1c1722653e1?w=500"},
  {name:"James",country:"Germany",topic:"Business",image:"https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?w=500"},
  {name:"Olivia",country:"France",topic:"Lifestyle",image:"https://images.unsplash.com/photo-1517841905240-472988babdf9?w=500"},
  {name:"Michael",country:"Australia",topic:"Travel",image:"https://images.unsplash.com/photo-1504593811423-6dd665756598?w=500"},
  {name:"Ava",country:"Italy",topic:"Language",image:"https://images.unsplash.com/photo-1529139574466-a303027c1d8b?w=500"},
  {name:"Noah",country:"USA",topic:"Culture",image:"https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=500"},
  {name:"Mia",country:"Canada",topic:"Lifestyle",image:"https://images.unsplash.com/photo-1531123897727-8f129e1688ce?w=500"},
  {name:"Lucas",country:"UK",topic:"Business",image:"https://images.unsplash.com/photo-1519085360753-af0119f7cbe7?w=500"},
  {name:"Isabella",country:"Germany",topic:"Travel",image:"https://images.unsplash.com/photo-1544005313-94ddf0286df2?w=500"},
  {name:"Ethan",country:"France",topic:"Language",image:"https://images.unsplash.com/photo-1504257432389-52343af06ae3?w=500"},
  {name:"Amara",country:"Tanzania",topic:"Culture",image:"https://images.unsplash.com/photo-1534528741775-53994a69daeb?w=500"},
  {name:"Leo",country:"Italy",topic:"Business",image:"https://images.unsplash.com/photo-1500648767791-00dcc994a43e?w=500"},
  {name:"Grace",country:"Australia",topic:"Lifestyle",image:"https://images.unsplash.com/photo-1517841905240-472988babdf9?w=500"},
  {name:"Oliver",country:"USA",topic:"Travel",image:"https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?w=500"}
];

const grid = document.getElementById("peopleGrid");

function renderPeople() {
  const search = document.getElementById("searchInput").value.toLowerCase();
  const country = document.getElementById("countryFilter").value;
  const topic = document.getElementById("topicFilter").value;

  const filtered = people.filter(person =>
    (person.name.toLowerCase().includes(search) ||
     person.country.toLowerCase().includes(search)) &&
    (!country || person.country === country) &&
    (!topic || person.topic === topic)
  );

  grid.innerHTML = "";

  filtered.forEach(person => {
    const card = document.createElement("div");
    card.className = "person-card";

    card.innerHTML = `
      <img class="person-image" src="${person.image}" alt="Sample profile">
      <div class="person-info">
        <div class="person-name">
          <h3>${person.name}</h3>
          <span class="status">● Profile</span>
        </div>
        <div class="country">🌍 ${person.country}</div>
        <span class="topic">${person.topic}</span>
        <button class="chat-button">View Chat</button>
        <div class="demo-label">Sample profile · Not a live user</div>
      </div>
    `;

    card.querySelector(".chat-button").addEventListener("click", () => {
      openChat(person);
    });

    grid.appendChild(card);
  });

  document.getElementById("emptyState").style.display =
    filtered.length ? "none" : "block";
}

document.getElementById("searchInput").addEventListener("input",renderPeople);
document.getElementById("countryFilter").addEventListener("change",renderPeople);
document.getElementById("topicFilter").addEventListener("change",renderPeople);

function openChat(person) {
  document.getElementById("chatName").textContent = person.name;
  document.getElementById("chatCountry").textContent = person.country;
  document.getElementById("chatImage").src = person.image;
  document.getElementById("chatModal").classList.add("show");
}

function closeChat() {
  document.getElementById("chatModal").classList.remove("show");
}

function chatNotice() {
  showToast("Real-time messaging will be enabled after backend setup.");
}

function walletMessage() {
  showToast("Wallet and withdrawals require account and payment integration.");
}

function showToast(message) {
  const toast = document.getElementById("toast");
  toast.textContent = message;
  toast.style.display = "block";
  setTimeout(() => toast.style.display = "none", 3500);
}

document.getElementById("chatModal").addEventListener("click", function(e) {
  if (e.target === this) closeChat();
});

renderPeople();
</script>

</body>
</html>
