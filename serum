<!doctype html>
<html lang='fa'>
<head>
<meta charset='utf-8'>
<meta name='viewport' content='width=device-width,initial-scale=1'>
<title>Dextrose Convertor</title>
<style>
body{font-family:sans-serif;background:#f5faff;display:flex;justify-content:center;align-items:center;height:100vh;margin:0}
.card{background:white;padding:24px;border-radius:16px;box-shadow:0 4px 12px rgba(0,0,0,0.1);width:320px}
h2{text-align:center;color:#5a8fdc;margin-bottom:20px}
label{font-size:14px;margin-top:10px;display:block;color:#3a4a68}
input{width:100%;padding:10px;margin-top:4px;border:1px solid #c6d7f5;border-radius:8px;background:#f8fbff}
button{width:100%;padding:12px;margin-top:20px;background:#7ab6ff;border:none;border-radius:10px;color:white;font-size:16px;cursor:pointer;transition:0.3s}
button:hover{background:#5ea6ff}
.result{margin-top:20px;padding:12px;background:#eaf3ff;border-radius:10px;color:#35507a}
</style>
</head>
<body>
<div class="card">
<h2>Dextrose Convertor</h2>
<label>درصد محلول رقیق</label><input id="cDilute" type="number" step="0.1">
<label>درصد محلول غلیظ</label><input id="cConcentrated" type="number" step="0.1">
<label>درصد نهایی هدف</label><input id="cFinal" type="number" step="0.1">
<label>حجم نهایی (سی‌سی)</label><input id="vFinal" type="number" step="0.1">
<button onclick="calc()">محاسبه</button>
<div id="res" class="result" style="display:none"></div>
</div>
<script>
function calc(){
let C1=parseFloat(document.getElementById('cDilute').value);
let C2=parseFloat(document.getElementById('cConcentrated').value);
let Cf=parseFloat(document.getElementById('cFinal').value);
let Vf=parseFloat(document.getElementById('vFinal').value);

if(isNaN(C1) || isNaN(C2) || isNaN(Cf) || isNaN(Vf)){
alert('لطفا همه مقادیر را وارد کنید');
return;
}

if(Cf < Math.min(C1, C2) || Cf > Math.max(C1, C2)){
alert('درصد هدف باید بین درصدهای ورودی باشد');
return;
}

let V2=(Cf*Vf - C1*Vf)/(C2 - C1);
let V1=Vf - V2;

document.getElementById('res').style.display='block';
document.getElementById('res').innerHTML=
`حجم مورد نیاز از محلول رقیق: <b>${V1.toFixed(1)} cc</b><br>
حجم مورد نیاز از محلول غلیظ: <b>${V2.toFixed(1)} cc</b>`;
}
</script>
</body>
</html>
