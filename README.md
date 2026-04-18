
# Rfx
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>RFX Studio | Rahul</title>

<!-- Google Font -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>

/* RESET */
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family:'Poppins',sans-serif;
}

body{
  background: linear-gradient(135deg,#0f0a1f,#1a0f2e,#2a1450);
  color:white;
  scroll-behavior:smooth;
}

/* NAVBAR */
header{
  position:sticky;
  top:0;
  display:flex;
  justify-content:space-between;
  padding:20px;
  backdrop-filter:blur(10px);
  z-index:100;
}

.logo{
  font-weight:700;
  font-size:22px;
  color:#c084fc;
}

nav a{
  margin-left:20px;
  text-decoration:none;
  color:#ccc;
  transition:0.3s;
}

nav a:hover{
  color:#c084fc;
}

/* HERO */
.hero{
  text-align:center;
  padding:80px 20px;
}

.profile img{
  width:130px;
  height:130px;
  border-radius:50%;
  object-fit:cover;
  box-shadow:0 0 30px #a855f7;
  transition:0.3s;
}

.profile img:hover{
  transform:scale(1.1);
}

#upload{
  margin-top:10px;
  color:white;
}

/* TEXT */
h1{
  font-size:40px;
  margin-top:20px;
}

.tag{
  color:#c084fc;
  margin:10px 0;
}

.desc{
  max-width:500px;
  margin:auto;
  color:#bbb;
}

/* CARD */
.card{
  margin:30px;
  padding:25px;
  border-radius:20px;
  background:rgba(255,255,255,0.05);
  backdrop-filter:blur(12px);
  box-shadow:0 0 20px rgba(168,85,247,0.2);
  transition:0.3s;
}

.card:hover{
  transform:translateY(-5px);
}

/* SKILLS */
.skill{
  margin:20px 0;
}

.bar{
  height:8px;
  background:#222;
  border-radius:10px;
  overflow:hidden;
}

.bar span{
  display:block;
  height:100%;
  background:linear-gradient(90deg,#a855f7,#c084fc);
  width:0;
}

/* BUTTON */
.btn{
  display:inline-block;
  padding:12px 25px;
  background:linear-gradient(45deg,#a855f7,#c084fc);
  border-radius:25px;
  text-decoration:none;
  color:white;
  margin-top:15px;
  box-shadow:0 0 20px #a855f7;
  transition:0.3s;
}

.btn:hover{
  transform:scale(1.05);
}

/* ANIMATION */
.reveal{
  opacity:0;
  transform:translateY(50px);
  transition:1s;
}

.reveal.active{
  opacity:1;
  transform:translateY(0);
}

/* SLIDE LEFT */
.slide-left{
  transform:translateX(-80px);
}

.slide-left.active{
  transform:translateX(0);
}

/* SLIDE RIGHT */
.slide-right{
  transform:translateX(80px);
}

.slide-right.active{
  transform:translateX(0);
}

</style>
</head>

<body>

<header>
  <div class="logo">RFX Studio</div>
  <nav>
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<section class="hero reveal">
  <div class="profile">
    <img id="profilePic" src="https://via.placeholder.com/150">
    <input type="file" id="upload">
  </div>

  <h1>RAHUL</h1>
  <p class="tag">🎬 Video Editor | Motion Designer</p>

  <p class="desc">
    Creative video editor with 2+ years experience in cinematic edits, reels,
    motion graphics and storytelling.
  </p>
</section>

<section id="about" class="card reveal slide-left">
  <h2>About Me</h2>
  <p>📍 Bengaluru, India</p>
  <p>📞 9900809042</p>
  <p>✉️ rahulxeditzrahulxeditz@gmail.com</p>
</section>

<section id="skills" class="card reveal slide-right">
  <h2>Skills</h2>

  <div class="skill">
    <p>Video Editing</p>
    <div class="bar"><span data-width="90%"></span></div>
  </div>

  <div class="skill">
    <p>Motion Graphics</p>
    <div class="bar"><span data-width="85%"></span></div>
  </div>

  <div class="skill">
    <p>Color Grading</p>
    <div class="bar"><span data-width="80%"></span></div>
  </div>

</section>

<section id="contact" class="card reveal">
  <h2>Contact</h2>
  <p>📞 9900809042</p>

  <a href="https://www.instagram.com/rfxs_tudio" target="_blank" class="btn">
    Instagram
  </a>
</section>

<script>

/* SCROLL ANIMATION */
window.addEventListener("scroll",()=>{
  document.querySelectorAll(".reveal").forEach(el=>{
    let top=el.getBoundingClientRect().top;
    let height=window.innerHeight;

    if(top<height-100){
      el.classList.add("active");
    }
  });
});

/* SKILL BAR ANIMATION */
window.addEventListener("scroll",()=>{
  document.querySelectorAll(".bar span").forEach(bar=>{
    let top=bar.getBoundingClientRect().top;
    if(top<window.innerHeight-50){
      bar.style.width=bar.dataset.width;
    }
  });
});

/* PROFILE UPLOAD */
document.getElementById("upload").addEventListener("change",function(e){
  const reader=new FileReader();
  reader.onload=function(){
    document.getElementById("profilePic").src=reader.result;
  }
  reader.readAsDataURL(e.target.files[0]);
});

</script>

</body>
</html>
rfx-logo.jpg<img width="1440" height="1440" alt="New Project 360  7566C79" src="https://github.com/user-attachments/assets/ef0b6c52-5e32-42ee-b252-cbd9b5d619df" />
