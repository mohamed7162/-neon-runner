<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Neon Runner - دكتور محمد</title>

<style>
body{
  margin:0;
  overflow:hidden;
  background:#050816;
  color:white;
  font-family:tahoma;
}

canvas{display:block}

#ui{
  position:fixed;
  top:10px;
  left:10px;
  right:10px;
  display:flex;
  justify-content:space-between;
  font-weight:bold;
}

#menu{
  position:fixed;
  inset:0;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  background:rgba(0,0,0,.7);
}

button{
  padding:12px 20px;
  font-size:18px;
  border:none;
  border-radius:10px;
  background:#ffd166;
  cursor:pointer;
}
</style>
</head>

<body>

<canvas id="game"></canvas>

<div id="ui">
  <div id="score">0</div>
  <div>© دكتور محمد</div>
  <div id="level">مرحلة 1</div>
</div>

<div id="menu">
  <h1>NEON RUNNER 🔥</h1>
  <p>اقفز وتجنب العوائق</p>
  <button onclick="start()">ابدأ</button>
</div>

<script>
let canvas=document.getElementById("game");
let ctx=canvas.getContext("2d");

let W,H,ground;

function resize(){
  W=canvas.width=innerWidth;
  H=canvas.height=innerHeight;
  ground=H*0.8;
}
resize();
window.onresize=resize;

let player,obs=[],score=0,speed=6,level=1,vy=0,jumpCount=0,run=false;

function reset(){
  player={x:100,y:ground-50,w:40,h:50};
  obs=[];
  score=0;
  speed=6;
  level=1;
  vy=0;
  jumpCount=0;
  spawn();
}

function spawn(){
  obs.push({x:W,y:ground-40,w:40,h:40});
}

function start(){
  document.getElementById("menu").style.display="none";
  reset();
  run=true;
  loop();
}

document.addEventListener("pointerdown",jump);
document.addEventListener("keydown",e=>{
  if(e.code==="Space") jump();
});

function jump(){
  if(!run) return;
  if(jumpCount<2){
    vy=-14;
    jumpCount++;
  }
}

function update(){
  score++;

  if(score%500===0){
    level++;
    speed+=1;
  }

  document.getElementById("score").innerText="النقاط: "+score;
  document.getElementById("level").innerText="مرحلة "+level;

  vy+=0.7;
  player.y+=vy;

  if(player.y+player.h>=ground){
    player.y=ground-player.h;
    vy=0;
    jumpCount=0;
  }

  obs.forEach(o=>o.x-=speed);

  if(obs.length && obs[0].x+obs[0].w<0) obs.shift();

  if(obs.length<3 && Math.random()<0.02) spawn();

  for(let o of obs){
    if(
      player.x<o.x+o.w &&
      player.x+player.w>o.x &&
      player.y<o.y+o.h &&
      player.y+player.h>o.y
    ){
      gameOver();
    }
  }
}

function draw(){
  ctx.clearRect(0,0,W,H);

  ctx.fillStyle="#1f2b58";
  ctx.fillRect(0,ground,W,H-ground);

  ctx.fillStyle="#38bdf8";
  ctx.fillRect(player.x,player.y,player.w,player.h);

  ctx.fillStyle="#ef4444";
  obs.forEach(o=>{
    ctx.fillRect(o.x,o.y,o.w,o.h);
  });
}

function loop(){
  if(!run) return;
  update();
  draw();
  requestAnimationFrame(loop);
}

function gameOver(){
  run=false;

  document.getElementById("menu").innerHTML=`
    <h1>خسرت 😅</h1>
    <p>نقاطك: ${score}</p>
    <p>© دكتور محمد</p>
    <button onclick="start()">إعادة</button>
  `;

  document.getElementById("menu").style.display="flex";
}
</script>

</body>
</html>
