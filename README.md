# plane-battle
/************************************
 * created by: Emmett Itoi
************************************/


var level = 4;
var backgrounds = {
    grass: function() {
        background(0, 255, 17);
        noStroke();
        fill(107, 107, 107);
        rect(310, 200, 64, 200);
    },//levels 1-3
    ocean: function() {
        background(0, 255, 255);
        noStroke();
        fill(107, 107, 107);
        rect(270, 154, 64, 200);
        fill(120, 120, 120);
        rect(334, 273, 25, 30);
        fill(43, 51, 44, 100);
        beginShape();
        vertex(334, 273);
        vertex(318, 254);
        vertex(294, 285);
        vertex(334, 334-30);
        endShape();
        strokeWeight(6);
        stroke(255, 247, 0);
        line(302, 326, 302, 160);
    },//level 4
};
var create_background = function() {
    if (level === 1 || level === 2 || level === 3) {
        backgrounds.grass();
    }
    if (level === 4) {
        backgrounds.ocean();
    }
};
draw = function() {
    create_background();
};
