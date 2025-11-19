## The Problem with Standard Training

**Soft labels vs hard labels:**
* Hard labels: `[cat: 1.0, rest: 0.0]`
* Soft labels: `[cat: 0.7, dog: 0.15, lynx: 0.08, tiger: 0.01, ...]`
* In normal supervised learning we only use the "correct" answer.
* But most neural networks output soft labels!

**Key insight:** 
* "0.15 dog" tells us this cat shares visual features with dogs
* "0.08 lynx" suggests similar texture or pose patterns
  
> Those "soft" predictions contain valuable information!
