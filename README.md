# CubeLutTest

![FkGtqlGUcAAPiGc](https://user-images.githubusercontent.com/343936/208119114-074d462b-b56e-4489-b861-c3379cebe1f6.jpeg)

A Unity sample project applying a LUT (`.cube` file exported from DaVinci Resolve) with Shader Graph.

## How to create a LUT

- Take a screenshot in Unity for grading.
- Create a new project in DaVinci Resolve.
- Change the Color Management settings in the project settings:
  - Color science: DaVinci YRGB Color Managed
  - Color processing mode: SDR Rec.709
  - Output color space: sRGB
- Import the screenshot and change the Input Color Space to sRGB.
- Grade it in the Color page.
- Generate LUT (right click menu on the clip) - 17/33/65 Point Cube

Now you can import the .cube file by simply drag-and-drop into Unity Editor.

## Frequently asked questions

### Why don't you use the post processing effect for grading?

They're useful for grading the render output from Unity. I use the LUT approach for grading a camera input (e.g. webcam).

### Why SDR? Not HDR?

Because I use it with the camera input. It would be Rec.709 or sRGB.
