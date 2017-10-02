# Random-Rain
var xPositions = [50, 75, 100, 125, 200, 250, 300, 310];
var yPositions = [0, 35, 10, 15, 20, 45, 55, 50];
var firstColor = random(50,150);  //fill with random colors 1st place (low to high)
var secColor = random(0, 250);
var thirdColor = random(100, 200);   //fill with random color 2nd place
var rainColor = fill(firstColor, secColor, thirdColor);


draw = function() {
    background(204, 247, 255);
    
    ellipse(250, 350, 90, 50); //frog
    ellipse(250, 315, 50, 30);
    ellipse(235, 300, 15, 15);
    ellipse(235, 300, 10, 10);
    ellipse(265, 300, 15, 15);
    ellipse(285, 370, 40, 10);   //feet
    ellipse(222, 372, 40, 10);  //feet
    text("Make it Rain!", 215, 266);
    
    for (var i = 0; i < xPositions.length; i++) {
        noStroke();
        ellipse(xPositions[i], yPositions[i], 5, 5);
        
         if (yPositions[i] > 400) {
             yPositions[i]=0;
            
               firstColor = random(50,150);
               secColor = random(0, 250);
               thirdColor = random(100, 200);
               rainColor = fill(firstColor, secColor, thirdColor); 
         }
        
         {
            yPositions[i] += 5;
                 }
}
    
};
