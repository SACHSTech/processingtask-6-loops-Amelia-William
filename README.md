[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-f059dc9a6f8d3a56e377f745f24479a46679e63a5d9fe6f495e02850cd0d8118.svg)](https://classroom.github.com/online_ide?assignment_repo_id=6657259&assignment_repo_type=AssignmentRepo)
# Processing Task 6 - Loops

## Learning Objectives
In this task, you will learn about using loop patterns to draw sequences of objects.



## Step 1 - Lesson
Acquire the learning objectives by reviewing [this page](https://happycoding.io/tutorials/processing/for-loops)

## Step 2 - Task

![](processing_task6.png)

Demonstrate your learning objectives by using loops to reproduce the graphic above, such that:

* Quadrant 1 is a 10 x 10 grid that scales to with the size of window.
* Quadrant 2 is 5 x grid of evenly spaced circles that scales to the size of the window.
* Quadrant 3 is a horizontal grayscale gradient 
* Quadrant 4 is a 8 petal flower that uses a loop to draw the petals evenly spaced around the center of the flower.


### Evaluation

#### Level 2
Successfully implements quadrant 1 & 2

#### Level 3
Successfully implements quadrant 1, 2, and 3

#### Level 4
Successfully implements all quadrants.



## Submission
1. Commit and push your code to this repository
2. Take a screenshot of your work and upload it to the Google Classroom assignment post.



import processing.core.PApplet;

public class Sketch extends PApplet {
	
  public void settings() {
	// put your size call here
    size(900, 900);
  }

  public void setup() {
    background(210, 255, 173);
  }

  public void draw() {
	  
    background(255, 255, 255);

    for (int circleY = 75; circleY <= 375; circleY += 75) {
      for (int circleX = 500; circleX <= 800; circleX += 75) {
        stroke(0);
        fill(204, 35, 122);
        ellipse(circleX, circleY, 25, 25);
      }
    }

    for (int i = 1; i <= 8; i++) {
      int lineY = i * 50;
      stroke(0);
      line(lineY, 0, lineY, 400);
    }

    for (int j = 1; j <= 8; j++) {
      int lineX = j * 50;
      stroke(0);
      line(0, lineX, 400, lineX);
    }
    
    
    for (int x = 0; x <= 450; x++) {
      stroke(x * 256 / 450);
      line(x * 1, 450, x + 1, 900);
    }
  }
}
