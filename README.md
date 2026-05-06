# Week 9 Homework: The Case of the Missing Festival Lanterns

## Student Info

Name: Arjun Shahi
Student number: 2412084
GitHub username: arjun shahi 805

---

## Summary

This program analyzes festival lantern records to detect issues in their placement and tracking. The function `analyze_lanterns` takes a set of expected lanterns, a log of lantern sightings, and a dictionary of correct sections. It processes this data to identify missing lanterns, unexpected lanterns, duplicates, and incorrectly placed lanterns. It also counts how many lanterns appear in each section. The function returns a structured report as a dictionary.

---

## Approach

* First, I created sets and dictionaries to track lantern data.
* I used `seen_lanterns` to store all unique lanterns found in the log.
* I used `seen_once` to help detect duplicate lanterns.
* I used `duplicate_lanterns` to store lanterns that appear more than once.
* I used `count_by_section` to count how many lanterns appear in each section.
* I used `wrong_section_lanterns` to store lanterns placed in incorrect sections.
* During the loop, I updated all these structures based on each record.
* After the loop, I used set operations to find missing and unexpected lanterns.
* Finally, I returned all results in a dictionary.

---

## How I Used Dictionaries and Sets

```text
Sets:
- seen_lanterns: to store all unique lanterns
- duplicate_lanterns: to store duplicates
- missing_lanterns: expected - seen
- unexpected_lanterns: seen - expected

Dictionaries:
- count_by_section: counts lanterns per section
- wrong_section_lanterns: stores expected vs actual section

Why sets and dictionaries:
- Sets allow fast lookup and easy difference operations
- Dictionaries allow storing structured data like counts and mappings
- Lists would be slower for searching and duplicate checking
```

---

## Complexity

```text
Time complexity: O(n)
Space complexity: O(n)

Explanation:
The function loops through lantern_log once, so time complexity is O(n).
There are no nested loops.
Extra space is used for sets and dictionaries, which grow with input size.
```

---

## Edge-Case Checklist

* [x] empty `lantern_log`
* [x] empty `expected_lanterns`
* [x] no missing lanterns
* [x] no unexpected lanterns
* [x] duplicate lanterns
* [x] wrong-section lanterns
* [x] unexpected lanterns ignored for wrong-section checking

Additional edge case:

```text
Lantern appears multiple times in wrong sections but only first wrong occurrence is recorded.
```

---

## Tests I Added

```text
Test name: test_empty_log
What it checks: Function works when lantern_log is empty
Why it matters: Ensures no crash and all expected lanterns are marked missing
```

---

## How to Run the Tests

```bash
pytest -q
```

Paste your final test result here:

```text
6 passed in 0.03s
```

---

## Assistance and Sources

```text
AI used? Y
What it helped with: Logic understanding, debugging, and explanations
Other sources used: Lecture notes and course materials
```

---

## Submission Self-Check

* [x] I completed `analyze_lanterns` in `src/challenges.py`.
* [x] I added at least one meaningful test of my own.
* [x] `pytest -q` passes.
* [x] I completed this README.
* [x] I pushed my latest work to GitHub.
