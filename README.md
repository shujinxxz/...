<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>uy engineer yohoo!</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background: #000;
            color: #fff;
            font-family: Georgia, "Times New Roman", serif;
            min-height: 100vh;
            overflow-x: hidden;
        }

        /* =========================
           FLOATING HEARTS
        ========================= */

        .heart {
            position: fixed;
            bottom: -30px;
            color: rgba(255, 255, 255, 0.15);
            font-size: 20px;
            animation: floatHeart linear infinite;
            pointer-events: none;
            z-index: 0;
        }

        .heart:nth-child(1) {
            left: 5%;
            animation-duration: 12s;
            animation-delay: 0s;
        }

        .heart:nth-child(2) {
            left: 15%;
            animation-duration: 15s;
            animation-delay: 3s;
        }

        .heart:nth-child(3) {
            left: 28%;
            animation-duration: 11s;
            animation-delay: 2s;
        }

        .heart:nth-child(4) {
            left: 42%;
            animation-duration: 16s;
            animation-delay: 5s;
        }

        .heart:nth-child(5) {
            left: 58%;
            animation-duration: 13s;
            animation-delay: 1s;
        }

        .heart:nth-child(6) {
            left: 70%;
            animation-duration: 17s;
            animation-delay: 4s;
        }

        .heart:nth-child(7) {
            left: 82%;
            animation-duration: 12s;
            animation-delay: 2s;
        }

        .heart:nth-child(8) {
            left: 93%;
            animation-duration: 15s;
            animation-delay: 6s;
        }

        @keyframes floatHeart {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 0;
            }

            10% {
                opacity: 1;
            }

            90% {
                opacity: 1;
            }

            100% {
                transform: translateY(-110vh) rotate(360deg);
                opacity: 0;
            }
        }

        /* =========================
           OPENING SCREEN
        ========================= */

        #openingScreen {
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 25px;
            position: relative;
            z-index: 1;
        }

        .card {
            width: 100%;
            max-width: 600px;
            text-align: center;
            padding: 50px 30px;
            border: 1px solid rgba(255, 255, 255, 0.15);
            border-radius: 25px;
            background: rgba(255, 255, 255, 0.04);
            backdrop-filter: blur(10px);
            box-shadow: 0 0 40px rgba(255, 255, 255, 0.04);
        }

        .opening-title {
            font-size: clamp(2rem, 6vw, 4rem);
            margin-bottom: 15px;
            letter-spacing: 1px;
        }

        .opening-text {
            font-size: 1.2rem;
            color: #ccc;
            margin-bottom: 35px;
        }

        /* =========================
           BUTTON
        ========================= */

        .main-button {
            border: none;
            outline: none;
            background: #fff;
            color: #000;
            padding: 14px 28px;
            border-radius: 30px;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .main-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(255, 255, 255, 0.2);
        }

        .main-button:active {
            transform: scale(0.97);
        }

        /* =========================
           PASSWORD SCREEN
        ========================= */

        #passwordScreen {
            min-height: 100vh;
            display: none;
            justify-content: center;
            align-items: center;
            padding: 25px;
            position: relative;
            z-index: 1;
        }

        .password-card {
            width: 100%;
            max-width: 500px;
            text-align: center;
            padding: 45px 30px;
            border: 1px solid rgba(255, 255, 255, 0.15);
            border-radius: 25px;
            background: rgba(255, 255, 255, 0.04);
            backdrop-filter: blur(10px);
        }

        .password-card h1 {
            font-size: 2rem;
            margin-bottom: 15px;
        }

        .password-card > p {
            color: #ccc;
            margin-bottom: 15px;
            line-height: 1.6;
        }

        .clue {
            font-size: 0.9rem;
            font-style: italic;
            color: #aaa !important;
            margin-top: 20px;
            margin-bottom: 20px !important;
        }

        #passwordInput {
            width: 100%;
            padding: 14px 18px;
            margin-bottom: 15px;
            border-radius: 25px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            background: rgba(255, 255, 255, 0.08);
            color: #fff;
            font-size: 1rem;
            text-align: center;
            outline: none;
        }

        #passwordInput::placeholder {
            color: #888;
        }

        #passwordInput:focus {
            border-color: rgba(255, 255, 255, 0.6);
        }

        #errorMessage {
            display: none;
            color: #ff8c8c !important;
            font-size: 0.9rem;
            margin-top: 15px;
        }

        /* =========================
           LETTER SECTION
        ========================= */

        #letterSection {
            display: none;
            min-height: 100vh;
            padding: 30px 20px 70px;
            position: relative;
            z-index: 1;
        }

        .letter-container {
            width: 100%;
            max-width: 850px;
            margin: 0 auto;
        }

        /* =========================
           MUSIC PLAYER
        ========================= */

        .music-player {
            text-align: center;
            margin-bottom: 25px;
            padding: 20px;
            border-radius: 18px;
            background: rgba(255, 255, 255, 0.04);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .spotify-button {
            display: inline-block;
            text-decoration: none;
            background: #fff;
            color: #000;
            padding: 12px 22px;
            border-radius: 25px;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        .spotify-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 7px 20px rgba(255, 255, 255, 0.15);
        }

        #musicStatus {
            display: block;
            color: #aaa;
            font-size: 0.85rem;
            margin-top: 10px;
        }

        .music-note {
            margin-top: 12px;
            color: #777;
            font-size: 0.85rem;
            font-style: italic;
        }

        /* =========================
           LETTER
        ========================= */

        .letter-card {
            background: #f5f5f5;
            color: #111;
            border-radius: 18px;
            padding: 55px 60px;
            box-shadow: 0 15px 50px rgba(0, 0, 0, 0.5);
            line-height: 1.8;
        }

        .letter-card p {
            margin-bottom: 22px;
            font-size: 1rem;
        }

        .letter-card p:first-child {
            margin-bottom: 30px;
        }

        /* =========================
           SIGNATURE
        ========================= */

        .signature {
            margin-top: 35px;
            margin-bottom: 0 !important;
            font-family: Georgia, "Times New Roman", serif;
            font-size: 1rem !important;
            font-style: italic;
            text-align: right;
        }

        /* =========================
           FADE ANIMATION
        ========================= */

        .fade {
            animation: fadeIn 1.2s ease forwards;
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

        /* =========================
           MOBILE
        ========================= */

        @media (max-width: 600px) {

            #openingScreen,
            #passwordScreen {
                padding: 18px;
            }

            .card,
            .password-card {
                padding: 40px 22px;
                border-radius: 20px;
            }

            .opening-title {
                font-size: 2.2rem;
            }

            .opening-text {
                font-size: 1rem;
            }

            .password-card h1 {
                font-size: 1.6rem;
            }

            #letterSection {
                padding: 20px 12px 50px;
            }

            .letter-card {
                padding: 35px 24px;
                border-radius: 14px;
            }

            .letter-card p {
                font-size: 0.95rem;
                line-height: 1.75;
            }

            .spotify-button {
                width: 100%;
                padding: 13px 15px;
            }

            .music-note {
                font-size: 0.8rem;
            }

            .signature {
                font-size: 0.95rem !important;
            }
        }
    </style>
</head>

<body>

    <!-- FLOATING HEARTS -->

    <div class="heart">🖤</div>
    <div class="heart">♡</div>
    <div class="heart">🖤</div>
    <div class="heart">♡</div>
    <div class="heart">🖤</div>
    <div class="heart">♡</div>
    <div class="heart">🖤</div>
    <div class="heart">♡</div>


    <!-- =========================
         OPENING SCREEN
    ========================== -->

    <section id="openingScreen">

        <div class="card fade">

            <h1 class="opening-title">
                uy engineer yohoo!
            </h1>

            <p class="opening-text">
                check this out
            </p>

            <button
                class="main-button"
                onclick="showPassword()"
            >
                palag na boi
            </button>

        </div>

    </section>


    <!-- =========================
         PASSWORD SCREEN
    ========================== -->

    <section id="passwordScreen">

        <div class="password-card fade">

            <h1>
                papansin may password pa 'no?
            </h1>

            <p>
                naaalala mo pa man siguro, 'no?
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
                Unlock 
            </button>

            <p id="errorMessage">
                saro pa boi
            </p>

        </div>

    </section>


    <!-- =========================
         LETTER SECTION
    ========================== -->

    <section id="letterSection">

        <div class="letter-container">

            <!-- MUSIC -->

            <div class="music-player fade">

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

                <p class="music-note">
                    play the song para damang-dama :)
                </p>

            </div>


            <!-- LETTER -->

            <div class="letter-card fade">

                <p>
                    To my fave human, my all-time fave i-ragebait, my taga-salo ng random thoughts ko, my pinsan by heart, and shempre, my Engr. Micah Jezra,
                </p>

                <p>
                    I'm not good with words, pero look oh, I wrote something for u kasi ikaw na baga yan hahahaha (di ko rin 'to branding at personality). Well, kidding aside, I just want to let u know how proud am I to u. Lakas mo, boi. Isipin mo, u took that exam despite everything u've been through: the efforts, sacrifices, the doubts(?), even ur silent cries. Pero ang brave mo, di ka sumuko, and that's one thing I'm very proud of u. We may not get the result that we wanted, but sa part pa lang na di ka sumuko, panalo ka na, boi.
                </p>

                <p>
                    I remember ang lagi mong sinasabi na, "Kuruahon ta na ang lisensyang an ngunyan na taon ta nuarin pa an kuruahon." Hanep, di natin nakuha, boi. Someone sabotage as siguro, baka linipat na lagayan kaya dai ta nakua (korni talaga sya, kainis HAHAHAHAHAHAHA).
                </p>

                <p>
                    Pero u know what? This battle we faced wouldn't be bearable without u guys (u &amp; Norelay), especially ikaw. Di ka ata aware na grabe impact mo sako. Like, sa mga panahon na wara akong tiwala sa sadiri ko, saro ka sa mga naniwala na kaya ko (kainis, bat ba ako naiiyaq hshshshs).
                </p>

                <p>
                    Ang gaan din ng feeling ko saimo. Like, I don't need magpanggap sayo kasi I'm comfortable na makita mo vulnerable side ko (siguro bff kita sa past life hahahahaha eme).Kainis nga kasi, bat ba u know me so well? Like, bat gets mo ako sa lahat. Sabagay, arog baga kita kaini 🤞🏻, senyasan lang nga pala, gets na agad natin each other kasi connected baga kita hahahaha.
                </p>

                <p>
                    I can still remember na pinagalitan mo pa ako nung nakwento ko saimo su time na hinapot ako ni Sol kung papasa ako, kasi pinag-isipan ko pa isasagot ko, plus sinabi ko pa na hindi. Kasi sabi mo, dapat ang mindset ay papasa tayo. Actually, lahat na time na pinagsasabihan mo ako is naa-appreciate ko kasi I can feel how genuine ur intentions are. Like, gusto mo lang naman ang best para sa friend mo.
                </p>

                <p>
                    U know what? I always thank God kasi I got the chance to meet a person like u in this lifetime. So, thank u for existing. Dami kong natutunan sayo.
                </p>

                <p>
                    Thank u for patiently teaching me sa mga topics na hindi ko magets, kahit wala ka namang napapala pag ikaw na magpapaturo sakin kasi hindi ako marunong mag-explain. Minsan ka na lang nga magpaturo sakin, tapos I hurt u pa :(. Sorry, I didn't mean to make u feel that way, pero wala naman na magagawa ang sorry ko kasi nangyare na. Pero pls know na it wasn’t my intention to hurt u, and sa lahat na kasalanan ko sayo, gusto ko mag-ask ng forgiveness kasi dai mo deserve makulugan dahil sa mga kalokohan ko :) I won't make u cry na kasi baka isumbong mo na naman ako kay Lord.
                </p>

                <p>
                    Ano pa ba, may nalimutan pa ba ako? Wala naman na siguro 'no?
                </p>

                <p>
                    Basta, as long as nahinga pa ako, I always got ur back, bruh. I'm here lang lagi, kaya don't hesitate to call/message me kahit saan (lalo na if need mo taga-sira ng araw mo hahahahhaha). On a serious note (wow serious note), if u need me man nanggad, just call/message me kasi I'll do everything man to help u. Kung need ko akyatin mga bundok or tumawid pa ako sa dagat (ay hanep, di imposible kay baka nasa isla ka), gagawin ko just to help u (oh panis hshshshs). Sana pautangin mo pa rin me pag pumaldo ka na sa bohai hshshshshs (fr fr istg).
                </p>

                <p>
                    Pahuway na muna muna, ner. RGE 2027 TOPNOTCHER na ites. Love u, pinsan ko (sending u virtual hugs and kisses). See u soonest!
                </p>
                
                <p>
                    P.S. Muya mo champorado, ner? (random midnight anes)
                </p>

                <p>
                    P.P.S. I missed ur sinigang.
                </p>

                <p class="signature">
                    bogs :)
                </p>

            </div>

        </div>

    </section>


    <!-- =========================
         JAVASCRIPT
    ========================== -->

    <script>

        const correctPassword = "072326";


        function showPassword() {

            document.getElementById("openingScreen").style.display = "none";

            document.getElementById("passwordScreen").style.display = "flex";

            document.getElementById("passwordInput").focus();

        }


        function handleEnter(event) {

            if (event.key === "Enter") {

                checkPassword();

            }

        }


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
