CUDA Stream Compaction
======================

**University of Pennsylvania, CIS 565: GPU Programming and Architecture, Project 2**

* Zach Corse
  * LinkedIn: https://www.linkedin.com/in/wzcorse/
  * Personal Website: https://wzcorse.com
  * Twitter: @ZachCorse
* Tested on: Windows 10, i7-6700HQ @ 2.60GHz 32GB, NVIDIA GeForce GTX 970M (personal computer)

## README

Introduction
------------

In this project I take a stab at implementing a scan algorithm on the GPU and compare the performance with a straightforward implementation on the CPU. For those not familiar with scan, this algorithm accepts an array idata of numbers then returns an array odata such that each element in odata is the sum of all elements in idata that precede the index in consideration (specifically, this is known as an exclusive scan, because the value stored at the index in consideration in idata is not included in the sum).

I also include a parallel implementation of the compact algorithm, which uses scan as part of its implementation. This algorithm accepts an array of data, converts this array into an array of booleans according to a predefined rule (in this case, is the value zero or not), then "removes" the values that are false, thereby compacting the original array into one which preserves the array's remaining useful information.

Scan Performance Analysis
------------



![graph1](img/scanCompare.png)

Compact Performance Analysis
------------

![graph1](img/compactCompare.png)
