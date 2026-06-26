## Experiment 1
Architecture:
32 → 64 → 128
Dropout- 0.2

Result:
76.9%

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
Dropout- 0.1

Result:
81.2%

Conclusion:
Increasing model width improved performance, but increasing depth had a substantially larger effect on reducing underfitting.

---

## Experiment 4
Base model but reduced dropout rate(0.2 → 0.1).
32 → 64 → 128

Result:
75.4%

Conclusion:
Dropout wasn't causing the as much high bias as previously thought.

## Experiment 5
Using both increased depth and width.
48-48 → 96-96 → 192-192
Dropout- 0.1

Result:
87.4%

Conclusion:
Combining increased depth and width produced the best overall performance, indicating that both architectural changes are complementary.

## Final Results

|Experipents|Train Accuracy|Val Accuracy|Test Accuracy|
|-|-|-|-|
|Base Model|75.9%|76.3%|76.2%|
|Deeper Model|87.8%|84.8%|84.4%|
|Wider Model|84.4%|81.7%|81.2%|
|Base Model'|75.2%|75.6%|75.4%|
|Final Model|91.8%|87.5%|87.4%|

## Key Insights

- Increasing network depth had the greatest impact on performance, improving test accuracy by over 8%.
- Increasing width alone also improved performance but less than increasing depth.
- Reducing dropout from 0.2 to 0.1 did not improve the baseline model, suggesting dropout was not the primary cause of underfitting.
- Combining increased depth and width produced the best results, achieving 87.4% test accuracy.

## Future Experiment?
Training the final model for more epochs(50) to get higher accuracy.