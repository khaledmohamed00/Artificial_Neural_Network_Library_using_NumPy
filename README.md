# Artificial_Neural_Network_Library_using_NumPy from scratch 
## how to use ANN.py to create Artificial_Neural_Network 

1. first choose network layers and neurons per layer from input unit to output unit 
   * Example network =[2,50,20,3] input unit=2 ,first hidden=50 ,second hidden=20 ,output softmax layer=3
2. then create network object ANN and choose 
   *  Optimizer=['adam','momentum','SGD']
   *  Regularization='[L2',dropout','none']
   *  Activation_function=['relu','sigmoid']
   *  Then choose hyperparameter
   *  Learning_rate
   *  Lambd, for L2 regularziation 
   *  Keep_prop for dropout
   *  Beta for optimizer ='momentum' 
   *  Batch_size  for minibatch 
   *    Example: 
        ```
        net=ANN(network,iteration=300,optimizer='adam',regularization='L2',activation_function='relu',
                        learning_rate=0.1,lambd=0.2,keep_prop=0.9,beta=0.9,batch_size=64)    
        ```
        
3. Then call fit function and feed it with input and output (hot encoded)
   *  ```
      loss=net.fit(X,y_hot) #fit function returns losses you can plot it
      ```
4. you can use to check training acuracy 
   * ```
   net.predict(X,y)
   ```

5. to make prediction use 
   *
    ``` 
    scores,zs = net.forward_prop(X) # scores[-1] is the softmax output unit
    ```


