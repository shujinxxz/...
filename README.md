<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>A Little Something For You 💌</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            min-height: 100vh;
            font-family: Georgia, "Times New Roman", serif;
            background: linear-gradient(135deg, #fff7f9, #f8dfe7, #e8b8c8);
            color: #4b3039;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 25px;
        }

        .container {
            width: 100%;
            max-width: 720px;
        }

        .password-box,
        .letter-box {
            background: rgba(255,255,255,0.96);
            border-radius: 25px;
            padding: 40px 30px;
            box-shadow: 0 15px 45px rgba(80,35,50,0.18);
        }

        .password-box {
            text-align: center;
        }

        .heart {
            font-size: 45px;
        }

        h1 {
            font-size: 30px;
        }

        .subtitle {
            color: #80606a;
            margin-bottom: 30px;
        }

        .clue {
            background: #fff1f5;
            border-radius: 15px;
            padding: 18px;
            margin: 20px 0;
        }

        input {
            width: 100%;
            max-width: 320px;
            padding: 14px 18px;
            border: 2px solid #e4b5c3;
            border-radius: 30px;
            font-size: 17px;
            text-align: center;
            outline: none;
        }

        button {
            margin-top: 15px;
            padding: 13px 28px;
            border: none;
            border-radius: 30px;
            background: #a95773;
            color: white;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background: #91445f;
        }

        #error {
            color: #b33b56;
            display: none;
        }

        .letter-box {
            display: none;
        }

        .letter-title {
            text-align: center;
            font-size: 30px;
            margin-bottom: 30px;
        }

        .letter {
            font-size: 18px;
            line-height: 1.9;
        }

        .letter p {
            margin-bottom: 22px;
        }

        .signature {
            margin-top: 35px;
            text-align: right;
            font-style: italic;
        }

        .music {
            margin: 30px 0;
            padding: 18px;
            background: #fff1f5;
            border-radius: 18px;
            text-align: center;
        }

        .music a {
            display: inline-block;
            text-decoration: none;
            background: #a95773;
            color: white;
            padding: 10px 20px;
            border-radius: 25px;
        }

        .small {
            font-size: 12px;
            color: #94717b;
            margin-top: 10px;
        }
    </style>
</head>

<body>

<div class="container">

    <!-- PASSWORD PAGE -->

    <div class="password-box" id="passwordScreen">

        <div class="heart">💌</div>

        <h1>A Little Something For You</h1>

        <p class="subtitle">
            Some words are meant for only one person.
        </p>

        <div class="clue">
            🔐 <strong>Clue</strong><br><br>
            the day I gave u a cake<br>
            <em>(mm/dd/yr)</em>
        </div>

        <input
            type="password"
            id="password"
            placeholder="Enter password"
        >

        <br>

        <button onclick="unlockLetter()">
            OPEN MY LETTER ♡
        </button>

        <p id="error">
            Hmm... that's not it. Try again. 💭
        </p>

    </div>


    <!-- LETTER PAGE -->

    <div class="letter-box" id="letterScreen">

        <div class="letter-title">
            To my fave hooman, my all-time fave i-ragebait, my taga-salo ng random thoughts ko, and shempre, my Engr. Micah Jezra, 🤍
        </div>

        <div class="music">

            <strong>🎵 Paalala — Twosday</strong>

            <br><br>

            <a
                href="https://open.spotify.com/search/Paalala%20Twosday"
                target="_blank"
                rel="noopener noreferrer"
            >
                🎧 Play the song
            </a>

            <div class="small">
                Play the song para damang-dama tas balik ka na lang here hahahaha. ♡
            </div>

        </div>


        <div class="letter">

            <p>
                I'm not good with words, but look, I wrote something
                for u kasi ikaw na baga yan HAHAHAHA.
            </p>

            <p>
                Well, kidding aside, I wrote this to let u know how
                proud I am of u for showing up, for taking that test
                despite everything you've been through, the efforts,
                sacrifices, and ur silent cries.
            </p>

            <p>
                We may not get the result that we wanted, but please
                know na u did great. U did ur best, so don't be too
                hard on yourself.
           
            <p>
               As long as nahinga pa ako, you'll always have someone who's proud of you.
        
        <div class="signature">
            bogs 🤍
        </div>

    </div>

</div>


<script>

    const correctPassword = "072326";

    function unlockLetter() {

        const enteredPassword =
            document.getElementById("password").value;

        const passwordScreen =
            document.getElementById("passwordScreen");

        const letterScreen =
            document.getElementById("letterScreen");

        const error =
            document.getElementById("error");

        if (enteredPassword === correctPassword) {

            passwordScreen.style.display = "none";
            letterScreen.style.display = "block";

            window.scrollTo({
                top: 0,
                behavior: "smooth"
            });

        } else {

            error.style.display = "block";

            document.getElementById("password").value = "";

        }
    }

</script>

</body>
</html>
