# **PHASE 1 — Graphics Foundations (Before Code)**

Learn the essential 3D concepts so you understand what Three.js/OpenGL are doing.

### **Core 3D Math**

- Coordinate systems (world, view, model, NDC)
    
- Vectors & vector operations
    
- Matrices (rotation, scaling, translation)
    
- Matrix multiplication order
    
- Homogeneous coordinates
    
- Perspective projection & FOV
    
- Quaternions (basic understanding)
    

### **Rendering Pipeline Basics**

- What is rasterization?
    
- What is a shader?
    
- How vertices → fragments → pixels
    

---

# **PHASE 2 — Three.js (High-Level 3D Engine)**

Goal: Learn 3D graphics through a simpler abstraction.

---

## **Stage 2.1 — Essentials**

- Creating a Scene
    
- PerspectiveCamera vs OrthographicCamera
    
- Renderer basics (WebGLRenderer)
    
- Mesh, Geometry, Material
    
- Lights (ambient, point, directional, spot)
    
- Shadows (basic shadow maps)
    
- OrbitControls
    

---

## **Stage 2.2 — Intermediate Topics**

- BufferGeometry (custom geometries)
    
- Texture mapping
    
    - UVs
        
    - normal maps
        
    - roughness/metalness maps
        
- Environment maps / HDRI lighting
    
- Physically Based Rendering (PBR)
    
- Animation
    
    - keyframe animation
        
    - skeletal animation (+ mixers)
        
- Raycasting (picking objects)
    
- Loading external assets (GLTF, OBJ)
    

---

## **Stage 2.3 — Advanced Three.js**

- Custom Shaders using **ShaderMaterial**
    
    - vertex shaders
        
    - fragment shaders
        
- Using node-based material system
    
- Post-processing (bloom, DOF, SSAO)
    
- Instancing / GPU-driven rendering
    
- GPGPU in Three.js
    
- Procedural meshes
    
- Procedural textures / noise (Perlin/Simplex/Worley)
    
- Physics engines integration (Cannon.js, Ammo.js)
    
- Performance optimization
    
    - draw calls
        
    - texture atlas
        
    - mipmaps
        
    - LOD
        

---

# **PHASE 3 — OpenGL Theory (The Real Pipeline)**

Before coding OpenGL, learn its architecture and workflow:

---

## **Stage 3.1 — Modern Graphics Pipeline**

- GPU pipeline overview
    
- Vertex processing
    
- Clipping & rasterization
    
- Fragment stage
    
- Framebuffer output
    

---

## **Stage 3.2 — Shaders in Depth**

- GLSL basics
    
- Vertex shader structure
    
- Fragment shader structure
    
- Types, uniforms, varyings
    
- Transform matrices manually (model, view, projection)
    
- Lighting equations (Phong, Blinn-Phong)
    
- Microfacet BRDF basics (PBR)
    

---

# **PHASE 4 — OpenGL (Low-Level)**

Shift to hands-on OpenGL (C++, WebGL2, or Rust).

---

## **Stage 4.1 — OpenGL Basics**

- Creating a window (GLFW/SDL)
    
- Creating a GL context
    
- Clearing buffers
    
- VAO, VBO
    
- Drawing triangles
    
- Writing shaders from scratch
    
- Passing uniforms
    
- Textures (2D textures, samplers)
    
- Projection and view matrices manually
    

---

## **Stage 4.2 — Intermediate OpenGL**

- Depth buffer
    
- Stencil buffer
    
- Model loading (Assimp)
    
- Lighting
    
    - directional
        
    - point
        
    - spot
        
    - attenuation
        
- Shadow mapping
    
- HDR
    
- Cubemaps
    
- Framebuffers
    
- Post-processing pipeline
    

---

## **Stage 4.3 — Advanced OpenGL**

- Instancing
    
- Deferred rendering
    
- PBR shaders (GGX, Smith, Fresnel)
    
- Skyboxes & IBL (image-based lighting)
    
- SSAO / SSR
    
- GPU particles
    
- Compute shaders (if using OpenGL 4.3+)
    

---

# **PHASE 5 — Performance, Architecture, and Engine Design**

To master both systems:

- Scene graph theory
    
- Culling (frustum, occlusion, HZB)
    
- BVH structures
    
- GPGPU concepts
    
- Optimizing draw calls
    
- Multi-pass rendering architecture
    
- Tiled/clustered forward+ rendering
    
- Basics of real-time ray tracing
    

---

# **PHASE 6 — Build Projects to Cement Knowledge**

### **Three.js Project Ideas**

- 3D product viewer
    
- Solar system simulation
    
- Procedural terrain generator
    
- Custom shader effects (water, fire, particles)
    

### **OpenGL Project Ideas**

- Write your own mini-engine
    
- Custom PBR pipeline
    
- Terrain renderer
    
- GPU particle system
    
- Deferred renderer
    

---

# 🧭 **OPTIONAL: Combined Master Path**

If you want to integrate both:

1. Build a project in Three.js
    
2. Rebuild parts of it in raw OpenGL
    
3. Implement custom shaders in both
    
4. Optimize performance using GPU techniques