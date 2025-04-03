# <span style="color:#ff5733;">🔥 Battle of Nets 🔥</span>

**Battle of Nets** is an experimental deep-learning project where models compete in real-world tasks. We evaluate how they handle different challenges under different constraints.

Follow along as we learn and push these architectures to their limits.
<img src="bn.jpg" alt="Logo" width="700" height="500" style="display: block; margin: 0 auto;">



---

## 🏆 <span style="color:#3498db;">Current Challenges</span>  

<table>
<tr>
<th>Name</th>
<th>Scientific Term</th>
<th>Start</th>
<th>End</th>
<th>Model Constraints</th>
<th>Current Leader</th>
<th>Challenge Details</th>
</tr>
<tr>
<td><b>Speedrun Mode</b></td>
<td>Quantization</td>
<td>January 1, 2025</td>
<td>Ongoing</td>
<td>Low-bit precision</td>
<td>VGG19</td>
<td><a href="notebooks/Speedrun_Quantization/README.md">Description Link</a></td>
</tr>
<tr>
<td><b>Puzzle Solver</b></td>
<td>Occlusion Test</td>
<td>March 1, 2025</td>
<td>Ongoing</td>
<td>Obscured inputs</td>
<td>InceptionNet</td>
<td><a href="notebooks/PuzzleSolver_Occlusion/README.md">Description Link</a></td>
</tr>
<tr>
<td><b>Adversarial Battle</b></td>
<td>Robustness Test</td>
<td>TBD</td>
<td>TBD</td>
<td>Adversarial attacks</td>
<td>TBD</td>
</tr>
</table>

---

## 🔍 <span style="color:#2ecc71;">Latest Results</span>  

### **First Results on Puzzle Solver Challenge**

The benchmarks for the Puzzle Solver Challenge are in! 
Robustness of models was analyzed against altered images using grid-based occlusion techniques. <a href="notebooks/PuzzleSolver_Occlusion/README.md">Description Link</a>


### **InceptionNet Joins the Battle**

A version inspired by *InceptionNet* was trained and quantized retaining **99.68%** of its original accuracy while achieving a **2.133x** speedup. *VGG19* previously led with a *2.168x* speedup and 99.46% accuracy, while ResNet20 held 99.74% accuracy but only improved speed by 1.2768x.

It's important to note ResNets still dominate in terms of sole speed, but are less affected by quantization.'

### **VGG19 vs ResNet20: Quantization Showdown**             

- **VGG19** retained **99.46%** of its original accuracy while achieving a **2.168x speedup**.  
- **ResNet20** held **99.74%** accuracy but only improved speed by **1.2768x**.  

With a stronger performance boost, **VGG19** leads as the first challenge winner in *Battle of Nets*. It's crucial to note that ResNet20 still is faster but less affected by quantization.

---

## 📊 <span style="color:#f1c40f;">Leaderboard</span>  

<table>
<tr>
<th>Model Name</th>
<th>Score</th>
<th>Number of Challenges</th>
<th>Unique Ability</th>
</tr>
<tr>
<td><b>VGG the Veteran</b> - <i>VGG19</i></td>
<td>18</td>
<td>2</td>
<td>Just simple</td>
</tr>
<tr>
  <td><b>Inception the Versatile</b> - <i>InceptionNet</i></td>
  <td>17</td>
  <td>2</td>
  <td>Multi-scale Thinking</td>
</tr>


<tr>
<td><b>ResNet the Agile</b> - <i>ResNet20</i></td>
<td>16</td>
<td>2</td>
<td>Residual Power</td>
</tr>
<tr>
<td><b>You can contriubute here</b></td>
<td>TBD</td>
<td>?</td>
<td>?</td>
</tr>
</table>

---

## 🚀 <span style="color:#9b59b6;">How to Contribute</span> 
### To Submit a Model:
- Fork the Repo – Click Fork and clone it to your local machine.
- Add Your Model – Implement your architecture in the notebooks/ directory. Optionally add your models in the models/ directory.
- Submit a PR – Push your changes and open a pull request for your model or challenge.

### To Create a New Challenge:
- Propose challenges by opening a new issue with challenge details (a cool name(required), scientific term, objective, constraints, etc.).

<!-- ### Keep Engaged: 
Don't forget to test your model, track performance, and contribute to new challenges! -->

---


Join the battle and may the best net win! 🚀 

<span style="color:#ff5733;">Created by Adonay Demewez Gebremedhin </span>

## License  
This project is licensed under the Apache License 2.0 - see the [LICENSE](./LICENSE) file for details.
