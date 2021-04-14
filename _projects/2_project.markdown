---
layout: page
title: On Losses for Modern Language Models
description: A thorough comparison of auxiliary pre-training tasks for BERT.
img: /assets/img/olfmlm.jpg
importance: 2
category: work
---


BERT, trained using a 'masked language model' (MLM) task and a 'next sentence prediction' (NSP) task, redefined the NLP landscape and, at it's release, established itself as the state-of-the-art (SoTA) on many natural language understanding (NLU) benchmarks. Many models inspired by BERT have since surpassed its performance. However, in contrast to the original BERT paper, many obtained better results by excluding the NSP task. Some rely solely on a MLM variant, while others incorporate one or more different auxiliary loss functions, however there had yet to be a proper comparison between all these auxiliary tasks.

With multi-task learning's long history in transfer learning, its use in language understanding models deserved further exploration. For this project, we studied existing and novel auxiliary tasks in a BERT paradigm to guide future research in an informed manner. Specifically, we tested and provided insight on: 1) NSP's effect on BERT pre-training; 2) the result of 14 other auxiliary tasks on BERT pre-training; 3) how to combine multiple tasks in BERT pre-training; and 4) the advantages of multi-task learning in BERT pre-training. 

By combining the top performing pre-training tasks, our final model (depicted below) managed to outperform BERT base using less a quarter of the amount of training data.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid " src="{{ '/assets/img/olfmlm.jpg' | relative_url }}" alt="" title="PROST example"/>
    </div>
</div>
<div class="caption">
    Example question from PROST.
</div>

For more information, see our [paper](https://www.aclweb.org/anthology/2020.emnlp-main.403/) and [github](https://github.com/StephAO/olfmlm).
