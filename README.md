# Deep-Federated-Learning

Federated Learning (FL) is a distributed machine learning process in which each participant node (or party) retains their data locally and interacts with other participants via a learning protocol. One main driver behind FL is the need to not share data with others due to privacy and confidentially concerns. Another driver is to improve the speed of training a machine learning model by leveraging other participants' training processes.

Setting up such a federated learning system requires setting up a communication infrastructure, converting machine learning algorithms to federated settings and in some cases knowing about the intricacies of security and privacy enabling techniques such as differential privacy and multi-party computation.

<h3>Pre-Requisite<h3>
<h6>pip install --upgrade tensorflow-federated<h6>
    
<h2>Federated Learning (FL)<h2> 
<b>Federated Learning (FL)<b> is a distributed machine learning process in which each participant node (or party) retains their data locally and interacts with other participants via a learning protocol. One main driver behind FL is the need to not share data with others due to privacy and confidentially concerns. Another driver is to improve the speed of training a machine learning model by leveraging other participants' training processes.

Setting up such a federated learning system requires setting up a communication infrastructure, converting machine learning algorithms to federated settings and in some cases knowing about the intricacies of security and privacy enabling techniques such as differential privacy and multi-party computation.

In the above  Notebook we use IBM FL to have multiple parties train a classifier to recognise handwritten digits in the MNIST dataset.

For a more technical dive into IBM FL, refer the whitepaper here.

In the following cells, we set up each of the components of a Federated Learning network (See Figure below) wherein all involved parties aid in training their respective local cartpoles to arrive at the upright pendulum state. In this notebook we default to 2 parties, but depending on your resources you may use more parties.
  
 <img width="937" alt="FL_Network" src="https://user-images.githubusercontent.com/43134572/120935769-c3546880-c71d-11eb-8c8d-b260e9437fac.png">

<h2>Digit Recognition<h2>
    
![MnistExamples](https://user-images.githubusercontent.com/43134572/120935899-5beae880-c71e-11eb-9b04-e44eec63f5c6.png)

  
Running the Aggregator
Next we pass the configuration parameters set in the previous cell to instantiate the Aggregator object. Finally, we start() the Aggregator process.
    
  <img width="866" alt="arch_party" src="https://user-images.githubusercontent.com/43134572/120935835-16c6b680-c71e-11eb-9067-e125ad2dca0b.png">
Starting Parties
Now that we have Aggregator running, next we go to Parties' notebooks (keras_classifier_p0.ipynb and keras_classifier_p1.ipynb) to start and register them with the Aggregator. Once all the parties are done with registration, we will move to next step to start training.

<h3>Training and Evaluation<h3>
Now that our network has been set up, we begin training the model by invoking the Aggregator's start_training() method.

This could take some time, depending on your system specifications. Feel free to get your doze of coffee meanwhile ☕
    
  
