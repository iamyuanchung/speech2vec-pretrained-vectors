# Speech2Vec Pre-Trained Vectors

The repository releases the speech embeddings learned by Speech2Vec proposed by [Chung and Glass (2018)](https://arxiv.org/abs/1803.08976). Feel free to contact [me](mailto:iamyuanchung@gmail.com) for any questions.

# Introduction
Speech2Vec is a recently proposed deep neural network architecture capable of representing variable-length speech segments as real-valued, fixed-dimensional speech embeddings that capture the semantics of the segments---It can be viewed as a speech version of Word2Vec! The training of Speech2Vec borrows the metholodogy of skip-grams & CBOW from Word2Vec and is thus unsupervised, i.e., we do not need to know the word identity of a speech segment. Please refer to the original paper for more details.

In this repository, we release the speech embeddings of different dimensionalities learned by Speech2Vec using skip-grams as the training methodology. The model is trained on a corpus consisting of about 500 hours of speech from [LibriSpeech](http://www.openslr.org/12/) (the clean-360 + clean-100 subsets). We also include the word embeddings learned by skip-grams Word2Vec trained on the transcript of the same speech corpus.

# Links
| Dim |          Speech2Vec          |          Word2Vec          |
|:---:|:----------------------------:|:--------------------------:|
| 50  | [file](./speech2vec/50.vec)  | [file](./word2vec/50.vec)  |
| 100 | [file](./speech2vec/100.vec) | [file](./word2vec/100.vec) |
| 200 | [file](./speech2vec/200.vec) | [file](./word2vec/200.vec) |
| 300 | [file](./speech2vec/300.vec) | [file](./word2vec/300.vec) |

The following figure shows the relationship between the dimensionality of the speech/word embeddings and the performance (higher the better) on a word similarity benchmark (MTurk-771) computed using this [toolkit](https://github.com/mfaruqui/eval-word-vectors). Again, please refer to the original paper for task descriptions.
![](https://github.com/iamyuanchung/speech2vec-pretrained-vectors/blob/master/example.png)

# Citation
If you use the embeddings in your work, please consider citing:
```
@inproceedings{chung2018speech2vec,
  title     = {Speech2vec: A sequence-to-sequence framework for learning word embeddings from speech},
  author    = {Chung, Yu-An and Glass, James},
  booktitle = {INTERSPEECH},
  year      = {2018}
}
```
