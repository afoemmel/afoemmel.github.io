<html>
<head>
    <title>
        Game
    </title>
    <script>
        var alerts = true;
        var aButtonText = 'on';
        function funButton() {
            var bigButton = document.getElementById("redButton");
            console.log(bigButton.style.backgroundColor);
            if (document.getElementById("redButton").style.backgroundColor === 'rgb(219, 0, 0)') {
                console.log("funButton");
                bigButton.style.backgroundColor='#89CFF0';
                if (alerts === true) {
                    alert("Hello");
                }
            }
            else {
                console.log("else");
                if (alerts === true) {
                    alert("Bye");
                }
                bigButton.style.backgroundColor='rgb(219,0,0)';
                console.log(bigButton.style.backgroundColor);
            }
        }
        function alertFun() {
            alerts = !alerts;
            if (alerts === true) {
                aButtonText = ":)";
            }
            else {
                aButtonText = ":(";
            }
            document.getElementById("alertButton").innerHTML = aButtonText;
        }
        window.onload = function(){  
            var bigButton = document.getElementById("redButton");
            console.log(bigButton);
            bigButton.style.backgroundColor = 'rgb(219, 0, 0)';
            console.log(bigButton.style.backgroundColor);
        }

    </script>
    <style>
        #redButton {
            height: 20vw;
            width: 20vw;
            padding-bottom: 20vw;
            border-radius: 50vw;
            border-width: 0.25vw;
            margin-top: 15vw;
            margin-bottom: 15vw;
            margin-left: 40vw;
        }
        body {
            height: 50vw;
        }
        .text {
            margin-top: 49vw;
        }
        #togAlerts {
            width: 5vw;
            font-family: "Tahoma", "Lucida Sans", "Times New Roman", "Gill Sans";
        }
        .text {
            margin-top: -5vw;
            font-family: "Tahoma", "Lucida Sans", "Times New Roman", "Gill Sans";
        }
    </style>
</head>
<body>
    <button id="redButton" type="button" onclick="funButton()">
    </button>
    <p class="text">Toggle Alerts</p>
    <button id="togAlerts" type="button" onclick="alertFun()">
        <p id="alertButton">:)</p>
    </button>
</body>
</html>
