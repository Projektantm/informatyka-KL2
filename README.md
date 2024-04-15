<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Budowanie Komputerów</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #333;
            color: #fff;
            padding: 20px;
        }

        nav ul {
            list-style-type: none;
            padding: 0;
        }

        nav ul li {
            display: inline;
            margin-right: 20px;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
        }

        main {
            padding: 20px;
        }

        footer {
            background-color: #333;
            color: #fff;
            padding: 10px 20px;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <header>
        <h1>Witaj na stronie o budowaniu komputerów!</h1>
        <nav>
            <ul>
                <li><a href="index.html">Strona Główna</a></li>
                <li><a href="porady.html">Porady</a></li>
                <li><a href="komponenty.html">Komponenty</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <p>Witaj na naszej stronie poświęconej budowaniu komputerów. Znajdziesz tutaj przydatne porady oraz listę niezbędnych komponentów.</p>
        <p id="date"></p>
        <p id="nameday"></p>
    </main>
    <footer>
        <p>&copy; 2024 Budowanie Komputerów</p>
    </footer>
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            // Wyświetlanie aktualnej daty
            var currentDate = new Date();
            var formattedDate = currentDate.toLocaleDateString('pl-PL');
            document.getElementById('date').innerText = 'Dzisiaj jest ' + formattedDate;

            // Wyświetlanie informacji o imieninach
            var namedays = {
                "01-01": "Mieczysław, Bazyl",
                "01-02": "Izydor, Bazyliszka",
                "01-03": "Łukasz, Dan",
                "01-04": "Sylwester, Eugeniusz",
                // itd...
                // dodaj więcej imion i dat
            };

            var today = new Date();
            var dd = String(today.getDate()).padStart(2, '0');
            var mm = String(today.getMonth() + 1).padStart(2, '0'); //Styczeń to 0!
            var currentDateFormatted = mm + '-' + dd;

            if (currentDateFormatted in namedays) {
                document.getElementById('nameday').innerText = 'Dziś imieniny obchodzą: ' + namedays[currentDateFormatted];
            } else {
                document.getElementById('nameday').innerText = 'Dziś nie obchodzą imieniny żadne z osób zapisanych w naszej bazie.';
            }
        });
    </script>
</body>
</html>
