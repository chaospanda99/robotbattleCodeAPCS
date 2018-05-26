package DarrenBot;
import robocode.*;
//import java.awt.Color;

// API help : http://robocode.sourceforge.net/docs/robocode/robocode/Robot.html

/**
 * DarrenBot - a robot by (your name here)
 */
public class DarrenBot extends Robot
{
	private boolean scanned;
	private int turns;
	
	public void run() {
		turns = 0;	
		scanned = false;
		scan(true);
		
		while(true){
			if(turns > 5)
				move(true);
			scanned = false;
			while(!scanned){
				turnGunLeft(15);
				turns++;
				if(turns > 5)
					break;
				}
				
				if(turns > 5)
					move(false);
			scanned = false;
			while(!scanned){
				turnGunRight(15);
				turns++;
				if(turns > 5)
					break;
				}
		}
	}

	/**
	 * onScannedRobot: What to do when you see another robot
	 */
	public void onScannedRobot(ScannedRobotEvent e) {
		fire(5);
		scanned = true;
	}

	
	private void scan(boolean right){
		//if right, scan right
		//otherwise scan left
		scanned = false;
		while(!scanned){
			if(right)
				turnGunRight(45);
			else
				turnGunLeft(45);
		}
	}
	
	private void move(boolean right){
		turns = 0;
		turnLeft(90);
		ahead(300);
		scan(right);
	}

	public void onHitByBullet(HitByBulletEvent e) {
		turns+=3;
	}
	
	
	/**
	 * onHitWall: What to do when you hit a wall
	 */
	public void onHitWall(HitWallEvent e) {
		turns++;
	}
	}
		

