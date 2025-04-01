<!DOCTYPE html><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gujarat University Result</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; background-color: #f8f9fa; }
        .container { width: 350px; margin: auto; padding: 20px; background: white; border-radius: 10px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); }
        input { display: block; width: 100%; padding: 10px; margin: 10px 0; border: 1px solid #ccc; border-radius: 5px; }
        button { padding: 10px; background-color: #007bff; color: white; border: none; cursor: pointer; width: 100%; border-radius: 5px; }
        button:hover { background-color: #0056b3; }
        #result { display: none; margin-top: 20px; padding: 15px; background: white; border-radius: 10px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); }
        .logo { width: 100px; margin-bottom: 10px; }
    </style>
</head>
<body>
    <h2>Gujarat University Exam Results</h2>
    <img src="https://upload.wikimedia.org/wikipedia/en/thumb/4/4b/Gujarat_University_Logo.svg/1200px-Gujarat_University_Logo.svg.png" class="logo" alt="University Logo">
    <div class="container">
        <input type="text" id="rollNumber" placeholder="Enter Roll Number">
        <input type="text" id="seatNumber" placeholder="Enter Seat Number">
        <button onclick="generateFakeResult()">View Result</button>
    </div>
    <div id="result">
        <h3>Exam Result</h3>
        <p id="resultText"></p>
    </div>
    <script>
        function generateFakeResult() {
            var rollNumber = document.getElementById("rollNumber").value;
            var seatNumber = document.getElementById("seatNumber").value;
            if (rollNumber === "" || seatNumber === "") {
                alert("Please enter both Roll Number and Seat Number");
                return;
            }
            var results = [
                "Fail in all subjects! Apply for re-exam!",
                "Congratulations! You are the University Topper!",
                "Error! Your result is not found. Contact the admin.",
                "You have got 99% marks! Unbelievable!",
                "Your result is under review due to suspected cheating."
            ];
            var randomResult = results[Math.floor(Math.random() * results.length)];
            document.getElementById("resultText").innerText = randomResult;
            document.getElementById("result").style.display = "block";
            setTimeout(() => {
                document.getElementById("resultText").innerHTML += "<br><br><strong>April Fools! This is a prank.</strong>";
            }, 5000);
        }
    </script>
</body>
</html>
