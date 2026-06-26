## Experiment 1
Architecture:
32 → 64 → 128

Result:
76.2%

Conclusion:
High bias.

---

## Experiment 2
Increasing depth by adding second Conv layer per block.
32-32 → 64-64 → 128-128
And decreasing dropout rate from 0.2 to 0.1. 

Result:
84.4%

Conclusion:
Increasing depth significantly reduced high bias.

---

## Experiment 3
Increasing width of base model.
64 → 128 → 256

Result:
...

Conclusion:
...