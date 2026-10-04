<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title> uy engineer yohoo!</title>

    <style>
        * {
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            margin: 0;
            min-height: 100vh;
            font-family: Georgia, "Times New Roman", serif;
            background: linear-gradient(to bottom, #181818, #000000);
            color: #eeeeee;
        }

        /* FLOATING HEARTS */

        .heart {
            position: fixed;
            bottom: -30px;
            color: #777;
            font-size: 22px;
            opacity: 0.4;
            animation: floatUp 10s linear infinite;
            pointer-events: none;
            z-index: 0;
        }

        .heart:nth-child(1) {
            left: 5%;
            animation-duration: 8s;
        }

        .heart:nth-child(2) {
            left: 20%;
            animation-duration: 11s;
            animation-delay: 2s;
        }

        .heart:nth-child(3) {
            left: 40%;
            animation-duration: 9s;
            animation-delay: 1s;
        }

        .heart:nth-child(4) {
            left: 60%;
            animation-duration: 12s;
            animation-delay: 3s;
        }

        .heart:nth-child(5) {
            left: 80%;
            animation-duration: 10s;
            animation-delay: 1s;
        }

        @keyframes floatUp {
            0% {
                transform: translateY(0);
                opacity: 0;
            }

            10% {
                opacity: 0.4;
            }

            100% {
                transform: translateY(-110vh);
                opacity: 0;
            }
        }

        /* MAIN */

        .container {
            position: relative;
            z-index: 1;
            width: 92%;
            max-width: 850px;
            margin: auto;
        }

        /* OPENING SCREEN */

        #openingScreen {
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        .card {
            background: rgba(20, 20, 20, 0.95);
            border: 1px solid #333;
            border-radius: 25px;
            padding: 40px 25px;
            width: 100%;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.8);
        }

        h1 {
            color: white;
        }

        .opening-title {
            font-size: clamp(30px, 7vw, 50px);
            margin-bottom: 25px;
        }

        .opening-text {
            font-size: 18px;
            line-height: 1.8;
            color: #ddd;
        }

        button {
            cursor: pointer;
            border: none;
            font-family: inherit;
        }

        .main-button {
            margin-top: 20px;
            padding: 15px 28px;
            border-radius: 50px;
            background: white;
            color: black;
            font-size: 16px;
            font-weight: bold;
            transition: 0.3s;
        }

        .main-button:hover {
            transform: scale(1.03);
            background: #f1f1f1;
        }

        /* PASSWORD */

        #passwordScreen {
            display: none;
            min-height: 100vh;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        .password-card {
            background: rgba(20, 20, 20, 0.95);
            border: 1px solid #333;
            border-radius: 25px;
            padding: 40px 25px;
            width: 100%;
            max-width: 450px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.8);
        }

        .password-card p {
            color: #ccc;
            line-height: 1.7;
        }

        .clue {
            color: #888 !important;
            font-size: 14px;
            margin-top: 20px;
        }

        #passwordInput {
            width: 100%;
            padding: 14px;
            margin-top: 15px;
            border-radius: 12px;
            border: 1px solid #444;
            background: #111;
            color: white;
            text-align: center;
            font-size: 17px;
            outline: none;
        }

        #passwordInput:focus {
            border-color: #888;
        }

        #errorMessage {
            display: none;
            color: #aaa !important;
        }

        /* LETTER */

        #letterSection {
            display: none;
            padding: 30px 0 60px;
        }

        /* SPOTIFY BUTTON */

        .music-player {
            position: sticky;
            top: 15px;
            z-index: 10;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
            flex-wrap: wrap;
            margin-bottom: 20px;
            padding: 12px;
            background: rgba(20, 20, 20, 0.95);
            border: 1px solid #333;
            border-radius: 50px;
        }

        .spotify-button {
            display: inline-block;
            padding: 10px 20px;
            border-radius: 30px;
            background: white;
            color: black;
            text-decoration: none;
            font-weight: bold;
            font-size: 15px;
            transition: 0.3s;
        }

        .spotify-button:hover {
            transform: scale(1.03);
            background: #f1f1f1;
        }

        #musicStatus {
            font-size: 14px;
            color: #aaa;
        }

        /* LETTER CARD */

        .letter-card {
            background: rgba(15, 15, 15, 0.97);
            border: 1px solid #2d2d2d;
            border-radius: 25px;
            padding: clamp(25px, 5vw, 55px);
            box-shadow: 0 20px 70px rgba(0, 0, 0, 0.8);
        }

        .letter-title {
            text-align: center;
            font-size: clamp(28px, 6vw, 40px);
            margin-bottom: 40px;
        }

        .letter {
            color: #ddd;
            font-size: 17px;
            line-height: 1.9;
        }

        .letter p {
            margin-bottom: 25px;
        }

        .closing {
            text-align: center;
            color: white;
            font-size: 20px;
            margin-top: 40px;
        }

        /* FADE */

        .fade {
            animation: fadeIn 1s ease;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(15px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* MOBILE */

        @media (max-width: 600px) {

            .card {
                padding: 35px 20px;
            }

            .letter-card {
                padding: 25px 20px;
            }

            .letter {
                font-size: 16px;
                line-height: 1.8;
            }

            .music-player {
                border-radius: 25px;
            }
        }
    </style>
</head>

<body>

    <!-- FLOATING HEARTS -->

    <div class="heart">♡</div>
    <div class="heart">♥</div>
    <div class="heart">♡</div>
    <div class="heart">♥</div>
    <div class="heart">♡</div>


    <div class="container">

        <!-- ========================= -->
        <!-- OPENING SCREEN -->
        <!-- ========================= -->

        <section id="openingScreen">

            <div class="card fade">

                <h1 class="opening-title">
                    For My Fave Hooman 🖤
                </h1>

                <p class="opening-text">
                    My all-time fave i-ragebait,<br>
                    my taga-salo ng random thoughts ko,<br>
                    my pinsan by heart,<br>
                    and shempre, my Engr. Micah Jezra.
                </p>

                <p class="opening-text">
                    I made something for you.
                </p>

                <button
                    class="main-button"
                    onclick="showPassword()"
                >
                    Open this for me 🖤
                </button>

            </div>

        </section>


        <!-- ========================= -->
        <!-- PASSWORD SCREEN -->
        <!-- ========================= -->

        <section id="passwordScreen">

            <div class="password-card fade">

                <h1>
                    🔐 A little secret...
                </h1>

                <p>
                    Before you read this,
                    you need to know the password. 🖤
                </p>

                <p class="clue">
                    Clue: the day i gave u a cake (mm/dd/yy)
                </p>

                <input
                    type="password"
                    id="passwordInput"
                    placeholder="Enter the password"
                    onkeydown="handleEnter(event)"
                >

                <button
                    class="main-button"
                    onclick="checkPassword()"
                >
                    Unlock 🖤
                </button>

                <p id="errorMessage">
                    Nope. Try again, boi. 😂
                </p>

            </div>

        </section>


        <!-- ========================= -->
        <!-- LETTER -->
        <!-- ========================= -->

        <section id="letterSection">

            <!-- SPOTIFY -->

            <div class="music-player">

                <a
                    class="spotify-button"
                    href="https://open.spotify.com/search/Paalala%20twosday"
                    target="_blank"
                    rel="noopener noreferrer"
                >
                    🎵 Open Paalala on Spotify
                </a>

                <span id="musicStatus">
                    Paalala by twosday 🖤
                </span>

            </div>


            <!-- LETTER -->

            <div class="letter-card fade">

                <h1 class="letter-title">
                    To My Fave Hooman 🖤
                </h1>

                <div class="letter">

                    <p>
                        To my fave human, my all-time fave i-ragebait, my taga-salo ng random thoughts ko, my pinsan by heart, and shempre, my Engr. Micah Jezra,
                    </p>

                    <p>
                        I'm not good with words, pero look oh, I wrote something for u kasi ikaw na baga yan hahahaha (di ko rin 'to branding at personality). Well, kidding aside, I just want to let u know how proud am I to u. Lakas mo, boi. Isipin mo, u took that exam despite everything u've been through: the efforts, sacrifices, the doubts(?), even ur silent cries. Pero ang brave mo, di ka sumuko, and that's one thing I'm very proud of u. Sa part pa lang na di ka sumuko, panalo ka na, boi.
                    </p>

                    <p>
                        I remember ang lagi mong sinasabi na, "Kuruahon ta na ang lisensyang an ngunyan na taon ta nuarin pa an kuruahon." Hanep, di natin nakuha, boi. Someone sabotage as siguro, baka linipat na lagayan kaya dai ta nakua (korni talaga sya, kainis HAHAHAHAHAHAHA).
                    </p>

                    <p>
                        Pero u know what? This battle we faced wouldn't be bearable without u guys (u & Norelay), especially ikaw. Di ka ata aware na grabe impact mo sako. Like, sa mga panahon na wara akong tiwala sa sadiri ko, saro ka sa mga naniwala na kaya ko (kainis, bat ba ako naiiyaq hshshshs).
                    </p>

                    <p>
                        Kainis nga kasi, bat ba u know me so well? Like, bat gets mo ako sa lahat. Sabagay, senyasan lang nga pala, gets na agad natin each other hahahaha.
                    </p>

                    <p>
                        I can still remember na pinagalitan mo pa ako nung nakwento ko saimo su time na hinapot ako ni Sol kung papasa ako, kasi pinag-isipan ko pa isasagot ko, plus sinabi ko pa na hindi. Kasi sabi mo, dapat ang mindset ay papasa tayo. Actually, lahat na time na pinagsasabihan mo ako is naa-appreciate ko kasi I can feel how genuine ur intentions are. Like, gusto mo lang naman ang best para sa friend mo.
                    </p>

                    <p>
                        U know what? I always thank God kasi I got the chance to meet a person like u in this lifetime. So, thank u for existing. Dami kong natutunan sayo.
                    </p>

                    <p>
                        Thank u for patiently teaching me sa mga topics na hindi ko magets, kahit wala ka namang napapala pag ikaw na magpapaturo sakin kasi hindi ako marunong mag-explain. Minsan ka na lang nga magpaturo sakin, tapos I hurt u pa :(. Sorry, I didn't mean to make u feel that way, pero wala naman na magagawa ang sorry ko kasi nangyare na. Pero pls know na it wasn’t my intention to hurt u, and sa lahat na kasalanan ko sayo, gusto ko mag-ask ng forgiveness kasi dai mo deserve makulugan dahil sa mga kalokohan ko :)
                    </p>

                    <p>
                        Ano pa ba, may nalimutan pa ba ako? Wala naman na siguro 'no?
                    </p>

                    <p>
                        Basta, as long as nahinga pa ako, I always got ur back, bruh (sana pautangin mo pa rin me pag pumaldo ka na sa buhay). RGE 2027 TOPNOTCHERS na ites. Love u, pinsan ko (virtual hugs and kisses). See u soonest!
                    </p>

                    <p>
                        P.S. Muya mo champorado, ner?
                    </p>

                    <p>
                        P.P.S. I missed ur sinigang.
                    </p>

                    <div class="closing">
                        🖤 From your pinsan by heart
                    </div>

                </div>

            </div>

        </section>

    </div>


    <script>

        /* PASSWORD */

        const correctPassword = "072326";


        /* SHOW PASSWORD */

        function showPassword() {

            document.getElementById("openingScreen").style.display = "none";

            document.getElementById("passwordScreen").style.display = "flex";

            document.getElementById("passwordInput").focus();

        }


        /* ENTER KEY */

        function handleEnter(event) {

            if (event.key === "Enter") {

                checkPassword();

            }

        }


        /* CHECK PASSWORD */

        function checkPassword() {

            const input =
                document.getElementById("passwordInput");

            const error =
                document.getElementById("errorMessage");

            if (input.value === correctPassword) {

                document.getElementById("passwordScreen").style.display = "none";

                document.getElementById("letterSection").style.display = "block";

                window.scrollTo({
                    top: 0,
                    behavior: "smooth"
                });

            } else {

                error.style.display = "block";

                input.value = "";

                input.focus();

            }

        }

    </script>

</body>
</html>
