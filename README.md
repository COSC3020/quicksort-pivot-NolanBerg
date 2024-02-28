[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/IF3rQO50)
# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

I believe the median-of-three strategy is more likely to pick a good pivot as compared to the leftmost element strategy. When choosing the leftmost element, each element has an equal chance of being chosen as the pivot. However, there is no bias towards selecting a pivot that contributes to balanced partitions. The number of splits can vary, and in the worst case, such as when the array is already sorted, it may result in $\Theta$(n^2) time complexity, which is less efficient compared to the median-of-three strategy. The 1/2 probability of selecting a good pivot using the median-of-three strategy is significant. It ensures that, on average, the pivot will be chosen from the middle n/2 elements, leading to a better chance of having a good pivot. The expected number of splits being at most 2log4/3n indicates that the algorithm efficiently divides the array into smaller parts, making it more scalable. The median-of-three strategy is favoured for its ability to create more balanced partitions, contributing to the efficiency of quicksort, especially when dealing with randomly ordered input arrays.
