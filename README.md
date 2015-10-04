# robocode1


package s13ec068;
import robocode.*;
import java.awt.Color;


// API help : http://robocode.sourceforge.net/docs/robocode/robocode/Robot.html

/**
 * a874_01 - a robot by (your name here)
 */
public class a874_01 extends Robot
{


	/**
	 **
	 * run: a874_01's default behavior
	 */
	

	
	public void run() {
		// Initialization of the robot should be put here

		// After trying out your robot, try uncommenting the import at the top,
		// and the next line:

		 setColors(Color.blue,Color.cyan,Color.darkGray); // body,gun,radar

        turnLeft(getHeading()-90);
		double LeftcornerX = 50;
		
		ahead(LeftcornerX-getX());
	
		
        turnLeft(90);
		double LeftcornerY1 = getBattleFieldHeight()-50;
		double LeftcornerY2 = 50;
		ahead(LeftcornerY1-getY());
		
		turnRight(90);
		turnGunRight(90);

		// Robot main loop
		while(true) {
			// Replace the next 4 lines with any behavior you would like
           if(getX()>=260){
		    
	    	ahead(LeftcornerX-getX());
           
            }
		  if(getY()<=200){
		   
       		ahead(LeftcornerY1-getY());
		    
		    
		  }	   



		   ahead(200);
		   back(200);
		   
		   turnRight(90);
		   turnGunRight(180);
		   
           ahead(200);
           back(200);
           turnLeft(90);
		   turnGunRight(180);
			
			}
	}

	/**
	 * onScannedRobot: What to do when you see another robot
	 */
	public void onScannedRobot(ScannedRobotEvent e) {
		// Replace the next line with any behavior you would like
		fire(1);
	}

	/**
	 * onHitByBullet: What to do when you're hit by a bullet
	 */
	public void onHitByBullet(HitByBulletEvent e) {
		// Replace the next line with any behavior you would like
		//turnGunRight(e.getBearing());
       
	}
	
	/**
	 * onHitWall: What to do when you hit a wall
	 */
	public void onHitWall(HitWallEvent e) {
		// Replace the next line with any behavior you would like
		
        turnLeft(getHeading()-90);
		double LeftcornerX = 50;
		
		ahead(LeftcornerX-getX());
		
        turnLeft(90);
		double LeftcornerY1 = getBattleFieldHeight()-50;
		ahead(LeftcornerY1-getY());
		
		turnRight(90);
		ahead(LeftcornerX-getX());
		ahead(LeftcornerY1-getY());
		turnRight(90);
		
	}	
	
    public void onHitRobot(HitRobotEvent e){
		
	}
}
