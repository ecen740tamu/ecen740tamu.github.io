1. Sorting algorithms

Complexity: is O(n) or $O(n^2)$
Stability: Ability to preserve order of equal elements as in the original input


def selection_sort():
    """
    Mutates lst so that it is sorted via selecting the minimum element and 
    swapping it with the corresponding index
    """
    for i in range(len(lst)):
        min_index = i
        for j in range(i+1,len(lst)):
        

sorting types: selection sort
               bubble sort
               insertion sort
               heap sort


bubble sort

def bubble_sort(unsorted):
    temp=0
    has_swapped= True
    while has_swapped:
          has_swapped = False
          for i in range(len(lst)-1):
                if lst[i] > lst[i+1]:
                    lst[i], lst[i+1] = lst[i+1],lst[i]
                    has_swapped = True


  
### batch normalization 

Feature wise normalization with two additional hyper-parameters gamma and beta. 

why there is need to normalize: as we progress through layers in neural networks, co-variance across layers builds up
and large values in one layer builds up and effects the gradients of other layers.

Batch norm has shown to reduce the co-variance of gradients.

#### Limitations of Batch Norm 
1. Small batch norms are not representative of norms of data distribution
2. batch is not useful for sequential data


### Layer normalization

Layer normalization is more useful for sequential data and for each batch take normalization over all the features nor accross the batch