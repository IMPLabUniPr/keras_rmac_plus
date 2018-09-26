# keras_rmac_plus
Keras implementation of R-MAC+ descriptors.

[[paper](https://arxiv.org/pdf/1806.08565.pdf] [[project](http://implab.ce.unipr.it/?page_id=858)]


![query phase](http://implab.ce.unipr.it/wp-content/uploads/2018/09/queryImage.png)

## Prerequisites for Python3
* Keras (> 2.0.0)
* Tensorflow (> 1.5)
* Scipy
* Sklearn
* OpenCV 3

## Networks
The pipeline was tested with VGG16 and ResNet50. For the VGG16 the best performance are reached when the features are extracted from the block5_pool, instead for ResNet from the activation_43.
It is possible to try with other networks. Please before to try it, check if there are available the Keras weight for the selected network.

## Datasets
* Oxford5k
* Paris6k

Download the datasets and put it into the data folder. Then compile the script for the evaluation of the retrieval system.

## Test
` python3 Keras_test_MAC.py  `

## Results


| Method        | Network           | Oxford5k  | Paris6k | Holidays |
| :------------- |:-------------:| :-----:| :---:| :---------:|
| R-MAC | VGG16   | 65.56% | 82.80% | 87.65% |
| R-MAC | ResNet50   | 71.77% | 83.31% | 92.55% |
| M-R RMAC+ | ResNet50   | 78.88% | 88.63% | 94.63% / 95.58% |
| M-R RMAC+ with retrieval based on 'db regions' | ResNet50   | 85.39 %   | 91.90%  | 94.37% / 95.87% |

## Reference

<pre>@article{magliani2018accurate,
  title={An accurate retrieval through R-MAC+ descriptors for landmark recognition},
  author={Magliani, Federico and Prati, Andrea},
  journal={arXiv preprint arXiv:1806.08565},
  year={2018}
}</pre>
