# Binary Search — Interview Roadmap

A search space + a way to eliminate half of it each step. That's the whole idea behind every pattern below. Practice in this order.

---

## 1. Classic Binary Search
**Idea:** Sorted array, find a target. Eliminate half by comparing `arr[mid]` to `target`.

**Practice:**
- LC 704 — Binary Search
- LC 35 — Search Insert Position
- LC 69 — Sqrt(x)
- LC 367 — Valid Perfect Square

---

## 2. Lower Bound / Upper Bound / First & Last Occurrence
**Idea:** Don't search for "the" target — search for the boundary where a condition flips from false to true (e.g. first index where `arr[i] >= target`).

**Practice:**
- LC 34 — Find First and Last Position of Element in Sorted Array
- LC 278 — First Bad Version
- LC 744 — Find Smallest Letter Greater Than Target

---

## 3. Binary Search on Answer ⭐ (most important pattern)
**Idea:** No array to search — the *answer itself* lies in a range `[low, high]`. Write a `canDo(mid)` check; binary search for the first value where it flips to true.

**Recognize it from phrases like:** "minimum speed", "minimum capacity", "minimum days", "maximum distance", "smallest divisor such that...".

**Practice:**
- LC 875 — Koko Eating Bananas
- LC 1011 — Capacity To Ship Packages Within D Days
- LC 1482 — Minimum Number of Days to Make m Bouquets
- LC 1552 — Magnetic Force Between Two Balls
- LC 410 — Split Array Largest Sum
- LC 774 — Minimize Max Distance to Gas Station
- LC 1283 — Find the Smallest Divisor Given a Threshold

---

## 4. Rotated Sorted Array
**Idea:** Array isn't globally sorted, but one half (left of mid or right of mid) always is. Identify the sorted half, check if target lies in it, discard the other half.

**Practice:**
- LC 33 — Search in Rotated Sorted Array
- LC 81 — Search in Rotated Sorted Array II (duplicates — breaks the "always sorted half" trick, needs a fallback)
- LC 153 — Find Minimum in Rotated Sorted Array
- LC 154 — Find Minimum in Rotated Sorted Array II

---

## 5. Peak / Mountain
**Idea:** Compare `arr[mid]` to `arr[mid+1]`. Going uphill → peak is to the right. Going downhill → peak is to the left (or at mid).

**Practice:**
- LC 162 — Find Peak Element
- LC 852 — Peak Index in a Mountain Array
- LC 1095 — Find in Mountain Array

---

## 6. 2D Matrix
**Idea (Pattern A):** Matrix is sorted like a flattened 1D array — binary search directly, converting `mid` to `(row, col)`.
**Idea (Pattern B):** Rows and columns are independently sorted — start top-right corner, move left/down based on comparison.

**Practice:**
- LC 74 — Search a 2D Matrix (Pattern A)
- LC 240 — Search a 2D Matrix II (Pattern B)

---

## Minimum Set (covers every pattern)
LC 704 → 34 → 875 → 1011 → 33 → 153 → 162 → 74 → 240

## Recognition Checklist
1. Is the search space sorted? → Classic BS
2. Is there a false→true boundary? → Lower/Upper Bound
3. Is the *answer* itself searchable (min/max something)? → Binary Search on Answer
4. Can I tell which half is sorted/valid from `mid`? → Rotated Array / Peak
5. Does the matrix have sorted structure? → 2D Matrix
