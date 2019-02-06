<head>
        <meta charset="utf-8">
        <title>Click Oh Noes!</title>
    </head>
    <body style = "background-color:#32CD32">
    <!----Welcome to CLICK OH NOES! Just click oh noes! --->
    <img id = "balloon" onmousedown = "popped()" src = "https://www.kasandbox.org/programming-images/creatures/OhNoes.png" style = "position:absolute; width:100px; top:500px; left:500px">
    <p id = "scoreText" style = "color:yellow; font-size:20px; font-family:Arial;">Clicks: 0 </p>
    </body>
    <script>
    var score = 0, speed = 1;
    function setLeft(id,x){
        document.getElementById("id").style.left=x + "px";
        
    }
    function setTop(id,y){
        document.getElementById("id").style.top=y + "px";
        
    }
    function getLeft(id){
        return document.getElementById("id").offsetLeft;
    }
    function getTop(id){
        return document.getElementById("id").offsetTop;
    }
    function randomNumber(low,high){
        return (Math.floor(low + Math.random()*(1+high-low)))
    }
    var gameTimer =window.setInterval(floatUp,25);
    function flowUp(){
        var y = getTop("balloon");
        if(y<50){
            gameOver();
            
        }
        
        setTop("balloon",y-speed);
        
    }
    function popped(){
        score++;
        speed++;
        document.getElementById("scoreText").innerText = "Clicks:" +  score;
        setLeft("balloon",randomNumber(0,innerWidth-100));
        setTop("balloon",window.innerHeight);
        
        
    }
    function gameOver(){
        clearInterval(gameTimer);
        alert("Game over! You clicked:"+ score)
        location.reload();
        
        
    }
        
        
        
        
    </script>
