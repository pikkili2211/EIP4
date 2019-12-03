# EIP4
Final Validation accuracy for Base Network
------------------------------------------
Accuracy on test data is: 82.19

model definition (model.add... ) with output channel size and receptive field
------------------------------------------------------------------------------

model.add(SeparableConv2D(48, 3, 3, border_mode='same', input_shape=(32, 32, 3))) #(output size is 32*32*48,R.F is 3*3)
model.add(BatchNormalization())
model.add(Activation('relu'))
model.add(SeparableConv2D(96, 3, 3,border_mode='same')) #(32*32*96,5*5)
model.add(BatchNormalization())
model.add(Activation('relu'))
model.add(SeparableConv2D(192, 3, 3,border_mode='same')) #(32*32*192,7*7)
model.add(BatchNormalization())
model.add(Activation('relu'))
model.add(SeparableConv2D(48, 1, 1,border_mode='same'))  #(32*32*48,7*7)
model.add(BatchNormalization())
model.add(Activation('relu'))
model.add(MaxPooling2D(pool_size=(2, 2))) #(16*16*48,14*14)
model.add(Dropout(0.2))

model.add(SeparableConv2D(96, 3, 3)) #(14*14*96,16*16)
model.add(BatchNormalization())
model.add(Activation('relu'))
model.add(SeparableConv2D(192, 3, 3)) #(12*12*192,18*18)
model.add(BatchNormalization())
model.add(Activation('relu'))
model.add(Dropout(0.2))
model.add(SeparableConv2D(48, 1, 1)) #(12*12*48,18*18)
model.add(BatchNormalization())
model.add(Activation('relu'))


model.add(SeparableConv2D(96, 3, 3)) #(10*10*96,20*20)
model.add(BatchNormalization())
model.add(Activation('relu'))
model.add(SeparableConv2D(192, 3, 3)) #(8*8*192,22*22)
model.add(BatchNormalization())
model.add(Activation('relu'))
model.add(SeparableConv2D(num_classes, 1, 1)) #(8*8*10,22*22)
model.add(GlobalAveragePooling2D(data_format=None)) #10,30*30)

model.add(Activation('softmax'))


50 epoch logs
------------------
Epoch 1/50
390/390 [==============================] - 25s 65ms/step - loss: 1.4808 - acc: 0.4700 - val_loss: 1.3247 - val_acc: 0.5454
Epoch 2/50
390/390 [==============================] - 19s 48ms/step - loss: 1.0157 - acc: 0.6353 - val_loss: 1.0217 - val_acc: 0.6375
Epoch 3/50
390/390 [==============================] - 19s 48ms/step - loss: 0.8554 - acc: 0.6961 - val_loss: 0.9432 - val_acc: 0.6801
Epoch 4/50
390/390 [==============================] - 19s 48ms/step - loss: 0.7591 - acc: 0.7307 - val_loss: 0.8285 - val_acc: 0.7168
Epoch 5/50
390/390 [==============================] - 19s 48ms/step - loss: 0.6972 - acc: 0.7560 - val_loss: 0.7751 - val_acc: 0.7425
Epoch 6/50
390/390 [==============================] - 19s 48ms/step - loss: 0.6362 - acc: 0.7771 - val_loss: 0.8591 - val_acc: 0.7191
Epoch 7/50
390/390 [==============================] - 19s 48ms/step - loss: 0.5986 - acc: 0.7914 - val_loss: 0.7297 - val_acc: 0.7596
Epoch 8/50
390/390 [==============================] - 19s 48ms/step - loss: 0.5683 - acc: 0.8012 - val_loss: 0.7979 - val_acc: 0.7335
Epoch 9/50
390/390 [==============================] - 19s 48ms/step - loss: 0.5453 - acc: 0.8093 - val_loss: 0.6509 - val_acc: 0.7845
Epoch 10/50
390/390 [==============================] - 19s 48ms/step - loss: 0.5178 - acc: 0.8202 - val_loss: 0.6711 - val_acc: 0.7763
Epoch 11/50
390/390 [==============================] - 18s 47ms/step - loss: 0.4983 - acc: 0.8256 - val_loss: 0.6559 - val_acc: 0.7874
Epoch 12/50
390/390 [==============================] - 19s 50ms/step - loss: 0.4804 - acc: 0.8304 - val_loss: 0.6638 - val_acc: 0.7885
Epoch 13/50
390/390 [==============================] - 19s 49ms/step - loss: 0.4599 - acc: 0.8400 - val_loss: 0.8392 - val_acc: 0.7427
Epoch 14/50
390/390 [==============================] - 19s 48ms/step - loss: 0.4444 - acc: 0.8436 - val_loss: 0.6114 - val_acc: 0.8011
Epoch 15/50
390/390 [==============================] - 19s 48ms/step - loss: 0.4315 - acc: 0.8482 - val_loss: 0.7280 - val_acc: 0.7674
Epoch 16/50
390/390 [==============================] - 19s 48ms/step - loss: 0.4147 - acc: 0.8534 - val_loss: 0.6360 - val_acc: 0.7889
Epoch 17/50
390/390 [==============================] - 19s 49ms/step - loss: 0.4005 - acc: 0.8584 - val_loss: 0.6914 - val_acc: 0.7867
Epoch 18/50
390/390 [==============================] - 19s 49ms/step - loss: 0.3843 - acc: 0.8656 - val_loss: 0.7956 - val_acc: 0.7675
Epoch 19/50
390/390 [==============================] - 19s 48ms/step - loss: 0.3823 - acc: 0.8670 - val_loss: 0.6319 - val_acc: 0.7953
Epoch 20/50
390/390 [==============================] - 19s 48ms/step - loss: 0.3685 - acc: 0.8685 - val_loss: 0.6484 - val_acc: 0.7994
Epoch 21/50
390/390 [==============================] - 19s 49ms/step - loss: 0.3579 - acc: 0.8747 - val_loss: 0.6025 - val_acc: 0.8111
Epoch 22/50
390/390 [==============================] - 19s 50ms/step - loss: 0.3492 - acc: 0.8766 - val_loss: 0.7072 - val_acc: 0.7813
Epoch 23/50
390/390 [==============================] - 19s 48ms/step - loss: 0.3345 - acc: 0.8826 - val_loss: 0.6684 - val_acc: 0.7990
Epoch 24/50
390/390 [==============================] - 19s 48ms/step - loss: 0.3284 - acc: 0.8844 - val_loss: 0.6871 - val_acc: 0.8005
Epoch 25/50
390/390 [==============================] - 19s 48ms/step - loss: 0.3207 - acc: 0.8876 - val_loss: 0.7714 - val_acc: 0.7781
Epoch 26/50
390/390 [==============================] - 19s 48ms/step - loss: 0.3135 - acc: 0.8879 - val_loss: 0.7900 - val_acc: 0.7759
Epoch 27/50
390/390 [==============================] - 19s 48ms/step - loss: 0.3126 - acc: 0.8888 - val_loss: 0.6940 - val_acc: 0.7972
Epoch 28/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2983 - acc: 0.8941 - val_loss: 0.6289 - val_acc: 0.8146
Epoch 29/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2879 - acc: 0.8989 - val_loss: 0.6044 - val_acc: 0.8194
Epoch 30/50
390/390 [==============================] - 19s 47ms/step - loss: 0.2899 - acc: 0.8951 - val_loss: 0.7029 - val_acc: 0.7969
Epoch 31/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2807 - acc: 0.8991 - val_loss: 0.5766 - val_acc: 0.8265
Epoch 32/50
390/390 [==============================] - 18s 47ms/step - loss: 0.2715 - acc: 0.9030 - val_loss: 0.7069 - val_acc: 0.7931
Epoch 33/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2709 - acc: 0.9032 - val_loss: 0.6179 - val_acc: 0.8205
Epoch 34/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2629 - acc: 0.9058 - val_loss: 0.6278 - val_acc: 0.8207
Epoch 35/50
390/390 [==============================] - 19s 47ms/step - loss: 0.2580 - acc: 0.9074 - val_loss: 0.6865 - val_acc: 0.8054
Epoch 36/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2518 - acc: 0.9096 - val_loss: 0.6895 - val_acc: 0.8129
Epoch 37/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2475 - acc: 0.9099 - val_loss: 0.6650 - val_acc: 0.8043
Epoch 38/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2405 - acc: 0.9135 - val_loss: 0.6641 - val_acc: 0.8189
Epoch 39/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2308 - acc: 0.9166 - val_loss: 0.7316 - val_acc: 0.8006
Epoch 40/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2346 - acc: 0.9159 - val_loss: 0.6304 - val_acc: 0.8123
Epoch 41/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2291 - acc: 0.9182 - val_loss: 0.7194 - val_acc: 0.8003
Epoch 42/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2192 - acc: 0.9218 - val_loss: 0.6677 - val_acc: 0.8138
Epoch 43/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2240 - acc: 0.9184 - val_loss: 0.7029 - val_acc: 0.8137
Epoch 44/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2227 - acc: 0.9191 - val_loss: 0.7231 - val_acc: 0.8046
Epoch 45/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2153 - acc: 0.9218 - val_loss: 0.6363 - val_acc: 0.8243
Epoch 46/50
390/390 [==============================] - 19s 47ms/step - loss: 0.2098 - acc: 0.9242 - val_loss: 0.6464 - val_acc: 0.8224
Epoch 47/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2108 - acc: 0.9232 - val_loss: 0.7517 - val_acc: 0.7971
Epoch 48/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2002 - acc: 0.9269 - val_loss: 0.6379 - val_acc: 0.8325
Epoch 49/50
390/390 [==============================] - 19s 48ms/step - loss: 0.2048 - acc: 0.9258 - val_loss: 0.7077 - val_acc: 0.8143
Epoch 50/50
390/390 [==============================] - 19s 48ms/step - loss: 0.1980 - acc: 0.9283 - val_loss: 0.6631 - val_acc: 0.8219
