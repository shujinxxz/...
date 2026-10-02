<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>For You, Micah 🤍</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            padding: 0;
            font-family: Arial, Helvetica, sans-serif;
            background: linear-gradient(135deg, #fff5f7, #ffe8ee);
            color: #4a3038;
            min-height: 100vh;
        }

        .container {
            width: 100%;
            max-width: 700px;
            margin: 0 auto;
            padding: 30px 20px 50px;
        }

        /* PASSWORD SCREEN */

        .password-screen {
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        .password-box {
            width: 100%;
            max-width: 450px;
            background: rgba(255, 255, 255, 0.95);
            padding: 40px 30px;
            border-radius: 25px;
            box-shadow: 0 15px 40px rgba(80, 35, 50, 0.15);
        }

        .password-box h1 {
            margin-top: 0;
            font-size: 30px;
            color: #a84d68;
        }

        .password-box p {
            line-height: 1.7;
            font-size: 15px;
        }

        .clue {
            margin-top: 20px;
            padding: 15px;
            background: #fff0f4;
            border-radius: 15px;
            font-size: 14px;
            color: #7a4b59;
        }

        .password-input {
            width: 100%;
            padding: 14px;
            margin-top: 20px;
            border: 1px solid #e5b8c5;
            border-radius: 12px;
            font-size: 16px;
            text-align: center;
            outline: none;
        }

        .password-input:focus {
            border-color: #c66b87;
        }

        .unlock-button {
            width: 100%;
            padding: 14px;
            margin-top: 15px;
            border: none;
            border-radius: 12px;
            background: #b85c78;
            color: white;
            font-size: 16px;
            cursor: pointer;
            transition: 0.3s;
        }

        .unlock-button:hover {
            background: #9f4965;
        }

        .error {
            color: #c0395c;
            margin-top: 15px;
            display: none;
            font-size: 14px;
        }

        /* LETTER SCREEN */

        .letter-screen {
            display: none;
        }

        .letter-card {
            background: rgba(255, 255, 255, 0.96);
            padding: 35px 30px;
            border-radius: 25px;
            box-shadow: 0 15px 40px rgba(80, 35, 50, 0.15);
        }

        .letter-title {
            text-align: center;
            font-size: 30px;
            font-weight: bold;
            color: #a84d68;
            margin-bottom: 25px;
        }

        /* PHOTO */

        .photo-container {
            text-align: center;
            margin: 25px 0 30px;
        }

        .photo-container img {
            width: 100%;
            max-width: 450px;
            height: auto;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(80, 35, 50, 0.18);
        }

        /* LETTER */

        .letter-content {
            font-size: 16px;
            line-height: 1.9;
            color: #4a3038;
        }

        .letter-content p {
            margin-bottom: 22px;
        }

        .greeting {
            font-weight: bold;
        }

        .signature {
            margin-top: 35px;
            text-align: right;
            font-style: italic;
            color: #9b526b;
            font-size: 17px;
        }

        /* MUSIC */

        .music-box {
            margin-top: 35px;
            padding: 20px;
            background: #fff0f4;
            border-radius: 18px;
            text-align: center;
        }

        .music-box h3 {
            margin-top: 0;
            color: #a84d68;
        }

        .music-box p {
            font-size: 14px;
            margin-bottom: 15px;
        }

        .music-button {
            display: inline-block;
            padding: 12px 20px;
            background: #b85c78;
            color: white;
            text-decoration: none;
            border-radius: 12px;
            transition: 0.3s;
        }

        .music-button:hover {
            background: #9f4965;
        }

        .footer {
            text-align: center;
            margin-top: 30px;
            font-size: 13px;
            color: #9a7882;
        }

        /* MOBILE */

        @media (max-width: 600px) {

            .container {
                padding: 20px 15px 40px;
            }

            .password-box {
                padding: 30px 20px;
            }

            .letter-card {
                padding: 25px 20px;
            }

            .letter-title {
                font-size: 26px;
            }

            .letter-content {
                font-size: 15px;
            }
        }
    </style>
</head>

<body>

    <!-- PASSWORD SCREEN -->

    <div class="password-screen" id="passwordScreen">

        <div class="container">

            <div class="password-box">

                <h1>For You, Micah 🤍</h1>

                <p>
                    There's something here that I wanted you to read.
                    But first... you need to know the password. 👀
                </p>

                <div class="clue">
                    <strong>Clue:</strong><br>
                    "the day i gave u a cake"<br>
                    <small>(mm/dd/yr)</small>
                </div>

                <input
                    type="password"
                    id="passwordInput"
                    class="password-input"
                    placeholder="Enter password"
                    onkeypress="checkEnter(event)"
                >

                <button
                    class="unlock-button"
                    onclick="unlockLetter()"
                >
                    Open the letter 💌
                </button>

                <div class="error" id="errorMessage">
                    Hmm... that's not the password. Try again. 🤭
                </div>

            </div>

        </div>

    </div>


    <!-- LETTER SCREEN -->

    <div class="letter-screen" id="letterScreen">

        <div class="container">

            <div class="letter-card">

                <div class="letter-title">
                    For You, Micah 🤍
                </div>


                <!-- PHOTO -->

                <div class="photo-container">

                    <img
                        src="micah-photo.jpg"
                        alt="A special photo"
                    >

                </div>


                <!-- LETTER -->

                <div class="letter-content">

                    <p class="greeting">
                        To my fave hooman, my all time fave iragebait,
                        my taga salo ng random thoughts ko,
                        and shempre my engr. micah jezra,
                    </p>

                    <p>
                        im not good with words but look oh i wrote something
                        for u kasi ikaw na baga yan hahahaha
                    </p>

                    <p>
                        well kidding aside i wrote this to let u know how
                        proud am i to u for showing up for taking that test
                        despite everything u've been through the efforts,
                        sacrifices, ur silent cries.
                    </p>

                    <p>
                        we may not get the result that we wanted but please
                        know na u did great u did ur best so dont be to hard
                        on yourself.
                    </p>

                </div>


                <!-- SIGNATURE -->

                <div class="signature">
                    Always rooting for you. 🤍
                </div>


                <!-- MUSIC -->

                <div class="music-box">

                    <h3>🎵 A little something to listen to</h3>

                    <p>
                        Play this while reading the letter. 🤍
                    </p>

                    <a
                        class="music-button"
                        href="https://open.spotify.com/search/Paalala%20Twosday"
                        target="_blank"
                        rel="noopener noreferrer"
                    >
                        🎧 Play "Paalala" by Twosday
                    </a>

                </div>


                <div class="footer">
                    Made with a little bit of courage and a lot of thought. 🤍
                </div>

            </div>

        </div>

    </div>


    <!-- JAVASCRIPT -->

    <script>

        function unlockLetter() {

            const password =
                document.getElementById("passwordInput").value;

            const correctPassword = "072326";

            const passwordScreen =
                document.getElementById("passwordScreen");

            const letterScreen =
                document.getElementById("letterScreen");

            const errorMessage =
                document.getElementById("errorMessage");


            if (password === correctPassword) {

                passwordScreen.style.display = "none";

                letterScreen.style.display = "block";

                window.scrollTo(0, 0);

            } else {

                errorMessage.style.display = "block";

            }

        }


        function checkEnter(event) {

            if (event.key === "Enter") {

                unlockLetter();

            }

        }

    </script>

</body>
</html>
