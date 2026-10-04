```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>For My Fave Hooman, Micah 🖤</title>

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
            background:
                radial-gradient(
                    circle at top,
                    #1d1d1d 0%,
                    #090909 45%,
                    #000000 100%
                );
            color: #eeeeee;
            overflow-x: hidden;
        }

        /* =========================
           FLOATING HEARTS
        ========================= */

        .heart {
            position: fixed;
            bottom: -50px;
            font-size: 20px;
            color: #777777;
            opacity: 0.45;
            animation: floatUp linear infinite;
            pointer-events: none;
            z-index: 0;
        }

        @keyframes floatUp {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 0;
            }

            10% {
                opacity: 0.45;
            }

            100% {
                transform: translateY(-110vh) rotate(360deg);
                opacity: 0;
            }
        }

        /* =========================
           MAIN CONTAINER
        ========================= */

        .container {
            position: relative;
            z-index: 1;
            width: min(92%, 850px);
            margin: 40px auto;
        }

        /* =========================
           OPENING SCREEN
        ========================= */

        .opening {
            min-height: 90vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        .opening-card {
            background: rgba(20, 20, 20, 0.92);
            padding: 45px 30px;
            border-radius: 25px;
            border: 1px solid #333333;
            box-shadow:
                0 20px 60px rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(10px);
            animation: fadeIn 1.5s ease;
        }

        .opening-card h1 {
            font-size: clamp(28px, 6vw, 48px);
            margin-bottom: 15px;
            color: #ffffff;
            letter-spacing: 1px;
        }

        .opening-card p {
            font-size: 18px;
            line-height: 1.7;
            color: #d0d0d0;
        }

        .small-note {
            font-size: 14px !important;
            opacity: 0.55;
            margin-top: 25px;
        }

        /* =========================
           BUTTONS
        ========================= */

        button {
            border: none;
            cursor: pointer;
            font-family: inherit;
        }

        .open-button {
            margin-top: 25px;
            padding: 15px 30px;
            border-radius: 50px;
            background: #eeeeee;
            color: #111111;
            font-size: 17px;
            font-weight: bold;
            box-shadow:
                0 8px 25px rgba(255, 255, 255, 0.08);
            transition: 0.3s;
        }

        .open-button:hover {
            transform: translateY(-3px);
            background: #ffffff;
            box-shadow:
                0 10px 30px rgba(255, 255, 255, 0.15);
        }

        /* =========================
           PASSWORD SCREEN
        ========================= */

        #passwordScreen {
            display: none;
            min-height: 90vh;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        .password-card {
            background: rgba(20, 20, 20, 0.95);
            padding: 40px 30px;
            border-radius: 25px;
            border: 1px solid #333333;
            box-shadow:
                0 20px 60px rgba(0, 0, 0, 0.8);
            width: min(100%, 450px);
        }

        .password-card h2 {
            color: #ffffff;
            margin-top: 0;
        }

        .password-card p {
            color: #cfcfcf;
            line-height: 1.7;
        }

        .clue {
            font-size: 14px !important;
            color: #888888 !important;
            margin-top: 20px;
        }

        .password-input {
            width: 100%;
            padding: 14px 16px;
            margin-top: 20px;
            border: 1px solid #444444;
            border-radius: 12px;
            font-size: 16px;
            outline: none;
            text-align: center;
            background: #111111;
            color: #ffffff;
        }

        .password-input::placeholder {
            color: #777777;
        }

        .password-input:focus {
            border-color: #888888;
        }

        .unlock-button {
            margin-top: 15px;
            padding: 13px 28px;
            border-radius: 30px;
            background: #eeeeee;
            color: #111111;
            font-size: 16px;
            font-weight: bold;
            transition: 0.3s;
        }

        .unlock-button:hover {
            background: #ffffff;
            transform: translateY(-2px);
        }

        .error {
            color: #999999 !important;
            margin-top: 12px;
            display: none;
        }

        /* =========================
           LETTER
        ========================= */

        #letterSection {
            display: none;
            animation: fadeIn 1.5s ease;
        }

        .letter-card {
            background: rgba(15, 15, 15, 0.96);
            padding: clamp(25px, 5vw, 55px);
            border-radius: 25px;
            border: 1px solid #2d2d2d;
            box-shadow:
                0 20px 70px rgba(0, 0, 0, 0.8);
            margin: 40px auto;
        }

        .letter-title {
            text-align: center;
            color: #ffffff;
            font-size: clamp(25px, 5vw, 38px);
            margin-bottom: 35px;
            letter-spacing: 1px;
        }

        .letter {
            font-size: 17px;
            line-height: 1.9;
            color: #dddddd;
        }

        .letter p {
            margin-bottom: 24px;
        }

        .closing {
            text-align: center;
            font-size: 20px;
            color: #ffffff;
            margin-top: 35px;
        }

        /* =========================
           MUSIC PLAYER
        ========================= */

        .music-player {
            position: sticky;
            top: 15px;
            z-index: 10;
            background: rgba(20, 20, 20, 0.96);
            padding: 12px 18px;
            border-radius: 50px;
            border: 1px solid #333333;
            box-shadow:
                0 8px 30px rgba(0, 0, 0, 0.6);
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
            margin-bottom: 20px;
        }

        .music-player button {
            background: #eeeeee;
            color: #111111;
            padding: 9px 17px;
            border-radius: 30px;
            font-weight: bold;
            transition: 0.3s;
        }

        .music-player button:hover {
            background: #ffffff;
        }

        .music-player span {
            font-size: 14px;
            color: #bdbdbd;
        }

        /* =========================
           FADE ANIMATION
        ========================= */

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
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

            .container {
                width: 94%;
            }

            .opening-card {
                padding: 35px 22px;
            }

            .letter {
                font-size: 16px;
                line-height: 1.8;
            }

            .letter-card {
                padding: 25px 20px;
            }

            .music-player {
                flex-wrap: wrap;
            }
        }

    </style>
</head>


<body>

    <!-- =========================
         FLOATING HEARTS
    ========================= -->

    <div
        class="heart"
        style="left:5%; animation-duration:8s;"
    >
        ♡
    </div>

    <div
        class="heart"
        style="
            left:15%;
            animation-duration:11s;
            animation-delay:2s;
        "
    >
        ♥
    </div>

    <div
        class="heart"
        style="
            left:28%;
            animation-duration:9s;
            animation-delay:1s;
        "
    >
        ♡
    </div>

    <div
        class="heart"
        style="
            left:42%;
            animation-duration:12s;
            animation-delay:3s;
        "
    >
        ♥
    </div>

    <div
        class="heart"
        style="
            left:58%;
            animation-duration:10s;
            animation-delay:1s;
        "
    >
        ♡
    </div>

    <div
        class="heart"
        style="
            left:72%;
            animation-duration:13s;
        "
    >
        ♥
    </div>

    <div
        class="heart"
        style="
            left:88%;
            animation-duration:9s;
            animation-delay:2s;
        "
    >
        ♡
    </div>


    <div class="container">


        <!-- =========================
             OPENING SCREEN
        ========================= -->

        <section
            class="opening"
            id="openingScreen"
        >

            <div class="opening-card">

                <h1>
                    For My Fave Hooman 🖤
                </h1>

                <p>
                    My all-time fave i-ragebait,<br>
                    my taga-salo ng random thoughts ko,<br>
                    my pinsan by heart,<br>
                    and shempre, my Engr. Micah Jezra.
                </p>

                <p>
                    I made something for you.
                </p>

                <button
                    class="open-button"
                    onclick="showPassword()"
                >
                    Open this for me 🖤
                </button>

                <p class="small-note">
                    This little message is meant especially for you.
                </p>

            </div>

        </section>


        <!-- =========================
             PASSWORD SCREEN
        ========================= -->

        <section
            id="passwordScreen"
        >

            <div class="password-card">

                <h2>
                    🔐 A little secret...
                </h2>

                <p>
                    Before you read this,<br>
                    you need to know the password. 🖤
                </p>

                <p class="clue">
                    Clue: the day i gave u a cake (mm/dd/yy)
                </p>

                <input
                    type="password"
                    id="passwordInput"
                    class="password-input"
                    placeholder="Enter the password"
                    onkeydown="
                        if(event.key === 'Enter')
                        checkPassword()
                    "
                >

                <br>

                <button
                    class="unlock-button"
                    onclick="checkPassword()"
                >
                    Unlock 🖤
                </button>

                <p
                    id="errorMessage"
                    class="error"
                >
                    Nope. Try again, boi. 😂
                </p>

            </div>

        </section>


        <!-- =========================
             LETTER
        ========================= -->

        <section
            id="letterSection"
        >


            <!-- MUSIC PLAYER -->

            <div class="music-player">

                <button
                    onclick="toggleMusic()"
                    id="musicButton"
                >
                    ▶ Play Paalala
                </button>

                <span id="musicStatus">
                    Paalala by twosday 🎵
                </span>

            </div>


            <!-- LETTER CARD -->

            <div class="letter-card">

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


    <!-- =========================
         MUSIC
    ========================= -->

    <!--
        Put your legally obtained audio file
        in the SAME FOLDER as this HTML file.

        File name:

        paalala.mp3
    -->

    <audio
        id="backgroundMusic"
        loop
    >

        <source
            src="paalala.mp3"
            type="audio/mpeg"
        >

    </audio>


    <script>

        /* =========================
           PASSWORD
        ========================= */

        const correctPassword = "072326";


        /* =========================
           SHOW PASSWORD SCREEN
        ========================= */

        function showPassword() {

            document.getElementById(
                "openingScreen"
            ).style.display = "none";

            document.getElementById(
                "passwordScreen"
            ).style.display = "flex";

        }


        /* =========================
           CHECK PASSWORD
        ========================= */

        function checkPassword() {

            const enteredPassword =
                document.getElementById(
                    "passwordInput"
                ).value;

            const errorMessage =
                document.getElementById(
                    "errorMessage"
                );


            if (
                enteredPassword ===
                correctPassword
            ) {

                document.getElementById(
                    "passwordScreen"
                ).style.display = "none";

                document.getElementById(
                    "letterSection"
                ).style.display = "block";

                startMusic();

                window.scrollTo({
                    top: 0,
                    behavior: "smooth"
                });

            }

            else {

                errorMessage.style.display =
                    "block";

                document.getElementById(
                    "passwordInput"
                ).value = "";

            }

        }


        /* =========================
           MUSIC
        ========================= */

        const music =
            document.getElementById(
                "backgroundMusic"
            );

        const musicButton =
            document.getElementById(
                "musicButton"
            );

        const musicStatus =
            document.getElementById(
                "musicStatus"
            );


        function startMusic() {

            music.play()

                .then(() => {

                    musicButton.innerHTML =
                        "⏸ Pause Paalala";

                    musicStatus.innerHTML =
                        "Now playing: Paalala by twosday 🎵";

                })

                .catch(() => {

                    musicStatus.innerHTML =
                        "Tap Play Paalala to start 🎵";

                });

        }


        function toggleMusic() {

            if (music.paused) {

                music.play();

                musicButton.innerHTML =
                    "⏸ Pause Paalala";

                musicStatus.innerHTML =
                    "Now playing: Paalala by twosday 🎵";

            }

            else {

                music.pause();

                musicButton.innerHTML =
                    "▶ Play Paalala";

                musicStatus.innerHTML =
                    "Music paused";

            }

        }

    </script>

</body>
</html>
```
