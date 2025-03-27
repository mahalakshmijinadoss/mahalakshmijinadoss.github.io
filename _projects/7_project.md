---
layout: page
title: Bias Mitigation 
description: Implementing and evaluating adversarial training methods for mitigating bias from downstream NLP tasks
img: assets/img/4.jpg
importance: 1
category: work
related_publications: true
---

Much of the work in debiasing within NLP has focused on removing bias from word embeddings produced by models like GloVe, BERT, and ELMo—a process that can be both time and resource intensive. In contrast, there’s been limited exploration of debiasing at the level of downstream tasks, and existing efforts often target only a single dimension of bias. In this project, we explored adversarial approaches to reduce bias in downstream NLP tasks to make models more fair and robust across different contexts.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

Our first baseline model, B1, uses a pre-trained BERT model and two linear layers. Our second baseline model, B2, has an embedding layer, a bidirectional LSTM encoder, an attention mechanism, and one linear layer. Our experimentation involved two kinds of adversarial debiasing architectures that we refer to as A1 and A2.  A1 was based on a conventional min-max style adversarial learning, whereas A2 introduced an extra hyperparameter α to regulate the equilibrium between the loss of the classifier and the adversary.


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
