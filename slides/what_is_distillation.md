## Teacher-Student Paradigm

<div style="display: flex; align-items: flex-start; margin-top: 20px;">
<div style="flex: 1; margin-right: 30px;">

**The Origin:**
* Hinton et al. 2015: ["Distilling the Knowledge in a Neural Network"](https://arxiv.org/pdf/1503.02531)
* Large teacher → Small student model
* Student learns from soft outputs

**Example:**
* **Hard label:** "This is a cat"
* **Teacher:** "70% cat, 15% dog, 8% lynx"
* **Student learns:** inter-class relationships

**Key Benefits:**
* Captures class relationships
* Learns nuanced patterns
* Similar performance, fraction of size

</div>
<div style="flex: 0 0 35%;">
<img src="images/hinton.jpg" style="width: 100%; height: auto; border-radius: 10px;">
<p style="text-align: center; font-size: 0.8em; margin-top: 10px;">Geoffrey Hinton<br>Father of Deep Learning</p>
</div>
</div>