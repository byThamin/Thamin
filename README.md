<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fotografie Webseite</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #333;
            color: #fff;
            padding: 10px 20px;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #444;
            padding: 10px;
        }
        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
        }
        nav a:hover {
            text-decoration: underline;
        }
        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            padding: 20px;
        }
        .gallery img {
            width: 200px;
            height: auto;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        .contact-form {
            background: #fff;
            max-width: 500px;
            margin: 20px auto;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        .contact-form label {
            display: block;
            margin-bottom: 5px;
        }
        .contact-form input, .contact-form textarea {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        .contact-form button {
            background-color: #333;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .contact-form button:hover {
            background-color: #555;
        }
        footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 10px;
            margin-top: 20px;
            position: relative;
        }
        .social-links a {
            margin: 0 10px;
            color: white;
            text-decoration: none;
        }
        .floating-instagram {
            position: fixed;
            bottom: 10px;
            right: 10px;
            background-color: #E1306C;
            color: white;
            padding: 10px 15px;
            border-radius: 50%;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
            text-align: center;
            font-size: 20px;
            cursor: pointer;
            text-decoration: none;
        }
        .floating-instagram:hover {
            background-color: #d32e62;
        }
        .impressum-link {
            position: absolute;
            bottom: 10px;
            left: 10px;
            color: white;
            text-decoration: none;
        }
        .impressum-link:hover {
            text-decoration: underline;
        }
    </style>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const blockedDates = ['2025-01-15', '2025-01-20', '2025-01-25']; // Blockierte Tage

            const dateInput = document.getElementById('appointment-date');
            const submitButton = document.querySelector('.contact-form button');

            dateInput.addEventListener('input', () => {
                const selectedDate = dateInput.value;
                if (blockedDates.includes(selectedDate)) {
                    alert('Dieser Termin ist bereits belegt. Bitte wählen Sie ein anderes Datum.');
                    submitButton.disabled = true;
                } else {
                    submitButton.disabled = false;
                }
            });
        });
    </script>
</head>
<body>

<header>
    <h1>Willkommen auf meiner Fotografie-Webseite</h1>
</header>

<nav>
    <a href="#gallery">Galerie</a>
    <a href="#contact">Kontakt</a>
</nav>

<section id="gallery">
    <h2 style="text-align: center; margin-top: 20px;">Galerie</h2>
    <div class="gallery">
        <img src="https://via.placeholder.com/200" alt="Beispielbild 1">
        <img src="https://via.placeholder.com/200" alt="Beispielbild 2">
        <img src="https://via.placeholder.com/200" alt="Beispielbild 3">
    </div>
</section>

<section id="contact">
    <h2 style="text-align: center; margin-top: 20px;">Kontakt</h2>
    <form class="contact-form" action="mailto:deine.email@example.com" method="post" enctype="text/plain">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required>

        <label for="email">E-Mail:</label>
        <input type="email" id="email" name="email" required>

        <label for="appointment-date">Wunschtermin:</label>
        <input type="date" id="appointment-date" name="appointment-date" required>

        <label for="message">Nachricht:</label>
        <textarea id="message" name="message" rows="5" required></textarea>

        <button type="submit">Absenden</button>
    </form>
</section>

<a href="https://instagram.com" target="_blank" class="floating-instagram">&#x1F426;</a>

<footer>
    <p>Folge mir auf:</p>
    <div class="social-links">
        <a href="https://instagram.com" target="_blank">Instagram</a>
        <a href="https://facebook.com" target="_blank">Facebook</a>
        <a href="https://twitter.com" target="_blank">Twitter</a>
    </div>
    <a href="#" class="impressum-link">Impressum</a>
    <p>&copy; 2025 Deine Fotografie</p>
</footer>

</body>
</html>
