
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kak Nia Anehhhhh💛</title>

<style>
*{
  box-sizing:border-box;
  font-family:'Segoe UI',sans-serif;
}

body{
  margin:0;
  overflow-x:hidden;
  overflow-y:auto;
}

/* ===== BACKGROUND ===== */
.wrapper{
  width:100vw;
  position:relative;
}

body{
  margin:0;
  overflow-x:hidden;
}

body::before{
  content:"";
  position:fixed;
  top:0;
  left:0;
  width:100vw;
  height:100vh;
  background:linear-gradient(135deg,#FFC371,#FF5F6D);
  z-index:-1;
}

.nebula{
  position:fixed;
  inset:0;
  background:
    radial-gradient(circle at 30% 40%, rgba(199,125,255,0.35), transparent 50%),
    radial-gradient(circle at 70% 60%, rgba(255,217,61,0.25), transparent 55%);
  filter:blur(60px);
  z-index:0;
  pointer-events:none;
}
.stars{
  position:fixed;
  inset:0;
  pointer-events:none;
  z-index:1;
  background:
    radial-gradient(2px 2px at 10% 20%, #fff, transparent),
    radial-gradient(2.5px 2.5px at 25% 80%, #ffe066, transparent),
    radial-gradient(2px 2px at 40% 40%, #fff, transparent),
    radial-gradient(3px 3px at 65% 30%, #ffd93d, transparent),
    radial-gradient(2px 2px at 85% 60%, #fff, transparent);
  background-size:250px 250px;
  animation:twinkle 6s infinite alternate;
}

@keyframes twinkle{
  from{opacity:.7;}
  to{opacity:1;}
}

.star-burst{
  position:fixed;
  font-size:22px;
  animation:burst 1.2s ease-out forwards;
  pointer-events:none;
  z-index:3;
}

@keyframes burst{
  0%{transform:scale(.2);opacity:1;}
  100%{transform:translate(var(--x),var(--y)) scale(1.4);opacity:0;}
}

/* ===== AUDIO BUTTON ===== */
.audio-control{
  position:fixed;
  top:15px;
  right:15px;
  padding:10px 18px;
  background:rgba(255,255,255,0.85);
  border-radius:30px;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:14px;
  font-weight:600;
  cursor:pointer;
  z-index:999;
  transition:all 0.4s ease;
}

/* === GLOW SAAT MUSIK PLAY (TAMBAHAN) === */
.audio-control.music-playing{
  animation:buttonGlow 2.5s ease-in-out infinite;
}

@keyframes buttonGlow{
  0%{
    box-shadow:0 0 6px rgba(255,217,61,0.5),
               0 0 12px rgba(199,125,255,0.4);
  }
  50%{
    box-shadow:0 0 12px rgba(255,217,61,0.9),
               0 0 22px rgba(199,125,255,0.8);
  }
  100%{
    box-shadow:0 0 6px rgba(255,217,61,0.5),
               0 0 12px rgba(199,125,255,0.4);
  }
}


/* ===== SLIDE ===== */
.slide{
  position:absolute;
  width:100%;
  min-height:100vh;
  display:flex;
  align-items:flex-start;
  justify-content:center;
  opacity:0;
  padding:40px 0;
  transform:translateY(30px);
  transition:all 0.8s ease;
  pointer-events:none;
}

.slide.active{
  opacity:1;
  transform:translateY(0);
  pointer-events:auto;
}

/* ===== CONTENT BOX ===== */
.content{
  max-width:700px;
  width:90%;
  background:rgba(255,255,255,0.9);
  border-radius:22px;
  padding:25px;
  text-align:center;
  box-shadow:0 15px 40px rgba(0,0,0,0.2);
}

/* ===== PHOTO (REVISI) ===== */
.photo-box{
  width:200px;
  height:200px;
  margin:0 auto 20px;
  border-radius:20px;
  padding:4px;
  background:
    linear-gradient(#fff,#fff) padding-box,
    linear-gradient(135deg,#FFD93D,#C77DFF,#FFD93D) border-box;
  border:3px solid transparent;
  animation:shimmer 4s linear infinite;
}

.photo-box img{
  width:100%;
  height:100%;
  object-fit:cover;
  border-radius:16px;
}

@keyframes shimmer{
  0%{filter:brightness(1);}
  50%{filter:brightness(1.15);}
  100%{filter:brightness(1);}
}

/* ===== TEXT ===== */
.text{
  font-size:18px;
  color:#333;
  line-height:1.7;
  min-height:100px;
}

/* ===== KHUSUS SLIDE 2 3 4 ===== */
.slide:not(#slide1) .text{
  position:relative;
  padding:20px;
  border:2px solid transparent;
  border-radius:16px;
  background:
    linear-gradient(#fff,#fff) padding-box,
    linear-gradient(135deg,#FFD93D,#C77DFF) border-box;
  font-family:'Georgia',serif;
}

.slide:not(#slide1) .text::before{
  content:"🌼";
  position:absolute;
  top:-12px;
  left:-12px;
  font-size:22px;
}

.slide:not(#slide1) .text::after{
  content:"🤍";
  position:absolute;
  bottom:-12px;
  right:-12px;
  font-size:20px;
}

/* ===== GLOW SAAT TYPING ===== */
.glow{
  text-shadow:
    0 0 6px rgba(255,217,61,0.9),
    0 0 14px rgba(199,125,255,0.8);
}

/* ===== GLOW MENGIKUTI MUSIK ===== */
.music-glow{
  animation:musicGlow 2.2s ease-in-out infinite;
}

@keyframes musicGlow{
  0%{
    text-shadow:
      0 0 6px rgba(255,217,61,0.6),
      0 0 12px rgba(199,125,255,0.5);
  }
  50%{
    text-shadow:
      0 0 10px rgba(255,217,61,0.9),
      0 0 18px rgba(199,125,255,0.8);
  }
  100%{
    text-shadow:
      0 0 6px rgba(255,217,61,0.6),
      0 0 12px rgba(199,125,255,0.5);
  }
}

/* ===== BUTTON ===== */
.btn{
  margin-top:25px;
  padding:12px 24px;
  border:none;
  border-radius:50px;
  font-size:24px;
  cursor:pointer;
  background:#FFD93D;
  box-shadow:0 5px 15px rgba(0,0,0,0.15);
}

/* ===== PASSWORD BOX ===== */
.password-box{
  background-color:#333;
  padding:20px;
  border-radius:10px;
  box-shadow:0 4px 12px rgba(255,255,255,0.3);
  width:300px;
  margin:20px auto 0;
  text-align:center;
}

.password-box input{
  padding:10px;
  border-radius:8px;
  border:2px solid #ddd;
  width:70%;
  margin-bottom:10px;
  font-size:1em;
}

@keyframes pulseGlow{
  0%{box-shadow:0 0 5px #4CAF50;}
  50%{box-shadow:0 0 20px #4CAF50;}
  100%{box-shadow:0 0 5px #4CAF50;}
}

.password-box button{
  background-color:#4CAF50;
  color:white;
  padding:10px 18px;
  border:none;
  border-radius:8px;
  font-size:1em;
  cursor:pointer;
  animation:pulseGlow 2s infinite;
}

.password-box button.success{
  animation:none;
  transform:scale(1.2);
}

/* ===== LOMPAT BUTTON ===== */
.jump{
  animation:jump 1.2s infinite;
}
@keyframes jump{
  0%,100%{transform:translateY(0);}
  50%{transform:translateY(-12px);}
}

/* ===== BACKGROUND EFFECT ===== */
.float{
  position:absolute;
  font-size:28px;
  animation:spread 3.5s ease-out forwards;
  pointer-events:none;
}

@keyframes spread{
  from{transform:scale(0.3);opacity:0;}
  to{transform:translate(var(--x),var(--y)) scale(1);opacity:1;}
}
</style>
</head>

<body>

<div class="wrapper">
<div class="nebula"></div>
<div class="stars"></div>
<audio id="bgMusic" loop>
  <source src="Memories (Instrumental).mp3" type="audio/mpeg">
</audio>

<div class="audio-control" onclick="toggleMusic()">Play Music</div>

<div class="slide active" id="slide1">
  <div class="content">
    <div class="photo-box"><img src="q1.jpeg"></div>
    <div class="text" data-text="Jadi kak ini dpe isi kurang lebih sama no dengan tahun lalu cm ada ta upgrade sdkt krn ada ta tmbh 1 tahun 🤣🤣🤣 dengan nda tahu ee apa queen da tls sbnrnya wkwkwk krn jujur queen lay nda tahu mo tls apa sbnrnya 😭😭😭 okeyy lanjuttt smga tu pass kak tahu wkwkwkw krn queen nda mo kase tahu 🤣🤣🤣🤣 smga tu isi di hlmn brktnya nda banya  fpe typo aminn 😭" ></div>
    <div class="password-box">
      <input type="password" id="password" placeholder="Masukkan password">
      <br>
      <button id="bukaBtn" onclick="checkPassword()">Buka</button>
    </div>
  </div>
</div>

<div class="slide" id="slide2">
  <div class="content">
    <div class="text" data-text="Pertana sbnrnya queen bersyukur karna kak boleh jd queen pe mtv jadi mi blng terimaksih pa Tuhan krn ada kak nia di kepengurusan ini 🤣🤣🤣🤣 bersyukur krn pas di pemerhati kak so jd queen pe mtv (ini sama lalu no kak wkwkwk) intinya bersyukur karna kak nia blh dampingi dipemerhati pdhl wktu itu queen kabal skli nda ba dngr, dengan bersyukur pa Tuhan krn kak blh jadi mtv di FAST krn kak blng nda mo jd mtv to wktu itu jadi sbnrnya bersyukur skli kak blh lanjut jadi mtv di fast nah intinya itu sbnrnya ini bagian dpe inti bersyukur ada kak nia di kepengurusan ini dengan bersyukur kak nia blh dampingi 👽
Bersyukur karna boleh dekat dengan kak boleh bljr banyak dari akak wkwk krn kak tahu to pertama kak jadiqueen pe MTV sbnrnya nda ada rencana mo dkt dengan kak wkwkwkw. lanjutttt ini bagian berikut ini yang beking queen tetwa dengan ragu mo kirim pa kak wkwk" ></div>
    <button class="btn jump" onclick="alienClick()">👽</button>
  </div>
</div>

<div class="slide" id="slide3">
  <div class="content">
    <div class="text" data-text="Sebenarnya dibagian ini dpe inti cuma mo bilang terimakasih kak 🤣🤣🤣 jadi mo bilang terimaksih karna kak so dampingi pa queen di tahun ini ee bln cm queen so dampingi nb eee tnggu bkn yg ini cm personal jadi nda ush nb tnggu beking baru 😭😭😭

Nah pertama itu terimaksih karn kak so ba iyo jd mtv di fast wkwkw 😭😭🤣 krn kalo kak nda ba iyo nda mo dampingi pa queen, terimaksih karna so dampingi 1 tahun ini, terimakasih karn so banya kak ada kase bljr pa queen, terimaksih karna setiap hari selalu dpa ceramah biasa 😭😭😭😭, terimaksih krn selalu revisi semua yg queen mo beking 😭😭😭🤣🤣 ee mksdnya kak terimaksih selalu jadi orng pertama yang queen mo tnya2 akng tentang surat tentang notulensi pokoknya tentang semua 😭 terimaksih karna selalu jadi orng pertama queen ja minta akng saran ja tnha pendapat dengan ja tnya pertanyaan yg sbnrnya so nda perlu mo tnya😭😭😭😭 

Satu tahun ini setiap hari ada kak mo kase bljr pa queen tnggu mo coba tls yang queen inga dulu (1) queen lupa kyp sampe kak blng ini kata2 cm itu kata2 so tertanam pa queen pe otak kak😭😭😭 jadi kak blng itu bgni iniisiatif memang butuh pengorbanan, terutama sikap hati bgtu kak blng mar lupa krn apa sampe blnh itu (2) nah ini kak blng pas apa na ihh aneh lupa trs queen krn queen blng banya proker di pemerhati sto nda jalan kong kak blng bgni kita nda bisa pelayanan itu jadi sempurna saat trng terbatas krn ketidaksempurnaan, tapi yang penting saat trng jalankan pelayanan trng tahu sapa yg trng kalo trng melayani Tuhan yang sempurna atau maha sempurna. 😭😭😭 kalontrng pe hati so betul² untuk Tuhan, semua pasti mo jalan sebagaimana harusnya atau mestinya kak ada blng😭😭😭 (3) ini yang kak blng orng2 yang pake alasan masih manusia itu cuma cari pembenaran nah ini sbbrnya 1 paket dngn yg kak ada blng yg dari kak irfan itu yg kalk ke adet ktb jngn pernah blng de kak ini masih manusia jad jangan iko pa kak ne bgtu sto😭😭😭 padahal harusnya fengan yrng ikut paulus pe kata2 trng blb lebih mi jaga, mo petbaiki denhan mo berusaha untuk nda buat hal2 yang nda baik krn itu perintah Tuhan for jadi sempurna. Jadi jnhn lake alasan masih manusia krn cm mo cari oembenaran😭 (4) nah ini waktu queen selalu tnya kyp di sek kong kak blng kalo semua ditutup dan diyakini kerna Tuhan pilib, itu so jawaban mutlak abis itu lanjut kak blng kadang oenjelasan dari mamudia itu bkn buat trng rendah hati mar tinggi hati, abis itu kak blng lagi kalo trng so dpt jwbn di awal kyp samoe ade di posisi itu ada 2 kemhngkinan trng mo jalankan oekayanan tulus krn Tuhan so pilih pa trng atau trng jalani pelayanan krn trng rasa blh tanpa Tuhan. Itu sbnrnya mantap skli kak😭😭😭 (5) oooo ini yang tentang memaklumi sto 😭😭 kak blng orng nda akn berubah kalau drng nda tahu apa frng pe kesalahan jadi trng itu harus kase tahu kalo drng slh, tegur dngn kasih karna lebih baik teguran yang nyata daripada kasih yang tersembunyi😭😭😭. Dengan ada lagi kak ada bilang apa ee merangkul bukan apa sto intinya soal memaklumi ini susah mo kase ilang kak vm kak prnh blng nnt drng nda berproses atau apa nah intinya bgtu cm susah mo kase ilang nda tahu bgm 😭😭😭😭 (6) oooo ini pas awal2 kak nia blng kalo trng berharap orng jd lebih baik trng yg harus kase cnth duluan disini lay kak ada blng tentang paulus😭😭😭 ikutilah teladan ku😭😭🤣🤣 jadi hngn bersembunyi di balik kata dek kalo kak nanti buat salah jang ikut ne 😭😭pdhl harudnya trng jadi teladan bgtuuu mantap skli luarbiasa 🤣 (7) nah ini kak kase inga pas apa ee yg kak ririn atau yg queen di sekre diam2 itu nah abis mon tag di grup 😭 kak blng mau secapek apapun, selelah apapun, semarah apapun, jangan samoe orng lain kena inbasnya oo nda ini kak blng krn kak ririn😭(8) nah ini kak kase inva pa queen jangan sering2 tnda, sering2 mengavaikan, sering2 bodo amta 😭😭😭 tembus dalam hati sampe jantung kak😭😭 (9) kak pe kata2 yang so tertanam 1 tahun ini yang lain blh dek gak boleh 😭😭 mar itu kata2 sbnrnya bgs skli beking tetap berthaan😭🤣🤣🤣 (10) nah ini kata2 baru skli td 😭😭 kak blng Jangan abaikan orang lagi dek.  Apalagi dek sudah dampingi pengurus sebagai MTV 🤣🤣🤣😭😭😭😭 

Nah jadi terimaksih kak karna semua yang kak blng2 itu queen blh ditegur dan disadarkan wkwkkw😭😭 iyo terimakasih krn kak selalu kase inga kalo harus rendah hati 😭😭😭 sama kak selalu blng proses untuk rendah hati de😭😭😭 jadi terimaksih kak untuk kata2 yg selalu menampar wkwkwkwkw terimakasih krn selalu marah2 😭😭😭 ooo dengan terimaksjh karna selalu bersedia kalk minta tolong buat renungan dadakan, terimaksih kak so selalu bantu pa queen 😭😭😭 (bantu ba revisi wkwkwkw, nda katu ee bercanda kak🤣🤣🤣) terimaksih karna selama 1 tahun ini kak selalu kase deadline for semua yang queen mo buat kak betul2 itu sangat membantu😭😭😭 oooo dengan sorry krn tu kalender kerja nda jd sampe akhir kak😭😭😭😭 terimaksih karna kak si bertahan dampingi pa queen wkwkw queen tahu no 1 tahun ini banya aneh2 queen ja beking ja tnya astaga 😭😭🤣🤣 ooo inj terimaksih kak ja ba teman kalo queen veking notulen (krn selalu kak yg queen mk tnya2 akng trs) terimakasih selalu ja bls chat tngh mlm kalo queen ja tnya2 akng😭😭😭 oiyo terimaksih selalu ja kase ingt jangan lupa makan wkwkwkw dengan minum air 😭🤣🤣🤣 oiyo biasa kalo queen so bingo mo buat apa duluan karna so banya mo buat sellau queen mo blng pa kak jadi terinmakasih for sikusi2 yg kak so kase 🤣😭 nah ini amper lupa terimaksih karn dari sempro sampe skripsi selalu sebelum mulai mo doa dengan kak krn itu doa mujarab sklj 😭🤣🤣🤣 terimaksih krn kak so srh hapus tu game spya fokus di studi dengab pelayanan kak blng bgtu ee wkwke, intinya kak terimakasih for 1 tahun ini wkwkwk so nda tahu queen mk tls apa😭😭😭😭 sbnrnya kak bkn cm sekedar jd pendamping mtv mar so sama queen pe kaka sendiri jadi terimaksih kak nia untuk 1 tahun ini ee nda 2 tahun ini so sabar menghadapi queen 🤣


Sebanrnya pas kak blng so nda mo lanjut jadi mtv rasa bgmn ee krn sbnrnya queen suka kak jadi mtv cm dari pas masih di pemerhati kan kak so blng to nda mo lanjut queen so terima dan pasrah wkwkw krn kak prnh blng to nda bersama di wadah pelayanan yang sama bukan berarti tidak bisa melayani sama-sama jadi wktu itu yah nda apa2 cm tahun ini wktu kak blng nfa mo hd mtv sbnrnya queen yakin kak mo ba iyo 😭😭🤣🤣krn kak nia bkn orng lain kan kak selalu se bljr nda afa alasn trng mo menolak pelayanan jadi bersyukur sbnrnya karna kak ba iyo jd koordi mtv 


Jadi terimaksih kak selalu jadi panutan dan teladan wkwkwkwk cm queen tetap tako kalo kak marah😭😭😭😭🤍"></div>
    <button class="btn jump" onclick="loveClick()">💛</button>
  </div>
</div>

<div class="slide" id="slide4">
  <div class="content">
    <div class="photo-box"><img src="q2.jpeg"></div>
    <div class="text" data-text="Ini sebenarnya harapan semoga kak boleh sempro di bulan januari aminn Tuhan, semoga kak blh wisuda tahun ini aminn, dengan apa lay na semoga kak nia nd marah2 amin😭😭🤣🤣🤣 cm nda apa2 no katu kalo kak mo marah apa lay kalo queen slh mar vm ba marah ne kak nda blh lain 😭😭😭😭 


Sudah kak jadi ini ucapan terimakasih pe isi cm sampe disini wmwkwk🤣🤣🤣🤣 nda tahu aoa semua yg queen tulis cm di jamin ini nda ada tyoi sama tahun lalu🤣😭😭😭 

dengan iyo kak pernah bilang to kalo kak khawattir queen mo jadi sama dengan kak kalo pa pengurus lain, karna queen sellau ba chat dengan kak, kak tako kalo queen mo contoh pa kak, nahhh masalahnya itu kak nia queen pe panutuan wkwk (geli da bilang ini 😭😭😭 mar kenyataan) jadi tetap biar skrng queen so jadi mtv sama de kak tetap kak itu queen pe panutan wkwkwkkw jadi semangat kakkkkk cm skrng queen so lebe tako karna so jadi mtv wwkwkkw, Tuhan Yeus berkati selalu 🌻🤍"></div>
  </div>
</div>

</div>

<script>
let music=document.getElementById("bgMusic");
let playing=true;
music.play();

function showSlide(n){
  document.querySelectorAll(".slide")
    .forEach(s => s.classList.remove("active"));

  const slide = document.getElementById("slide" + n);
  slide.classList.add("active");

  // BALIK KE ATAS
  window.scrollTo({
    top: 0,
    behavior: "smooth"
  });
}
function nextSlide(n){
  document.querySelectorAll(".slide").forEach(s=>s.classList.remove("active"));
  let slide=document.getElementById("slide"+n);
  slide.classList.add("active");
  startTyping(slide);

  // BALIK KE ATAS SAAT PINDAH SLIDE
  window.scrollTo({
    top: 0,
    behavior: "instant"
  });
}
function toggleMusic(){
  if(playing){
    music.pause();
    document.querySelector(".audio-control").innerHTML = "Play Music";
  }else{
    music.play();
    document.querySelector(".audio-control").innerHTML = "Pause Music";
  }
  playing = !playing;

  document.querySelectorAll(".text").forEach(t=>{
    t.classList.toggle("music-glow", playing);
  });
}


function spawn(icon,count){
  for(let i=0;i<count;i++){
    let e=document.createElement("div");
    e.className="float";
    e.innerText=icon;
    e.style.left="50%";
    e.style.top="50%";
    e.style.setProperty("--x",(Math.random()*600-300)+"px");
    e.style.setProperty("--y",(Math.random()*400-200)+"px");
    document.body.appendChild(e);
    setTimeout(()=>e.remove(),3500);
  }
}

function checkPassword(){
  let pass=document.getElementById("password").value;
  let btn=document.getElementById("bukaBtn");
  if(pass==="kak nia aneh"){
    btn.classList.add("success");
    spawn("🌼",16);
    setTimeout(()=>nextSlide(2),400);
  }else alert("Password salah 😆");
}

function alienClick(){spawn("🤍",22);nextSlide(3);}
function loveClick(){spawn("🌻",22);nextSlide(4);}

function nextSlide(n){
  document.querySelectorAll(".slide").forEach(s=>s.classList.remove("active"));
  let slide=document.getElementById("slide"+n);
  slide.classList.add("active");
  startTyping(slide);
}

function startTyping(slide){
  let t=slide.querySelector(".text");
  let txt=t.getAttribute("data-text");
  t.innerHTML="";
  t.classList.add("glow");

  let i=0;
  (function typing(){
    if(i<txt.length){
      t.innerHTML+=txt.charAt(i++);
      setTimeout(typing,35);
    }else{
      setTimeout(()=>t.classList.remove("glow"),400);
    }
  })();
}

startTyping(document.getElementById("slide1"));

document.addEventListener("click",e=>{
  for(let i=0;i<10;i++){
    let s=document.createElement("div");
    s.className="star-burst";
    s.innerText=Math.random()>0.5?"⭐":"✨";
    s.style.left=e.clientX+"px";
    s.style.top=e.clientY+"px";
    s.style.color=Math.random()>0.5?"#C77DFF":"#FFD93D";
    s.style.setProperty("--x",(Math.random()*200-100)+"px");
    s.style.setProperty("--y",(Math.random()*200-100)+"px");
    document.body.appendChild(s);
    setTimeout(()=>s.remove(),1200);
  }
});

setInterval(()=>{
  let s=document.createElement("div");
  s.className="shooting-star";
  s.style.top=Math.random()*200+"px";
  s.style.left=Math.random()*200+"px";
  document.body.appendChild(s);
  setTimeout(()=>s.remove(),1200);
},8000);

for(let i=0;i<3;i++){
  let c=document.createElement("div");
  c.className="cloud";
  c.style.top=(20+i*25)+"vh";
  c.style.animationDuration=(50+Math.random()*30)+"s";
  document.body.appendChild(c);
}
</script>

</body>
</html>
