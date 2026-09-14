
## Evolution and Basics of AI

- AI began in the 1950s with simple games and evolved through machine learning in the 1980s, which used statistical models and human-defined features.
- Deep learning emerged around 2010, leveraging large datasets, improved hardware, and neural networks to automate feature extraction, leading to advances like generative AI and large language models.

## Typical AI Workflow

- The AI workflow includes data preparation (collecting and cleaning data), model training (learning patterns from data), model optimization (fine-tuning for accuracy and efficiency), and inference (using the trained model to make predictions on new data).
- Tools like NVIDIA RAPIDS, PyTorch, TensorFlow, TensorRT, and Triton Inference Server support these workflow steps, enabling scalable and efficient AI deployment.

### Deep Learning and Neural Networks

- Deep learning uses artificial neural networks inspired by the human brain's neurons to recognize complex patterns.
- Training involves feeding labeled datasets through a neural network, adjusting connection weights based on prediction accuracy, and iterating to improve performance.
- Models can be optimized post-training for faster inference and integrated into applications for real-time use.

### Challenges and Enterprise Adoption

- AI models are growing in size and complexity, requiring significant computational resources and posing accessibility challenges.
- Delivering rich AI experiences often requires multiple models working together, demanding high performance and scalability.
- Enterprises face challenges in managing evolving AI workloads, infrastructure demands, and ensuring efficient deployment.

### NVIDIA's Role in AI Deployment

- NVIDIA provides an end-to-end AI software stack that accelerates the AI lifecycle from data preparation to inference.
- Their platform offers tools, frameworks, pre-trained models, and management solutions to support AI practitioners, IT professionals, and business leaders.
- This stack enables flexible deployment across cloud, data centers, and edge devices, reducing risks in moving AI from pilot to production.

## The main steps in a typical AI workflow are:

1. **Data Preparation**
    
    - Collecting, cleaning, and preprocessing raw data to make it suitable for training and evaluation.
2. **Model Training**
    
    - Using machine learning or deep learning models to learn patterns from labeled datasets by applying mathematical algorithms.
3. **Model Optimization**
    
    - Fine-tuning the trained model to improve accuracy, efficiency, and suitability for the intended use case.
4. **Inference (Deployment)**
    - Using the trained and optimized model to make predictions or generate outputs on new, unseen data in a real-world environment.
![[Pasted image 20260913064315.png]]

Let's see a typical AI workflow example for deploying an image recognition solution alongside the tools that can be used in each step. ​ImageMe is a radiology clinic that provides services such as MRIs, X-rays and CT scans to several doctor offices. 

​They want to enhance their services by adding image recognition of fractures and tumors, helping doctors and their diagnostics. ​Sarah, an ML engineer, gathers historical datasets containing X-rays, CT scans and MRIs from hospital, research institutes and their own inventory. ​For the data preparation step, she uses RAPIDS, an open-source suite of GPU-accelerated Python libraries built on NVIDIA AI, to perform analytics and to prepare data for machine learning. ​She leverages the RAPIDS accelerator for Apache Spark, a plug-in software that automatically intercepts and accelerates operations that can be sped up with RAPIDS software and GPUs while allowing other operations to continue running on the CPU. ​Once the data prep is complete, PyTorch and TensorFlow are the GPU-accelerated computational frameworks that can be used to train the model at scale. ​They are now integrated with NVIDIA RAPIDS to simplify enterprise AI development. ​Once the model training is complete, it can be optimized using NVIDIA TensorRT, a deep learning inference optimizer to fine-tune and improve the model's performance, making it ready to be deployed, executed and scaled. 

​Lastly, AI inference applies logical rules to the knowledge base to evaluate and analyze new information. ​She uses NVIDIA Triton inference server as an open-source software that standardizes AI model deployment, execution and takes care of all IT and DevOps deployment aspects, such as load balancing. ​
![[Pasted image 20260913064644.png]]

![[Pasted image 20260913064720.png]]

![[Pasted image 20260913064737.png]]![[Pasted image 20260913064758.png]]

![[Pasted image 20260913064825.png]]

![[Pasted image 20260913065035.png]]

## Deep Learning Workflow
Consider an application that automatically identifies various types of animals, in other words, a classification task. ​The first step is to assemble a collection of representative examples to be used as a training dataset, ​which will serve as the experience from which a neural network will learn. ​As we just learned, neural networks are algorithms that draw inspiration from the human brain in understanding complex patterns. ​If the classification is only cats versus dogs, then only cat and dog images are needed in the training dataset. ​In this case, several thousand images will be needed, each with a label indicating whether it is a cat image or a dog image. 

​To ensure the training dataset is representative of all the pictures of cats and dogs that exist in the world, ​it must include a wide range of species, poses, and environments in which dogs and cats may be observed. ​The next component that is needed is a deep neural network model. ​Typically, this will be an untrained neural network designed to perform a general task, ​like detection, classification, or segmentation, on a specific type of input data, like images, text, audio, or video. ​![[Pasted image 20260913065349.png]]Shown here is a simple model of an untrained neural network. ​At the top of the model, there is a row, or layer, that has five input nodes, ​and at the bottom there is a layer that has two output nodes. ​Between the input layer and the output layer are a few hidden layers with several nodes each. ​The interconnecting lines show which nodes in the input layer share their results with nodes in the first hidden layer, ​and so on, all the way down to the output layer. ![[Pasted image 20260913065432.png]]

​Nodes may be referenced as artificial neurons or perceptrons, ​since their simple behavior is inspired by the neurons in the human brain. ​A typical deep neural network model would have many hidden layers between the input layer and the output layer, ​which is why it is called deep. ​We use a simplified representation on this slide for brevity. ​The design of the neural network model is what makes it suitable for a particular task. ​For example, image classification models are very different from speech recognition models. ​The differences can include the number of layers, the number of nodes in each layer, ​the algorithms performed in each node, and the connections between the nodes. ​There are readily available deep neural network models for image classification, ​object recognition, image segmentation, and several other tasks, ​but it is often necessary to modify these models to achieve high levels of accuracy for a particular dataset. 

​For the image classification task to distinguish images of cats versus dogs, ​a convolutional neural network, such as AlexNet, would probably be used. ​AlexNet is comprised of nodes that implement simple generalized algorithms. ​Using these simple generalized algorithms is a key difference and advantage ​for deep learning versus earlier approaches to machine learning, ​which required many custom data-specific feature extraction algorithms ​to be developed by specialists for each dataset and task. ​Once a training dataset has been assembled and a neural network model selected, ​a deep learning framework is used to feed the training dataset through the neural network. ​For each image that is processed through the neural network, ​each node in the output layer reports a number that indicates ​how confident it is that the image is a dog or a cat. ​In this case, there are only two options, ​so the model needs just two nodes in the output layer, ​one for dogs and one for cats. ​When these final outputs are sorted in a most-confident to least-confident manner, ​the result is called a **==confidence vector==.** 
![[Pasted image 20260913065739.png]]

​The deep learning framework then looks at the label for the image ​to determine whether the neural network guessed or inferred the result. ​inferred the correct answer. If it inferred correctly, the framework strengthened the ​weights of the connections that contributed to getting the correct answer. And vice versa, ​if the neural network inferred the incorrect result, the framework reduces the weights ​of the connections that contributed to getting the wrong answer. ​![[Pasted image 20260913065856.png]]After processing the entire training dataset once, the neural network will generally have ​enough experience to infer the correct answer a little more than half of the time, slightly ​better than a random coin toss. It'll require several additional rounds to achieve higher ​levels of accuracy. ​Now that the model has been trained on a large representative dataset, it has become better ​at distinguishing between cats and dogs. But if it were shown a picture of a raccoon, it ​would likely assign comparable confidence scores to both the dog and cat, as it wouldn't ​be certain about identifying either one. If it was necessary to classify raccoons as ​well as dogs and cats, the design topology of the model would need to be modified to ​add a third node to the output layer. The training dataset would be expanded to include ​thousands of representative images of raccoons and use the deep learning framework to retrain ​the model. ![[Pasted image 20260913070008.png]]

​Once the model has been trained, much of the generalized flexibility that was necessary ​during the training process is no longer needed, so it is possible to optimize the model for ​significantly faster runtime performance. Common optimizations include fusing layers ​to reduce memory and communication overhead, pruning nodes that do not contribute significantly ​to the results, and other techniques. ​The fully trained and optimized model is then ready to be integrated into an application ​that will feed it new data, in this case, images of cats and dogs that it hasn't seen ​before. As a result, it will be able to quickly and accurately infer the correct answer based ​on its training.![[Pasted image 20260913070057.png]] ​Let's summarize the key differences in the realm of AI we've covered till now. ​When most technology companies talk about doing AI, they're talking about using machines ​to mimic human abilities to learn, analyze, and predict. Machine learning achieves that ​by using large datasets and sophisticated statistical methods to train a model to predict ​outcomes from new incoming information.
![[Pasted image 20260913070155.png]]

## Deploying AI in Real-World Applications
![[Pasted image 20260913070244.png]]



## How can NVIDIA's AI software stack optimize AI deployment?

NVIDIA's AI software stack optimizes AI deployment by providing:

- **Comprehensive Tools and Frameworks:** Supports the entire AI lifecycle from data preparation (using RAPIDS) through model training (with GPU-accelerated frameworks like PyTorch and TensorFlow) to model optimization (using TensorRT).
    
- **Efficient Inference Management:** Uses Triton Inference Server to standardize model deployment, handle load balancing, and simplify IT and DevOps tasks.
    
- **Performance and Scalability:** Optimizes models for faster runtime, reduces memory overhead, and ensures high availability and security.
    
- **Flexibility:** Enables deployment across various environments—public cloud, data centers, and edge devices—reducing risks when moving AI solutions from pilot to production.
![[Pasted image 20260913070536.png]]

![[Pasted image 20260913121945.png]]
file:///home/amit/Downloads/Unit%2002%20-%20Introduction%20to%20Artificial%20Inteligence%20-%20Summary.pdf

