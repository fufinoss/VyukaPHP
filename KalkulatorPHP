<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kalkulačka</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
        }
 
        input, select, button {
            margin: 10px;
            padding: 8px;
            font-size: 16px;
        }
        h3{
            color: green
        }
        
    </style>
</head>
<body>
 
<?php
$result = '';
if (isset($_POST['submit'])) {
    $num1 = $_POST['num1'];
    $num2 = $_POST['num2'];
    $operator = $_POST['operator'];
 
    switch ($operator) {
        case 'add':
            $result = $num1 + $num2;
            break;
        case 'subtract':
            $result = $num1 - $num2;
            break;
        case 'multiply':
            $result = $num1 * $num2;
            break;
        case 'divide':
            if ($num2 != 0) {
                $result = $num1 / $num2;
            } else {
                $result = 'Nelze dělit nulou';
            }
            break;
        default:
            $result = 'Špatný inpuut';
            break;
    }
}
?>
 
<h2>Kalkulačka</h2>
 
<form method="post" action="">
    <input type="text" name="num1" placeholder="Zadejte první čislo" required>
    <select name="operator" required>
        <option value="add">+</option>
        <option value="subtract">-</option>
        <option value="multiply">*</option>
        <option value="divide">/</option>
    </select>
    <input type="text" name="num2" placeholder="Zadejte druhé číslo" required>
    <button type="submit" name="submit">Spočítej</button>
</form>
 
<?php
if ($result !== '') {
    echo '<h3>Výsledek je: ' . $result . '</h3>';
}
?>
 
</body>
</html>
