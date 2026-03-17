<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Interactive Reveal What's That Animal UI</title>
        <style>
            .container { border: 2px solid #ff8000; padding: auto; max-width: 1500px; max-height: 1500px; margin: auto; }
            .container2 { border: 2px solid #ff8000; padding: auto; height: 50px; width: 250px; margin: auto; }
            .animalbtn { border: 2px solid #ff8000; padding: 10px; max-width: 150px; margin: auto; background-color: white; }
            .hideBtn { background-color: #5a69dc; color: white; padding: auto; margin: auto; width: 285px; }
            .imageContainer {border: 2px solid #ff8000; padding: auto; margin-right: auto; max-height: 300px; max-width: 300px; display: inline-block; position: relative; display: none;}
            p {border: 2px solid #ff8000; padding-top: auto; height: 50px; margin: auto; text-align: center; font-size: x-large; }
            button:hover {background-color: rgba(32, 117, 192, 0.582); }
        </style>
    </head>
    <body>
        <div class="container">
            <p>Welcome to the Interactive Reveal What's that Animal UI</p>
            <br>
            <p>Click on the buttons below to reveal the animal images</p>
            <br>
           
            <section class="imageContainer">
                <img src="dog.jpg" alt="Picture of a small dog" height="250px" width="300px">
                <button class="hideBtn">Hide Reveal</button>
            </section>            

            <section class="imageContainer">
                <img src="tabby-cat.jpg" alt="Picture of a tabby cat" height="250px" width="300px">
                <button class="hideBtn">Hide Reveal</button>
            </section>

            <section class="imageContainer">
                <img src="cow.jpg" alt="Picture of a cow" height="250px" width="300px">
                <button class="hideBtn">Hide Reveal</button>
            </section>
            <br>
            <button class="animalbtn">Reveal a DOG</button>
            <button class="animalbtn">Reveal a CAT</button>
            <button class="animalbtn">Reveal a COW</button>

        
    </div>

    <span>
        <button class="animalbtn">Reset Zoo</button>
        <p class="container2">Number of Animals: </p>
    </span>
    
    
    <script>
            let numberAnimals = 0;
            const btn1 = document.querySelectorAll('.animalbtn')[0];
            const btn2 = document.querySelectorAll('.animalbtn')[1];
            const btn3 = document.querySelectorAll('.animalbtn')[2];
            const btn7 = document.querySelectorAll('.animalbtn')[3];
            const btn4 = document.querySelectorAll('.hideBtn')[0];
            const btn5 = document.querySelectorAll('.hideBtn')[1];
            const btn6 = document.querySelectorAll('.hideBtn')[2];
            const hidden1 = document.querySelectorAll('.imageContainer')[0];
            const hidden2 = document.querySelectorAll('.imageContainer')[1];
            const hidden3 = document.querySelectorAll('.imageContainer')[2];
            const count = document.querySelector('.container2')
            count.textContent += `${numberAnimals}`;

            btn1.addEventListener('click', function() {
                hidden1.style.display = "inline-block";
                btn1.style.backgroundColor = "#75df13";
                btn1.style.borderRadius = "5px";
                numberAnimals += 1;
                count.textContent = `Number of Animals: ${numberAnimals}`;
            });

            btn2.addEventListener('click', function() {
                hidden2.style.display = "inline-block";
                btn2.style.backgroundColor = "#75df13";
                btn2.style.borderRadius = "5px";
                numberAnimals += 1;
                count.textContent = `Number of Animals: ${numberAnimals}`;
            });

            btn3.addEventListener('click', function() {
                hidden3.style.display = "inline-block";
                btn3.style.backgroundColor = "#75df13";
                btn3.style.borderRadius = "5px";
                numberAnimals += 1;
                count.textContent = `Number of Animals: ${numberAnimals}`;
            });

            btn4.addEventListener('click', function() {
                hidden1.style.display = "none";
                btn1.style.backgroundColor = "#ffffff";
                btn1.style.borderRadius = "0px";
                numberAnimals -= 1;
                count.textContent = `Number of Animals: ${numberAnimals}`;
            });

            btn5.addEventListener('click', function() {
                hidden2.style.display = "none";
                btn2.style.backgroundColor = "#ffffff";
                btn2.style.borderRadius = "0px";
                numberAnimals -= 1;
                count.textContent = `Number of Animals: ${numberAnimals}`;
            });

            btn6.addEventListener('click', function() {
                hidden3.style.display = "none";
                btn3.style.backgroundColor = "#ffffff";
                btn3.style.borderRadius = "0px";
                numberAnimals -= 1;
                count.textContent = `Number of Animals: ${numberAnimals}`;
            });

            btn7.addEventListener('click', function() {
                hidden1.style.display = "none";
                btn1.style.backgroundColor = "#ffffff";
                btn1.style.borderRadius = "0px";
                hidden2.style.display = "none";
                btn2.style.backgroundColor = "#ffffff";
                btn2.style.borderRadius = "0px";
                hidden3.style.display = "none";
                btn3.style.backgroundColor = "#ffffff";
                btn3.style.borderRadius = "0px";
                numberAnimals = 0;
                count.textContent = `Number of Animals: ${numberAnimals}`;
            })
        </script>
    </body>
</html>
