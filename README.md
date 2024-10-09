<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <link href="https://fonts.googleapis.com/css2?family=Caveat:wght@700&display=swap" rel="stylesheet">

    <style>
        body {
            background-image: url('https://media.discordapp.net/attachments/781047263233179692/1293577746374463499/Projekt_bez_nazwy.png?ex=6707e1a8&is=67069028&hm=9d2aa0a868cfe2552eeee83b686b89c2fd25c45a12806186667cd6045f264bac&=&format=webp&quality=lossless&width=1062&height=753'); 
            background-size: cover;
            background-repeat: no-repeat;
            background-position: center;
            font-family: 'Caveat', sans-serif; 
            text-align: center;
            margin: 0;
            padding: 0;
            color: #FF69B4;
        }

        .overlay {
            background-color: rgba(0, 0, 0, 0.2); 
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }

        .container {
            position: relative;
            z-index: 1;
            margin-top: 50px;
            padding: 20px;
        }

        h1 {
            font-size: 4.5rem;
            margin-bottom: 20px;
        }

        p {
            font-size: 3rem;
            margin-bottom: 30px;
        }

        .question {
            font-size: 2.5rem;
            margin: 20px 0;
        }

        .btn {
            background-color: #FF69B4;
            color: white;
            padding: 15px 30px;
            font-size: 1.2rem;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            transition: background-color 0.3s ease;
            margin: 10px;
        }

        .btn:hover {
            background-color: #FF69B4;
        }

        .calendar {
            margin-top: 20px;
        }

        input[type="date"] {
            padding: 10px;
            border-radius: 10px;
            border: 2px solid #ff1493;
            font-size: 1.2rem;
        }

        footer {
            margin-top: 50px;
            font-size: 0.9rem;
            color: #FF69B4;
        }
    </style>

    <script>
        function showResponse(response) {
            alert('Wybrałeś opcję: ' + response + '. Już nie mogę się doczekać! 🎉');
        }

        function datePicked() {
            const selectedDate = document.getElementById('datePicker').value;
            if (selectedDate) {
                alert('Wybrałeś datę: ' + selectedDate + '. Zarezerwuję termin! 📅');
            }
        }
    </script>
</head>
<body>

    <div class="overlay"></div> 

    <div class="container">
        <h1>Co Ty na Halloweenową randkę? 👉👈</h1>
        <p>Hej, chciałabym Cię zaprosić na wyjątkową randkę w klimacie Halloween! 🎃</p>
        <p>Co powiesz na wspólną zabawę w escaperoomie?</p>

        <div class="question">
            <p>Czy chcesz iść na randkę?</p>
            <button class="btn" onclick="showResponse('Tak!')">Tak!</button>
            <button class="btn" onclick="showResponse('Definitywnie tak!')">Definitywnie tak!</button>

        </div>

        <div class="calendar">

          <form action="https://formspree.io/f/xeoqjdny" method="POST">
            <p>Wybierz datę randki:</p>
            <input type="date" id="datePicker" name="date" required>
            <input type="submit" class="btn" value="Wyślij">
          </form>

        </div>
    </div>

</body>
</html>
