# ImageProcessing-Transformation
🔁 1. Similarity Transformation

📄 File: similarity_transform

A similarity transformation includes rotation, uniform scaling, and translation.

The transformation matrix is a 2x3 matrix composed of:

Scaled rotation matrix.

Translation vector.

The square is scaled by 1.5, rotated by 30°, and moved to a new position.

Key functions:

similarity_matrix(...) – builds the transformation matrix.

apply_transform(...) – applies the matrix to the shape.

🖼️ Result: The square maintains its shape (angles preserved) but becomes larger and rotated.

🎯 2. Projective Transformation (Homography)

📄 File: projective_transform

A projective transformation (or homography) maps points from one plane to another using a 3×3 matrix.

This transformation can introduce perspective distortion, such as turning a square into a trapezoid.

It’s commonly used in computer vision and image warping.

Key functions:

apply_homography(...) – applies the homography and handles homogeneous coordinates.

🖼️ Result: The square is warped into a trapezoidal shape with perspective effects.

📐 3. Euclidean Transformation

📄 File: euclidean_transform

This transformation preserves distances and angles, meaning the shape doesn’t stretch or distort.

It only includes:

Rotation (around a center point).

Translation.

The square is rotated around its center and then translated.

Key functions:

rotation_matrix(...) – builds the rotation matrix.

🖼️ Result: The square is rigidly moved and rotated without changing its size or shape.

🧮 4. Affine Transformation

📄 File: affine_transform

Affine transformations include scaling, rotation, translation, and shearing.

Represented by a 2x2 matrix (A) and 2x1 translation vector (t).

Demonstrates:

Non-uniform scaling (e.g., x scaled 2×, y unchanged).

Shearing in x-direction.

Rotation + Translation as part of affine space.

🖼️ Result: The square can stretch, rotate, or shear, but parallel lines remain parallel.

📊 Visualization

All transformations are visualized using Matplotlib:

The original square is plotted in blue.

Transformed versions are plotted in different colors.

Grid and aspect ratio are adjusted for clear visualization.
