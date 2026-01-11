<h1 align="center">Optimization of Electric Bus</h1>

<p align="center">
  <strong>Optimize the battery and scheduling of the electric bus at Binghamton University bus routes — New York.</strong>
</p>

<p align="center">
  <a href="https://www.sciencedirect.com/science/article/abs/pii/S0360544220319629">
    <img src="https://img.shields.io/badge/Paper-ScienceDirect-blue?style=for-the-badge" alt="Paper Link">
  </a>
</p>

<hr />

<h2>🚍 Energy-Feasible Route Optimization for Electric Transit Buses (OCCT Case Study)</h2>

<p>
  This project implements an <strong>energy-aware routing model</strong> for electric transit buses using real route-segment data from the <strong>Orange County Transportation Authority (OCCT)</strong>. The goal is to determine <strong>which sequences of road segments (sub-arcs) form a feasible and optimal route</strong> between two terminals, subject to <strong>battery capacity and vehicle physics constraints</strong>.
</p>

<p>
  The model is written in <b>Julia</b> and executed using <b>Jupyter Notebook</b>.
</p>

<hr />

<h2>📌 Project Objectives</h2>
<p>Electric buses must follow routes that are not only short or fast, but also <strong>energy-feasible</strong>. This project answers:</p>
<ul>
  <li>Which combinations of route segments can connect an origin to a destination?</li>
  <li>How much <strong>energy</strong> does each segment require?</li>
  <li>Which routes <strong>respect battery limits</strong>?</li>
  <li>Which feasible route <strong>minimizes energy consumption</strong>?</li>
</ul>

<hr />

<h2>📂 Project Structure</h2>
<pre>
DWC_OCCT/
│
├── DWC_OCCT case study_Final-Segments only.ipynb   # Main Julia notebook
├── OCCT_Routes Info.csv                            # Route segment data
└── README.md                                       # Project documentation
</pre>

<hr />

<h2>🧠 Model Overview</h2>
<p>The system models the transit network as a <strong>directed graph of route segments</strong> (sub-arcs):</p>
<ul>
  <li><strong>Each segment has:</strong>
    <ul>
      <li>Distance</li>
      <li>Speed</li>
      <li>Road grade (slope)</li>
    </ul>
  </li>
  <li><strong>Energy is computed using vehicle physics:</strong>
    <ul>
      <li>Rolling resistance</li>
      <li>Aerodynamic drag</li>
      <li>Gravity (grade)</li>
    </ul>
  </li>
</ul>
<p align="center">
  <i>A route is feasible if the bus <strong>never drops below a minimum battery level</strong> while traversing segments.</i>
</p>
