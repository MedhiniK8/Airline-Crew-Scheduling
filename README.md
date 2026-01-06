<div align="center">
  <h1>✈️ Airline Crew Scheduling System</h1>
  <h3>Optimizing Aviation Logistics using Advanced Algorithms</h3>

  <p>
    <a href="#project-overview"><b>📋 Overview</b></a> &nbsp;|&nbsp; 
    <a href="#algorithm-analysis"><b>📊 Algorithm Analysis</b></a> &nbsp;|&nbsp; 
    <a href="#reflections"><b>🧠 Reflections</b></a> &nbsp;|&nbsp; 
    <a href="#sdgs"><b>🌍 SDGs Addressed</b></a> &nbsp;|&nbsp;
    <a href="#about"><b>ℹ️ About</b></a>
  </p>

  <img src="https://img.shields.io/badge/Language-C++-00599C?style=flat-square" alt="C++" />
  <img src="https://img.shields.io/badge/Subject-DAA-orange?style=flat-square" alt="DAA" />
  <img src="https://img.shields.io/badge/Focus-Optimization-success?style=flat-square" alt="Optimization" />
  <img src="https://img.shields.io/badge/Status-Completed-blueviolet?style=flat-square" alt="Status" />
</div>

---

<br>

<a id="project-overview"></a>

<div style="border:1px solid #ddd; padding:24px; border-radius:6px;">

## 1. Project Overview & Details

### **The Problem**
Airline operations run on extremely tight schedules, where even minor inefficiencies can lead to cascading issues. Traditional manual crew scheduling often results in:
- **Operational Conflicts:** Crew members being assigned to overlapping or incompatible flights.
- **Safety Risks:** Violations of mandatory rest requirements, increasing the risk of pilot fatigue.
- **Financial Losses:** Excessive paid idle time where crew remain inactive between assignments.

These challenges highlight the need for an automated, algorithm-driven approach to crew rostering.

### **The Solution**
To address these issues, we developed a **C++-based Airline Crew Scheduling System** that automates the entire rostering process. By modeling **time as a linear resource** and **crew members as independent entities**, the system efficiently assigns flights while ensuring all operational and safety constraints are satisfied. The result is a conflict-free schedule generated within seconds.

### **Key Features**
* **Conflict Detection:** Automatically checks crew availability to prevent overlapping assignments.
* **Rest Enforcement:** Incorporates mandatory post-flight cool-down periods (e.g., 15 minutes) to comply with safety regulations.
* **Cost Optimization:** Applies greedy decision-making to chain compatible flights together, minimizing idle gaps and reducing operational costs.

</div>

<br>

<a id="algorithm-analysis"></a>

<div style="border:1px solid #ddd; padding:24px; border-radius:6px;">

## 2. Analysis of Algorithms

The system follows a structured **Sort–Search–Assign** pipeline to ensure efficiency and scalability.

| Component | Algorithm Used | Complexity | Why this choice? |
| :--- | :--- | :--- | :--- |
| **Timeline Construction** | **Merge Sort** | $O(N \log N)$ | A **stable sorting algorithm** is required to maintain the relative order of flights with identical start times. Unlike QuickSort, Merge Sort guarantees stability. |
| **Crew Lookup** | **Binary Search** | $O(\log M)$ | With thousands of crew members, linear search becomes inefficient. Binary search allows rapid identification of the most suitable available crew member. |
| **Assignment Logic** | **Greedy Strategy** | $O(1)$ | Selecting the crew member with the minimum waiting time provides a locally optimal choice that significantly reduces total idle time and overall cost. |

> **Overall Time Complexity:** $O(N \log N)$  
> Since sorting dominates the pipeline, the system remains highly scalable even for thousands of daily flight records.

</div>

<br>

<a id="reflections"></a>

<div style="border:1px solid #ddd; padding:24px; border-radius:6px;">

## 3. Individual Reflections

### **Student Details**
* **Name:** [Your Name Here]
* **Course:** Design and Analysis of Algorithms (DAA)

### **Learning Outcomes**
This project transformed my understanding of problem-solving from merely writing correct code to designing **efficient, real-world systems**.
1. **Importance of Algorithm Selection:** A naive approach of checking every crew member for every flight would result in $O(N \times M)$ complexity. By integrating binary search, the system was optimized to $O(N \log M)$, yielding a substantial performance improvement.
2. **Constraint Handling:** The most challenging aspect was incorporating real-world constraints such as mandatory rest periods. This experience taught me how classical algorithms must often be adapted rather than applied directly.
3. **Practical Use of STL:** I gained strong hands-on experience with C++ STL components such as `std::sort`, `std::lower_bound`, and custom `struct` design for modeling real entities.

</div>

<br>

<a id="sdgs"></a>

<div style="border:1px solid #ddd; padding:24px; border-radius:6px;">

## 4. Sustainable Development Goals (SDG)

This project contributes meaningfully to several **United Nations Sustainable Development Goals**.

### **SDG 3: Good Health and Well-being**
* **Objective:** Reduce occupational fatigue and enhance workforce well-being.
* **Implementation:** By strictly enforcing a **15-minute mandatory rest period** after each flight, the system minimizes pilot fatigue, ensuring safer operations and improved mental and physical health.

### **SDG 8: Decent Work and Economic Growth**
* **Objective:** Improve productivity through efficient workforce utilization.
* **Implementation:** The optimized scheduling ensures predictable work patterns for crew members while minimizing idle time, leading to both improved working conditions and reduced financial waste.

### **SDG 9: Industry, Innovation, and Infrastructure**
* **Objective:** Promote innovation and modernize operational infrastructure.
* **Implementation:** The project replaces manual, error-prone scheduling with a **robust algorithmic infrastructure**, significantly enhancing efficiency in aviation logistics.

</div>

<br>

<a id="about"></a>

<div style="border:1px solid #ddd; padding:24px; border-radius:6px;">

## About

This project was developed as part of the **Design and Analysis of Algorithms (DAA)** coursework.  
The system demonstrates the practical application of algorithmic concepts to real-world aviation logistics.

> _Student details, institution name, project guide, and acknowledgements will be added here._

</div>

---

<div align="center">
  <p><i>Created for DAA Term Project 2026</i></p>
  <a href="#airline-crew-scheduling-system">⬆️ Back to Top</a>
</div>
