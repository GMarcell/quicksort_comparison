# Pararell & Normal Quicksort Comparison
Pararell VS Normal Quicksort Time Comparison (Operating System UPH 2017/2018)

## Author

Grand Marcell

## Requirement
[GCC](https://linuxconfig.org/how-to-install-gcc-the-c-compiler-on-ubuntu-18-04-bionic-beaver-linux)

## Installation
1. Download the files from the repository

2. Compile the files using "make" on the terminal in the quicksort directory

3. Execute the program using "./quicksort (sample file)" for sequential sort and "./quicksort-p

## Sample Input and Time Data
Test is done with both sequential and parallel quicksort programs to find the average time taken to finish quicksorting with a sample size of 10, 100, 1000 and 10000.

### Sequential Quicksort

|Sample     |Test 1    |Test 2    |Test 3    |Test 4    |Average Time|
|-----------|----------|----------|----------|----------|------------|
|10         |0.000001 s|0.000001 s|0.000001 s|0.000002 s|0.00000125 s|
|100        |0.000020 s|0.000028 s|0.000023 s|0.000021 s|0.00002300 s|
|1000       |0.001540 s|0.001203 s|0.001214 s|0.001180 s|0.00128425 s|
|10000      |0.078870 s|0.077260 s|0.068465 s|0.071040 s|0.07390875 s|

### Parallel Quicksort

|Sample     |Test 1     |Test 2     |Test 3     |Test 4     |Average Time |
|-----------|-----------|-----------|-----------|-----------|-------------|
|10         |0.0021460 s|0.0022910 s|0.0024890 s|0.0021190 s|0.002261250 s|
|100        |0.0315610 s|0.0227560 s|0.0368460 s|0.0218820 s|0.028261300 s|
|1000       |0.8093180 s|0.5799720 s|0.7615440 s|0.6815239 s|0.708089475 s|
|10000      |23.721842 s|39.074091 s|27.364068 s|38.899358 s|32.26483980 s|

## Explanation and Comparison
The above data might differ as it is different time process using one machine and another. After test is done, we would like to see the data compared in a graph from the average time of each sample as below. With the orange line as parallel quicksort while blue line as sequential quicksort.

### Singular Quicksort vs Parallel Quicksort Time Comparison

|Sample     |Sequential  |Parallel     |
|-----------|------------|-------------|
|10         |0.00000125 s|0.002261250 s|
|100        |0.00002300 s|0.028261300 s|
|1000       |0.00128425 s|0.708089475 s|
|10000      |0.07390875 s|32.26483980 s|

![SeqAndPar](https://github.com/winstonrenatan/quicksort_comparison/blob/master/SeqAndPar.PNG)<br>

### Result
As the result we could see that parallel quicksort takes more time compared to sequential quicksort. That happens especially when the sample size increase to bigger size. Where at 10-1000 samples, it may takes 0. seconds and it increase much bigger when the data becomes 10000. When working with parallel quicksort there are some jobs that should be done such as parallelism job, spawning thread, synchronization time, etc. On the other hand, sequential sort is just doing the sort normally with algorithm given without any supplement on parallelism tasks.

## Acknowledgements
- [Quicksort Program](https://github.com/markwkm/quicksort)
- [Guidebook Quicksort Algorithm](https://pdfs.semanticscholar.org/cba9/770c4fad941fe5e501539525953a242a36f8.pdf)
