# touristAI

The second Capstone project as part of the [Artificial Intelligence Nanodegree](https://www.udacity.com/course/artificial-intelligence-nanodegree--nd889), and focuses on Machine Translation Project from english to french. It foucses on using multiple variants of RNNs implemented via Keras!

## Model 1: Basic RNN

![](images/rnn.png)

## Model 2: Embedded RNN

![RNN](images/embedding.png)

## Model 3: Bidrectional RNN

![RNN](images/bidirectional.png)

## Model 4: Encoder Decoder

[???](https://github.com/google/seq2seq)

## Model 5: Custom

All 3!

Final model and training:

```python
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
input_9 (InputLayer)         (None, 21)                0         
_________________________________________________________________
embedding_4 (Embedding)      (None, 21, 256)           50944     
_________________________________________________________________
bidirectional_7 (Bidirection (None, 21, 512)           787968    
_________________________________________________________________
bidirectional_8 (Bidirection (None, 21, 512)           1181184   
_________________________________________________________________
bidirectional_9 (Bidirection (None, 21, 512)           1181184   
_________________________________________________________________
time_distributed_9 (TimeDist (None, 21, 344)           176472    
=================================================================
Total params: 3,377,752
Trainable params: 3,377,752
Non-trainable params: 0
_________________________________________________________________

Train on 110288 samples, validate on 27573 samples
Epoch 1/10
110288/110288 [==============================] - 70s 634us/step - loss: 2.4100 - acc: 0.5148 - val_loss: nan - val_acc: 0.6534
Epoch 2/10
110288/110288 [==============================] - 68s 621us/step - loss: 0.9249 - acc: 0.7439 - val_loss: nan - val_acc: 0.8198
Epoch 3/10
110288/110288 [==============================] - 69s 622us/step - loss: 0.4829 - acc: 0.8567 - val_loss: nan - val_acc: 0.8862
Epoch 4/10
110288/110288 [==============================] - 69s 622us/step - loss: 0.3154 - acc: 0.9034 - val_loss: nan - val_acc: 0.9186
Epoch 5/10
110288/110288 [==============================] - 69s 621us/step - loss: 0.2395 - acc: 0.9257 - val_loss: nan - val_acc: 0.9315
Epoch 6/10
110288/110288 [==============================] - 69s 622us/step - loss: 0.1977 - acc: 0.9380 - val_loss: nan - val_acc: 0.9458
Epoch 7/10
110288/110288 [==============================] - 69s 622us/step - loss: 0.1645 - acc: 0.9490 - val_loss: nan - val_acc: 0.9522
Epoch 8/10
110288/110288 [==============================] - 69s 622us/step - loss: 0.1409 - acc: 0.9566 - val_loss: nan - val_acc: 0.9528
Epoch 9/10
110288/110288 [==============================] - 69s 622us/step - loss: 0.1273 - acc: 0.9610 - val_loss: nan - val_acc: 0.9591
Epoch 10/10
110288/110288 [==============================] - 69s 622us/step - loss: 0.1176 - acc: 0.9643 - val_loss: nan - val_acc: 0.9670
Sample 1:
il a vu un vieux camion jaune <PAD> <PAD> <PAD> <PAD> <PAD> <PAD> <PAD> <PAD> <PAD> <PAD> <PAD> <PAD> <PAD> <PAD>
Il a vu un vieux camion jaune
Sample 2:
new jersey est parfois calme au l' automne et il est il en <PAD> <PAD> <PAD> <PAD> <PAD> <PAD> <PAD> <PAD>
new jersey est parfois calme pendant l' automne et il est neigeux en avril <PAD> <PAD> <PAD> <PAD> <PAD> <PAD> <PAD>
```

97% Accuracy on unseen data! Pas mal, non? :D
