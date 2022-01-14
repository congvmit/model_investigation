# Model Investigation with Tensorboard

## Requirements

```
tensorflow==2.7.0
python==3.8.12
```

## How to run

Just open `main.ipynb` and run. The log is written in `tensorboard` folder.

You can open tensorboard by running the following command:

```
tensorboard --logdir  tensorboard
```

The code is borrowed from this [link](https://github.com/aymericdamien/TensorFlow-Examples/blob/master/tensorflow_v2/notebooks/4_Utils/tensorboard.ipynb)

## Results

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-c3ow">n_hidden_1</th>
    <th class="tg-c3ow">n_hidden_2</th>
    <th class="tg-c3ow">learning_rate</th>
    <th class="tg-c3ow">optimizer</th>
    <th class="tg-c3ow">Accuracy</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky">128</td>
    <td class="tg-0pky">256</td>
    <td class="tg-0pky">0.1</td>
    <td class="tg-0pky">sgd</td>
    <td class="tg-0pky">0.0972</td>
  </tr>
  <tr>
    <td class="tg-0pky">128</td>
    <td class="tg-0pky">256</td>
    <td class="tg-0pky">0.01</td>
    <td class="tg-0pky">sgd</td>
    <td class="tg-0pky">0.9752</td>
  </tr>
  <tr>
    <td class="tg-0pky">128</td>
    <td class="tg-0pky">256</td>
    <td class="tg-0pky">0.001</td>
    <td class="tg-0pky">sgd</td>
    <td class="tg-0pky">0.9356</td>
  </tr>
  <tr>
    <td class="tg-0pky">128</td>
    <td class="tg-0pky">256</td>
    <td class="tg-0pky">0.0001</td>
    <td class="tg-0pky">sgd</td>
    <td class="tg-0pky">0.735</td>
  </tr>
  <tr>
    <td class="tg-0pky">128</td>
    <td class="tg-0pky">256</td>
    <td class="tg-0pky">0.01</td>
    <td class="tg-0pky">adam</td>
    <td class="tg-0pky">0.9764</td>
  </tr>
  <tr>
    <td class="tg-0pky">128</td>
    <td class="tg-0pky">256</td>
    <td class="tg-0pky">0.01</td>
    <td class="tg-0pky">rmsprop</td>
    <td class="tg-0pky">0.9778</td>
  </tr>
  <tr>
    <td class="tg-0pky">128</td>
    <td class="tg-0pky">256</td>
    <td class="tg-0pky">0.01</td>
    <td class="tg-0pky">adagrad</td>
    <td class="tg-0pky">0.9504</td>
  </tr>
  <tr>
    <td class="tg-0pky">128</td>
    <td class="tg-0pky">128</td>
    <td class="tg-0pky">0.01</td>
    <td class="tg-0pky">rmsprop</td>
    <td class="tg-0pky">0.9782</td>
  </tr>
  <tr>
    <td class="tg-0pky">128</td>
    <td class="tg-0pky">64</td>
    <td class="tg-0pky">0.01</td>
    <td class="tg-0pky">rmsprop</td>
    <td class="tg-0pky">0.9762</td>
  </tr>
</tbody>
</table>

## Raised Questions

1 - Which layers should be visualized and analyzed? \
2 - How the weights distribution should be? \
3 - Why are almost weights and biases nearly equal 0? \
Answer: [1, 2] \
TODO: Add details\
4 - Why does different model (different weights and biases) have the same performance? \
5 - Why distribution of weights and biases diverge over iterations? \

## References

[1] https://stats.stackexchange.com/questions/198762/understanding-weight-distribution-in-neural-network \
[2] https://stackoverflow.com/questions/47745313/how-to-interpret-weight-distributions-of-neural-net-layers
