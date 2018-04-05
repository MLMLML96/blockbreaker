
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8" />
	<title>Blockbuster game for webdev course</title>
	<style>
		* {padding: 0; margin: 0;}
		canvas {background: #eee; display: block; margin: 0 auto;}
	</style>
</head>

<body>

<canvas id="Canvas" width="960" height="640"></canvas>

<script>
var canvas = document.getElementById("Canvas");
var ctx = canvas. getContext("2d");

// ball variables here

var dx = 19;
var dy = 0.01;
var ballRadius = 7;
var x = canvas.width/2;
var y = canvas.height/2;

// paddle variables here
var paddleHeight = 10;
var paddleWidth = 125;
var paddleX = (canvas.width-paddleWidth)/2;
var rightbutton = false;
var leftbutton = false;

document.addEventListener("keydown", keyDownHandler, false);
document.addEventListener("keyup", keyUpHandler, false);
document.addEventListener("mousemove", mouseMoveHandler, false);


// destroyable blockfields here
	var brickRowCount = 12;
	var brickColumnCount = 20;
	var brickWidth = 45;
	var brickHeight = 45;
	var brickPadding = 0;
	var brickOffsetTop = 30;
	var brickOffsetLeft = 30;
	var bricks=[];
	
	
	
for(c=0; c<brickColumnCount; c++) 
{
    bricks[c] = [];
    for(r=0; r<brickRowCount; r++) 
	{
        bricks[c][r] = { x: 0, y: 0, status: 1 };
    }
}

// player here
var score = 0;
var lives = 300;
var destroyed = 0;



function drawBall() {
	if (y + dy < ballRadius) 
	{
		dy = -dy;
	}
	else if(y + dy > canvas.height-ballRadius-10)
	{
		if(x > paddleX && x < paddleX + paddleWidth)
		{
			dy = -dy;
			dx += -(((paddleX+paddleWidth/2)-x)/paddleWidth)*20;
		}
		else
		{
			lives --;
			if(!lives)
			{
				alert("GAME OVER");
				document.location.reload();
				// game over actions here
			}
			else
			{
				x = canvas.width/2;
				y = canvas.height/2;
				dx = 0;
				dy = 0;
				paddleX = (canvas.width-paddleWidth)/2;
			}
			
			//document.location.reload();
			
			//alert("GAME OVER");
		}
	}
	
	if ((x + dx < ballRadius) || (x + dx > canvas.width-ballRadius))
	{
		dx = -dx;
	}
    ctx.beginPath();
    ctx.arc(x, y, ballRadius, 0, Math.PI*2);
	if (dy > 0)
	{
		ctx.fillStyle = "Tomato";
	}
	else
	{
		ctx.fillstyle = "Blue";
	}
   
    ctx.fill();
    ctx.closePath();
}

function drawPaddle()
{
	ctx.beginPath();
	ctx.rect(paddleX, canvas.height-paddleHeight-10, 
	paddleWidth, paddleHeight);
	ctx.fillStyle = "#0009DD";
	ctx.fill();
	ctx.closePath();
}


function drawBricks() 
{
    for(c=0; c<brickColumnCount; c++) 
	{
        for(r=0; r<brickRowCount; r++) 
		{
			if(bricks[c][r].status == 1)
			{
				var brickX = (c*(brickWidth+brickPadding))+brickOffsetLeft;
				var brickY = (r*(brickHeight+brickPadding))+brickOffsetTop;
				bricks[c][r].x = brickX;
				bricks[c][r].y = brickY;
				ctx.beginPath();
				ctx.rect(brickX, brickY, brickWidth, brickHeight);
				ctx.fillStyle = "#0095DD";
				ctx.fill();
				ctx.closePath();
			}
        }
    }
}

function drawScore()
{
	ctx.font = "20px Times New Roman";
	ctx.fillStyle = "#0095DD";
	ctx.fillText("Score: "+score, 8, 20);
}

function drawLives() 
{
	ctx.font = "20px Times New Roman";
	ctx.fillStyle = "#0095DD";
	ctx.fillText("Lives: "+lives, 160, 20);
}


function draw() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    drawBall();
	drawPaddle();
	collisionDetection();
	drawBricks();
	drawScore();
	drawLives();
    x += dx;
    y += dy;

	if (score >	 0)
	{
		--score;
	}
	if(rightbutton && paddleX < canvas.width-paddleWidth)
	{
		paddleX +=5;
	}
	else if(leftbutton && paddleX > 0)
	{
		paddleX -=5;
	}
	requestAnimationFrame(draw);
	
}

function keyDownHandler(e)
{
	if(e.keyCode == 39)
	{
		rightbutton = true;
	}
	else if(e.keyCode == 37)
	{
		leftbutton = true;
	}
}

function keyUpHandler(e)
{
	if(e.keyCode == 39)
	{
		rightbutton = false;
	}
	else if(e.keyCode == 37)
	{
		leftbutton = false;
	}
}

function mouseMoveHandler(e)
{
	var relativeX = e.clientX - canvas.offsetLeft;
	if(relativeX > 0 && relativeX < canvas.width)
	{
		paddleX = relativeX - paddleWidth/2;
	}
}

function collisionDetection()
{
	for(c=0; c<brickColumnCount; c++)
	{
		for(r=0;r<brickRowCount; r++)
		{
			var b = bricks[c][r];
			if(b.status == 1)
			{
				if(x>b.x-ballRadius && x<b.x+brickWidth+ballRadius/2
				&& y>b.y-ballRadius && y<b.y+brickHeight+ballRadius/2)
				{
					var dysave = dy;
					var dxsave = dx;
					dy = 0;
					dx = 0;
					// checks which direction the collision came from and 
					// ricochets appropriately 
					if((dysave > 0 && y < b.y)||(dysave < 0 && y < b.y+brickHeight))
					{
						dx = -dxsave;
						dy = dysave;
					}
					else
					{
						dy = -dysave;
						dx = dxsave;
					}
					b.status = 0;
					score += 1000;
					destroyed++;
					if(destroyed == brickRowCount*brickColumnCount)
					{
						alert("YOU WIN!")
						// game end actions here (save score?)
						document.location.reload();
					}
				}
			}
		}
	}
}


draw();
</script>
