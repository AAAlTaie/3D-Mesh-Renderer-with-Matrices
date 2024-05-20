# 3D-Mesh-Renderer-with-Matrices

Welcome to the 3D Mesh Renderer with Matrices repository! This project aims to demonstrate the use of matrices in conjunction with 3D mesh data to create and render objects in a 3D space, providing a deeper understanding of 3D graphics programming concepts.

# Objective

The primary objective of this project is to showcase a 3D mesh renderer capable of rendering objects in a 3D space using three different matrices: World Matrix, View Matrix, and Projection Matrix. These matrices serve different purposes in positioning and rendering objects within the scene, adding depth and perspective to the rendered output.

# Core Development info:

1. Vertex Information Creation: Begin by creating vertex information for a grid and a cube. Determine the total number of vertices required for drawing lines for the grid and cube. Ensure that the grid is positioned around the origin (0, 0, 0) and the cube is translated upwards by half of its height.

2. World Matrices Creation: Create world matrices for each object. The world matrix for the grid can be the identity matrix, while the world matrix for the cube should include translation upwards by half of its height and rotation over time on its y-axis.

3. View Matrix Integration: Develop a 4x4 rotation matrix rotated -18 degrees on the X axis and translate this matrix backwards along the local Z-axis by -1 unit. Inverse this matrix temporarily to transform it into a proper view matrix (reverse motion).

4. Projection Matrix Creation: Create a projection matrix with the specified parameters: Near Plane at 0.1, Far Plane at 10.0, Vertical Field Of View at 90 degrees, and Aspect Ratio based on the window's dimensions.

5. Vertex Shader Implementation: Develop a vertex shader that multiplies each vertex by the world, view, and projection matrices in a specific order: VertexW = VertexL times World, VertexV = VertexW times View, VertexP = VertexV times Projection.

6. Perspective Divide: Perform perspective divide to adjust the depth perception and finalize the rendering of the scene.
