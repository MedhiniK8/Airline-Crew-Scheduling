<div align="center">
  <h1>✈️ Airline Crew Scheduling System</h1>
  <h3>Optimizing Aviation Logistics using Advanced Algorithms</h3>

  <p>
    <a href="#-1-project-overview--details"><b>📋 Overview</b></a> &nbsp;|&nbsp; 
    <a href="#-2-analysis-of-algorithms"><b>📊 Algorithm Analysis</b></a> &nbsp;|&nbsp; 
    <a href="#-3-individual-reflections"><b>🧠 Reflections</b></a> &nbsp;|&nbsp; 
    <a href="#-4-sustainable-development-goals-sdg"><b>🌍 SDGs Addressed</b></a>
  </p>

  <img src="https://img.shields.io/badge/Language-C++-00599C?style=flat-square" alt="C++" />
  <img src="https://img.shields.io/badge/Subject-DAA-orange?style=flat-square" alt="DAA" />
  <img src="https://img.shields.io/badge/Focus-Optimization-success?style=flat-square" alt="Optimization" />
  <img src="https://img.shields.io/badge/Status-Completed-blueviolet?style=flat-square" alt="Status" />
</div>

---

## 1. Project Overview & Details

### **The Problem**
Airlines operate on tight margins where efficiency is everything. Manual crew scheduling leads to:
 **Operational Conflicts:** Crew double-booked on overlapping flights.
 **Safety Risks:** Violations of mandatory rest periods (pilot fatigue).
 **Financial Loss:** Excessive "paid idle time" where crew wait at airports.

### **The Solution**
We developed a C++ application that automates the rostering process. By treating time as a linear resource and crew as distinct entities, our system generates a conflict-free schedule in seconds.

### **Key Features**
* **Conflict Detection:** Automatically flags if a pilot is busy.
* **Rest Enforcement:** Adds mandatory "cool-down" periods (e.g., 15 mins) post-flight.
* **Cost Optimization:** Uses greedy logic to chain flights together, minimizing idle gaps.

---

## 2. Analysis of Algorithms

We utilized a "Sort-Search-Assign" pipeline to solve the problem efficiently.

| Component | Algorithm Used | Complexity | Why this choice? |
| :--- | :--- | :--- | :--- |
| **Timeline** | **Merge Sort** | $O(N \log N)$ | We need a **stable** sort to arrange flights chronologically. QuickSort is unstable and could mess up the order of simultaneous flights. |
| **Crew Lookup** | **Binary Search** | $O(\log M)$ | Searching linearly through 5,000+ crew members is too slow ($O(M)$). Binary search finds the best fit instantly. |
| **Assignment** | **Greedy Strategy** | $O(1)$ | A "Greedy" choice (picking the pilot who waits the least) provides a locally optimal solution that saves costs globally. |

> **Overall Complexity:** $O(N \log N)$  
> The system is dominated by the sorting step, making it highly scalable for thousands of daily flights.

---

## 3. Individual Reflections

### **Student Details**
* **Name:** [Your Name Here]
* **Course:** Design and Analysis of Algorithms (DAA)

### **Learning Outcomes**
Building this project shifted my perspective from just "writing code" to "engineering solutions."
1.  **Algorithmic selection matters:** I initially considered checking every pilot for every flight, but realized that would be $O(N \times M)$. Switching to Binary Search reduced this to $O(N \log M)$, which is a massive performance gain.
2.  **Handling Constraints:** The hardest part was not the logic, but the *constraints* (like the mandatory rest period). I learned how to modify standard algorithms to fit real-world rules.
3.  **Standard Template Library (STL):** I gained deep proficiency in C++ STL tools like `std::sort`, `std::lower_bound`, and `structs`.

---

## 4. Sustainable Development Goals (SDG)

This project aligns with the United Nations SDGs to promote a better future.

### **💚 SDG 3: Good Health and Well-being**
* **Target:** Prevent workforce burnout.
* **Implementation:** By algorithmically enforcing a strict **15-minute rest period** after every flight, we prevent pilot fatigue. This ensures the physical and mental well-being of the crew and the safety of passengers.

### **📈 SDG 8: Decent Work and Economic Growth**
* **Target:** Higher economic productivity through diversification and technological upgrading.
* **Implementation:** The system optimizes the workforce, ensuring "Decent Work" (predictable schedules) and preventing financial waste (idle time), which contributes to the airline's economic stability.

### **🏗️ SDG 9: Industry, Innovation, and Infrastructure**
* **Target:** Upgrade infrastructure and retrograde industries.
* **Implementation:** We replaced error-prone manual rostering with a **modern computational infrastructure**. This is a direct upgrade to aviation logistics efficiency.

---

<div align="center">
  <p><i>Created for DAA Term Project 2026</i></p>
  <a href="#-airline-crew-scheduling-system">⬆️ Back to Top</a>
</div>
