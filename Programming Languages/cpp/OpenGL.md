GLFW (Graphics Library Framework) is an independent, open-source library that helps you:
	1. Create windows with OpenGL contexts
	2. Handle input (keyboard, mouse, gamepad)
	3. Manage timing and events	
	4. Use multiple monitors, high-DPI displays, etc.

OpenGL is a graphics rendering API, but it doesn't handle window creation or input.

$(SolutionDir) // shows solution path (helps when setting relative paths)


The file opengl32.lib is:
✅ Included with Visual Studio
✅ Part of the Windows SDK (which installs automatically with Visual Studio)

GLEW stands for OpenGL Extension Wrangler Library.
It’s a cross-platform C/C++ library that helps you:
✔️ Load and use modern OpenGL functions beyond version 1.1.
On many systems (especially Windows), the default OpenGL headers only support up to OpenGL 1.1. Anything newer needs to be manually loaded.
GLEW handles this for you by:
Querying the GPU at runtime.
Loading pointers to all available OpenGL functions and extensions.
Letting you call modern OpenGL functions easily.


🟦 Vertex Shader (VS) – What It Does
Executes once per vertex.
Transforms 3D vertex positions to clip space.
Inputs typically include:
Vertex position (e.g., vec3 position)
Optional attributes like color, texture coords, normals
Outputs data to the fragment shader, if needed.
Must assign a value to gl_Position (final position on screen).

🟥 Fragment Shader (FS) – What It Does
Executes once per pixel (fragment) generated from rasterized primitives.
Calculates the final color of each pixel.
Inputs come from the vertex shader (interpolated across pixels).
Must assign a color to an output variable (usually FragColor).