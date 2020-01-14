# workshop_boilerplate

/* Hovergame Workshop

Set score and lives

Make target move to an assigned location when we hover and add a point to your score. (onmouseover)

Make speed changeable. (getSpeed, setSpeed)

Check the screen to place your target randomly on the screen. Don't forget the bar at the top

Make an enemy that reduces your lives when you touch them.

When your lives reach 0 make a game over feature

Make the enemy move

Make a boss that instantly kills you

Add enemies every 10 points you get

Add the boss when you get 60 points

Make a health bonus that gives you 1 life

Remove the bonus when you take it

add a life every 30 points

Make it visually a bit better

Fix collision

Fix immunity
 */
 
 function detectTarget() {
    setInterval(function () {
        if (findCollision(target) === true) {
            getPoint();
        }
    }, 50);
}

function findCollision(element) {
    if (mouseX >= element.getBoundingClientRect().left &&
        mouseX <= element.getBoundingClientRect().right &&
        mouseY >= element.getBoundingClientRect().top &&
        mouseY <= element.getBoundingClientRect().bottom) {
        return true;
    }
}

function findMouse(e) {
    mouseX = e.pageX;
    mouseY = e.pageY;
}
