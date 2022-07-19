# GUIDELINE FOR USTH PROJECT 1:

## Project name: Projectile Motion
## Project description:
In this project you will simulate the motion of a projectile in two dimensions with air resistance.
**Projectile motion** is a form of motion experienced by an object that is projected near the Earth’s surface and moves along a curved path. This type of motion can also be known as a **ballistic trajectory**. 
## Equations of motion:
The equations of motion describe the acceleration, velocity and position in the for both horizontal and vertical motion at every timestep. Projectile motion can be determined completely by the constant acceleration of gravity (g), the launch speed (u) and the launch angle (θ) provided that air friction is negligible. Horizontal and vertical motions are typically separated and described by general equations of motion with this constant acceleration. On Earth, assuming we use metric units and that we are at the surface, gravity (g) is approximated as 9.8 m/s² downwards.

Assuming that we initialize at horizontal and vertical position of 0 and end at vertical position of 0, these are the equations:

aₓ = 0

vₓ = u*cos(θ)

x = u*cos(θ)*t

aᵧ = -g

vᵧ = u*sin(θ)-g*t

y = u*sin(θ)*t-0.5*g*t²

Notice these are parametric equations. In other words, these equations require the input of the independent variable time (t). We can combine them to write height (y) directly in terms of horizontal position (x):

y = tan(θ)*x-g*x²/(2*u²*cos²θ)

**Time of Flight**
The time of flight (T) is the total amount of taken taken by an object to travel from launch until landing. If you imagine throwing a ball, it is the number of seconds the ball is flying before it hits the ground. To solve for T, realize that at the final time, the vertical position is 0. In other words, you need to use the quadratic formula and solve for 0 = u*sin(θ)*T-0.5*g*T² and you will find the expression for T:

T = 2*u*sin(θ)/g

As can be seen, for the same launch speed, T is greatest when θ is 90 degrees which is when the projectile is launched straight up vertically.

### Input parameters:
1. Initial velocity
2. Initial angle
3. Air resistance coefficient
4. Gravitational acceleration
### Output results:
1. Horizontal range, flight time, highest point
2. A static plot showing 2D projectile's trajectory
3. An animating plot showing 2D projectile's trajectory in real-time
## Project requirements:
1. Physics-based algorithm
2. GUI design (Tkinter, turtle, pygame, etc...)
3. Simple animating demonstration

## References:
1. http://hyperphysics.phy-astr.gsu.edu/hbase/traj.html
2. https://www.coursehero.com/study-guides/physics/3-4-projectile-motion/
3. https://phet.colorado.edu/en/simulations/projectile-motion
