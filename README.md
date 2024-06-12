<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nutella Abstimmung</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }
        h1 {
            color: #333;
        }
        .vote-container {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        .vote-button {
            background-color: #007BFF;
            color: white;
            border: none;
            padding: 10px 20px;
            margin: 5px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }
        .vote-button:hover {
            background-color: #0056b3;
        }
        .results {
            margin-top: 20px;
        }
    </style>
</head>
<body>

    <h1>Wie isst du dein Nutella?</h1>
    <div class="vote-container">
        <button class="vote-button" onclick="vote('mitButter')">Mit Butter</button>
        <button class="vote-button" onclick="vote('ohneButter')">Ohne Butter</button>
        <div class="results">
            <p>Mit Butter: <span id="mitButterVotes">0</span></p>
            <p>Ohne Butter: <span id="ohneButterVotes">0</span></p>
        </div>
    </div>

    <script>
        let mitButterVotes = 0;
        let ohneButterVotes = 0;

        function vote(option) {
            if (option === 'mitButter') {
                mitButterVotes++;
                document.getElementById('mitButterVotes').innerText = mitButterVotes;
            } else if (option === 'ohneButter') {
                ohneButterVotes++;
                document.getElementById('ohneButterVotes').innerText = ohneButterVotes;
            }
        }
    </script>

</body>
</html>
