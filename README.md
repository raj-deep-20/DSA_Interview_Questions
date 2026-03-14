# DSA Interview Reference Guide

This guide is a practical, interview-focused reference for common Data Structures and Algorithms (DSA) patterns.

It is organized to help with:
- Fast revision before interviews
- Pattern recognition during problem solving
- AI/ML company interview preparation (where coding rounds often emphasize optimization, reasoning quality, and clean implementation)

## 1) How to Use This Guide

Use this flow during practice:
1. Read the problem and classify the input type (array, string, graph, tree, stream, interval).
2. Identify the likely pattern from constraints (sorted, contiguous subarray, repeated lookup, shortest path, top-k, etc.).
3. Pick a baseline solution, then improve time/space complexity.
4. Explain trade-offs clearly.
5. Test edge cases before coding and again after coding.

## 2) Big Picture: Core DSA Types

### Arrays and Strings
- Most frequent in interviews
- Skills tested: indexing, prefix/suffix logic, in-place updates, window boundaries, hash-assisted lookup

### Linked Lists
- Pointer manipulation and cycle detection
- Skills tested: constant-space thinking, careful edge handling

### Stacks and Queues
- LIFO/FIFO modeling
- Skills tested: monotonic structures, parsing, BFS setup

### Hash Maps and Sets
- Constant-time membership and counting
- Skills tested: frequency maps, deduplication, complement matching

### Trees and Binary Search Trees
- Hierarchical recursion and traversal
- Skills tested: DFS/BFS traversal, subtree logic, balancing ideas

### Heaps / Priority Queues
- Repeated min/max extraction
- Skills tested: top-k, median streaming, scheduling

### Graphs
- Connectivity and shortest path
- Skills tested: BFS/DFS, topological sort, union-find, path cost optimization

### Tries
- Prefix-based storage
- Skills tested: autocomplete, dictionary/prefix constraints, bitwise trie variants

### Dynamic Programming
- Reused subproblems with optimal substructure
- Skills tested: state design, transitions, memoization/tabulation

### Backtracking / Recursion
- Combinatorial search
- Skills tested: pruning, state rollback, constraint enforcement

### Greedy Algorithms
- Local choice with global proof
- Skills tested: sorting-based reasoning, exchange argument intuition

### Bit Manipulation
- Compact state and low-level optimizations
- Skills tested: parity tricks, masks, XOR properties

## 3) High-Value Interview Patterns

### Pattern A: Two Pointers
When to use:
- Sorted arrays
- Pair/triplet sum
- Opposite-end shrinking

Typical complexity:
- Time: O(n)
- Space: O(1)

Common questions:
- 2-sum in sorted array
- Remove duplicates in place
- Container with most water

### Pattern B: Sliding Window (Fixed and Variable)
When to use:
- Contiguous subarray/substring
- Max/min/count under constraints

Typical complexity:
- Time: O(n)
- Space: O(k) for map/set

Common questions:
- Longest substring without repeating characters
- Minimum window substring
- Max sum subarray of size k

### Pattern C: Prefix Sum / Difference Array
When to use:
- Repeated range queries
- Subarray sum checks

Typical complexity:
- Preprocess O(n), query O(1)

Common questions:
- Subarray sum equals k
- Range sum query

### Pattern D: Fast and Slow Pointers
When to use:
- Linked list cycle detection
- Middle node location

Typical complexity:
- Time: O(n)
- Space: O(1)

Common questions:
- Linked list cycle
- Happy number

### Pattern E: Binary Search on Answer
When to use:
- Monotonic feasibility condition
- Optimize min/max value

Typical complexity:
- O(n log M) where M is value range

Common questions:
- Capacity to ship packages within D days
- Koko eating bananas

### Pattern F: Monotonic Stack
When to use:
- Next greater/smaller element
- Histogram/temperature-style nearest constraints

Typical complexity:
- Time: O(n)
- Space: O(n)

Common questions:
- Daily temperatures
- Largest rectangle in histogram

### Pattern G: BFS / Multi-source BFS
When to use:
- Shortest path in unweighted graph/grid
- Layer-by-layer propagation

Typical complexity:
- O(V + E)

Common questions:
- Rotting oranges
- 01 matrix distance

### Pattern H: DFS + Backtracking
When to use:
- Generate all valid combinations/permutations/subsets
- Path existence with constraints

Typical complexity:
- Exponential in search space (with pruning)

Common questions:
- Subsets, permutations
- Word search
- N-queens

### Pattern I: Top K with Heap
When to use:
- Largest/smallest k elements
- Stream-based ranking

Typical complexity:
- O(n log k)

Common questions:
- Top k frequent elements
- K closest points

### Pattern J: Union-Find (Disjoint Set)
When to use:
- Dynamic connectivity
- Cycle detection in undirected graphs

Typical complexity:
- Near O(1) amortized per operation

Common questions:
- Number of connected components
- Redundant connection

### Pattern K: Dynamic Programming
When to use:
- Overlapping subproblems + optimal choices

Typical complexity:
- Depends on state count and transitions

Common questions:
- 0/1 knapsack style
- Longest increasing subsequence
- Edit distance

### Pattern L: Greedy + Sorting
When to use:
- Interval scheduling/merging
- Earliest finish or smallest available choice

Typical complexity:
- O(n log n)

Common questions:
- Merge intervals
- Non-overlapping intervals
- Meeting rooms

## 4) Pattern-to-Problem Clues (Quick Mapping)

If you see these clues, try these patterns first:
- "contiguous", "substring", "subarray" -> Sliding Window / Prefix Sum
- "sorted array" -> Two Pointers / Binary Search
- "top k", "most frequent" -> Heap + Hash Map
- "shortest path in grid (unweighted)" -> BFS
- "dependencies/prerequisites" -> Topological Sort
- "all combinations" -> Backtracking
- "max/min with choices each step" -> DP or Greedy
- "dynamic connectivity" -> Union-Find

## 5) AI/ML Company Interview Focus

Many AI/ML-oriented teams still use standard DSA rounds, but with stronger emphasis on:
- Efficient handling of large-scale data
- Streaming and online algorithms
- Clear complexity trade-offs
- Correctness under edge cases
- Communication quality and reasoning

### Most common pattern groups in AI/ML interviews

1. Arrays, Hashing, and String transforms
- Frequency analysis
- Deduplication
- Token/window operations
- Log parsing style operations

2. Heaps and selection
- Top-k frequent terms/events
- Streaming median
- Priority scheduling

3. Graph basics
- BFS/DFS in knowledge or dependency graphs
- Connected components and traversal
- Shortest path for unweighted/weighted variants

4. Dynamic Programming fundamentals
- Sequence modeling style tasks (LIS, edit distance, partition)
- Resource-constrained optimization

5. Binary Search and monotonic optimization
- Hyperparameter-like search framing in coding form
- Feasibility-based threshold problems

6. Intervals and event sweeps
- Time-window overlaps
- Scheduling and conflict resolution

### AI/ML-friendly practice themes
- Stream processing:
  - Running median in data stream
  - Sliding window maximum
- Ranking and retrieval:
  - Top-k frequent words
  - K closest points/items
- Sequence and text:
  - Longest substring variants
  - Edit distance
- Graph-based reasoning:
  - Course schedule
  - Word ladder
- Scale-aware coding:
  - Design with O(n) or O(n log n)
  - Memory-aware alternatives

## 6) Complexity Targets to Remember

General interview expectations:
- Prefer O(n) over O(n^2) when possible for array/string scans
- For sorting-based methods, O(n log n) is often acceptable
- For graph traversal, target O(V + E)
- For top-k, target O(n log k) rather than full sort O(n log n)

Space trade-off guidance:
- Explain why extra O(n) memory may be worth a faster runtime
- Mention in-place alternatives when practical

## 7) Interview Execution Checklist

Before coding:
- Clarify constraints and input guarantees
- Ask about duplicates, negative values, empty input, value range
- State target complexity

While coding:
- Keep variable naming clear (left, right, freq, heap, visited)
- Handle edge cases early
- Avoid unnecessary nested loops

After coding:
- Dry run with 1 normal + 2 edge cases
- Confirm complexity and assumptions
- Mention optional improvements

## 8) 6-Week DSA Plan (Interview Prep)

Week 1:
- Arrays, strings, hashing
- Two pointers + sliding window

Week 2:
- Stack/queue, monotonic stack
- Prefix sum + binary search patterns

Week 3:
- Linked list, trees (DFS/BFS), recursion

Week 4:
- Graphs (BFS/DFS, topo sort, union-find)

Week 5:
- Heaps + intervals + greedy

Week 6:
- Dynamic programming + mixed mock rounds

Daily structure:
- 2 easy warmups
- 2 medium pattern-focused problems
- 1 review/refactor of prior solution

## 9) Curated Problem Buckets to Build Mastery

Arrays/Hashing:
- Two Sum
- Product of Array Except Self
- Subarray Sum Equals K

Sliding Window:
- Longest Substring Without Repeating Characters
- Minimum Size Subarray Sum
- Minimum Window Substring

Binary Search:
- Find Peak Element
- Search in Rotated Sorted Array
- Capacity To Ship Packages Within D Days

Trees/Graphs:
- Binary Tree Level Order Traversal
- Number of Islands
- Course Schedule

Heaps:
- Kth Largest Element in an Array
- Top K Frequent Elements
- Find Median from Data Stream

Dynamic Programming:
- House Robber
- Coin Change
- Longest Increasing Subsequence

## 10) Final Advice for AI/ML Interview Tracks

- Treat DSA rounds as a systems-thinking filter, not only coding.
- Narrate your optimization choices clearly.
- Prefer robust solutions that scale to large inputs.
- Build confidence in heap, graph, and streaming patterns.
- Practice explaining trade-offs in plain language.

---
