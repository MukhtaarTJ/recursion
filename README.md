# recursion
# Insertion Sort Algorithm

Insertion Sort is a simple and intuitive sorting algorithm that builds the final sorted array one element at a time. It's often compared to the way we sort playing cards in our hands – each time we pick a new card, we insert it into the right place in our hand.

## How It Works

1. The algorithm starts with the second element (at index 1) since a single element can be considered sorted.
2. For each subsequent element, it's compared with the previous elements in the sorted part of the array.
3. If the current element is smaller than any of the previous elements, those elements are shifted one position to the right to make space for the current element.
4. The current element is then placed in its correct sorted position.
5. This process is repeated for each element until the entire array is sorted.

## Time Complexity

- Best Case: O(n) - When the input array is nearly sorted, each element requires only a few comparisons.
- Worst Case: O(n^2) - When the input array is in reverse order, each element may need to be compared with all previous elements.
- Average Case: O(n^2) - On average, the number of comparisons and shifts for each element follows a quadratic pattern.

## Usage Example

Here's how you can use the Insertion Sort algorithm in Python:

```python
def insertion_sort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        while j >= 0 and key < arr[j]:
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = key

# Example usage
arr = [5, 2, 9, 1, 5, 6]
insertion_sort(arr)
print("Sorted array:", arr)
