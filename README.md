# Ic4d-designer.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aku Rindu Kau</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin: 50px; }
        h1 { font-size: 30px; }
        .hidden { display: none; }
        button { padding: 10px 20px; margin: 10px; font-size: 16px; cursor: pointer; }
        #idgf { background-color: red; color: white; }
        #next { background-color: blue; color: white; }
        #no { position: absolute; transition: 0.3s; }
    </style>
</head>
<body>

    <!-- Page 1 -->
    <div id="page1">
        <h1>Aku Rindu Kau 🫂</h1>
        <button id="next" onclick="goToPage2()">Next</button>
        <button id="idgf" onclick="idgfClick()">IDGF</button>
    </div>

    <!-- Page 2 -->
    <div id="page2" class="hidden">
        <h1>Boleh tak nak call? ❤️</h1>
        <button onclick="goToPage3()">Yes</button>
        <button id="no" onclick="moveNoButton()">No</button>
    </div>

    <!-- Page 3 -->
    <div id="page3" class="hidden">
        <h1 style="color: red;">AKU SAYANG KAU LAGIIIIII</h1>
        <h2>Jangan end relay setahun kita pleaseee</h2>
    </div>

    <script>
        let nextButtonSize = 16;

        function idgfClick() {
            let nextButton = document.getElementById("next");
            nextButtonSize += 5;
            nextButton.style.fontSize = nextButtonSize + "px";
        }

        function goToPage2() {
            document.getElementById("page1").classList.add("hidden");
            document.getElementById("page2").classList.remove("hidden");
        }

        function goToPage3() {
            document.getElementById("page2").classList.add("hidden");
            document.getElementById("page3").classList.remove("hidden");
        }

        function moveNoButton() {
            let button = document.getElementById("no");
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            button.style.left = x + "px";
            button.style.top = y + "px";
        }
    </script>

</body>
</html>
