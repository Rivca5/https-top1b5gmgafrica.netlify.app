<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>TOP1B5 MAGIQUE VOL5</title>
<style>
body{margin:0;font-family:Arial;background:#000;color:#fff;text-align:center}
.screen{display:none;padding:20px;min-height:100vh}
.active{display:block}
.btn{padding:15px 25px;margin:10px;border:none;border-radius:10px;font-weight:bold;font-size:18px;width:90%}
.btn-jeune{background:#FFD700;color:#000}
.btn-central{background:#C00000;color:#fff}
.card{background:#111;border:1px solid #FFD700;border-radius:12px;padding:15px;margin:10px}
input{padding:12px;width:80%;border-radius:8px;margin:10px}
</style>
</head>
<body>
<div id="accueil" class="screen active">
<h1 style="color:#FFD700">TOP1B5 🇧🇫</h1>
<h3>BASE CENTRALE MAGIQUE VOL5</h3>
<button class="btn btn-jeune" onclick="show('jeunesse')">JE SUIS JEUNESSE</button>
<button class="btn btn-central" onclick="show('login')">GROUPEMENT CENTRALE - PDG</button>
<p style="font-size:12px;margin-top:30px">RIVCA SARL - Faso Dan Fani<br>BCLCC 25 39 58 41</p>
</div>
<div id="jeunesse" class="screen">
<h2 style="color:#FFD700">ESPACE JEUNESSE - PART</h2>
<div class="card">Catalogue 9 Tenues Faso Dan Fani</div>
<div class="card">Commander</div>
<div class="card">Contact 51 41 40 99</div>
<button class="btn btn-jeune" onclick="show('accueil')">Retour</button>
</div>
<div id="login" class="screen">
<h2 style="color:#C00000">GROUPEMENT CENTRALE</h2>
<input type="password" id="pin" placeholder="Code PIN PDG">
<button class="btn btn-central" onclick="checkPin()">ENTRER</button>
<p id="error" style="color:red"></p>
<button class="btn" onclick="show('accueil')" style="background:#333;color:#fff">Retour</button>
</div>
<div id="centrale" class="screen">
<h2 style="color:#C00000">BASE CENTRALE - PDG</h2>
<div class="card">Montre Tournante Detecteur Danger</div>
<div class="card">Transmission AES BCLCC</div>
<div class="card">Gestion Commandes</div>
<div class="card">DSI-2026-RIVCA-22651414099</div>
<button class="btn btn-central" onclick="show('accueil')">Deconnexion</button>
</div>
<script>
function show(id){document.querySelectorAll('.screen').forEach(s=>s.classList.remove('active'));document.getElementById(id).classList.add('active');}
function checkPin(){let c=document.getElementById('pin').value;if(c==='51414099'||c==='22651414099'){show('centrale');document.getElementById('pin').value='';document.getElementById('error').innerText='';}else{document.getElementById('error').innerText='Code incorrect - Acces refuse';}}
</script>
</body>
</html>
