Major changes:

1. PerspectiveCamera is changed to OrthographicCamera. PerspectiveCamera is more realistic, OrthographicCamera (arguemnts) is more intuitive for beginners.
2. Bounding box values for the face mesh is checked at line no 42/43 and used to set the arguments for OrthographicCamera. To keep it simple, width (left to right) and height (top to bottom) are both kept to equal values so that the aspect ratio is 1. Accordingly, renderer size is set to a square in line no 32. Otherwise the face will look over-stretched horizontally or vertically.
3. By default, back faces (triangles) are culled in 3D graphics. That is, triangles with normals facing away from the camera position are not rendered. Backface culling here is switched off by setting side to DoubleSide in line no 56.

Other changes:

1. Camera is positioned on -ve x axis so that viewing starts with side pose.
2. orbitControls is set to autoRotate so that one can observe the rendered object at different camera positions. Please notice that for the frontal face, one cannot make out much about the face in this example. Why so? Use a more advanced material than BasicMaterial.

You can use mouse for random rotation of the face.

What next: 

1. Improve rendering of face by using more appropriate materials and lights.
2. Modify code to replace obj file based face mesh data by MediaPipe computed data.