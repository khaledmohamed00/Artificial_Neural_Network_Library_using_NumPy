# Artificial_Neural_Network_Library_using_NumPy
## how to use ANN.py to create Artificial_Neural_Network 

1.first choose network layers and neurons per layer from input unit to output unit 
   *network=[2,50,20,3]
   *then create network object and choose 
   *optimizer=['adam','momentum','SGD']
   *regularization='[L2',dropout','none']
   *activation_function=['relu','sigmoid']

2.then choose hyperparameter
-learning_rate=0.1,
-lambd=0.2, for L2 regularziation 
-keep_prop=0.9, for dropout
-beta=0.9, for optimizer ='momentum' 
-batch_size=64
#example:

net=ANN(network,iteration=300,optimizer='adam',regularization='L2',activation_function='relu',learning_rate=0.1,lambd=0.2,keep_prop=0.9,beta=0.9,batch_size=64)    

then call fit function and feed it with input and output (hot encoded)

loss=net.fit(X,y_hot)

fit function returns losses you can plot it
plt.plot(loss)
Show the plot
plt.show

