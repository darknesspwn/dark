<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DarkAnime</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
    body {
    font-family: Arial, sans-serif;
    background-color: #121212;
    color: #fff;
    background-image: url('');
    background-size: cover;       /* Фото будет растягиваться на весь экран */
    background-position: center;  /* Центрирование изображения */
    background-attachment: fixed; /* Фиксация изображения при прокрутке */
}
        }

        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            animation: fadeIn 1s forwards;
        }

        @keyframes fadeIn {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .anime-list, .anime-detail {
            opacity: 0;
            transform: translateY(20px);
            animation: fadeIn 0.8s forwards;
        }


   header {
    background-image: url('https://img.freepik.com/premium-photo/abstract-background-design-hd-dark-sceptre-red-color_851755-157751.jpg?semt=ais_hybrid');
    background-size: cover;       /* Растягивает изображение на весь элемент */
    background-position: center;
    background-repeat: no-repeat; /* Отключает повтор изображения */
    padding: 20px;
    text-align: center;
}

        header h1 {
            font-size: 2.5em;
        }

        nav {
            background-color: #333;
            text-align: center;
            padding: 10px;
        }

        nav a {
            color: white;
            padding: 10px 15px;
            text-decoration: none;
            margin: 0 10px;
            font-size: 1.1em;
        }

        nav a:hover {
            background-color: #555;
        }

        main {
            padding: 20px;
        }

        .genres {
            margin-bottom: 20px;
            display: flex;
            justify-content: space-around;
        }

        .genre {
            background-color: #333;
            padding: 10px 20px;
            border-radius: 8px;
            cursor: pointer;
        }

        .anime-list {
            display: flex;
            overflow-x: auto;
            gap: 20px;
            padding-bottom: 10px;
            margin-top: 20px;
        }

        .anime-item {
            background-color: #333;
            padding: 10px;
            border-radius: 8px;
            text-align: center;
            color: #fff;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            flex-shrink: 0;
            width: 200px;
        }

        .anime-item img {
            width: 100%;
            border-radius: 8px;
            height: auto;
            transition: opacity 0.3s ease;
        }

        .anime-item h3 {
            margin-top: 10px;
        }

        .anime-item:hover {
            transform: scale(1.05);
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
        }

        .anime-item:hover img {
            opacity: 0.9;
        }

        .anime-detail {
            display: flex;
            flex-direction: row;
            gap: 20px;
            background-color: #333;
            padding: 20px;
            border-radius: 8px;
            max-width: 800px;
            margin: 0 auto;
        }

        .anime-detail img {
            width: 250px;
            border-radius: 8px;
            height: auto;
        }

        .anime-description {
            flex: 1;
        }

        .series-list {
            margin-top: 20px;
        }

        .series-list button {
            background-color: #444;
            color: white;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
        }

        .series-list button:hover {
            background-color: #555;
        }

        footer {
            background-color: #222;
            color: #bbb;
            text-align: center;
            padding: 10px;
            position: fixed;
            width: 100%;
            bottom: 0;
        }

        .back-button {
            background-color: #808080;
            color: #fff;
            padding: 12px 24px;
            font-size: 1.2em;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            display: inline-block;
            margin-bottom: 20px;
            text-align: center;
            transition: background-color 0.3s ease, transform 0.3s ease;
        }

        .back-button:hover {
            background-color: #6c6c6c;
            transform: scale(1.05);
        }

        .back-button:active {
            background-color: #555;
        }

        @media (max-width: 768px) {
            .anime-list {
                flex-direction: column;
            }

            header h1 {
                font-size: 2em;
            }

            nav a {
                font-size: 1em;
            }

            .anime-detail {
                flex-direction: column;
            }

            .anime-detail img {
                width: 100%;
            }
        }
    </style>
</head>
<body>

    <header>
        <h1>DarkAnime</h1>
        <p>Смотрите лучшие аниме онлайн бесплатно</p>
    </header>

    <nav>
        <a href="#" onclick="showPage('main')">Главная</a>
        <a href="#">Категории</a>
        <a href="#">Топ аниме</a>
        <a href="#">О нас</a>
    </nav>

    <main id="main" style="display: block;">
        <section class="genres">
            <div class="genre">Приключения</div>
            <div class="genre">Фантастика</div>
            <div class="genre">Драма</div>
            <div class="genre">Комедия</div>
            <div class="genre">Экшен</div>
            <div class="genre">Мистика</div>
        </section>

        <h2>Популярные аниме</h2>
        <div class="anime-list">
            <div class="anime-item" onclick="showAnimePage('anime1')">
                <img src="https://static.hdrezka.ac/i/2022/10/6/z8e7ec46fa26ddq84x50f.png" alt="Восхождение в тени">
                <h3>Восхождение в тени</h3>
            </div>
            <div class="anime-item" onclick="showAnimePage('anime2')">
                <img src="https://animego.online/uploads/posts/2024-03/milyj-vo-frankse_poster.webp" alt="Милый во франксе">
                <h3>Милый во франксе</h3>
            </div>
            <div class="anime-item" onclick="showAnimePage('anime3')">
                <img src="https://static.wikia.nocookie.net/tensei-shitara-slime-datta-ken/images/2/22/Anime_Cover.jpg/revision/latest?cb=20181023140639" alt="О моём перерождении в слизь">
                <h3>О моём перерождении в слизь</h3>
            </div>
            <div class="anime-item" onclick="showAnimePage('anime4')">
                <img src="https://nyaa.shikimori.one/uploads/poster/animes/40496/main_2x-59e3f73c72bd05e2ae814953f3a51e6e.webp" alt="Непризнанный школой владыка демонов">
                <h3>Непризнанный школой владыка демонов</h3>
            </div>
            <div class="anime-item" onclick="showAnimePage('anime5')">
                <img src="https://static.hdrezka.ac/i/2022/11/14/f0abc113b4935ws27e81i.png" alt="Атака титанов">
                <h3>Атака титанов</h3>
            </div>
            <div class="anime-item" onclick="showAnimePage('anime6')">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTFE34AuOBihJv6npdiXgdUtOLmvaw99vHSyA&s"" alt="Наруто">
                <h3>Наруто</h3>
            </div>
            <div class="anime-item" onclick="showAnimePage('anime7')">
                <img src="https://images.kinorium.com/movie/1080/2638559.jpg?1668512656"Лимонные девочки" alt="">
                <h3>Лимонные девочки</h3>
            </div>
            <div class="anime-item" onclick="showAnimePage('anime8')">
                <img src="https://nyaa.shikimori.one/uploads/poster/animes/11757/main_2x-fb19a1dedc2ab1a976439ae7dd4b5eae.webp"Мастера меча онлайн" alt="">
                <h3>Мастера меча онлайн</h3>
            </div>
        </div>
    </main>

    <main id="anime-detail" style="display: none;">
        <button class="back-button" onclick="showPage('main')">Назад в главное меню</button>
        <div id="anime-detail-content"></div>
    </main>

    <footer>
        <p>&copy; 2024 DarkAnime Online. Все права защищены.</p>
    </footer>

    <script>
        function showPage(page) {
            if (page === 'main') {
                document.getElementById('main').style.display = 'block';
                document.getElementById('anime-detail').style.display = 'none';
            }
        }

        function showAnimePage(animeId) {
            document.getElementById('main').style.display = 'none';
            document.getElementById('anime-detail').style.display = 'block';

            const animeDetailContent = document.getElementById('anime-detail-content');
            let animeContent = '';

            if (animeId === 'anime1') {
                animeContent = `
                    <div class="anime-detail">
                        <img src="https://static.hdrezka.ac/i/2022/10/6/z8e7ec46fa26ddq84x50f.png" alt="Восхождение в тени">
                        <div class="anime-description">
                            <h2>Восхождение в тени</h2>
                            <p>Краткое описание аниме: Восхождение в тени — это история...</p>
                            <div class="series-list">
                                <button onclick="showEpisode('anime1', 1)">Серия 1</button>
                                <button onclick="showEpisode('anime1', 2)">Серия 2</button>
                                <button onclick="showEpisode('anime1', 3)">Серия 3</button>
                            </div>
                            <div id="anime1-episode" style="margin-top: 20px;"></div>
                        </div>
                    </div>
                `;
            } else if (animeId === 'anime2') {
                animeContent = `
                    <div class="anime-detail">
                        <img src="https://animego.online/uploads/posts/2024-03/milyj-vo-frankse_poster.webp" alt="Милый во франксе">
                        <div class="anime-description">
                            <h2>Милый во франксе</h2>
                            <p>Краткое описание аниме: Милый во франксе — это история о...</p>
                            <div class="series-list">
                                <button onclick="showEpisode('anime2', 1)">Серия 1</button>
                                <button onclick="showEpisode('anime2', 2)">Серия 2</button>
                                <button onclick="showEpisode('anime2', 3)">Серия 3</button>
                            </div>
                            <div id="anime2-episode" style="margin-top: 20px;"></div>
                        </div>
                    </div>
                `;
            } else if (animeId === 'anime3') {
                animeContent = `
                    <div class="anime-detail">
                        <img src="https://static.wikia.nocookie.net/tensei-shitara-slime-datta-ken/images/2/22/Anime_Cover.jpg/revision/latest?cb=20181023140639" alt="О моём перерождении в слизь">
                        <div class="anime-description">
                            <h2>О моём перерождении в слизь</h2>
                            <p>Краткое описание аниме: О моём перерождении в слизь — это...</p>
                            <div class="series-list">
                                <button onclick="showEpisode('anime3', 1)">Серия 1</button>
                                <button onclick="showEpisode('anime3', 2)">Серия 2</button>
                                <button onclick="showEpisode('anime3', 3)">Серия 3</button>
                            </div>
                            <div id="anime3-episode" style="margin-top: 20px;"></div>
                        </div>
                    </div>
                `;
            } else if (animeId === 'anime4') {
                animeContent = `
                    <div class="anime-detail">
                        <img src="https://nyaa.shikimori.one/uploads/poster/animes/40496/main_2x-59e3f73c72bd05e2ae814953f3a51e6e.webp" alt="Непризнанный школой владыка демонов">
                        <div class="anime-description">
                            <h2>Непризнанный школой владыка демонов</h2>
                            <p>Краткое описание аниме: Непризнанный школой владыка демонов...</p>
                            <div class="series-list">
                                <button onclick="showEpisode('anime4', 1)">Серия 1</button>
                                <button onclick="showEpisode('anime4', 2)">Серия 2</button>
                                <button onclick="showEpisode('anime4', 3)">Серия 3</button>
                            </div>
                            <div id="anime4-episode" style="margin-top: 20px;"></div>
                        </div>
                    </div>
                `;
            } else if (animeId === 'anime5') {
                animeContent = `
                    <div class="anime-detail">
                        <img src="https://static.hdrezka.ac/i/2022/11/14/f0abc113b4935ws27e81i.png" alt="Атака титанов">
                        <div class="anime-description">
                            <h2>Атака титанов</h2>
                            <p>Краткое описание аниме: Атака титанов — это...</p>
                            <div class="series-list">
                                <button onclick="showEpisode('anime5', 1)">Серия 1</button>
                                <button onclick="showEpisode('anime5', 2)">Серия 2</button>
                                <button onclick="showEpisode('anime5', 3)">Серия 3</button>
                            </div>
                            <div id="anime5-episode" style="margin-top: 20px;"></div>
                        </div>
                    </div>
                `;
            } else if (animeId === 'anime6') {
                animeContent = `
                    <div class="anime-detail">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTFE34AuOBihJv6npdiXgdUtOLmvaw99vHSyA&s" alt="Наруто">
                        <div class="anime-description">
                            <h2>Наруто</h2>
                            <p>Краткое описание аниме: Наруто — это...</p>
                            <div class="series-list">
                                <button onclick="showEpisode('anime6', 1)">Серия 1</button>
                                <button onclick="showEpisode('anime6', 2)">Серия 2</button>
                                <button onclick="showEpisode('anime6', 3)">Серия 3</button>
                            </div>
                            <div id="anime6-episode" style="margin-top: 20px;"></div>
                        </div>
                    </div>
                `;
            } else if (animeId === 'anime7') {
                animeContent = `
                    <div class="anime-detail">
                        <img src="https://images.kinorium.com/movie/1080/2638559.jpg?1668512656" alt="Лимонные девочки">
                        <div class="anime-description">
                            <h2>Наруто</h2>
                            <p>Краткое описание аниме: Лимонные девочки — это...</p>
                            <div class="series-list">
                                <button onclick="showEpisode('anime7', 1)">Серия 1</button>
                                <button onclick="showEpisode('anime7', 2)">Серия 2</button>
                                <button onclick="showEpisode('anime7', 3)">Серия 3</button>
                            </div>
                            <div id="anime7-episode" style="margin-top: 20px;"></div>
                        </div>
                    </div>
                `;
            }else if (animeId === 'anime8') {
                animeContent = `
                    <div class="anime-detail">
                        <img src="https://nyaa.shikimori.one/uploads/poster/animes/11757/main_2x-fb19a1dedc2ab1a976439ae7dd4b5eae.webp" alt="Мастера меча онлайн">
                        <div class="anime-description">
                            <h2>Наруто</h2>
                            <p>Краткое описание аниме: Мастера меча онлайн — это...</p>
                            <div class="series-list">
                                <button onclick="showEpisode('anime8', 1)">Серия 1</button>
                                <button onclick="showEpisode('anime8', 2)">Серия 2</button>
                                <button onclick="showEpisode('anime8', 3)">Серия 3</button>
                            </div>
                            <div id="anime8-episode" style="margin-top: 20px;"></div>
                        </div>
                    </div>
                `;
            }

            animeDetailContent.innerHTML = animeContent;
        }

        function showEpisode(animeId, episodeNumber) {
            const episodeContainer = document.getElementById(`${animeId}-episode`);
            episodeContainer.innerHTML = `<p>Содержание серии ${episodeNumber}...</p>`;
        }
    function showEpisode(animeId, episodeNumber) {
    const episodeContainer = document.getElementById(`${animeId}-episode`);

    let videoUrl = ''; // Переменная для хранения ссылки на видео

    // Пример условной логики, которая изменяет видео в зависимости от серии
    if (animeId === 'anime1') {
        if (episodeNumber === 1) {
            videoUrl = 'C:/Users/artyr/Downloads/1.720.696462bf80705fcd.mp4';  // Путь к видео для первой серии
        } else if (episodeNumber === 2) {
            videoUrl = 'path/to/anime1-episode2.mp4';  // Путь ко второй серии
        }
    } else if (animeId === 'anime2') {
        if (episodeNumber === 1) {
            videoUrl = 'path/to/anime2-episode1.mp4';  // Путь к видео для первой серии
        }
    }

    // Добавление HTML плеера для видео
    episodeContainer.innerHTML = `
        <video width="100%" controls>
            <source src="${videoUrl}" type="video/mp4">
            Ваш браузер не поддерживает элемент video.
        </video>
    `;
}
    </script>

</body>
</html>
