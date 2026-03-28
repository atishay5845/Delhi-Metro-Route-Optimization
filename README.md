🚇 Delhi Metro Route Optimization System (C++)

A graph-based route optimization system built in C++ to compute the shortest metro route and fare between two stations using classic Data Structures and Algorithms.
The project models a real-world metro network and applies Dijkstra’s Algorithm, priority queues (min-heaps), and graph traversal techniques to deliver accurate and efficient results.

📌 Problem Statement

Navigating a large metro network efficiently requires identifying the shortest possible route between two stations while considering distances and travel cost.

This project solves the problem by:
Modeling metro stations as nodes
Modeling metro routes as weighted edges
Computing the shortest path between source and destination
Calculating the fare based on total travel distance

🎯 Project Objectives

Apply graph data structures to a real-world transportation problem
Implement Dijkstra’s Algorithm for shortest path computation
Use priority queues (min-heaps) for performance optimization
Compare BFS and DFS traversal strategies
Demonstrate clean, modular, and maintainable C++ code

🛠 Tech Stack

Language: C++
Core Concepts:
Graphs (Adjacency List)
Dijkstra’s Algorithm
Priority Queue (Min-Heap)
BFS & DFS

Tools:
VS Code
Git & GitHub
🧠 System Design Overview
Graph Representation

Each metro station is represented as a node

Each route between stations is a weighted edge

Graph is implemented using an adjacency list for memory efficiency

Station A ----(distance)---- Station B

⚙️ Algorithms Used
1️⃣ Dijkstra’s Algorithm (Core Algorithm)

Used to compute the shortest path between two stations in a weighted graph.

Why Dijkstra?

Metro routes have different distances

BFS fails for weighted graphs

Guarantees shortest path efficiently

Time Complexity:

O((V + E) log V) using min-heap

2️⃣ Priority Queue (Min-Heap)

Used to:

Always process the station with minimum current distance

Optimize Dijkstra’s performance

Implemented using C++ STL:

priority_queue<pair<int, int>, vector<pair<int, int>>, greater<>> pq;

3️⃣ BFS & DFS (Traversal Comparison)

Implemented to analyze route exploration behavior

Helps understand why BFS/DFS are not suitable for weighted shortest-path problems

Algorithm	Suitable for Shortest Path
BFS	❌ (only unweighted graphs)
DFS	❌
Dijkstra	✅
💰 Fare Calculation Logic

Total fare is calculated based on the sum of distances along the shortest path

Demonstrates real-world application of algorithm output

Example:

Total Distance: 18 km
Fare: ₹45

📂 Project Structure
Delhi-Metro-Route-Optimization/
│
├── src/
│   ├── main.cpp        # Program entry point
│   ├── graph.h         # Graph class definition
│   └── graph.cpp       # Graph implementation
│
├── data/
│   └── metro_map.txt   # Station & route data
│
├── README.md

▶️ How to Run the Project
Prerequisites

C++ Compiler (g++, clang)

VS Code or any C++ IDE

Compile
g++ src/main.cpp src/graph.cpp -o metro

Run
./metro

🧪 Sample Output
Enter Source Station: Rajiv Chowk
Enter Destination Station: Kashmere Gate

Shortest Route:
Rajiv Chowk -> New Delhi -> Chandni Chowk -> Kashmere Gate

Total Distance: 12 km
Total Fare: ₹30
