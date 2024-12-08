# Parallel BFS

<p align="start">
  <img src="pictures/img1.png" alt="Image 1" width="400"/>
  <img src="pictures/img2.png" alt="Image 2" width="400"/>
</p>



## Project structure
Everything is done in Kotlin. Here are descriptions of all the classes

| **Class Name**         | **Description**                                                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **BFSRealization**     | A sealed class that serves as the base for bfs implementations, containing the `bfs()` method.                                                  |
| **SequentialBFS**      | A data object that implements the `BFSRealization` interface and performs bfs sequentially (single-threaded) using queue.                       |
| **ParallelBFS**        | A data object that implements the `BFSRealization` interface and performs bfs using parallelism (multi-threaded) and frontier approach.         |
| **BFSRealizationTest** | A unit test class that verifies the correctness of the bfs algorithms and checks that both sequential and parallel approach return same values. |
| **BFSPerformanceTest** | A unit test class that measures and compares the performance of the sequential and parallel bfs algorithms.                                     |

---

## Performance Testing Results

The BFS algorithms were tested on a **12th Gen Intel® Core™ i5-12450H processor** to evaluate their efficiency. The tests compared the performance of sequential and parallel BFS implementations using a cubic graph with the side of 500 nodes, averaged over 5 iterations. Below are the detailed results:

### Sequential BFS

| **Iteration** | **Time (ms)** |
|---------------|---------------|
| 1             | 76191         |
| 2             | 74328         |
| 3             | 79170         |
| 4             | 79506         |
| 5             | 93775         |

**Average sequential BFS time:** **80594.0 ms**

### Parallel BFS

| **Iteration** | **Time (ms)** |
|---------------|---------------|
| 1             | 21204         |
| 2             | 19578         |
| 3             | 19577         |
| 4             | 19813         |
| 5             | 19710         |

**Average parallel BFS time:** **19976.4 ms**

### Performance Comparison
The parallel BFS algorithm is approximately **4.03 times faster** than the sequential BFS algorithm.