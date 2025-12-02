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
  3. processing (sorting)
     - Set swapped = True to begin
     - While swapped is true -> set swapped = False -> loop from the start of the list to the end -> for each index i, compare arr[i] and
     arr[i+ 1] -> if arr[i] > arr[i+1] swap and swapped = True -> record each comparison and swap as a step
  5. output
     - after the loop finishes (i.e. no swaps in final pass), return: the sorted list and the list of steps in order to make the algorithm
     comprehensible

## Hugging Face Link & Steps to Run

The link to my application is here: https://huggingface.co/spaces/marianagonzalezv/Bubble-Sort-CISC-121

#### What are the steps to run?
  1. Open the Hugging Face space link
  2. Enter a list of numbers in the input textbox (must be seperated by commas or spaces)
  3. Click the "Click to sort!" button
  4. Then you are able to view:
     - the sorted result in the first box
     - the step-by-step explanation of the "Bubble Sort" in the second box
## Screenshots of Demos
Below you can see the [] test cases I chose to run

1. Empty Input
   #### Input:
   " " (blank input)
<img width="581" height="474" alt="Screenshot 2025-11-29 at 11 49 42 PM" src="https://github.com/user-attachments/assets/d4b33b2a-3005-40e8-8c5d-d3d928630dd8" />

2. One Number Only
   #### Input:
   "5"
<img width="472" height="370" alt="Screenshot 2025-11-29 at 11 51 33 PM" src="https://github.com/user-attachments/assets/08df8380-bf33-4f11-8e01-fbafdf1df11f" />

3. Already Sorted List
   #### Input:
   "1 2 3 4 5"
<img width="458" height="533" alt="Screenshot 2025-11-29 at 11 52 42 PM" src="https://github.com/user-attachments/assets/80d59b6b-27b3-45b4-8ecc-b827eae6e74c" />

4. Reverse Order
   #### Input:
   "5 4 3 2 1"
<img width="437" height="620" alt="Screenshot 2025-11-30 at 12 04 28 AM" src="https://github.com/user-attachments/assets/bf810a4b-6b50-4b53-8572-1ef3d3550656" />

<img width="490" height="407" alt="Screenshot 2025-11-30 at 12 04 46 AM" src="https://github.com/user-attachments/assets/89057586-caa5-49de-8b44-25ae69d8ab1b" />
<img width="474" height="424" alt="Screenshot 2025-11-30 at 12 05 05 AM" src="https://github.com/user-attachments/assets/7ff70b4f-e7d3-4bb4-80f5-4ed3f3ec43be" />

5. Repeated Value
   #### Input:
   "4 1 4 3 4"
<img width="693" height="616" alt="Screenshot 2025-11-30 at 12 08 33 AM" src="https://github.com/user-attachments/assets/a64c6591-70f9-4f27-a3fd-83b79c1230f1" />
<img width="440" height="378" alt="Screenshot 2025-11-30 at 12 08 55 AM" src="https://github.com/user-attachments/assets/3238c4dd-9875-4bf4-90d5-8ab5ee631edb" />

6. Negative Numbers
   #### Input:
   "3 -1 5 -2"
<img width="595" height="622" alt="Screenshot 2025-11-30 at 12 10 04 AM" src="https://github.com/user-attachments/assets/05a3734b-9398-44f6-a7fd-703ed2addecb" />
<img width="486" height="381" alt="Screenshot 2025-11-30 at 12 10 21 AM" src="https://github.com/user-attachments/assets/04014da9-6d9a-4279-bbec-0d4b50539819" />

7. Comma-Seperated
   #### Input:
   "5, 4, 7, 2"
<img width="618" height="617" alt="Screenshot 2025-11-30 at 12 11 49 AM" src="https://github.com/user-attachments/assets/52b1b9a1-30db-423e-8581-5f7da549d823" />
<img width="476" height="381" alt="Screenshot 2025-11-30 at 12 12 09 AM" src="https://github.com/user-attachments/assets/90bf2961-d2a1-43aa-8ff5-d90e49216f85" />

8. Both Comma and Space Seperated
   #### Input:
   "5, 4 7, 2"
<img width="619" height="610" alt="Screenshot 2025-11-30 at 12 13 16 AM" src="https://github.com/user-attachments/assets/24653c0c-e5a7-4e21-a962-ad76fd52d94c" />
<img width="574" height="377" alt="Screenshot 2025-11-30 at 12 13 27 AM" src="https://github.com/user-attachments/assets/9bf76dc8-2f54-4ac9-90f1-6ca6f123324d" />

9. Non-Number Input
   #### Input:
   "4 3 2 x 6"
<img width="598" height="237" alt="Screenshot 2025-11-30 at 12 14 15 AM" src="https://github.com/user-attachments/assets/a4769bb6-ce2a-4aad-97be-737f19c2cbd7" />

All of the above test cases came back with what was the predicted result, therefore we can conclude that this application works correctly.

## Author & Acknowledgment

This code was written by Mariana Gonzalez

AI Disclaimer: Chat-GPT was used in order to correct the Gradio UI code, and help guide the making of the theme and the "wrapping".

Other sources used:

https://www.gradio.app/guides/theming-guide 

https://www.gradio.app/guides/the-interface-class 


   
   
   


