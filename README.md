const Engine = Matter.Engine;
const World = Matter.World;
const Bodies = Matter.Bodies;


var engine,world,ball;


function setup() {
  createCanvas(400,400);
  engine = Engine.create();
  world = engine.World;

  var ball_options ={
     restitution: 1.0
     }
      ball = Bodies.circle(200,100,20, ball_options);
       World.add(world,ball);
 
  
}

function draw() {
  background(0);  
 Engine.update(engine);
 ellipseMode(RADIUS);
 ellipse(ball.position.x,ball.position.y,20,20);

}
