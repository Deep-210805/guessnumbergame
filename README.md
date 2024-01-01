<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Guess the number</title>
    <link rel="shortcut icon" href="man.png" type="image/x-icon">
    <link rel="stylesheet" href="work7.css">
</head>
<style>
.para{
    color:black;
    font-size: 25px;
    min-height: 10px;
}
.guess2{
    font-size: 30px;
    font-weight: 450px;
    margin-left: 90px;
}
#deep{font-size:50px;
    font-weight:450px;
    text-align: center;
    margin-top: 120px;
}
.guessSubmit{
    font-size: 20px;
    color: blue;
} .guessField{
    height: 23px;
    width: 80px;
    color: brown;
    font-size:20px;
    font-weight: 500px;
    }
      *{
        margin: 0%;
        padding: 0%;
    }
    .container{
        background-color: #8BC6EC;
        background-image: linear-gradient(135deg, #8BC6EC 0%, #9599E2 100%);
        border:#9599E2 4px;

        height:100%;
width:100%;
          }
          .heading{
            font-size: 65px;
            color: #c4c5c7;
          }
       .item{
        text-decoration: none;
        display: flex;
        justify-content: space-between;
        gap:38px;
        font-size: 28px;
        padding:30px;
       }
       .items{
        display: flex;
        justify-content: space-between;
       }
       .navigation{
        min-height: 6px;
        border:2px;
        border-style: ridge;
        border-radius: 2px;
        background-image: radial-gradient( circle farthest-corner at 10% 20%,  rgba(38,51,97,1) 0%, rgba(65,143,222,1) 79% );
        
       }
       .imggulab{
        transition: all 2s ease-in 0s;
        box-shadow: 0px 0px 15px black;
        border-radius: 13px;
        width: 190px;
        height:260px;
        margin:15px;
       }
       .imggulab:hover{
        transform: scale(1.1);
       }
       .imgbarfi{
        transition: all 2s ease-in 0s;
        box-shadow: 0px 0px 15px black;
        border-radius: 13px;
        width: 190px;
        height:260px;
        margin:15px;
       }
       .imgbarfi:hover{
        transform: scale(1.1);
       }
       .imggol{
        transition: all 2s ease-in 0s;
        box-shadow: 0px 0px 15px black;
        border-radius: 13px;
        width: 190px;
        height:260px;
        margin:15px;
       }
       .imggol:hover{
        transform: scale(1.1);
       }
       .box{
        width:70%;
        height: 82vh;
        margin:auto;
        display: flex;
        flex-direction: column;
        box-shadow: 0px 0px 30px black;
        align-items: center;
       }
       .main{
        display: flex;
       }
       .main1{
        display: flex;
       }
       .main2{
        display: flex;
       }
       .leftbox h1{
        font-size: 30px;
       }
       #footer p{
font-size: 25px;
background-image: radial-gradient( circle farthest-corner at 10% 20%,  rgba(38,51,97,1) 0%, rgba(65,143,222,1) 79% );
border: 1px;
margin:auto;
color: aliceblue;
text-align: center;
       }
</style>


<body>
    <div class="container">
        <nav class="navigation">
<ul class="items">
    <li><p class="heading">Deep Games</p></li>
    <li class="item">
        <div><a href="#">Home</a></div>
        <div><a href="tel:8708425219">Contact Us</a></div>
        <div><a href="#">About</a></div>
    </li>
</ul>
</nav>
<div class="box">
<div class="main">
<section class="leftbox">
    <div class="container">
        <h1 id="deep">Guess The Number</h1>
        <p class="para">
            We have selected a random number 
            between 1 - 10. See if you can
            guess it.
        </p>
 <br> <br> <br> 
        <div class="form">
            <label for="guessField" class="guess2">
                Enter a guess: 
            </label>
            
            <input type="text" id="guessField"
                class="guessField">
            
            <input type="submit" value="Submit guess"
                class="guessSubmit" id="submitguess">
        </div>
    </div>
</section></div>

</div>
<footer id="footer">
    <p> Copyright &#x24B8;Deepgames Pvt.Ltd 2023 All Rights Reserved </p>
</footer>
    </div>
    <script type="text/javascript">

		// Generate a Random Number
		let y = Math.floor(Math.random()*10+1 );

		// Counting the number of guesses
		// made for correct Guess
		let guess = 1;

		document.getElementById("submitguess").onclick = function () {

			// Number guessed by user 
			let x = document.getElementById("guessField").value;

			if (x == y) {
				alert("CONGRATULATIONS!!! YOU GUESSED IT RIGHT IN "
					+ guess + " GUESS ");
			}

			/* If guessed number is greater than actual number*/
			else if (x > y) {
				guess++;
				alert("OOPS SORRY!! TRY A SMALLER NUMBER");
			}
			else {
				guess++;
				alert("OOPS SORRY!! TRY A GREATER NUMBER")
			}
		}
	</script>
</body>
</html>
