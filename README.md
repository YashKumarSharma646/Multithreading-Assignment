# 🚀 Multithreading Performance Analysis using C++

## 📌 Overview
This project demonstrates the use of **multithreading in C++** to optimize matrix multiplication. The goal is to analyze how execution time varies with different numbers of threads and to understand the relationship between performance and CPU cores.

---

## 🎯 Objective
- Implement matrix multiplication using multithreading  
- Compare execution time for different thread counts  
- Identify optimal thread usage based on system capabilities  

---

## ⚙️ Methodology

- A constant matrix **B** is generated once.
- Multiple random matrices **A** are generated.
- Each matrix is multiplied with matrix **B**.
- The workload is divided among threads by splitting matrix rows.
- Execution time is recorded for thread counts ranging from **1 to 12**.

---

## 🧵 Multithreading Approach

- Each thread is assigned a subset of rows from the result matrix.
- Threads execute in parallel to improve computation speed.
- All threads are synchronized using \`join()\` before proceeding.
- The program repeats the computation multiple times to simulate real workload.

---

## 📊 Results

| Threads | Time (seconds) |
|--------|----------------|
| 1 | 16.0855 |
| 2 | 9.0761 |
| 3 | 6.45175 |
| 4 | 5.06928 |
| 5 | 5.65618 |
| 6 | 5.76355 |
| 7 | 4.60821 |
| 8 | 4.28391 |
| 9 | 4.01976 |
| 10 | 3.74098 |
| 11 | 3.8142 |
| 12 | 3.89822 |

---

## 📈 Performance Graph

![Execution Time Graph](graph.png)

---

## 🖥️ CPU Utilization

![CPU Usage](cpu_usage.png)

---

## 🧠 Key Observations

- Execution time decreases significantly as the number of threads increases.
- Performance continues improving even beyond the number of physical cores (**6 cores**).
- The best performance is observed around **10 threads**.
- After this point, performance stabilizes due to **thread overhead and context switching**.
- This shows that optimal thread count may slightly exceed core count depending on workload.

---

## ⚠️ Note

Due to hardware limitations, matrix size and number of iterations were reduced while maintaining the behavior of multithreading for analysis purposes.

---

## 🛠️ Technologies Used

- **C++**
- **Multithreading (\`std::thread\`)**
- **MinGW-w64 (GCC 15)**
- **Google Sheets / Excel (for graph)**

---

## ▶️ How to Run

\`\`\`bash
g++ main.cpp -o main -pthread -std=c++11
./main
\`\`\`

---

## 📂 Project Structure

\`\`\`
multithreading-assignment/
│
├── main.cpp
├── README.md
├── graph.png
└── cpu_usage.png
\`\`\`

---

## 💡 Conclusion

This project demonstrates how multithreading can significantly improve performance in computational tasks. It also highlights that optimal performance depends not only on hardware (CPU cores) but also on how effectively workload is distributed among threads.

---

## 👨‍💻 Author

Yash Sharma