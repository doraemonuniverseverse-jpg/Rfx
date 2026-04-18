<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>RFX Studio | Rahul</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>

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
}

.logo{
  font-weight:700;
  color:#c084fc;
}

nav a{
  margin-left:20px;
  color:#ccc;
  text-decoration:none;
}

nav a:hover{
  color:#c084fc;
}

/* HERO */
.hero{
  text-align:center;
  padding:60px 20px;
}

/* PROFILE */
.profile{
  position:relative;
}

.profile img{
  width:150px;
  height:150px;
  border-radius:50%;
  object-fit:cover;
  border:3px solid #c084fc;
  background:black;
  box-shadow:0 0 40px #a855f7;
}

/* Upload Button */
.upload-btn{
  margin-top:10px;
  color:#c084fc;
  font-size:14px;
}

/* TEXT */
h1{
  margin-top:20px;
  font-size:36px;
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
    <!-- Default Image -->
    <img id="profilePic" src="rfx-logo.jpg">

    <!-- Upload Option -->
    <input type="file" id="upload" class="upload-btn">
  </div>

  <h1>RAHUL</h1>
  <p class="tag">🎬 Video Editor | Motion Designer</p>

  <p class="desc">
    Creative video editor with 2+ years experience in cinematic edits,
    reels, motion graphics and storytelling.
  </p>

</section>

<section id="about" class="card reveal">
  <h2>About Me</h2>
  <p>📍 Bengaluru, India</p>
  <p>📞 9900809042</p>
  <p>✉️ rahulxeditzrahulxeditz@gmail.com</p>
</section>

<section id="skills" class="card reveal">
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
    if(top<window.innerHeight-100){
      el.classList.add("active");
    }
  });
});

/* SKILL BAR */
window.addEventListener("scroll",()=>{
  document.querySelectorAll(".bar span").forEach(bar=>{
    let top=bar.getBoundingClientRect().top;
    if(top<window.innerHeight-50){
      bar.style.width=bar.dataset.width;
    }
  });
});

/* IMAGE UPLOAD (Preview only) */
document.getElementById("upload").addEventListener("change",function(e){
  const file = e.target.files[0];
  if(file){
    const reader=new FileReader();
    reader.onload=function(){
      document.getElementById("profilePic").src=reader.result;
    }
    reader.readAsDataURL(file);
  }
});

</script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>RFX Studio | Rahul</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>

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
}

.logo{
  font-weight:700;
  color:#c084fc;
  font-size:22px;
}

nav a{
  margin-left:20px;
  color:#ccc;
  text-decoration:none;
}

nav a:hover{
  color:#c084fc;
}

/* HERO */
.hero{
  text-align:center;
  padding:60px 20px;
}

/* PROFILE (FIXED CENTER) */
.profile{
  display:flex;
  flex-direction:column;
  align-items:center;
}

.profile img{
  width:150px;
  height:150px;
  border-radius:50%;
  object-fit:cover;
  border:3px solid #c084fc;
  background:black;
  box-shadow:0 0 40px #a855f7;
}

/* Upload */
.upload-btn{
  margin-top:10px;
  color:#c084fc;
}

/* TEXT */
h1{
  margin-top:20px;
  font-size:36px;
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

<!-- HERO -->
<section class="hero reveal">

  <div class="profile">
    <!-- ONLY ONE IMAGE (FIXED) -->
    <img id="profilePic" src="rfx-logo.jpg">

    <!-- Upload (optional preview only) -->
    <input type="file" id="upload" class="upload-btn">
  </div>

  <h1>RAHUL</h1>
  <p class="tag">🎬 Video Editor | Motion Designer</p>

  <p class="desc">
    Creative video editor with 2+ years experience in cinematic edits,
    reels, motion graphics and storytelling.
  </p>

</section>

<!-- ABOUT -->
<section id="about" class="card reveal">
  <h2>About Me</h2>
  <p>📍 Bengaluru, India</p>
  <p>📞 9900809042</p>
  <p>✉️ rahulxeditzrahulxeditz@gmail.com</p>
</section>

<!-- SKILLS -->
<section id="skills" class="card reveal">
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

<!-- CONTACT -->
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
    if(top<window.innerHeight-100){
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

/* IMAGE UPLOAD PREVIEW */
document.getElementById("upload").addEventListener("change",function(e){
  const file=e.target.files[0];
  if(file){
    const reader=new FileReader();
    reader.onload=function(){
      document.getElementById("profilePic").src=reader.result;
    }
    reader.readAsDataURL(file);
  }
});

</script>

</body>
</html>