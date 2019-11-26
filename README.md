# EIP4
Logs for 20 epochs:
------------------

Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 9s 150us/step - loss: 0.5227 - acc: 0.8552 - val_loss: 0.1230 - val_acc: 0.9707
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 6s 102us/step - loss: 0.2543 - acc: 0.9249 - val_loss: 0.0614 - val_acc: 0.9867
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 6s 105us/step - loss: 0.2008 - acc: 0.9396 - val_loss: 0.0556 - val_acc: 0.9860
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 6s 105us/step - loss: 0.1705 - acc: 0.9461 - val_loss: 0.0525 - val_acc: 0.9864
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 6s 105us/step - loss: 0.1571 - acc: 0.9471 - val_loss: 0.0334 - val_acc: 0.9910
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 6s 106us/step - loss: 0.1429 - acc: 0.9505 - val_loss: 0.0287 - val_acc: 0.9918
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 6s 104us/step - loss: 0.1361 - acc: 0.9518 - val_loss: 0.0321 - val_acc: 0.9911
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 6s 105us/step - loss: 0.1255 - acc: 0.9537 - val_loss: 0.0273 - val_acc: 0.9935
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 6s 104us/step - loss: 0.1170 - acc: 0.9553 - val_loss: 0.0227 - val_acc: 0.9944
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 6s 104us/step - loss: 0.1162 - acc: 0.9555 - val_loss: 0.0243 - val_acc: 0.9934
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 6s 104us/step - loss: 0.1124 - acc: 0.9549 - val_loss: 0.0216 - val_acc: 0.9944
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 6s 104us/step - loss: 0.1086 - acc: 0.9556 - val_loss: 0.0219 - val_acc: 0.9941
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 6s 105us/step - loss: 0.1095 - acc: 0.9545 - val_loss: 0.0189 - val_acc: 0.9955
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 6s 106us/step - loss: 0.1036 - acc: 0.9561 - val_loss: 0.0249 - val_acc: 0.9922
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 6s 103us/step - loss: 0.1019 - acc: 0.9565 - val_loss: 0.0192 - val_acc: 0.9948
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 6s 102us/step - loss: 0.1001 - acc: 0.9566 - val_loss: 0.0205 - val_acc: 0.9946
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 6s 105us/step - loss: 0.0992 - acc: 0.9568 - val_loss: 0.0181 - val_acc: 0.9953
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 6s 105us/step - loss: 0.0970 - acc: 0.9569 - val_loss: 0.0190 - val_acc: 0.9953
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 6s 105us/step - loss: 0.0982 - acc: 0.9567 - val_loss: 0.0195 - val_acc: 0.9946
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 6s 104us/step - loss: 0.0959 - acc: 0.9559 - val_loss: 0.0185 - val_acc: 0.9953
<keras.callbacks.History at 0x7fa7d68d74e0>


result of model.evaluate (on test data)
---------------------------------------
[0.018549398415803442, 0.9953]

Strategy
--------

After running the eigth example, Observed more computations @32 kernels in second layer.
So, thought of reducing the kernels and started with 8 kernels.

Received the desired results with this change.
