## The Temperature Trick

**The Problem:**
Teacher outputs are already very confident: `[0.99, 0.009, 0.001]`
* Almost as hard as one-hot labels
* Little information about relationships

**Solution: Temperature Scaling during student training**

<div style="display: flex; margin-top: 30px;">
<div style="flex: 1; margin-right: 20px;">

**T=1 (Normal)**
* `[0.99, 0.009, 0.001]`
* Very confident
* Minimal relationship info

</div>
<div style="flex: 1;">

**T=5 (Heated)**
* `[0.4, 0.35, 0.25]`
* Emphasizes hidden relationships
* More "dark knowledge" transferred

</div>
</div>

> Higher temperature = softer probabilities = more information about inter-class similarities