# calculator
I am Creat a landing page using HTML and JS
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>Calculate me! -A calculator made by me</title>
  <link href="style.css" rel="stylesheet" type="text/css" />
  <link href="utils.css" rel="stylesheet" type="text/css" />
</head>

<body>
  <h1 class="text-center">Welcome to calculate me !</h1>
  <div class="container flex flex-col items-center mx-auto m-w-20">
    <div class="row">
      <input class="input" type="text" />
      <div class="row">
        <button class="button">C</button>
        <button class="button">-</button>
        <button class="button">M+</button>
        <button class="button">M-</button>
      </div>
      <div class="row">
        <button class="button">7</button>
        <button class="button">8</button>
        <button class="button">9</button>
        <button class="button">*</button>
      </div>
      <div class="row">
        <button class="button">4</button>
        <button class="button">5</button>
        <button class="button">6</button>
        <button class="button">/</button>
      </div>
      <div class="row">
        <button class="button">1</button>
        <button class="button">2</button>
        <button class="button">3</button>
        <button class="button">+</button>
      </div>
      <div class="row">
        <button class="button">0</button>
        <button class="button">.</button>
        <button class="button">=</button>
        <button class="button">-</button>
      </div>
    </div>
    <script src="basic.js"></script>
</body>

</html>
  let screen = document.getElementById("screen");
let buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListerner('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }

        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }
    })
}
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@500&display=swap');
html ,body {
  height: 100%;
  width: 100%;
  font-family: 'Roboto',sans-serif;
  border: 5px solid #244624;
}
button{
  width: 66px;
  padding:20px;
  margin: 03px;
  border:2px solid black;
  border-radius: 11px;
  cursor:pointer;
  background-color: aquamarine;
  font-size: 23px;
}
.row{
  margin:8px 0;
}.row input{
  font-size:20px;
  margin:0;
  padding:10px 20px;
  border: 5px solid black;
  border-radius:5px;
}.calculator{
    display: inline;
    border-color: black;
    padding: 23px;
    border: radius 18px;;
}
  .text-center{
    text-align: center;
  }
  
  .bg-red{
    background : black ;
  }
  .mx-auto{
    margin:auto;
  }
  .flex{
    display:flex;
  }
  .flex-col{
    flex-direction: column;
  }
  .items-center{
    align-items: center;
  }
