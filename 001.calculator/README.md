<!DOCTYPE html>
<html>
<head>
	<title>MyCalculator</title>
	<style>
	input {background-color: white ; margin-left: 3px;}
	td {background-color: yellow }
	</style>
</head>
<body>
	<script>
		function GetNum(num){
			document.getElementById("result").value += num;
		}
		function GetRes(){
			obj = document.getElementById("result");
			obj.value = obj.value + "=" + eval(obj.value);
		}
		function Clear(){
			document.getElementById("result").value = null;
		}
		function Signal(){
				document.getElementById("result").value =-document.getElementById("result").value;
		}
		function Square(){
			document.getElementById("result").value *= document.getElementById("result").value;
		}
	</script>
	<table border = "4" cellpadding = "4" align = "center">
		<tr>
			<td colspan = "4"><input type = "text" id = "result"/></td>
		</tr>
		<tr>
			<td><input type = "button" onclick = "Clear()" value = "C">
			<td><input type = "button" onclick = "Signal()" value = "S">
			<td><input type = "button" onclick = "GetNum('%')" value = "%">
			<td><input type = "button" onclick = "GetNum('/')" value = "/">
		</tr>
		<tr>
			<td><input type = "button" onclick = "GetNum(7)" value = "7">
			<td><input type = "button" onclick = "GetNum(8)" value = "8">
			<td><input type = "button" onclick = "GetNum(9)" value = "9">
			<td><input type = "button" onclick = "GetNum('*')" value = "*">
		</tr>
		<tr>
			<td><input type = "button" onclick = "GetNum(4)" value = "4">
			<td><input type = "button" onclick = "GetNum(5)" value = "5">
			<td><input type = "button" onclick = "GetNum(6)" value = "6">
			<td><input type = "button" onclick = "GetNum('+')" value = "+">
		</tr>
		<tr>
			<td><input type = "button" onclick = "GetNum(1)" value="1">
			<td><input type = "button" onclick = "GetNum(2)" value="2">
			<td><input type = "button" onclick = "GetNum(3)" value="3">
			<td><input type = "button" onclick = "GetNum('-')" value="-">
		</tr>
		<tr>
			<td><input type = "button" onclick = "GetNum(0)" value = "0">
			<td><input type = "button" onclick = "GetNum('.')" value = ".">
			<td><input type = "button" onclick = "Square()" value  = "^">
			<td><input type = "button" onclick = "GetRes()" value = "=">
		</tr>

	</table>
</body>
</html>
