# WaveGrid: CML Lab

Online Demo: http://webdombot.com/automat/

This is a javascript implementation of a CML which uses color (R,G,B) as the primary parameter space.  The rule-set for cell interaction is based on the thre rule Boids algorithm, with a Von Neumann neighborhood as the coupling scheme.  Cells are laid out in 2D space as a continuous grid representing the coupling structure.  The main difference between this and other CMLs is that the coupling strength between cells is also a parameter used as an exponent for vector multiplication in the color space, causing a dynamic coupling which can be between the "ease max" and "min"

Currently this works in Firefox only.

Start Exploring

To use it, simply open index.html and use the color palette on the bottom to paint a cell a color.  The grid always initializes with every cell having a (0,0,0,0) velocity vector and with all cell locations at the center of the entire color space.

To draw something on the grid, select a color and use the left mouse button to draw that color on the grid. What you are doing by drawing is setting that boid/cell to a fixed R, G, B color with 0 ease, meaning that it's color will not change or be affected by it's neighbors. To Erase a drawn on cell, (or make it dynamic again), use the right mouse button. 

The "Show" link shows the ease along with the color of each cell. Ease is represented visually as the opposite of black. So you will see black cells where there is very low ease. Likewise, higher-ease cells are seen more as the color which represents the RGB point of that cell. This way, ease looks like an extra texture over the current color grid, where color moves slower through darker cells. 

The "3D View" is a direct boids view of the current grid. It shows the same exact data, but as positions in orthogonal 3D space. (color of each cell is included so you can identify which boid represents which grid cell). Click on it again to change back to normal grid view.

Changing Ease to get Different patterns

Ease Max and Ease Min can be changed to any real number 0 - Infinity as long as Max is greater than Min.  This will generate different limits on the coupling strength for cells globally and will generate a different "Ease" pattern which causes the color patterns to change.

You can generate everything from chaotic behaviour to spirals to travelling waves, etc.
