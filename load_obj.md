Major changes:

1. PerspectiveCamera is changed to OrthographicCamera. PerspectiveCamera is more realistic, OrthographicCamera (arguemnts) is more intuitive for beginners.
2. Bounding box values for the face mesh is checked at line no 42/43 and used to set the arguments for OrthographicCamera.
3. By default back faces (triangles) are culled in 3D graphics. That i, triangles with normals facing away from the camera position are not rendered. Backface culling is switched off by setting side to DoubleSide in line no 56.

Other changes:

1. Camera is positioned on -ve x axis so that viewing starts with side pose.
2. orbitControls is set to autoRotate so that one can observe the rendered object at different camera positions. Please notice that for the front facing position, one cannot make out much about the face. Why so? needs use of a more advanced material setting than BasicMaterial.

You can use mouse for random rotation of the face.

What next: 

1. Improve rendering of face by using more appropriate materials and lights.
2. Modify code to replace obj file based face mesh data by MediaPipe computed data.