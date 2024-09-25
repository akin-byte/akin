<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Relaksasi untuk decahee</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background: linear-gradient(to right, #74ebd5, #acb6e5);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #333;
        }

        .container {
            background-color: white;
            width: 90%;
            max-width: 600px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            padding: 30px;
            text-align: center;
        }

        h1 {
            font-size: 2.5em;
            margin-bottom: 20px;
            color: #333;
        }

        .quote {
            font-size: 1.5em;
            margin-bottom: 30px;
            color: #555;
            font-style: italic;
            min-height: 60px;
            transition: color 0.3s ease;
        }

        .buttons {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            gap: 20px;
            margin-bottom: 30px;
        }

        button {
            background-color: #008CBA;
            color: white;
            border: none;
            padding: 15px;
            font-size: 1.1em;
            border-radius: 8px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        button:hover {
            background-color: #005f73;
        }

        #relaxation {
            font-size: 1.2em;
            color: #2f4f4f;
            min-height: 40px;
            transition: opacity 0.3s ease;
        }

        @media (max-width: 600px) {
            .buttons {
                grid-template-columns: 1fr;
            }

            h1 {
                font-size: 2em;
            }

            button {
                font-size: 1em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>semangatt untuk Decaa</h1>
        <p class="quote" id="quote">"Kerja keras deca hari ini pasti jadi kesuksesan untuk masa depan deca."</p>

        <div class="buttons">
            <button onclick="showQuote()">Kutipan Baru</button>
            <button onclick="breathingExercise()">Latihan Pernapasan</button>
            <button onclick="quickMeditation()">Meditasi Singkat</button>
        </div>

        <p id="relaxation"></p>
    </div>

    <script>
        const quotes = [
            '"Cape tu wajar, yang pasti jangan terlalu keras samo diri dea dewek. okkeyy?"',
            '"aku percyo kalo dea agek biso nyelesaikenyo, intiny jangan lupo istirahat. kalo dea sakit kan susah jadinyoo."',
            '"Istirahat sbntar, truss lanjutke samo semangat yang baru."',
            '"pelan-pelan tapi pasti."',
            '"semayy ya cantikk, ayabadoo"'
        ];

        function showQuote() {
            const randomIndex = Math.floor(Math.random() * quotes.length);
            const quoteElement = document.getElementById('quote');
            quoteElement.style.color = '#333';
            quoteElement.innerText = quotes[randomIndex];
        }

        function breathingExercise() {
            const relaxationText = "Tarik napas dalam-dalam... Tahan... Hembuskan perlahan... Ulangi 5 kali men biso 100 kali haha.";
            displayRelaxation(relaxationText);
        }

        function quickMeditation() {
            const relaxationText = "Pejamkan mata, tenangi pikiran, fokus samo napas.";
            displayRelaxation(relaxationText);
        }

        function displayRelaxation(text) {
            const relaxationElement = document.getElementById('relaxation');
            relaxationElement.style.opacity = '0';
            setTimeout(() => {
                relaxationElement.innerText = text;
                relaxationElement.style.opacity = '1';
            }, 300);
        }
    </script>
</body>
</html>
