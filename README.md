<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Home - GaryNYZ.me</title>
        <link rel="shortcut icon" href="logo.png" type="image/x-icon" />
        <style>
            * {
                margin: 0;
                padding: 0;
            }
            body{
                font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
            }
            .head > h1 > span {
                transform: translate(1rem, -4rem);
                display: inline-flex;
            }
            .head {
                display: flex;
                margin: 10px auto;
                width: fit-content;
            }
            .head > h1 > *[alt="Logo"] {
                outline: 1px solid rgb(212, 212, 212);
            }
            .navbar{
                list-style: none;
                display: inline-flex;
                padding: 5px;
            }
            .navbar > li:not(:last-of-type){
                margin-right: 10px;
            }
            .content{
                display: flex;
                margin: 10px;
            }
            .footer{
                position: fixed;
                left: 0;
                bottom: 0;
                padding: 15px;
                width: 100%;
                text-align: center;
            }
        </style>
    </head>
    <body>
        <div class="head">
            <h1>
                <img src="logo.png" alt="Logo" width="150px" /><span
                    >Welcome Home</span
                ><br>
                <ul class="navbar">
                    <li><a href="#1">Home</a></li>
                    <li><a href="#2">About me</a></li>
                    <li><a href="#3">Blog</a></li>
                    <li><a href="#4">Specs / Hardware</a></li>
                </ul>
            </h1>
        </div>
        <div class="content"></div>
        <div class="footer">
            <span class="copyright">&copy; GaryNYZ - 2024</span><br>
            <span>Data used to load everything: <span id="size"></span></span>
        </div>
    </body>
    <script>
        // tells you how much data was used in this shit
        // credit: https://stackoverflow.com/a/23866862
        function getPageLoadTime() {
            var request = new XMLHttpRequest();
            request.open("GET", document.location, false);
            request.send();
            var size = request
                .getAllResponseHeaders()
                .toLowerCase()
                .match(/\d+/);
            document.getElementById("size").innerHTML = size + " bytes";
        }
        getPageLoadTime();
    </script>
</html>
