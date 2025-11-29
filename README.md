# cisc121-final-project
application using bubble sort

## Algorithm Name
I have chosen to visualize the bubble sort algorithm. Bubble sort is a simple comparison based sorting algorithm where a pair of element, which are side by side, are compared, and are then appropriately sorted. (i.e. swapped if they are in the wrong order, left alone if they are in the right order). This process repeats until the whole list is sorted. I have picked to do bubble sort for this project for a few reasons:
  1. I feel as though bubble sort, specially for me, is the sorting alogorithm that is most intuative and easiest to understand conceptually
  2. The behaviour of this algorithm is very visual as you can clearly show each comparison and swap.
  3. Although it might not be the most efficient algorithm for sorting, it still demonstrates important ideas that are crucial to understand   sorting algorithms as a whole.

## Problem Breakdown and Computational Thinking
In this section, I will explaining my plan to develop this algorithm and app using the four main computational thinking ideas:
#### Decomposition - breaking the problem into smaller steps
To build this bubble sort app, I have proken the problem into smaller pieces
  1. input:
     - First you must get a list of numbers from the user as a single text input (i.e. 3, 2, 4, 1, 5).
     - For this app, we will just assume that the direction of the sort is ascending.
     - Next, convert the input string into a list of integers.
  2. running the algorithm
     - Loop over the list multiple times.
     - On each pass, compare each pair of adjacent integers.
     - Swap them, if they are out of order
     - Track if any swaps happened during this pass (helps us know when the list is sorted).
  3. connection to UI and displaying results
     - Take the final sorted list and send them back to the Gradio interface as outputs
     - Show the sorted list to the user.
#### Pattern Recognition
Bubble sort is full of repetition and patterns, for example:
  1. looping through the list:
     You repeatedly loop through the list, comparing adjacent elements
  2. patterns for each pair
     For each pair: compare -> possibly swap -> move to the next pair
  3. After each full pass, the largest unsorted element is at the end of the list
  4. The algorithm repeats these steps until no swaps happen in a full pass -> the list is sorted

In the end, repetition is helpful because it helps me and the user visualize each step the same way, leading to internalizing the concept a lot quicker.
#### Abstraction
Abstraction is about simplifying what the user sees on the app
  1. When making this application, I want to make sure the user doesn't see the complexity of the indices, loops, or the code itself.
     Instead I want to make sure they:
     - See a box where they may enter the numbers they wish to be.
     - A button to run the sorting
     - Explanation of the steps
     - The final result
       
So, instead of the user seeing the actual code of the algorithm (i.e. loops, if statements etc), the app would abstract these processes into something more commonly understandable. The goal of this app is that it makes this algorithm easier to learn without forcing the user to read raw code.
#### Algorithm Design
Here is the plan of how the app will work from input to output:
  1. input
    - User types in a list of numbers into a textbook -> app turns this string into a list
  2. processing (sorting)
    - Set swapped = True to begin
    - While swapped is true -> set swapped = False -> loop from the start of the list to the end -> for each index i, compare arr[i] and
     arr[i+ 1] -> if arr[i] > arr[i+1] swap and swapped = True -> record each comparison and swap as a step
  3. output
    - after the loop finishes (i.e. no swaps in final pass), return: the sorted list and the list of steps in order to make the algorithm
     comprehensible

