<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>KDP Master Pro</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body{
  font-family:system-ui,sans-serif;
  background:#0f172a;
  color:#e5e7eb;
  display:flex;
  justify-content:center;
  align-items:center;
  min-height:100vh;
}
.card{
  background:#111827;
  padding:20px;
  border-radius:12px;
  width:320px;
}
input,button{
  width:100%;
  margin-top:10px;
  padding:10px;
  border-radius:6px;
  border:none;
}
button{
  background:#f59e0b;
  font-weight:600;
}
#results{display:none;margin-top:15px;}
</style>
</head>
<body>

<div class="card">
<h2>KDP Master Pro</h2>

<label>Width</label>
<input id="w" type="number" value="6">

<label>Height</label>
<input id="h" type="number" value="9">

<label>Pages</label>
<input id="p" type="number" placeholder="Total pages">

<button onclick="calculate()">Calculate Now</button>

<div id="results">
  <p>Spine: <span id="outS"></span> inch</p>
</div>
</div>

<script>
function calculate(){
  const pages = Number(document.getElementById("p").value);
  if(!pages){
    alert("Enter total pages");
    return;
  }
  const spine = (pages * 0.002252).toFixed(3);
  document.getElementById("outS").innerText = spine;
  document.getElementById("results").style.display="block";
}
</script>

</body>
</html>tml
