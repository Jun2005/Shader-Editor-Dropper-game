# Shader Editor: Dropper game
https://github.com/user-attachments/assets/c4009a32-93b9-47d8-b2b9-25fe0a9c6bdf

### Description
This is a mobile game made entirely using shader code (GLSL) in an application called "Shader Editor". Players need to rotate their phone to dodge obstacles and reach a high score.

### Features
- Phone orientation controls
- Custom ray casting rendering

### Challenges
As this is a mobile game, performance was a big issue during development. The major contributor to the performance issue was the chosen rendering method. The game originally utilized ray marching as a rendering algorithm. However, this approach was very computationally expensive, and rendering just 12 cuboids dropped the fps to <10. 

Ray marching is a rendering method involving iterative steps through the scene using signed distance fields (SDFs), and it offers many unique qualities, such as the ability to easily create metaballs, infinitely detailed geometry, and infinite tiling of geometry. My game did not utilize these qualities, so I swapped the rendering method to ray casting, which dramatically improved performance (roughly 4 to 5 times more fps).

https://github.com/user-attachments/assets/7cfd3ef5-3a4f-412e-99cc-4a87758cce7c

Video showcasing the ability to create metaballs using ray marching.

https://github.com/user-attachments/assets/32b459a9-8abf-4bb8-863e-b9b4ab71d6e4

Video showcasing the ability to render infinitely tiling geometry using ray marching.

### How to play
- Install Shader Editor on your mobile device and copy the code onto the editor.
- Press the play button to start the game
- The default orientation of the phone needs to be flat (parallel to the ground).
- Moving up or down: Rotate the phone away or toward you
- Moving left or right: Tilt the phone left or right
