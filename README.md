# Sorting Algorithm Comparison

This project compares the performance of three sorting algorithms: Merge Sort, Insertion Sort, and TimSort (a hybrid of Merge Sort and Insertion Sort). The algorithms are tested on different data sizes, and their execution times are analyzed to understand their efficiency.

## Algorithms Tested

1. **Merge Sort**: A divide-and-conquer algorithm that recursively divides the array into halves, sorts them, and then merges them back together.

2. **Insertion Sort**: An algorithm that builds the final sorted array one item at a time, iterating through the elements and moving each one to its correct position.

3. **TimSort**: A hybrid sorting algorithm derived from merge sort and insertion sort. It is used as the default sorting algorithm in Python's `sorted` function.

## Test Data Sizes

The algorithms were tested on the following data sizes:

- 100 elements
- 500 elements
- 1000 elements
- 3000 elements

## Results

The execution times for each algorithm at different data sizes are as follows:

| Data Size |          Merge Sort       |       Insertion Sort     |          TimSort          |
|-----------|---------------------------|--------------------------|---------------------------|
| 100       | 0.004221447999995576 sec  | 0.001012048000006871 sec | 2.9049999994867903e-05 sec|
| 500       | 0.03827931200000023  sec  | 0.024876241000001187 sec | 0.00014606499999558764 sec|
| 1000      | 0.05720707700000105  sec  | 0.10972772499999905  sec | 0.0002928410000038184  sec|
| 3000      | 0.10638130699999238  sec  | 0.7517639619998135   sec | 0.005939822999835087   sec|

## Analysis and Conclusions

### Merge Sort vs. Insertion Sort

- **Merge Sort**: Demonstrates consistent performance across varying data sizes. Its time complexity of O(n log n) ensures efficient sorting, making it suitable for large datasets. However, it incurs higher space complexity due to the need for additional storage during the merging phase.

- **Insertion Sort**: Performs well on small datasets due to its simplicity and lower time complexity (O(n^2)). However, as the dataset grows, its efficiency diminishes compared to Merge Sort. The algorithm's advantage lies in its space efficiency as it sorts in-place.

### TimSort Efficiency

- **TimSort**: Outperforms both Merge Sort and Insertion Sort across all tested data sizes. The hybrid nature of TimSort, combining the strengths of Merge Sort and Insertion Sort, results in a versatile and efficient sorting algorithm. It is particularly effective in real-world scenarios where datasets may have inherent order or partially sorted sections.

### Practical Considerations

- The empirical results support the practical preference for TimSort over Merge Sort and Insertion Sort in Python applications. TimSort's inclusion in the standard library's `sorted` function makes it a convenient and efficient choice for general-purpose sorting tasks.

- While Merge Sort and Insertion Sort have their merits in specific contexts, TimSort strikes a balance, making it a reliable option for a wide range of scenarios.


- In conclusion, the project highlights the effectiveness of TimSort, offering a compelling reason why Python developers often leverage the built-in `sorted` function rather than implementing custom sorting algorithms.
