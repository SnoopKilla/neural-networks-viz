# 📈 Gradient Descent Visualization: Understanding Exploding Gradients

An interactive web-based visualization that demonstrates the phenomenon of exploding gradients in gradient descent optimization on a simple U-shaped function.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-green)](https://snoopkilla.github.io/neural-networks-viz/)

## 🚀 Live Demo

**[View the Interactive Visualization](https://snoopkilla.github.io/neural-networks-viz/)**

## 📊 What This Visualization Shows

This interactive tool demonstrates how different learning rates affect gradient descent optimization on the function **f(x) = x²**. You can observe:

- **✅ Stable Convergence** (low learning rates)
- **⚡ Fast Optimization** (optimal learning rates) 
- **❌ Exploding Gradients** (high learning rates)

### Key Visual Elements

| Element | Color | Description |
|---------|--------|-------------|
| 🔵 Blue Curve | `#2196F3` | The U-shaped function f(x) = x² |
| 🔴 Red Dot | `#FF5722` | Current position during optimization |
| 🟢 Green Arrow | `#4CAF50` | Gradient vector (steepest descent direction) |
| 🟣 Purple Trail | `#9C27B0` | Path taken by the optimizer |

## 🎮 How to Use

1. **Adjust Learning Rate** (0.01 - 2.0): Controls the step size of each optimization step
2. **Set Starting Position** (-5 to 5): Where the optimization begins
3. **Click "Start Descent"** to begin the animation
4. **Observe the behavior**:
   - Learning Rate < 0.5: Smooth convergence
   - Learning Rate ≈ 0.5: Optimal performance
   - Learning Rate = 1.0: Perfect oscillation
   - Learning Rate > 1.0: Exploding gradients!

## 🧠 Educational Concepts

### The Mathematics Behind It

For the quadratic function **f(x) = x²**:
- **Gradient**: f'(x) = 2x
- **Update Rule**: x_new = x_old - learning_rate × gradient
- **Critical Learning Rate**: 1.0 (boundary between convergence and divergence)

### Why Exploding Gradients Occur

```
When: learning_rate × |gradient| > |distance_to_minimum|
Result: Algorithm overshoots and error grows with each step
```

This creates a feedback loop:
1. Large gradient → Large weight update
2. Overshoot minimum → Even larger gradient
3. Even larger weight update → Further overshoot
4. **Exponential divergence!**

## 🔬 Recommended Experiments

| Learning Rate | Expected Behavior | Educational Value |
|---------------|-------------------|-------------------|
| **0.01 - 0.05** | Slow, steady convergence | Shows stable optimization |
| **0.1 - 0.5** | Fast, efficient convergence | Demonstrates optimal learning |
| **0.8 - 0.99** | Oscillation with eventual convergence | Near-critical behavior |
| **1.0** | Perfect oscillation (boundary case) | Mathematical boundary |
| **1.1 - 2.0** | Clear exploding gradients | Demonstrates the problem |

## 🚀 Getting Started

### Method 1: Direct Download
1. Download `index.html` from this repository
2. Open the file in any modern web browser
3. Start experimenting with different parameters!

### Method 2: Clone and Serve
```bash
git clone https://github.com/yourusername/gradient-visualization.git
cd gradient-visualization
# Open index.html in your browser or serve with a local server
python -m http.server 8000  # Python 3
# or
python -m SimpleHTTPServer 8000  # Python 2
```

### Method 3: GitHub Pages (Recommended)
1. Fork this repository
2. Enable GitHub Pages in repository settings
3. Visit `https://yourusername.github.io/neural-networks-viz/`

## 📖 References and Further Reading

### 📚 Essential Papers
- [Gradient-Based Learning Applied to Document Recognition](http://yann.lecun.com/exdb/publis/pdf/lecun-98.pdf) - LeCun et al.
- [On the difficulty of training Recurrent Neural Networks](https://arxiv.org/abs/1211.5063) - Pascanu et al.
- [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385) - He et al.

### 🎓 Educational Resources
- [CS231n: Convolutional Neural Networks for Visual Recognition](http://cs231n.github.io/)
- [Deep Learning Book](https://www.deeplearningbook.org/) - Goodfellow, Bengio, and Courville
- [Neural Networks and Deep Learning](http://neuralnetworksanddeeplearning.com/) - Michael Nielsen

## 📞 Contact

- **GitHub**: [@SnoopKilla](https://github.com/SnoopKilla)

---

⭐ **Found this useful?** Give it a star to help others discover this educational tool!