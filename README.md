# 🖥️ Computer Graphics Project

## 🎯 Grade 17/20 

This repository contains the practical work developed for the **Computer Graphics** course (3rd year, Computer Science).  
The project is divided into **four phases**, progressively extending the capabilities of a **C++ OpenGL engine** and a **geometry generator**.

<img width="1016" height="1019" alt="image" src="https://github.com/user-attachments/assets/3af4dab5-e1ef-4576-aa9e-4b58fc58f93b" />

---

## 👥 Authors
- Pedro Manuel Pereira dos Santos
- João Manuel Franqueira da Silva
- David Alberto Agra
- João Pedro da Silva Faria

---

## 🌓 Project Phases
Each phase builds upon the previous one:

1. **Phase 1 – Generator & Engine Basics**
   - Implemented a **generator** capable of producing 3D primitives (plane, box, sphere, cone).  
   - Implemented an **engine** to read `.3d` files and **render objects** to the screen.  
   - Introduced **XML parsing** for scene description.  
   - Focus: hierarchical scene construction and first rendering pipeline.

2. **Phase 2 – Transformations & Hierarchy**
   - Extended the **engine** to support **geometric transformations**: translation, rotation, scale.  
   - Allowed **hierarchical modeling** from XML.  
   - Added **new primitive**: **torus** (used for Saturn’s rings).  
   - **Solar System scene** introduced with planets, moons, and rings.  

3. **Phase 3 – Animation & Bezier Surfaces**
   - Added support for **Catmull-Rom curves** (for smooth translations).  
   - Introduced **time-based rotations**.  
   - Implemented **Bezier surfaces** (generator creates complex geometry like a teapot/comet).  
   - Transitioned rendering to **VBOs** for better performance.  
   - Extended XML with attributes to enable/disable axes and curve drawing.  
   - Solar System demo with **animated orbits** and a **Bezier comet**.

4. **Phase 4 – Lighting & Textures**
   - Generator updated to compute **normals** and **texture coordinates** for all primitives (plane, box, sphere, cone, torus, Bezier).  
   - Engine extended with:  
     - **Lighting** (ambient, diffuse, specular, emissive, shininess).  
     - **Texture mapping** from image files.  
     - **VBO support** for vertices, normals, and texture coordinates.  
   - Camera improvements: **zoom in/out**.  
   - Final **Solar System** demo:  
     - Version 1 with only lights.  
     - Version 2 with **realistic textures** applied to celestial bodies.

---

## 🎥 Preview
1. **Phase 1**
   
   <img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/e3c3332d-c8e3-498d-83d1-701f57e81880" /> <img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/61381b94-41c9-4b15-81cd-02277ae1338a" /> <img width="300" height="350" alt="image" src="https://github.com/user-attachments/assets/cdbd11a7-1f49-44b5-b659-3ed1f3e01879" />

2. **Phase 2**

   <img width="500" height="450" alt="image" src="https://github.com/user-attachments/assets/3e758994-25db-4250-b3ff-d627ea278e1d" />

3. **Phase 3**

   <img width="700" height="750" alt="image" src="https://github.com/user-attachments/assets/39722336-86ae-4ca4-9094-cbf72552577d" />

5. **Phase 4**

    <img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/0247fcd8-550f-4121-9acd-d1ec22c0341c" />

---

## ⚙️ Technologies Used

- C++
- OpenGL / GLUT
- TinyXML (for XML parsing)
- GLUT / GLEW (for rendering support)

---

## 🚀 Running the Project

Each phase contains its own generator and engine programs. To Run on Linux do:
```bash
cmake CMakeLists.txt
make
```

- Use the generator to create .3d model files (plane, sphere, torus, Bezier surface, etc.).
- Launch the engine with a given XML scene file to visualize it.

Example:
```bash
./generator sphere 1 50 50 sphere.3d
./engine solar_system.xml
```

---

## 🌌 Demonstration Scene – Solar System

The Solar System is used across all phases as the main test scene:

- Phase 2: static planets + hierarchical moons.
- Phase 3: animated orbits, Catmull-Rom curves, Bezier comet.
- Phase 4: realistic lighting & textures.
