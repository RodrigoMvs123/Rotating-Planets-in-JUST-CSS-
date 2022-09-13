# Rotating-Planets-in-JUST-CSS-

##

https://www.youtube.com/watch?v=6M-rZIukXy0

##

https://raw.githubusercontent.com/RodrigoMvs123/Rotating-Planets-in-JUST-CSS-/main/README.md

##

index.html 
<!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>CSS Planets</title>
        <link rel ="stylessheet" href="styles.css">
    </head>
    <body>
        
        <div class="planets-container">

            <div class="sun"></div>
          <div>class="planet-index" id="fisrt-planet-index"
            <div class="route">
                <div class="planet-container" id="first-planet-container">
                    <div class="planet" id="first-planet"></div>    
                </div>
            </div>
        </div>
           <div class="planet" id="first-planet"></div>
        </div>
        <div>class="planet-index" id="second-planet-index"
        <div class="route">
            <div class="planet-container" id="second-planet-container">
                <div class="planet" id="second-planet"></div>  
            </div>  
          </div>
        </div>
        
        <div>class="planet-index" id="third-planet-index"
        <div class="route">
            <div class="planet-container" id="third-planet-container">
                <div class="planet" id="third-planet"></div>
            </div>
          </div>
        </div>
        
    </body>
    </html>
    
    ##
    
    styles.css
    
    body {
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: rgb(33, 33, 33);
}

.planets-container {
     width: 150px;
     height: 150px;
     border-radius: 50%;
     transform: scaleX(5);
}

.sun {
    position: absolute;
    width: 150px;
    height: 150px;
    border-radius: 50%;
    background-color: rgb(248, 244, 163);
    box-shadow: 0 0 60px rgb(253, 203, 163), 0 0 98px rgb(184, 160, 26);
    transform: scaleX(0.2);
}

.planet {
    width: 60px;
    height: 60px;
    border-radius: 50%;
    transform: scaleX(0.2);

}

.planet:after {
    content: '';
    position: absolute;
    inset: 0;
    border-radius: 50%;

}


.planet-index {
    width: 100%;
    height: 100%;
    position: absolute;
}


.route {
    width: 100%;
    height: 100%;
    animation: rotate 12s infinite linear;
    position: absolute;
    
}

.planet-container {
    width: 60px;
    height: 60px;
    animation: correct 12s infinite linear;
    position: absolute;

}

#first-planet-index {
    animation hideFirstPlanet 12s infinite;
}

#second-planet-index {
    animation hideSecondPlanet 12s infinite;
}

#third-planet-index {
    animation hideThirdPlanet 12s infinite;
}


#second-planet-container {
    left: 85px;

}

#third-planet-container {
    left: 42.5px;
    top: 100px;

}


#first-planet {
    animation: firstPlanetRender 12s infinite linear; 
}

#first-planet:after {
    animation: firstPlanetRenderRotator 12s infinite linear;

#second-planet {
    animation: secondPlanetRender 12s infinite linear; 
}

#second-planet:after {
    animation: secondPlanetRenderRotator 12s infinite linear;
}

#third-planet {
    animation: thirdPlanetRender 12s infinite linear; 
}

#third-planet:after {
    animation: thirdPlanetRenderRotator 12s infinite linear;
}

@keyframes firstPlanetRender {
    0% {
        background: linear-gradient(-90deg, rgb(blue) 50%, rgb(60, 60, 175) 50%);
    }
    12% {
        background: linear-gradient(-90deg, rgb(blue) 50%, rgb(60, 60, 175) 50%);
    }
    12.1% {
        background: linear-gradient(90deg, rgb(blue) 50%, rgb(60, 60, 175) 50%);
    }
    62% {
        background: linear-gradient(90deg, rgb(blue) 50%, rgb(60, 60, 175) 50%);
    }
    62.1% {
        background: linear-gradient(-90deg, rgb(blue) 50%, rgb(60, 60, 175) 50%);
    }

    100% {
        background: linear-gradient(-90deg, rgb(blue) 50%, rgb(60, 60, 175) 50%);
    }

}

@keyframes firstPlanetRenderRotater {
    0% {transform: scaleX(0.2); background-color: rgb(86, 86, 253);}
    12% {transform: scaleX(-1); background-color: rgb(86, 86, 253);}
    12.1 {transform: scaleX(1); background-color: rgb(86, 86, 253);}
    37% {transform: scaleX(0); background-color: rgb(86, 86, 253);}
    37.1 {transform: scaleX(0); background-color: rgb(60, 60, 175);}
    62% {transform: scaleX(-1); background-color: rgb(60, 60, 175);}
    62.1 {transform: scaleX(1); background-color: rgb(86, 86, 253);}
    87% {transform: scaleX(0); background-color: rgb(60, 60, 175);}
    87.1% {transform: scaleX(0); background-color: rgb(86, 86, 253);}
    100% {transform: scaleX(0.2); background-color: rgb(86, 86, 253);}
}

@keyframes secondPlanetRender [
    0% {
        background: linear-gradient (90deg, rgb(95, 185, 95) 50%, rgb(65, 128, 65) 50%);
    }   

    40% {
        background: linear-gradient (90deg, rgb(95, 185, 95) 50%, rgb(65, 128, 65) 50%);
    }
    40.1% {
        background: linear-gradient (-90deg, rgb(95, 185, 95) 50%, rgb(65, 128, 65) 50%);
    } 
    90% {
        background: linear-gradient (-90deg, rgb(95, 185, 95) 50%, rgb(65, 128, 65) 50%);
    }
    90.1% {
        background: linear-gradient (90deg, rgb(95, 185, 95) 50%, rgb(65, 128, 65) 50%);
    }
    100% {
        background: linear-gradient (90deg, rgb(95, 185, 95) 50%, rgb(65, 128, 65) 50%);
    }
}

@keyframes secondPlanetRenderRotator {
    0% {transform: scaleX(0.5); background-color: rgb(95, 185, 95);}
    15% {transform: scaleX(0); background-color: rgb(95, 185, 95);}
    15.1% {transform: scaleX(0); background-color: rgb(65, 128, 65);}
    40% {transform: scaleX(-1); background-color: rgb(65, 128, 65);}
    40.1% {transform: scaleX(1); background-color: rgb(65, 128, 65);}
    65% {transform: scaleX(0); background-color: rgb(65, 128, 65);}
    65.1% {transform: scaleX(0); background-color: rgb(95, 185, 95);}
    90% {transform: scaleX(-1); background-color: rgb(95, 185, 95);}
    90.1% {transform: scaleX(-1); background-color: rgb(95, 185, 95);}
    100% {transform: scaleX(0.5); background-color: rgb(95, 185, 95);} 

@keyframes thirdPlanetRender {
    0% { background: linear-gradient(-90deg, rgb(255, 66, 113) 50%, rgb(168, 47, 77), 50% );}
    49% { background: linear-gradient(-90deg, rgb(255, 66, 113) 50%, rgb(168, 47, 77), 50% );}
    49.1% { background: linear-gradient(90deg, rgb(255, 66, 113) 50%, rgb(168, 47, 77), 50% );}
    99% { background: linear-gradient(90deg, rgb(255, 66, 113) 50%, rgb(168, 47, 77), 50% );}
    99.1% { background: linear-gradient(-90deg, rgb(255, 66, 113) 50%, rgb(168, 47, 77), 50% );}
    100% { background: linear-gradient(-90deg, rgb(255, 66, 113) 50%, rgb(168, 47, 77), 50% );}
}

@keyframes thirdPlanetRenderRotater {
    0% {transform: scaleX(1); background-color: rgb(168, 47, 77); }
    25% {transform: scaleX(0); background-color: rgb(168, 47, 77); }
    25.1% {transform: scaleX(0); background-color: rgb(255, 66, 113); }
    49% {transform: scaleX(-1); background-color: rgb(255, 66, 113); }
    49.1% {transform: scaleX(1); background-color: rgb(255, 66, 113); }
    75% {transform: scaleX(0); background-color: rgb(255, 66, 113); }
    75.1% {transform: scaleX(0); background-color: rgb(168, 47, 77); }
    100% {transform: scaleX(1); background-color: rgb(168, 47, 77); }
}


@keyframes rotate {
    0% {
        transform: rotateZ(0deg);

    }
    100% {
        transform: rotateZ(360deg);
    }

}


@keyframes correct {
    0% {
        transform: rotateZ(360deg);
    }
    100% {
        transform: rotateZ(0deg);
    }
}

@keyframes hideFirstPlanet {
    0% {
        z-index: 999;
        transform: scale(0.9)
    }
    25% {
        z-index: -999;
        transform: scale(0.8);
    }
    50%{
        transform: scale(0.9);
    }
    75% {
        transform: scale(1.1);
    }
    100% {
        z-index: 999;
        transform: scale(0.9)
    }
}

@keyframes hideSecondPlanet {
    0% {
        z-index: -999;
        transform: scale(0.95);
    }
    50% {
        z-index: 999;
        transform: scale(1.1);
    }
    90% {
        transform: scale(0.9);
    }
    100% {
        z-index: -999;
        transform: scale(0.95);
    }
}

@keyframes hideThirdPlanet {
    0% {
        z-index: 999;
        transform: scale(1.1);
    }
    50% {
        z-index: -999;
        transform: scale(0.8);
    }
    100% {
        z-index: 999;
        transform: scale(1.1);
    }
}

##

