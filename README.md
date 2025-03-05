<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>D.R. Horizons - Auteur</title>
    <meta name="description" content="Découvrez l'univers captivant de D.R. Horizons, écrivain de thrillers psychologiques et de récits mystérieux. Soutenez son œuvre littéraire." />
    <meta property="og:title" content="D.R. Horizons - Auteur" />
    <meta property="og:description" content="Plongez dans l'univers troublant de D.R. Horizons, où rêve et réalité se confondent." />
    <meta property="og:image" content="cover.png" />
    <meta property="og:url" content="https://votre-site.com" />
    <link rel="stylesheet" href="styles.css">
    <style>
        nav {
            background: #222;
            padding: 15px;
            text-align: center;
        }
        nav a {
            color: white;
            text-decoration: none;
            font-size: 20px;
            margin: 0 20px;
            font-weight: bold;
        }
        header span {
            font-size: 32px;
            font-weight: bold;
        }
        .stars {
            font-size: 40px;
            color: gold;
            cursor: pointer;
        }
        .section {
            margin-bottom: 80px;
        }
        .big-button {
            display: block;
            width: 250px;
            margin: 20px auto;
            padding: 15px;
            font-size: 20px;
            font-weight: bold;
            background-color: #ff8c00;
            color: white;
            text-align: center;
            border-radius: 10px;
            text-decoration: none;
        }
    </style>
</head>
<body>
    <header>
        <img src="photo.jpeg" alt="Portrait de l'écrivain D.R. Horizons" class="photo">
        <span>D.R. Horizons - Aux frontières du réel</span>
    </header>

    <nav>
        <a href="#oeuvres">Mon Livre</a>
        <a href="#about">À propos</a>
        <a href="#contact">Contact</a>
        <a href="#don">Soutenir</a>
    </nav>
    
    <section class="section" id="oeuvres">
        <h1>Mon premier livre</h1>
        <p>Après des vacances paradisiaques au Mexique, Chloé et Madison...</p>
        <img src="Cover.png" alt="Couverture du livre de D.R. Horizons" class="book-cover">
        <p>Bientôt disponible. Plongez dans une œuvre captivante et hors du commun.</p>
        <a href="https://www.amazon.com/dp/votre_livre" class="big-button">Acheter sur Amazon</a>
        
        <h3>Notez ce livre :</h3>
        <div class="stars" aria-live="polite">
            <span class="star" data-value="1">★</span>
            <span class="star" data-value="2">★</span>
            <span class="star" data-value="3">★</span>
            <span class="star" data-value="4">★</span>
            <span class="star" data-value="5">★</span>
        </div>
        <p id="rating-feedback" aria-live="polite"></p>
    </section>
    
    <section class="section" id="about">
        <h2>À propos</h2>
        <p>D.R. Horizons est un conteur passionné par les atmosphères envoûtantes et les récits à suspense où chaque détail compte. À travers une écriture fluide et immersive, il entraîne ses lecteurs dans des univers où le mystère côtoie l’émotion, et où les apparences sont souvent trompeuses.</p>
    </section>
    
    <section class="section" id="contact">
        <h2>Contact & Soutien</h2>
        <form id="contact-form">
            <label for="name">Nom :</label>
            <input type="text" id="name" name="name" required>

            <label for="email">Email :</label>
            <input type="email" id="email" name="email" required>

            <label for="message">Message :</label>
            <textarea id="message" name="message" rows="4" required></textarea>

            <button type="submit" class="big-button">Envoyer</button>
        </form>
    </section>
    
    <section class="section" id="don">
        <h2>Soutenez mon écriture</h2>
        <p>Votre soutien me permet de continuer à écrire et à publier des œuvres qui sortent des sentiers battus.</p>
        <a href="https://paypal.me/DRHorizons?country.x=CA&locale.x=fr_CA" class="big-button">Faire un don</a>
    </section>
    
    <footer>
        © 2025 D.R. Horizons - Un écrivain hors limites
    </footer>

    <script>
        document.querySelectorAll('.star').forEach(star => {
            star.addEventListener('click', function() {
                document.querySelectorAll('.star').forEach(s => s.style.color = '#ccc');
                let value = this.getAttribute('data-value');
                for (let i = 0; i < value; i++) {
                    document.querySelectorAll('.star')[i].style.color = 'gold';
                }
                document.getElementById('rating-feedback').textContent = 'Merci pour votre note : ' + value + ' étoiles !';
            });
        });
    </script>
</body>
</html>
