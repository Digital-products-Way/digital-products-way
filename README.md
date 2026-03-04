<!DOCTYPE html><html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>KDP Spine Calculator</title><style>

body{
font-family: Arial, Helvetica, sans-serif;
background: linear-gradient(135deg,#0f172a,#1e3a8a);
margin:0;
padding:0;
display:flex;
justify-content:center;
align-items:center;
height:100vh;
color:white;
}

.container{
background:#ffffff;
color:#222;
padding:25px;
border-radius:12px;
width:320px;
box-shadow:0 8px 25px rgba(0,0,0,0.25);
}

h2{
text-align:center;
margin-bottom:20px;
color:#1e3a8a;
}

label{
font-size:14px;
font-weight:bold;
}

input,select{
width:100%;
padding:8px;
margin-top:4px;
margin-bottom:12px;
border-radius:6px;
border:1px solid #ccc;
font-size:14px;
}

button{
width:100%;
padding:10px;
border:none;
background:#f59e0b;
color:white;
font-size:16px;
border-radius:6px;
cursor:pointer;
}

button:hover{
background:#d97706;
}

.result{
margin-top:15px;
font-size:18px;
text-align:center;
font-weight:bold;
color:#1e3a8a;
}

</style></head><body><div class="container"><h2>KDP Master Pro</h2><label>Book Width (inch)</label>
<input type="number" id="width" value="6">

<label>Book Height (inch)</label>
<input type="number" id="height" value="9">

<label>Pages</label>
<input type="number" id="pages" value="100">

<label>Paper Type</label>
<select id="paper">

<option value="white">White Paper</option>
<option value="cream">Cream Paper</option>
</select><button onclick="calculate()">Calculate Spine</button>

<div class="result" id="result">
Spine: 0 inch
</div></div><script>

function calculate(){

let pages = document.getElementById("pages").value;
let paper = document.getElementById("paper").value;

let spine;

if(paper === "cream"){
spine = pages * 0.0025;
}
else{
spine = pages * 0.002252;
}

document.getElementById("result").innerHTML =
"Spine: " + spine.toFixed(3) + " inch";

}

</script></body>
</html>
