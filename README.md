# CubeLutTest

![FkGtqlGUcAAPiGc](https://user-images.githubusercontent.com/343936/208119114-074d462b-b56e-4489-b861-c3379cebe1f6.jpeg)

A Unity sample applying a .cube LUT (edited with DaVinci Resolve) using Shader Graph.

### Why don't you use the post processing effect for grading?

They're useful for grading the render output. I use the LUT approach for grading a camera input (e.g. webcam).

### How to create a LUT

- Take a screenshot for grading.
- Create a new project on DaVinci Resolve.
- Change the Color Management settings in the project settings:
  - Color science: DaVinci YRGB Color Managed
  - Color processing mode: SDR Rec.709
  - Output color space: sRGB
- Import the screenshot and change Input Color Space to sRGB.
- Grade it on the Color page.
- Generate LUT (right click menu on the clip) -> 17/33/65 Point Cube

Now you can import the .cube file by simply dragging-and-dropping into Unity Editor.
