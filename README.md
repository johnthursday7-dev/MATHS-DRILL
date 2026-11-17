# MATHS-DRILL
"Boost math skills with fun drills and exercises!"
<!DOCTYPE html>
<html>
<head>
<title>MATHS Drills - Founded by Mr John Thursday</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
  *{box-sizing:border-box}
  body{font-family:Inter, Arial, sans-serif; margin:0; background:#0a0f1e; color:#e2e8f0; padding:20px;}
  .wrap{max-width:720px; margin:auto;}
  .header{text-align:center; padding:20px 0;}
  .header h1{font-size:34px; letter-spacing:2px; margin:0;}
  .header h1 span{color:#38bdf8}
  .header p{color:#94a3b8; margin:5px 0;}
  .founder{color:#facc15; font-weight:600; font-size:13px; text-transform:uppercase; letter-spacing:1px;}
  .card{background:#111827; border:1px solid #1f2937; border-radius:14px; padding:24px; margin:16px 0;}
  .card h2{margin-top:0; font-size:22px;}
  .card p, .card li{line-height:1.7; color:#cbd5e1; font-size:15px;}
  input{width:100%; padding:13px; background:#0f172a; border:1px solid #334155; color:white; border-radius:10px; font-size:16px; margin:8px 0;}
  button{width:100%; padding:13px; border:none; border-radius:10px; font-size:15px; font-weight:700; cursor:pointer; margin-top:8px;}
  .primary{background:#38bdf8; color:#0f172a;}
  .secondary{background:#1e293b; color:white; border:1px solid #334155;}
  .ghost{background:transparent; color:#38bdf8; border:1px solid #38bdf8;}
  .grid{display:grid; grid-template-columns:1fr 1fr; gap:12px;}
  .topic{background:#1e293b; border:1px solid #334155; padding:16px; border-radius:12px; cursor:pointer; text-align:left;}
  .topic:hover{border-color:#38bdf8}
  .topic.locked{opacity:.45; cursor:not-allowed;}
  .topic b{font-size:16px; color:white;}
  .topic span{display:block; font-size:13px; color:#94a3b8; margin-top:4px;}
  .hidden{display:none}
  .learn{background:#0f172a; border-left:4px solid #38bdf8; padding:16px; border-radius:8px; text-align:left; line-height:1.7; font-size:15px; color:#e2e8f0;}
  .learn h3{color:#38bdf8; margin:12px 0 6px;}
  #question{font-size:24px; font-weight:700; background:#0f172a; padding:18px; border-radius:10px; margin:14px 0; white-space:pre-line; line-height:1.6;}
  #result{font-weight:700; min-height:22px; margin:10px 0;}
  .meta{display:flex; justify-content:space-between; font-size:13px; color:#94a3b8;}
  .bar{height:8px; background:#1e293b; border-radius:20px; overflow:hidden; margin:10px 0;}
  .bar div{height:100%; background:#38bdf8; width:0%;}
  .footer{text-align:center; font-size:12px; color:#64748b; margin-top:20px;}
  .plans{display:grid; grid-template-columns:1fr 1fr; gap:14px; margin-top:15px;}
  .plan{background:#0f172a; border:2px solid #334155; border-radius:14px; padding:18px; text-align:left; position:relative;}
  .plan.popular{border-color:#facc15; background:#1a1705;}
  .plan.vip{border-color:#38bdf8; background:#0a1a2e;}
  .plan h3{margin:0; font-size:18px;}
  .plan .price{font-size:26px; font-weight:800; margin:8px 0; color:white;}
  .plan .price small{font-size:13px; color:#94a3b8; font-weight:400;}
  .plan ul{padding-left:18px; margin:10px 0;}
  .plan ul li{font-size:13.5px; margin:5px 0;}
  .tag{position:absolute; top:-10px; right:12px; background:#facc15; color:#000; font-size:11px; font-weight:800; padding:4px 8px; border-radius:20px;}
  .tag-blue{background:#38bdf8;}
  .contact-box{background:#0f172a; border:1px solid #38bdf8; padding:14px; border-radius:10px; margin-top:15px; text-align:center;}
  .contact-box a{color:#38bdf8; font-weight:800; text-decoration:none; font-size:18px;}
  .lock-msg{background:#7f1d1d; border:1px solid #ef4444; padding:16px; border-radius:12px; text-align:center; margin-top:15px;}
  @media(max-width:560px){.grid,.plans{grid-template-columns:1fr}}
</style>
</head>
<body>
<div class="wrap">
<div class="header">
  <h1>MATHS <span>DRILLS</span></h1>
  <p class="founder">Founded by Mr John Thursday</p>
  <p>Advanced Practice Platform</p>
</div>

<!-- TIER SELECTION - SAME DESIGN AS BEFORE -->
<div id="pricingScreen" class="card">
  <h2>Choose Your Learning Plan</h2>
  <p>Select a tier. You will be asked for that tier's password. Don't have password? Contact <b>+234 814 153 8038</b>.</p>
  <div class="plans">
    <div class="plan">
      <h3>Starters Platform</h3>
      <div class="price">₦5,000 <small>/ Unlimited</small></div>
      <ul><li>Addition & Subtraction</li><li>Multiplication & Division</li><li>Basic theory</li><li>Score tracking</li></ul>
      <button class="secondary" onclick="chooseTier('starters')">Choose Starters</button>
    </div>
    <div class="plan">
      <h3>Go Go Platform</h3>
      <div class="price">₦10,000 <small>/ 2 Months + 1 Week Extra Trial</small></div>
      <ul><li>Everything in Starters</li><li>Fractions & Decimals</li><li>Percentages & Ratio</li><li>Unlimited practice</li></ul>
      <button class="primary" onclick="chooseTier('gogo')">Choose Go Go</button>
    </div>
    <div class="plan popular">
      <div class="tag">MOST POPULAR</div>
      <h3>Premium Learning Platform</h3>
      <div class="price">₦20,000 <small>/ 3 Months + 2 Weeks</small></div>
      <ul><li>Everything in Go Go</li><li>Algebra</li><li>Geometry</li><li>Indices & Surds</li><li>Hard / Exam-level questions</li></ul>
      <button class="primary" onclick="chooseTier('premium')">Choose Premium</button>
    </div>
    <div class="plan vip">
      <div class="tag tag-blue">BEST VALUE</div>
      <h3>VIP Learning Platform</h3>
      <div class="price">₦35,000 <small>/ Includes Live Lessons</small></div>
      <ul><li>Everything in Premium</li><li>Matrices - Full Course</li><li><b>LIVE:</b> Saturdays 4:00PM - 4:45PM with Top Class Maths Teacher</li><li>Certificate</li></ul>
      <button class="primary" onclick="chooseTier('vip')">Choose VIP</button>
    </div>
  </div>
  <div class="contact-box">To Pay & Get Password, WhatsApp: <a href="https://wa.me/2348141538038">+234 814 153 8038</a></div>
</div>

<!-- PASSWORD FOR SELECTED TIER -->
<div id="loginScreen" class="card hidden">
  <button class="ghost" style="width:auto; padding:8px 14px;" onclick="backToTiers()">Back to Plans</button>
  <h2 id="loginTitle">Enter Password</h2>
  <p id="loginDesc">Enter password for this plan.</p>
  <input type="password" id="passInput" placeholder="Enter Tier Password">
  <button class="primary" onclick="unlock()">Unlock My Plan</button>
  <p id="passError" style="color:#f87171; font-weight:700;"></p>
  <div id="lockMsg" class="lock-msg hidden">
    <h3 style="margin:0;">Access Locked</h3>
    <p>Please contact the number to access our website.</p>
    <p style="font-size:22px; font-weight:800; color:white; margin:5px 0;">+234 814 153 8038</p>
    <a href="https://wa.me/2348141538038" style="display:block; background:#25D366; color:white; padding:12px; border-radius:10px; text-decoration:none; font-weight:800;">Chat on WhatsApp Now</a>
  </div>
  <div class="contact-box">Don't have password? WhatsApp: <a href="https://wa.me/2348141538038">+234 814 153 8038</a></div>
</div>

<!-- HOME / TOPICS -->
<div id="homeScreen" class="card hidden">
  <div class="meta"><span>Welcome, Learner</span><span>Plan: <b id="currentPlan" style="color:#facc15">Starters</b></span></div>
  <div class="meta" style="margin-top:6px;"><span>Total Score: <b id="totalScore" style="color:white">0</b></span><span style="cursor:pointer; color:#38bdf8;" onclick="backToTiers()">Change Plan</span></div>
  <h2>Select a Topic</h2>
  <p id="planNote"></p>
  <div class="grid">
    <div class="topic" id="t-addition" onclick="openTopic('addition')"><b>Addition & Subtraction</b><span>Large numbers, borrowing, multi-step</span></div>
    <div class="topic" id="t-multiplication" onclick="openTopic('multiplication')"><b>Multiplication & Division</b><span>3-digit, long division, remainders</span></div>
    <div class="topic" id="t-fractions" onclick="openTopic('fractions')"><b>Fractions & Decimals</b><span>Simplify, mixed numbers, operations</span></div>
    <div class="topic" id="t-percent" onclick="openTopic('percent')"><b>Percentages & Ratio</b><span>Increase, decrease, profit, proportion</span></div>
    <div class="topic" id="t-algebra" onclick="openTopic('algebra')"><b>Algebra</b><span>Equations, expansion, factorisation</span></div>
    <div class="topic" id="t-geometry" onclick="openTopic('geometry')"><b>Geometry</b><span>Area, perimeter, angles, Pythagoras</span></div>
    <div class="topic" id="t-indices" onclick="openTopic('indices')"><b>Indices & Surds</b><span>Powers, roots, laws of indices</span></div>
    <div class="topic" id="t-matrix" onclick="openTopic('matrix')"><b>Matrices</b><span>Full course - determinant, inverse, transpose</span></div>
  </div>
  <div class="contact-box">Questions? WhatsApp: <a href="https://wa.me/2348141538038">+234 814 153 8038</a></div>
  <button class="secondary" onclick="backToTiers()">Lock Platform</button>
</div>

<!-- TOPIC -->
<div id="topicScreen" class="card hidden">
  <button class="ghost" style="width:auto; padding:8px 14px;" onclick="goHome()">Back to Topics</button>
  <h2 id="topicTitle"></h2>
  <div class="learn" id="learnText"></div>
  <div class="bar"><div id="progressBar"></div></div>
  <div class="meta"><span>Question <span id="qNum">1</span> of 10</span><span>Topic Score: <b id="topicScore" style="color:white">0</b> | Streak: <b id="streak" style="color:white">0</b></span></div>
  <div id="question">?</div>
  <input type="text" id="answer" placeholder="Enter your answer (e.g. 12 or -3)" onkeydown="if(event.key==='Enter') checkAnswer()">
  <button class="primary" onclick="checkAnswer()">Submit Answer</button>
  <button class="secondary" onclick="nextQuestion()">Next Question</button>
  <div id="result"></div>
  <p style="font-size:13px; color:#94a3b8;">For matrices, enter answers as numbers separated by comma. Example: 5,7,9,11</p>
</div>

<div class="footer">MATHS DRILLS | Founded by Mr John Thursday | Contact: +234 814 153 8038 | All Rights Reserved</div>
</div>

<script>
const TIER_PASSWORDS = {
  starters: { pass:"STARTER5000", name:"Starters Platform" },
  gogo: { pass:"GOGO10000", name:"Go Go Platform" },
  premium: { pass:"PREMIUM20000", name:"Premium Learning Platform" },
  vip: { pass:"VIP35000", name:"VIP Learning Platform" }
};
const MASTER_PASS = "THURSDAY67";
let selectedTier = "";
let totalScore=0, topicScore=0, streak=0, qCount=0, currentTopic="", correct="", currentQ="", currentPlan="starters", currentPlanName="Starters Platform";
const planAccess={ starters:['addition','multiplication'], gogo:['addition','multiplication','fractions','percent'], premium:['addition','multiplication','fractions','percent','algebra','geometry','indices'], vip:['addition','multiplication','fractions','percent','algebra','geometry','indices','matrix'] };
const topics={
addition:{title:"Addition & Subtraction - Advanced", learn:`<h3>1. Core Concept</h3>Addition combines values. Subtraction finds the difference.<br><h3>2. Rules</h3><ul><li>Adding a negative = subtracting: 8 + (-3) = 5</li><li>Subtracting a negative = adding: 10 - (-4) = 14</li></ul><h3>3. Worked Example</h3>457 + 289 - 134 = 612`},
multiplication:{title:"Multiplication & Division", learn:`<h3>1. Core Concept</h3>Multiplication is repeated addition. Division is the inverse.<br><h3>2. Key Rules</h3><ul><li>Negative x Positive = Negative</li><li>Negative x Negative = Positive</li><li>Remainder: 47 / 5 = 9 remainder 2</li></ul><h3>3. Worked Example</h3>234 x 6 = 1404`},
fractions:{title:"Fractions & Decimals", learn:`<h3>1. Core Concept</h3>A fraction is a/b.<br><h3>2. Rules</h3><ul><li>Simplify: 12/18 = 2/3</li><li>Add: 1/2 + 1/3 = 5/6</li><li>Multiply: 2/3 x 3/4 = 1/2</li></ul>`},
percent:{title:"Percentages & Ratio", learn:`<h3>1. Core Concept</h3>Percent means per 100.<br><h3>2. Formulas</h3><ul><li>Percentage = (Part / Whole) x 100</li><li>Increase: New = Old x (1 + %/100)</li></ul>`},
algebra:{title:"Algebra", learn:`<h3>1. Core Concept</h3>Algebra uses letters for unknowns.<br><h3>2. Rules</h3><ul><li>3x + 5x = 8x</li><li>Expansion: 3(x+4) = 3x + 12</li><li>Solve: 2x + 6 = 16 -> x = 5</li></ul>`},
geometry:{title:"Geometry", learn:`<h3>1. Formulas</h3><ul><li>Triangle Area = 1/2 x base x height</li><li>Rectangle Area = length x width</li><li>Pythagoras: a^2 + b^2 = c^2</li></ul>`},
indices:{title:"Indices & Surds", learn:`<h3>1. Laws</h3><ul><li>a^m x a^n = a^(m+n)</li><li>a^0 = 1</li></ul><h3>2. Example</h3>2^4 x 2^3 = 128`},
matrix:{title:"Matrices - Complete Guide", learn:`<h3>1. What is a Matrix?</h3>A matrix is a rectangular array of numbers.<br><h3>2. Types</h3><ul><li>Row, Column, Square, Zero, Identity [1 0 / 0 1], Diagonal, Symmetric</li></ul><h3>3. Addition</h3>Add matching positions.<br><h3>4. Scalar</h3>Multiply EVERY element.<br><h3>5. Multiplication</h3>Row x Column.<br><h3>6. Transpose</h3>Swap rows and columns.<br><h3>7. Determinant (2x2)</h3>det = ad - bc. Example: [4 3 / 2 1] det = -2<br><h3>8. Determinant (3x3)</h3>Expansion: a(EI-FH) - b(DI-FG) + c(DH-EG)<br><h3>9. Inverse (2x2)</h3>Inverse = 1/det x [d -b / -c a]. If det = 0, NO inverse.`}
};
function chooseTier(tier){
  selectedTier = tier;
  document.getElementById("pricingScreen").classList.add("hidden");
  document.getElementById("loginScreen").classList.remove("hidden");
  document.getElementById("loginTitle").innerText = "Enter Password for " + TIER_PASSWORDS[tier].name;
  document.getElementById("loginDesc").innerText = "You selected " + TIER_PASSWORDS[tier].name + ". Enter its password to unlock. If you don't have it, contact +234 814 153 8038.";
  document.getElementById("passInput").value = "";
  document.getElementById("passError").innerText = "";
  document.getElementById("lockMsg").classList.add("hidden");
}
function backToTiers(){
  document.getElementById("loginScreen").classList.add("hidden");
  document.getElementById("homeScreen").classList.add("hidden");
  document.getElementById("topicScreen").classList.add("hidden");
  document.getElementById("pricingScreen").classList.remove("hidden");
}
function unlock(){
  let p = document.getElementById("passInput").value.trim().toUpperCase();
  // Master password unlocks any tier you clicked
  if(p === MASTER_PASS || p === TIER_PASSWORDS[selectedTier].pass){
    currentPlan = selectedTier;
    currentPlanName = TIER_PASSWORDS[selectedTier].name;
    document.getElementById("currentPlan").innerText = currentPlanName;
    document.getElementById("loginScreen").classList.add("hidden");
    document.getElementById("homeScreen").classList.remove("hidden");
    let all=['addition','multiplication','fractions','percent','algebra','geometry','indices','matrix'];
    all.forEach(t=>{ let el=document.getElementById("t-"+t); if(planAccess[currentPlan].includes(t)) el.classList.remove("locked"); else el.classList.add("locked"); });
    document.getElementById("planNote").innerText = "You are on " + currentPlanName + ". Locked topics need an upgrade. Contact +234 814 153 8038.";
  } else {
    document.getElementById("passError").innerText = "Wrong password.";
    document.getElementById("lockMsg").classList.remove("hidden");
    alert("Please contact the number to access our website: +234 814 153 8038");
  }
}
function goHome(){ document.getElementById("topicScreen").classList.add("hidden"); document.getElementById("homeScreen").classList.remove("hidden"); }
function openTopic(k){
  if(!planAccess[currentPlan].includes(k)){ alert("Please contact the number to access our website: +234 814 153 8038. This topic is locked on " + currentPlanName + "."); return; }
  currentTopic=k; topicScore=0; streak=0; qCount=0; document.getElementById("homeScreen").classList.add("hidden"); document.getElementById("topicScreen").classList.remove("hidden"); document.getElementById("topicTitle").innerText=topics[k].title; document.getElementById("learnText").innerHTML=topics[k].learn; updateUI(); nextQuestion();
}
function updateUI(){ document.getElementById("totalScore").innerText=totalScore; document.getElementById("topicScore").innerText=topicScore; document.getElementById("streak").innerText=streak; document.getElementById("qNum").innerText=Math.min(qCount+1,10); document.getElementById("progressBar").style.width=(qCount/10*100)+"%"; }
function rnd(a,b){return Math.floor(Math.random()*(b-a+1))+a}
function nextQuestion(){
  qCount++;
  if(qCount>10){ alert("Topic Complete. Score: "+topicScore+" / 100"); qCount=0; topicScore=0; streak=0; }
  let a,b,c,d;
  if(currentTopic==="addition"){ let type=rnd(1,3); if(type===1){a=rnd(250,980); b=rnd(250,980); correct=String(a+b); currentQ="Solve:\n"+a+" + "+b+" = ?";} if(type===2){a=rnd(400,999); b=rnd(120,a-10); correct=String(a-b); currentQ="Solve:\n"+a+" - "+b+" = ?";} if(type===3){a=rnd(-80,80); b=rnd(-80,80); c=rnd(-50,50); correct=String(a+b-c); currentQ="Solve (watch signs):\n"+a+" + ("+b+") - ("+c+") = ?";} }
  if(currentTopic==="multiplication"){ let type=rnd(1,3); if(type===1){a=rnd(123,489); b=rnd(12,19); correct=String(a*b); currentQ="Solve:\n"+a+" x "+b+" = ?";} if(type===2){b=rnd(7,16); c=rnd(12,48); a=b*c+rnd(1,b-1); correct=String(Math.floor(a/b)); currentQ="Find quotient (ignore remainder):\n"+a+" / "+b+" = ?";} if(type===3){a=rnd(12,28); b=rnd(12,28); correct=String(a*b); currentQ="Solve:\n"+a+" x "+b+" = ?";} }
  if(currentTopic==="fractions"){ let type=rnd(1,3); if(type===1){let den=rnd(4,12); let num=rnd(2,den-1); correct=String(num*2)+"/"+String(den*2); currentQ="Find equivalent:\nWhat is "+num+"/"+den+" x 2/2 ?\nEnter as num/den e.g. 4/8";} if(type===2){a=rnd(2,9); b=rnd(2,9); correct=String(a*b); currentQ="Multiply:\n"+a+"/3 x 3/"+b+" = ?";} if(type===3){a=rnd(20,120); b=[2,4,5,10][rnd(0,3)]; correct=String(a/b); currentQ="Find:\n1/"+b+" of "+a+" = ?";} }
  if(currentTopic==="percent"){ let type=rnd(1,3); if(type===1){let p=[15,20,25,30,40][rnd(0,4)]; let n=[400,600,800,1200][rnd(0,3)]; correct=String(n*p/100); currentQ=p+"% of "+n+" = ?";} if(type===2){let oldP=rnd(200,800); let inc=[10,20,25][rnd(0,2)]; correct=String(oldP*(100+inc)/100); currentQ="A price of "+oldP+" increases by "+inc+"%. New price = ?";} if(type===3){let part=rnd(20,90); correct=String(part); currentQ="What percentage is "+part+" out of 100? Enter just number.";} }
  if(currentTopic==="algebra"){ let type=rnd(1,3); if(type===1){let x=rnd(5,28); let m=rnd(3,7); let c1=rnd(4,15); correct=String(x); currentQ="Solve for x:\n"+m+"x + "+c1+" = "+(m*x+c1);} if(type===2){let x=rnd(4,20); correct=String(3*x+12); currentQ="If x = "+x+", find value of:\n3x + 12 = ?";} if(type===3){let x=rnd(6,18); correct=String(2*x); currentQ="Expand and evaluate if x="+x+":\n2(x + 5) - 10 = ?";} }
  if(currentTopic==="geometry"){ let type=rnd(1,3); if(type===1){let l=rnd(12,28); let w=rnd(8,19); correct=String(l*w); currentQ="Area of rectangle:\nLength = "+l+", Width = "+w;} if(type===2){let a1=rnd(3,12); let b1=rnd(3,12); correct=String(Math.sqrt(a1*a1+b1*b1)); currentQ="Right triangle, sides "+a1+" and "+b1+". Find hypotenuse (Pythagoras).";} if(type===3){let r=rnd(7,14); correct=String(2*r); currentQ="Diameter of circle with radius "+r+" = ?";} }
  if(currentTopic==="indices"){ let type=rnd(1,3); if(type===1){let base=rnd(2,5); let e1=rnd(2,4); let e2=rnd(2,4); correct=String(Math.pow(base,e1+e2)); currentQ="Simplify:\n"+base+"^"+e1+" x "+base+"^"+e2+" = ?";} if(type===2){let v=rnd(4,9); correct=String(v*v); currentQ="Evaluate:\n("+v+")^2 = ?";} if(type===3){correct="1"; currentQ="Evaluate:\nAny number to power 0 = ?";} }
  if(currentTopic==="matrix"){
    let type=rnd(1,5);
    if(type===1){ a=rnd(2,9); b=rnd(2,9); c=rnd(2,9); d=rnd(2,9); correct=String(a*d-b*c); currentQ="MATRIX - Determinant\nFind det of:\n[ "+a+"  "+b+" ]\n[ "+c+"  "+d+" ]\ndet = ad - bc = ?"; }
    if(type===2){ a=rnd(1,9); b=rnd(1,9); c=rnd(1,9); d=rnd(1,9); let e=rnd(1,9); let f=rnd(1,9); let g=rnd(1,9); let h=rnd(1,9); correct=(a+e)+","+(b+f)+","+(c+g)+","+(d+h); currentQ="MATRIX - Addition\nAdd:\n[ "+a+" "+b+" ] + [ "+e+" "+f+" ]\n[ "+c+" "+d+" ]   [ "+g+" "+h+" ]\nEnter as: 5,7,9,11"; }
    if(type===3){ a=rnd(2,6); b=rnd(2,6); c=rnd(2,6); d=rnd(2,6); correct=String(a*d-b*c); currentQ="MATRIX - Determinant Check\nFind det of:\n[ "+a+" "+b+" ]\n[ "+c+" "+d+" ]"; }
    if(type===4){ a=rnd(2,5); b=rnd(2,5); c=rnd(2,5); d=rnd(2,5); let k=rnd(2,4); correct=(a*k)+","+(b*k)+","+(c*k)+","+(d*k); currentQ="MATRIX - Scalar Multiplication\nFind "+k+" x\n[ "+a+" "+b+" ]\n[ "+c+" "+d+" ]\nEnter as: a,b,c,d"; }
    if(type===5){ a=rnd(1,5); b=rnd(1,5); c=rnd(1,5); d=rnd(1,5); correct=String(a*d-b*c); currentQ="MATRIX - Transpose + Determinant\n[ "+a+" "+b+" ]\n[ "+c+" "+d+" ]\ndet = ?"; }
  }
  document.getElementById("question").innerText=currentQ;
  document.getElementById("answer").value="";
  document.getElementById("result").innerText="";
  updateUI();
  document.getElementById("answer").focus();
}
function checkAnswer(){
  let user=document.getElementById("answer").value.trim().toLowerCase().replace(/\s/g,"");
  let r=document.getElementById("result");
  if(!user){r.innerText="Enter an answer first."; r.style.color="#facc15"; return;}
  let corr=String(correct).toLowerCase().replace(/\s/g,"");
  if(user===corr){ topicScore+=10; totalScore+=10; streak++; r.innerText="Correct. +10 points"; r.style.color="#4ade80"; }
  else { streak=0; r.innerText="Incorrect. Correct answer: "+correct; r.style.color="#f87171"; }
  updateUI();
  setTimeout(nextQuestion,1600);
}
</script>
</body>
</html>
