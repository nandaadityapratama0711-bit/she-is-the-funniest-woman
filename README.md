<html lang="en">
<head>
<meta charset="UTF-8">
<title>She Is The Funniest Woman</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family:'Poppins', sans-serif;
}

body{
  background: linear-gradient(120deg,#ffe6f0,#fff);
  color:#444;
  overflow-x:hidden;
}

/* ===== Floating Background Blob ===== */
.blob{
  position:fixed;
  width:500px;
  height:500px;
  background:radial-gradient(circle at 30% 30%,#ff9acb,#ffc1dd);
  filter: blur(80px);
  top:-100px;
  right:-100px;
  animation: floatBlob 12s infinite alternate;
  z-index:-1;
}

@keyframes floatBlob{
  from{ transform:translate(0,0); }
  to{ transform:translate(-150px,150px); }
}

/* ===== Header ===== */
header{
  height:100vh;
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
  position:relative;
}

.hero{
  animation: fadeUp 2s ease;
}

.hero h1{
  font-size:3.5rem;
  font-weight:700;
  color:#ff5fa2;
  animation: pulse 3s infinite;
}

.hero p{
  font-size:1.3rem;
  margin-top:15px;
  color:#777;
}

@keyframes pulse{
  0%{ transform:scale(1); }
  50%{ transform:scale(1.05); }
  100%{ transform:scale(1); }
}

/* ===== Sections ===== */
section{
  padding:100px 10%;
}

/* ===== About ===== */
.about{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
  gap:50px;
  align-items:center;
}

.about img{
  width:100%;
  border-radius:30px;
  box-shadow:0 20px 40px rgba(255,95,162,0.3);
  animation: floatImage 5s ease-in-out infinite;
}

@keyframes floatImage{
  0%,100%{ transform:translateY(0); }
  50%{ transform:translateY(-15px); }
}

.about-text h2{
  font-size:2.5rem;
  color:#ff5fa2;
  margin-bottom:20px;
}

.about-text p{
  line-height:1.8;
  font-size:1.05rem;
}

/* ===== Gallery ===== */
.gallery{
  text-align:center;
}

.gallery h2{
  font-size:2.5rem;
  color:#ff5fa2;
  margin-bottom:50px;
}

.gallery-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:30px;
}

.gallery-grid img{
  width:100%;
  border-radius:25px;
  transition:0.5s;
  box-shadow:0 10px 25px rgba(0,0,0,0.15);
}

.gallery-grid img:hover{
  transform:translateY(-15px) scale(1.05);
  box-shadow:0 25px 50px rgba(255,95,162,0.4);
}

/* ===== Quote ===== */
.quote{
  background:#fff;
  border-radius:40px;
  padding:60px;
  text-align:center;
  box-shadow:0 20px 40px rgba(255,95,162,0.25);
  animation: fadeUp 1.8s ease;
}

.quote h3{
  font-size:1.8rem;
  color:#ff5fa2;
}

.quote p{
  margin-top:15px;
  font-style:italic;
  color:#777;
}

/* ===== Footer ===== */
footer{
  padding:25px;
  text-align:center;
  background:#ff5fa2;
  color:#fff;
  font-size:0.9rem;
}

/* ===== Scroll Animation ===== */
.reveal{
  opacity:0;
  transform:translateY(60px);
  transition:1s;
}

.reveal.active{
  opacity:1;
  transform:translateY(0);
}

/* ===== Animations ===== */
@keyframes fadeUp{
  from{
    opacity:0;
    transform:translateY(60px);
  }
  to{
    opacity:1;
    transform:translateY(0);
  }
}
</style>
</head>

<body>

<div class="blob"></div>

<header>
  <div class="hero">
    <h1>She Is The Funniest Woman</h1>
    <p>Her laugh makes everything feel lighter 💗</p>
  </div>
</header>

<section class="reveal">
  <div class="about">
    <img src="k10.jpg">
    <div class="about-text">
      <h2>Her Magic</h2>
      <p>
        She doesn’t force humor — it flows naturally.  
        Her laughter, expressions, and silly moments make people forget their worries.
      </p>
    </div>
  </div>
</section>

<section class="gallery reveal">
  <h2>Funny Moments</h2>
  <div class="gallery-grid">
    <img src="k1.jpg">
    <img src="k4.jpg">
    <img src="k6.jpg">
    <img src="k5.jpg">
  </div>
</section>

<section class="reveal">
  <div class="quote">
    <h3>“Some people don’t just make you smile —  
    they make life feel warmer.”</h3>
    <p>— She Is The Funniest Woman</p>
  </div>
</section>

<footer>
  © 2025 | Made with 💗
</footer>

<script>
window.addEventListener("scroll", ()=>{
  document.querySelectorAll(".reveal").forEach(el=>{
    const top = el.getBoundingClientRect().top;
    if(top < window.innerHeight - 100){
      el.classList.add("active");
    }
  });
});
</script>

</body>
</html>
