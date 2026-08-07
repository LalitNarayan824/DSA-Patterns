# Core Queue DSA Patterns

*Interview revision guide — queue mechanics, not BFS/graph applications*

## 1. Implementation-Based Problems

- Implement Queue using Arrays
- Implement Queue using Two Stacks (LeetCode 232 - Implement Queue using Stacks)
- Implement Stack using Queue(s) (LeetCode 225 - Implement Stack using Queues)
- Design Circular Queue (LeetCode 622)
- Design Circular Deque (LeetCode 641)

**Key idea:** Master amortized O(1) analysis for the two-stack queue, and modulo arithmetic for circular buffer indexing.

## 2. Sliding Window with Deque

- Sliding Window Maximum (LeetCode 239)
- First Negative Number in Every Window of Size K (GfG)
- Max of All Subarrays of Size K (GfG)

**Key idea:** Maintain a monotonic decreasing deque of indices — pop from the back while it violates order, pop from the front when the index falls outside the window.

## 3. Queue Reversal / Reordering

- Reverse a Queue (using a stack or recursion) (GfG)
- Reverse First K Elements of a Queue (GfG)
- Interleave the First Half of a Queue with the Second Half (GfG)

**Key idea:** These test whether you can manipulate queue order using only queue/stack operations — no direct indexing allowed.

## 4. Generate / Simulate Using a Queue

- Generate Binary Numbers from 1 to N using a Queue (GfG)
- First Non-Repeating Character in a Stream (LeetCode 387 variant / GfG)
- Circular Tour / Gas Station Problem (LeetCode 134)

**Key idea:** The queue here acts as a working buffer for simulation or generation, not just storage.

## 5. Stack + Queue Combined Design

- Design a Stack that Supports getMin() in O(1) — queue-based variant (LeetCode 155 related)
- Check if a Queue Can Be Sorted Using a Stack (GfG)
- LRU Cache (LeetCode 146) — deque + hashmap design

**Key idea:** Focus on when to combine queue with another structure to get O(1) operations you couldn't get from either alone.

## 6. Priority Queue Basics

- Kth Largest Element in a Stream (LeetCode 703)
- Merge K Sorted Lists (LeetCode 23)
- Top K Frequent Elements (LeetCode 347)

**Key idea:** Priority queues (heaps) generalize the queue concept by ordering on priority instead of insertion time.

---

## Priority Order If Time Is Short

If you only have time for a handful, focus on these five, in order:

1. **Sliding Window Maximum** — deque, very frequently asked
2. **Implement Queue using Stacks / Stack using Queue** — fundamentals
3. **Design Circular Queue**
4. **Reverse a Queue / Reverse First K Elements**
5. **First Non-Repeating Character in a Stream**
