# Optimization-of-Electric-Bus
Optimize the battery and scheduling of the electric bus at Binghamton University bus routes- New York.
Paper link: https://www.sciencedirect.com/science/article/abs/pii/S0360544220319629
 --- # 🚍 Energy-Feasible Route Optimization for Electric Transit Buses (OCCT Case Study) This project implements an **energy-aware routing model** for electric transit buses using real route-segment data from the **Orange County Transportation Authority (OCCT)**. The goal is to determine **which sequences of road segments (sub-arcs) form a feasible and optimal route** between two terminals, subject to **battery capacity and vehicle physics constraints**. The model is written in **Julia** and executed using **Jupyter Notebook**. --- ## 📌 Project Objectives Electric buses must follow routes that are not only short or fast, but also **energy-feasible**. This project answers: * Which combinations of route segments can connect an origin to a destination? * How much **energy** does each segment require? * Which routes **respect battery limits**? * Which feasible route **minimizes energy consumption**? --- ## 📂 Project Structure
DWC_OCCT/
│
├── DWC_OCCT case study_Final-Segments only.ipynb   # Main Julia notebook
├── OCCT_Routes Info.csv                           # Route segment data
├── README.md                                     # Project documentation
--- ## 🧠 Model Overview The system models the transit network as a **directed graph of route segments** (sub-arcs): * Each segment has: * Distance * Speed * Road grade (slope) * Energy is computed using **vehicle physics**: * Rolling resistance * Aerodynamic drag * Gravity (grade) A route is feasible if the bus **never drops below a minimum battery level** while traversing segments. ---
