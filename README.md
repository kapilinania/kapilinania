<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kapil | AI Portfolio</title>

<style>
body {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background: radial-gradient(circle at top, #0f2027, #000);
  color: white;
  overflow-x: hidden;
}

/* 🔥 HOLOGRAM EFFECT */
.glow {
  color: #00f7ff;
  text-shadow: 0 0 10px #00f7ff, 0 0 20px #00f7ff;
}

/* NAV */
header {
  display: flex;
  justify-content: space-between;
  padding: 20px 10%;
}

/* HERO */
.hero {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 50px 10%;
  flex-wrap: wrap;
}

/* 🤖 AVATAR */
.avatar {
  width: 300px;
  border-radius: 50%;
  box-shadow: 0 0 50px #00f7ff;
  animation: float 4s ease-in-out infinite;
}

@keyframes float {
  0%,100% { transform: translateY(0); }
  50% { transform: translateY(-20px); }
}

/* BUTTON */
.btn {
  padding: 12px 25px;
  background: #00f7ff;
  color: black;
  border-radius: 30px;
  text-decoration: none;
}

/* CHATBOT */
.chatbot {
  position: fixed;
  bottom: 20px;
  right: 20px;
  width: 300px;
  background: rgba(255,255,255,0.05);
  backdrop-filter: blur(10px);
  border-radius: 15px;
  overflow: hidden;
}

.chat-header {
  background: #00f7ff;
  color: black;
  padding: 10px;
}

.chat-body {
  height: 200px;
  overflow-y: auto;
  padding: 10px;
}

.chat-input {
  display: flex;
}

.chat-input input {
  flex: 1;
  padding: 10px;
  border: none;
}

.chat-input button {
  padding: 10px;
  background: #00f7ff;
  border: none;
}

/* SKILLS */
.skills {
  padding: 50px 10%;
}

.skill-box {
  display: inline-block;
  padding: 10px 20px;
  margin: 10px;
  border: 1px solid #00f7ff;
  border-radius: 20px;
}

/* RESPONSIVE */
@media(max-width:768px){
.hero {flex-direction: column; text-align:center;}
.avatar {margin-top:20px;}
}
</style>

</head>
<body>

<header>
  <h2 class="glow">Kapil.dev</h2>
</header>

<section class="hero">
  <div>
    <h1>Hi 👋 I'm <span class="glow">Kapil</span></h1>
    <h2>AI + Frontend Developer 🚀</h2>
    <p>Building futuristic web experiences</p>
    <a href="#" class="btn">Hire Me</a>
  </div>

  <!-- 🤖 AVATAR -->
  <img class="avatar" src="https://i.imgur.com/6VBx3io.png" alt="avatar">
</section>

<!-- SKILLS -->
<section class="skills">
  <h2 class="glow">Tech Stack</h2>
  <div class="skill-box">HTML</div>
  <div class="skill-box">CSS</div>
  <div class="skill-box">JavaScript</div>
  <div class="skill-box">React</div>
  <div class="skill-box">AI</div>
</section>

<!-- 🤖 CHATBOT -->
<div class="chatbot">
  <div class="chat-header">AI Assistant 🤖</div>
  <div class="chat-body" id="chatBody">
    <p>Hi! Ask me anything 👋</p>
  </div>
  <div class="chat-input">
    <input type="text" id="userInput" placeholder="Type...">
    <button onclick="sendMessage()">➤</button>
  </div>
</div>

<script>
function sendMessage(){
  let input = document.getElementById("userInput");
  let chat = document.getElementById("chatBody");

  let userText = input.value;
  if(userText === "") return;

  chat.innerHTML += "<p><b>You:</b> " + userText + "</p>";

  let reply = "I am your AI assistant 🤖";

  if(userText.toLowerCase().includes("skill")){
    reply = "Kapil knows HTML, CSS, JS, React & AI 🚀";
  }

  if(userText.toLowerCase().includes("contact")){
    reply = "Email: Inaniyakapil2000@gmail.com";
  }

  setTimeout(()=>{
    chat.innerHTML += "<p><b>Bot:</b> " + reply + "</p>";
    chat.scrollTop = chat.scrollHeight;
  },500);

  input.value="";
}
</script>

</body>
</html>
