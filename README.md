# 🚀 CPM Analyzer & Network Grapher

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Vis.js](https://img.shields.io/badge/Vis.js-Network_Graph-blue?style=for-the-badge)
![Industrial Engineering](https://img.shields.io/badge/Industrial_Engineering-Operations_Research-10b981?style=for-the-badge)

**CPM Analyzer** is an interactive Decision Support System (DSS) developed based on project management and Operations Research principles. By analyzing the durations and dependencies of user-inputted activities, it calculates the project's **Critical Path** and visualizes the results on the screen according to Graph Theory rules.

🔗 **[Explore Live Simulation (Live Demo)](https://onurfgg.github.io/critical-path-dashboard)**

## 📊 Mathematical Background & Methodology

This tool uses a custom JavaScript algorithm in the background to solve complex network topologies. The system follows these stages:

1. **Forward Pass:** Calculates the Earliest Start (ES) and Earliest Finish (EF) times for each activity to determine the minimum project completion time.
2. **Backward Pass:** Moves from the end to the beginning of the network to find the Latest Start (LS) and Latest Finish (LF) times.
3. **Slack Calculation:** Determines the delay tolerances of the activities. Nodes with a slack value of 0 are considered on the **Critical Path**.
4. **Cyclic Graph Protection:** The algorithm prevents the user from accidentally entering predecessors that create an infinite loop (e.g., A -> B and B -> A).

## 🌟 Highlighted Features

* **Dynamic Data Entry:** Any number of activities (Nodes) can be added, and duration and predecessor dependencies can be dynamically defined.
* **Custom SVG Node Engine:** Using the industry-standard Vis.js library, custom vector (SVG) boxes are generated for each node. These boxes contain the ES, EF, LS, and LF values in the 4 corners of the activity, perfectly mirroring academic textbooks.
* **Visual Critical Path Map:** The critical path that creates the project's bottleneck is automatically highlighted with red arrows (Edges) and red nodes on the interactive network map.
* **Auto-Fit and Pan-Zoom:** In large-scale projects, the network map automatically fits the screen constraints (Auto-fit), and the user can navigate or zoom the map smoothly.
* **Detailed Analysis Table:** All calculated values are formatted into a readable matrix table.

## ⚙️ Installation and Usage

The project runs 100% "Client-Side". No server installation or backend configuration is required.

1. Clone the repository to your local machine:
   ```bash
   git clone [https://github.com/onurfgg/BU_KISMA_REPO_ADINI_YAZ.git](https://github.com/onurfgg/BU_KISMA_REPO_ADINI_YAZ.git)
