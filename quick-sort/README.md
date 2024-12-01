# Parallel quick sort

<p align="start">
  <img src="pictures/img1.png" alt="Image 1" width="400"/>
  <img src="pictures/img2.png" alt="Image 2" width="400"/>
</p>



## Project structure
Everything is done in Kotlin. Here are descriptions of all the classes

| **Class Name**        | **Description**                                                                                      |
|------------------------|-----------------------------------------------------------------------------------------------------|
| **Sorter**            | A sealed class that serves as the base for sorting implementations, containing the `sort()` method. |
| **SequentialSorter**  | A data object that implements the `Sorter` interface and performs sorting sequentially (single-threaded). |
| **ParallelSorter**    | A data object that implements the `Sorter` interface and performs sorting using parallelism (multi-threaded). |
| **SorterTest**        | A unit test class that verifies the correctness of the sorting algorithms.                          |
| **SorterPerformanceTest** | A unit test class that measures and compares the performance of the sequential and parallel sorting algorithms. | 

Here’s the updated README section with a table for better clarity:

---

## Performance Testing Results

The sorting algorithms were tested on a **12th Gen Intel® Core™ i5-12450H processor** to evaluate their efficiency. The tests compared the performance of sequential and parallel sorting implementations using a randomly generated array of \(10^8\) elements, averaged over 5 iterations. Below are the detailed results:

### Sequential Sorting
The sequential sorting implementation processes the array on a single thread.

| **Iteration** | **Time (ms)** |
|---------------|---------------|
| 1             | 9516          |
| 2             | 9425          |
| 3             | 9423          |
| 4             | 9462          |
| 5             | 13534         |

**Average sequential sort time:** **10272.0 ms**

### Parallel Sorting
The parallel sorting implementation leverages multiple threads to process the array concurrently.

| **Iteration** | **Time (ms)** |
|---------------|---------------|
| 1             | 4617          |
| 2             | 3281          |
| 3             | 2828          |
| 4             | 2823          |
| 5             | 2840          |

**Average parallel sort time:** **3277.8 ms**

### Performance Comparison
The parallel sorting algorithm is approximately **3.13 times faster** than the sequential sorting algorithm.