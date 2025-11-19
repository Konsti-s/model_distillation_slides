## Practical example

1. **Generate teaching data**
   * Feed millions of prompts to the teacher and save the results
   * Can even use unlabeled text - teacher provides the "labels"

2. **Train the smaller student**
   * Student learns mostly from teacher's soft outputs (T-scaling)
   * Also sees some original hard labels to stay grounded
   * Often trained on way more examples than the original teacher

**What Gets Lost?** Distilled models excel at pattern matching but struggle with:

* Complex multi-step reasoning
* Creative problem solving
* Emergent capabilities

> Students can match teacher performance on familiar tasks but fail on novel problems requiring true understanding