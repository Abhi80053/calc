<!DOCTYPE html>
<html>
<head>
	<title>Calculator</title>
	<style type="text/css">
		body {
			background-color: #626262;
		}
		.main {
			margin-top: 100px;
		}
		.cal input {
			padding: 20px;
			font-size: 24px;
			font-weight: bold;
			margin: 10px;
			border-radius: 5px;
			border-color: aqua;
		}
		#result {
			padding: 20px;
			margin: 10px;
			width: 250px;
			border-color: aqua;
			font-size: 24px;
			font-weight: bold;
		}
	</style>
</head>
<body>
	<center class="main">
		<input type="text" readonly id="result" placeholder="0">
		<div class="cal">
			<input type="button" value="1" onclick="addToDisplay('1')">
			<input type="button" value="2" onclick="addToDisplay('2')">
			<input type="button" value="3" onclick="addToDisplay('3')">
			<input type="button" value="/" onclick="addToDisplay('/')">
			<br>
			<input type="button" value="4" onclick="addToDisplay('4')">
			<input type="button" value="5" onclick="addToDisplay('5')">
			<input type="button" value="6" onclick="addToDisplay('6')">
			<input type="button" value="*" onclick="addToDisplay('*')">
			<br>
			<input type="button" value="7" onclick="addToDisplay('7')">
			<input type="button" value="8" onclick="addToDisplay('8')">
			<input type="button" value="9" onclick="addToDisplay('9')">
			<input type="button" value="-" onclick="addToDisplay('-')">
			<br>
			<input type="button" value="0" onclick="addToDisplay('0')">
			<input type="button" value="c" onclick="clearDisplay()">
			<input type="button" value="=" onclick="calculateResult()">
			<input type="button" value="+" onclick="addToDisplay('+')">
		</div>
	</center>
	<script type="text/javascript">
		function clearDisplay() {
			document.getElementById('result').value = '';
		}

		function addToDisplay(value) {
			document.getElementById('result').value += value;
		}

		function calculateResult() {
			try {
				let result = eval(document.getElementById('result').value);
				document.getElementById('result').value = result;
			} catch (e) {
				document.getElementById('result').value = 'Error';
			}
		}
	</script>
</body>
</html>
