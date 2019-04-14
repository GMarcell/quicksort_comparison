# Sequential and Parallel Quicksort Comparison
This repository is created to compare the time needed for sequential and parallel quicksort on Ubuntu, the quicksort file is build on C programming language and sample datas are provided in txt file format.

## Author
Winston Renatan (01082170030) - Informatics 2017

## Requirement
[GCC](https://linuxconfig.org/how-to-install-gcc-the-c-compiler-on-ubuntu-18-04-bionic-beaver-linux)

## Installation/running instruction
- Download the files on folder "Quicksort".
- Open terminal and get to the directory path (the place where you put the files).
- Type on "g++ quicksort.c -o quicksort -fopenmp" to compile the sequential quicksort. While "g++ quicksort_parallel.c -o quicksort_parallel -fopenmp" for parallel quicksort. Those command are written without quotations marks.
* For parallel quicksort if the above command fails, try "g++ quicksort_parallel.c -o quicksort_parallel -fopenmp -fpermissive" without quotes.
- After successfully compiling the file, execute it with the command "./quicksort (samplesize).txt" without quotes. (samplesize) will be changed with 10, 100, 1000, or 10000. Remember to delete the brackets.

## Sample Input and Time Data
These are the result of testing with both sequential and parallel quicksort from the txt data given. Here, I tried to test for four times and take the average result for the comparison.

### Sequential Quicksort

|Sample     |Test 1    |Test 2    |Test 3    |Test 4    |Average Time|
|-----------|----------|----------|----------|----------|------------|
|10         |0.000001 s|0.000001 s|0.000001 s|0.000002 s|0.00000125 s|
|100        |0.000019 s|0.000026 s|0.000024 s|0.000019 s|0.000022   s|
|1000       |0.001536 s|0.001197 s|0.001207 s|0.001171 s|0.00127775 s|
|10000      |0.078862 s|0.077264 s|0.068457 s|0.071036 s|0.07390475 s|

### Parallel Quicksort

|Sample     |Test 1     |Test 2     |Test 3     |Test 4     |Average Time |
|-----------|-----------|-----------|-----------|-----------|-------------|
|10         |0.002145  s|0.002289  s|0.002487  s|0.002119  s|0.00226     s|
|100        |0.031561  s|0.022758  s|0.036844  s|0.021882  s|0.02826125  s|
|1000       |0.809316  s|0.57997   s|0.761541  s|0.681523  s|0.7080875   s|
|10000      |23.721832 s|39.074071 s|27.364098 s|38.899388 s|32.26484725 s|

## Explanation and Comparison
The above data might differ as it is different time process using one machine and another. After test is done, we would like to see the data compared in a graph from the average time of each sample as below. With the orange line as parallel quicksort while blue line as sequential quicksort.

### Singular Quicksort vs Parallel Quicksort Time Comparison

|Sample     |Sequential  |Parallel     |
|-----------|------------|-------------|
|10         |0.00000125 s|0.00226     s|
|100        |0.000022   s|0.02826125  s|
|1000       |0.00127775 s|0.7080875   s|
|10000      |0.07390475 s|32.26484725 s|

![SeqAndPar](https://github.com/winstonrenatan/quicksort_comparison/blob/master/SeqAndPar.PNG)<br>

### Result
As the result we could see that parallel quicksort takes more time compared to sequential quicksort. That happens especially when the sample size increase to bigger size. Where at 10-1000 samples, it may takes 0. seconds and it increase much bigger when the data becomes 10000. When working with parallel quicksort there are some jobs that should be done such as parallelism job, spawning thread, synchronization time, etc. On the other hand, sequential sort is just doing the sort normally with algorithm given without any supplement on parallelism tasks.

## Acknowledgements
- [Quicksort Program](https://github.com/markwkm/quicksort)
- [Guidebook Quicksort Algorithm](https://pdfs.semanticscholar.org/cba9/770c4fad941fe5e501539525953a242a36f8.pdf)
