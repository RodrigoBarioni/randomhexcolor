<?php 
$i=0;
function random_color_part() {
	return str_pad( dechex( mt_rand( 0, 255 ) ), 2, '0', STR_PAD_LEFT);
}

function random_color() {
	return random_color_part() . random_color_part() . random_color_part();
}
$color = "#".random_color();
If($color == "#FFFFFF"){
	$color = "#".random_color();
}
?>
<script>
function copiarTexto() {
	var textoCopiado = document.getElementById("link");
	textoCopiado.select();
	document.execCommand("Copy");
	alert("Texto Copiado: " + textoCopiado.value);
}
</script>
<html>
<style>
@import url('https://fonts.googleapis.com/css2?family=Aleo:wght@300&display=swap');
</style>
<style>
body
{
	background-color:<?php echo $color;?>;
}
.centered {
	position: fixed;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
}
input{
	text-transform: ;
	width:auto;
	text-shadow: 1px 1px 2px #000000;
	background-color:transparent; 
	border-radius:0; 
	text-align: center; 
	font-size: 20px;
border:0;
	color:#ffffff;
	font-family:"Aleo";
	caret-color: transparent;
}
input:hover{
	width:auto;
	text-shadow: 1px 1px 2.5px #000000;
	cursor: pointer;
}
textarea:focus, input:focus, select:focus {
	box-shadow: 0 0 0 0;
	border: 0 none;
	outline: 0;
} 
</style>
<center>
<input class="centered" title="Clique para copiar o texto" id="link" name="link" onClick="copiarTexto();" value="<?php echo $color;?>">
</center>
</html>
