# 1046.-Last-Stone-Weight
LeetCode Style question for Algorithms Class

Last Stone Weight — LeetCode 1046

C++ Solution (Class Quiz Submission)

-Problem Summary

You are given a list of stone weights.
Each turn, smash the two heaviest stones:

If they are equal → both are destroyed

If they are different → the new stone has weight difference = larger − smaller

Continue until 0 or 1 stone remains.
Return the weight of the last stone, or 0 if none remain.

-Approach (Max-Heap / Priority Queue)

To repeatedly get the two heaviest stones efficiently, a max-heap (priority_queue<int>) is used.

Steps:

    Push all stones into a max-heap.

    While the heap has at least two stones:

        Remove the top two (the heaviest).

        Compute the difference.

        If the difference > 0, push it back.

    Return the final stone weight or 0.

This approach runs in O(n log n) time and is optimal for this problem.