# Geometry, Differential and Integral Calculus, Statistics: Mathematics in the Production of Plastic Products
### Преводът на английски е с лошо качество, но се оказа нелепо изискване към проекта. В този си вид, проекта може да е доста неясен или с сгрешени термини. На български език, проект щеше да е чист от грешки, в доста по-голяма степен.
Plastic products are all around us. At first glance, the process appears quick and simple. My previous project, [QCS - Quality Control System](https://qcs.ishistack.dev) — [GitHub project repo](https://github.com/KamenKadiyski/QCS) — focused on the accessible and visible aspects of this process.
However, a great deal of mathematics lies behind every single product. This ranges from mold design and the mathematical relationships governing the injection of molten plastic, to cooling times and the statistical control of production processes. As a supervisor at one of the manufacturing facilities of [What More UK Ltd](https://www.whatmoreuk.com), I am required to have a deep understanding of the critical details involved in production. With the assistance of **Rob Walker (Manufacturing Director)**, **Matteo Sampaolesi (Product and Tool Designer)**, and **Lee Hugman (Quality Manager)**, I aim to illustrate aspects of the production process through the lens of mathematics. As the creator of this project, I do not claim that the information presented is exhaustive. Some of the material is used for training newly appointed "setters" (staff responsible for configuring, starting up, and maintaining the machinery). Another source is [https://www.ptonline.com](https://www.ptonline.com) — a specialized website covering techniques, practices, technologies, and other topics related to the manufacturing of plastic products.
Several of the company's most frequently manufactured products are featured here; for three of these, data was also collected directly from the machines during the production run. The `data` folder contains images of the trend charts from the three machines from which the data was extracted.
## Project Structure
The project is divided into several modules:
1. Geometry and Linear Algebra: Why calculating shrinkage is important for designing the mold for a specific product [modul1.ipynb](modul1.ipynb)
2. Differential and Integral Calculus: Cooling and thermodynamics are critical for productivity [modul2.ipynb](modul2.ipynb)
3. Numerical Methods: The relationship between pressure, volume, and temperature [modul3.ipynb](modul3.ipynb)
4. Statistics and Probability, and their connection to quality control [modul4.ipynb](modul4.ipynb) [modul5.ipynb](modul5.ipynb) [modul6.ipynb](modul6.ipynb)

**Note:** The project is based on an actual production environment, and the product data is real. It also utilizes real data regarding the materials used in actual production.


---

## Brief Glossary of Technical Terms for BMB eKW Hybrid Machines (Various Models)

To ensure this project is fully understandable, here are the definitions of the most important terms found on the machine screens and components, explained with accessible examples:

### 1. Screw
*   **What it is:** A large metal screw located inside the machine's barrel.
*   **Real-world example:** It functions exactly like the mechanism inside a **household meat grinder**. As it rotates, it draws solid plastic granules from the hopper, works them until they melt, and gathers the material at the front, ready for injection. It then acts like a **syringe plunger**, injecting the molten plastic into the mold.

### 2. Residual Cushion (Cushion position)
*   **What it is:** A small amount of molten plastic (typically a few millimeters) that remains in front of the screw after the injection and mold-filling process is complete.
*   **Why it matters:** It acts as a **hydraulic buffer (cushion)**. Its purpose is to absorb pressure, preventing the metal screw from striking the front of the barrel (metal-on-metal contact). If the cushion drops to 0 mm, the part may end up hollow or incompletely filled, as the machine would lack the material needed to apply the pressure required to compact the plastic.

### 3. Torque (Maximum & Mean torque)
*   **What it is:** The force with which the electric motor rotates the screw to process and melt the plastic granules. It is measured in Newton-meters (Nm).
*   **Real-world example:** Imagine mixing thick dough with a mixer. If the dough is thin, the mixer spins easily (low torque). If you add too much flour, the mixer begins to struggle and requires much more force to keep turning (high torque). In the machine, *Mean torque* represents the average load on the motor, while *Maximum torque* is the peak load (strain) reached during rotation.

### 4. Plasticizing (Plasticizing time / position)
*   **What it is:** The process of taking solid material from the hopper, melting it via the rotation of the screw, and preparing the precise dose for the next part.
*   **In short:** This is the time (in seconds) and distance (in mm) during which the machine "chews up" and prepares the next batch of molten plastic.

### 5. Switch-over pressure
*   **What it is:** The pressure at the exact moment the machine stops the rapid filling of the mold and shifts into a slow "packing" mode (holding under pressure).
*   **Real-life example:** It is like driving a car fast, then—just before a traffic light—releasing the gas pedal and gently applying the brakes. If the switch-over happens too early, the part will be underfilled. If it happens too late, the plastic...