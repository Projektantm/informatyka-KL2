<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Budowanie Komputerów</title>
    <link rel="stylesheet" href="styles.css">
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
    </main>
    <footer>
        <p>&copy; 2024 Budowanie Komputerów</p>
    </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Porady dotyczące budowy komputerów</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Porady dotyczące budowy komputerów</h1>
        <nav>
            <ul>
                <li><a href="index.html">Strona Główna</a></li>
                <li><a href="porady.html">Porady</a></li>
                <li><a href="komponenty.html">Komponenty</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <h2>Podstawowe porady:</h2>
        <ol>
            <li>Wybierz odpowiedni procesor i płytę główną kompatybilną ze sobą.</li>
            <li>Dobierz odpowiednią kartę graficzną do swoich potrzeb.</li>
            <li>Pamiętaj o odpowiedniej ilości i typie pamięci RAM.</li>
            <li>Wybierz zasilacz o odpowiedniej mocy dla wszystkich podzespołów.</li>
            <li>Zainstaluj odpowiedni system chłodzenia dla procesora.</li>
        </ol>
    </main>
    <footer>
        <p>&copy; 2024 Budowanie Komputerów</p>
    </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lista niezbędnych komponentów do budowy komputera</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Lista niezbędnych komponentów do budowy komputera</h1>
        <nav>
            <ul>
                <li><a href="index.html">Strona Główna</a></li>
                <li><a href="porady.html">Porady</a></li>
                <li><a href="komponenty.html">Komponenty</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <h2>Komponenty:</h2>
        <ul>
            <li>Procesor</li>
            <li>Płyta główna</li>
            <li>Karta graficzna</li>
            <li>Pamięć RAM</li>
            <li>Dysk twardy lub SSD</li>
            <li>Zasilacz</li>
            <li>Obudowa</li>
            <li>System chłodzenia procesora</li>
            <li>Klawiatura i mysz</li>
            <li>Monitor</li>
        </ul>
    </main>
    <footer>
        <p>&copy; 2024 Budowanie Komputerów</p>
    </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Budowanie Komputerów</title>
    <link rel="stylesheet" href="styles.css">
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
    <script src="scripts.js"></script>
</body>
</html>
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
