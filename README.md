# Class-work-
<!DOCTYPE html>
<html>
<head>
    <title>Admission Check</title>
</head>
<body>

<form method="POST">
    JAMB Score: <input type="number" name="jamb_score"><br><br>
    Age: <input type="number" name="age"><br><br>
    <button type="submit">Check Admission</button>
</form>

<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $jamb_score = (int) $_POST['jamb_score'];
    $age = (int) $_POST['age'];

    if ($jamb_score >= 200 && $age >= 16) {
        echo "<p>Congratulations! You are admitted.</p>";
    } elseif ($jamb_score >= 320 && $age >= 15) {
        echo "<p>Congratulations! You are admitted.</p>";
    } else {
        echo "<p>Sorry, you do not meet the admission criteria.</p>";
    }
}
?>

</body>
</html>
