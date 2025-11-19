## The Core Mystery 🤔

### "If small models can mimic large ones, why not train them directly?"

**The Valley:**
Training goal = reaching the valley.

<div style="display: flex; margin-top: 30px;">
<div style="flex: 1; margin-right: 20px;">


**Small Model (5 hikers)**
* Sometimes climbing vertically
* Limited exploration capacity
* Heavy backpacks
* -> Get stuck in local minima
  
</div>
<div style="flex: 1;">

**Large Model (100 hikers)**
* Walking moderate gradients
* Multiple paths to explore
* Light equipment
* -> Can find the global minimum

</div>
</div>

> Small models have the representational capacity but lack the exploration capacity to find good solutions from scratch

--

### Technical Explanation: Optimization Landscape

**When training from scratch on raw data, you navigate a complex loss landscape**

<img src="images/optimization_landscape.png" style="width: 50%; height: auto; margin: 20px auto; display: block;">

<div style="display: flex; margin-top: 30px;">
<div style="flex: 1; margin-right: 20px;">


**Small Models**
* Rugged, spiky landscape
* Limited parameter budget
* Fewer degrees of freedom
* Easily stuck in poor local minima

</div>
<div style="flex: 1;">

**Large Models**
* Smoother paths through landscape
* Can represent multiple hypotheses simultaneously
* More degrees of freedom
* Many ways to escape local minima

</div>
</div>

> The optimization landscape is fundamentally different for models of different sizes
--

### Technical Explanation: Lossy Cascade

**Learning happens in layers - each builds on the previous**

<img src="images/feature_hierarchy.png" style="width: 40%; height: auto; margin: 20px auto; display: block;">

<div style="display: flex; margin-top: 30px;">
<div style="flex: 1; margin-right: 20px;">


**Small Models**
* Early layers must compress heavily
* Layer 10 builds on degraded Layer 9 features
* Creates a "lossy cascade"
* Errors compound through layers

</div>
<div style="flex: 1;">

**Large Models**
* Rich representations at each layer
* Layer 10 builds on high-quality Layer 9 features
* Creates a "virtuous cycle"
* Sophisticated features compound

</div>
</div>

--

### Technical Explanation: Credit Assignment Problem

**How parameters learn to solve different aspects of the task**

<div style="display: flex; margin-top: 40px;">
<div style="flex: 1; margin-right: 20px;">

**Small Models**
* Every parameter must multitask heavily
* Fewer "shots" at finding right features
* Progress on one task interferes with another
* **Catastrophic interference**
* Limited capacity forces harmful compromises
  
</div>
<div style="flex: 1;">

**Large Models**
* Different parameter subsets specialize:
  * Some detect syntax
  * Some detect semantics
  * Some detect context
* More chances to find good features
* Can explore competing hypotheses in parallel


</div>
</div>