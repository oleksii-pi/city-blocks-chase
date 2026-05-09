I want to quickly hack a game with kids, so all implementations should be done quickly and simply.  
Implement a single-file HTML document with JavaScript and CSS included.

I want to build a GTA 1-style game with a top-down view.

I want to render a simple square city that contains 16x16 O-shaped blocks.
Bloc contains of 8 houses. It should be visible building windows.

Here is a typical block
HHH
H H
HHH
H - House

There also other blocks

HHH
H H
PPP

P - police station

I want to see pedestrian areas. Where car stil can move.  
On a single screen, it should be possible to see a few blocks only, not so many.  
Each street should have two directions for cars.

I want to see streets with detailed rendering of houses, their windows:

Warmer city palette with tan sidewalks and dark roads.
Buildings now have simple projected top/side faces for an isometric-like look.
Windows are larger/brighter with yellow frames and blue glass, with small gradients.
Added small pedestrians moving along sidewalks.

I want to draw a car and control its movements.  
This car should have speed, direction, and momentum.  
I want to control this car with arrow buttons.  
I want to have other cars moving in the city.  
Cars should be implemented with simple vector sprites.  
As the speed of the car increases, the camera view height should also increase.

Optimize graphics, but keep it simple.
Other cars should always move in some random algorithm, and never disapear.
It should not be possible to move car on top of buildings
Cars can crash, it is not possible to draw one car on top of another.
Draw a few police cars.
Cars should change direction sometimes.
Cars should follow right side road direction.

Cars should not dissapear suddenly.
It should be 100 cars on a map.
When cars moving in the city they change direction sometimes, every 1-7 blocks.
When I hit a car, nearest police car should chase me.
When police riched me it is no stuck, round restarts.
Police should build an optimal route to my car and follow it.

---

Focus on detailization of street rendering and smooth car move.
Render 4 lanes (2 in each direction) with delimiter dashed lanes,
and double solid line in the middle.

Create a stylized isometric street scene.

1. Street
   Dark asphalt surface.
   Use an orthographic/isometric camera angle.
2. Two sides of the street
   Sidewalk on both sides of the road.
   Sidewalks should be lighter than the road.
   Each sidewalk runs parallel to the street.
3. Street delimiter

Add clear road delimiters:

Dashed line should be made from repeated white rectangular strips.

Place buildings along both sides of the street.
Buildings should be simple rectangular blocks.
Buildings should be taller than the street and sidewalks.
Use different wall colors for each side to separate them visually.
Buildings should align parallel to the road.

5. Windows

Each building must have repeated windows.

Each window should include:

Glass panel
Blue or cyan rectangle.
Slightly inset or placed on the wall surface.
Outer frame
Light cream/white rectangular border around the glass.
Dividers
One vertical frame strip splitting the glass into two panes.
Optional horizontal strip splitting the window into upper/lower panes. 6. Window layout
Arrange windows in rows and columns.
Keep spacing regular.
Windows should be repeated across the building facades.
Windows should face the street.
Minimal object list
Scene
├── Road
├── Sidewalk left
├── Sidewalk right
├── Center dashed delimiter
├── Optional road-edge delimiters
├── Building row left
│ └── Repeated windows
│ ├── Glass
│ ├── Outer frame
│ └── Divider frame
└── Building row right
└── Repeated windows
├── Glass
├── Outer frame
└── Divider frame
Visual style
Low-poly / clean 3D.
Bright colors.
Beveled edges.
Soft shadows.
