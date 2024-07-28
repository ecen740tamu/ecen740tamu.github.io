### Coding Prep

take an example 

unsorted=[4,3,10,5,1]

bubble sort changes order of elements one at a time.
untill there are no more swaps possible


unsorted=[4,10,5,1,0]

step 1:
  4 10 5 1 0
step 2:
  4 5 10 1 0
step 3:
  4 5 1 10 0
step 4:
  4 5 1 0 10
step 5:
  4 1 5 0 10
step 6:
  4 1 0 5 10
step 7:
  4 0 1 5 10
step 8:
  4 0 1 5 10
step 9:
  0 4 1 5 10
step 10:
  0 1 4 5 10
step 11-16: done


write logic first then keep all the variables inside a 

I need a variable to keep track of swaps
I have to loop through as many times as possible, so while with a condition works
and since the complexity is O(n2), we have two loops

Look for loops

Small repetitive tasks go to functions

What are the fail conditions: 1 what if the entire array has same values

Is the list empty

Example

use enumerate, instead of 

bubble sort is stable sorting algorithm

first write logic and then insert them into a function
what is the concluding condition of the logic

i=0
(-> None) return type

def function() (-> None):
while has_swapped:
    if unsorted[i]>unsorted[i+1]:
            temp=unsorted[i+1]
            unsorted[i+1]=unsorted[i]
            unsorted[i]=temp
            has_swapped=True
            i+=1
If at least one swap doesn't happen after looping through all the elements in the list
then the 

### Insert sort
Insert at the right place
1. going from left to right

2. take each element and insert it at the right place by swapping them in the place

3. Swap in reverse manner each element until there are no swaps required

4. Insert sort is stable and 


### Quick Sort


### Python uses tim sort: a variant of merge and insertion sort

