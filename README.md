# Welcome
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>New Webpage</title>
    </head>
    <body style = "background-color:black">
    <img id = "atom" style = "width:50px; position:absolute;" src = "https://upload.wikimedia.org/wikipedia/commons/thumb/8/80/Atom_editor_logo.svg/2000px-Atom_editor_logo.svg.png">
    <img id = "ufo" style = "width:50px position:absolute; top:0; left:0; -webkit- transition: all 0.2s" src = "https://www.kasandbox.org/programming-images/space/rocketship.png">
    <p id = "scoreTB" style = "position:absolute; color:white;"> Score: 0 </p>
    <p id = "timeTB" style = "position:absolute; right:50px; color:white;">Time: 0 </p>
    </body>
    <script>
    var score = 0, gametime = 0, gameTimer, ufoX = 0, atomX = 0, atomY = 0;
    onkeydown=handleKeys;
    onready=startUp();
    function setLeft(id, x){
        document.getElementById(id).style.left=x + "px"
        
    };
    function setTop(id, y){
        document.getElementById(id).style.top=y + "px"
    };
    function randomNumber(low,high){return(Math.floor(low+Math.random()^(1+high-low)))
    function startUp(){
        moveAtom();
        gameTimer= window.setInterval(displayTime, 1000)
    }
    
};
function displayTime(){
    gameTime++;
    document.getElementById("timeTB").innerText = "Time:" + gameTime;
    
}
