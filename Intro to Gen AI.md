​Generative AI is making inroads into every industry, transforming traditional practices ​and bringing forth unprecedented operational efficiency and innovation. ​
**Finance**- It enhances fraud detection, personalized banking, and provides valuable investment ​insights. ​
**Healthcare** - It powers molecule simulation, drug discovery, and clinical trial data analysis. ​Retail benefits from personalized shopping, automated catalog descriptions, and automatic ​price optimization. 
**Manufacturing** - It transforms factory simulation, product design, and predictive maintenance. .

## Foundation Models
* Foundation models are the basis for the creation & evolution of GenAI systems.
* Initial framework for understanding complex language structures, semantics, & contextual nuances.
* Consist of AI neural networks trained on massive unlabeled datasets, generally with unsupervised learning.
* Rely on finding patterns & structures in the data on its own, without requiring labeled data.
### Examples of Foundation Models
![[Pasted image 20260913131211.png]]

## How foundation models are trained.
A foundation model is trained on a large amount of unlabeled data, thatt is, data that does not have any predefined categories, labels, or annotations, such as raw text, images, audio, or video. **Unlabeled Data** is abundant & diverse, and can be obtained from various sources, such as the Internet, Social media platforms, or proprietary datasets. A foundation model trained on text data can be used to solve problems related to natural language processing such as question answering, information extration, etc.
![[Pasted image 20260913132113.png]]

## Transformer Architecture 
* Large Language Models (LLMs) utilize a specialized neural network known as the Transformer to grasp patterns & relationships within textual data. 
* LLMs undergo pre-training on extensive text datasets & can be fine-tuned for specific tasks. 
* The goal of the language model is to predict the next word in a sequence.
While this example pertains to the English language, the prediction could apply to a ​computer programming language or another language. ​The model generates text one word at a time based on an input prompt provided by the user. ​In this case, the input prompt is, write a review about an Italian restaurant I visited ​and enjoyed. ​The input prompt is broken down into smaller tokens that are then fed back into the model. ​The model then predicts the next word in the sequence based on the tokens it has received. 
​This process continues until the user stops providing input or the model reaches a predetermined ​stopping point.

![[Pasted image 20260913132739.png]]

![[Pasted image 20260913132810.png]]

### Tokens
LLMs are constructed based on tokens, which represent the smallest units of meaning in a language. Tokens encompass words, characters, sub-words, or other symbols representing linguistic elements. 
The transformer model architecture empowers the LLM to comprehend & recognize relationships & connections betwen tokens & concepts using a self-atttention mechanism. This mechanism assigns a score, commonly referred to as a **weight**, to a given item or token to determine the relationship.

Generative AI models often involve complex mathematical operations and require intensive ​computations. ​GPUs are designed to be highly effective for parallel processing.
![[Pasted image 20260913133443.png]]
This parallelism enables faster training and inference times for generative AI models compared ​to using traditional CPUs. ​GPUs excel in parallel processing, matrix operations, memory capacity, and memory bandwidth, ​making them an ideal choice for powering up generative AI. ​

![[Pasted image 20260913133512.png]]

![[Pasted image 20260913133605.png]]

Generative AI use cases in the healthcare and financial sectors should be monitored ​very closely to forestall any **money-related or sensitive data leakages**. ​IP rights and copyright ​Generative AI platforms should **mitigate copyright infringement of the creator's work**. ​Bias, errors, and limitations ​Generative AI is just as prone to biases as humans are because in many ways it is trained ​on our own biases. ​**Ethical implications** ​Determining responsibility for the outputs of generative AI can be challenging. ​If AI systems generate harmful content, it may be unclear who bears responsibility – the ​developers, the users, or the technology itself. ​**Malevolent activities** ​There is no state-of-the-art know-how that wrongdoers can't put to their evil uses, ​and generative AI is not an exception where fraudulent scams of various kinds can be created. ​

## Practical Applications of GenAI in the Enterprise

![[Pasted image 20260913133837.png]]

GenAI produces new content based on patterns & trends learned from trainign data. 
Traditional AI on the other hand, focuses on detecting patters, making decisions, honing analytics, classifying data, and detecting fraud. 
** Gen AI & Traditional AI are not mutually exclusive, but complementary.**
![[Pasted image 20260913134108.png]]


![[Pasted image 20260913134127.png]]

## Requirements for Building Custom LLMs
* Data Training - To get these models to understand, predict & generate human-like text, we need to feed them with a substantial corpus of diverse & high-quality data. 
* Accelerated Computing - The sheer scale of computations required for training these models is immense. It demands a robust, large-scale computing infrastructure, which is expensive. Implementing LLMs requires more than just the right hardware. 
* Inferencing & Training Tools - Orgs need tools that address both training & inference challenges, from algorithm development to accelerating inference on a distributed infrastructure. LLMs are complex & sophisticated. 
* AI Expertise - Developing & fine-tuning these models require teams with a high degree of technical expertise in these areas which can be difficult to find & retain.
![[Pasted image 20260913135036.png]]

## Getting started with GenAI
![[Pasted image 20260913135123.png]]

​This involves identifying our internal resources and coupling them with AI expertise from partners ​and application providers, forming an interdisciplinary team that understands both our business and ​the AI landscape. ​Analyze data for training and customization. ​This is where we acquire, refine, and protect our data in order to build data-intensive ​foundation models or customize existing ones. ​Invest in accelerated infrastructure. ​This includes assessing our current infrastructure, architecture, and operating model, while carefully ​considering associated costs and energy consumption. ​The right infrastructure will enable an efficient and effective deployment of our AI solutions. ​Develop a plan for responsible AI. ​This means leveraging tools and best practices. ​practices to ensure that our AI models and applications uphold ethical standards and ​operate responsibly.

![[Pasted image 20260913135352.png]]

## Workflow to Build a GenAI Soultion 
![[Pasted image 20260913135429.png]]

The **data acquisition** phase involves collecting and preparing the data that'll be used to ​train and fine-tune the LLM. ​The data can come from various sources, such as public datasets, web scraping, user-generated ​content, or proprietary data. ​It's important that the data is diverse and representative of the target domain. ​Once there is enough data gathered, comes **data curation**. 
​This phase involves cleaning, filtering, and organizing the data that'll be used to ​train and fine-tune the LLM. ​The **pre-training** phase of an LLM involves exposing the model to a vast corpus of text ​data to facilitate the learning of language patterns, relationships, and representations. ​This phase typically incorporates a foundational model as the starting point. ​**Customization** allows the adaptation of a generic model to the specific requirements of a given ​task or domain, thereby improving its accuracy, efficiency, and effectiveness. ​**Model evaluation** is the process of assessing the performance and effectiveness of a machine ​learning model. ​It involves measuring how well the model has learned from the training data and how accurately ​it can make predictions on unseen or new data. ​After a model has been trained on a dataset, it is deployed for inference, where it processes ​input data and produces output, such as classifications, predictions, or recommendations, depending ​on the specific task it was trained for.
Adding **guardrails**=to an LLM is crucial for fostering responsible AI practices and mitigating ​the risks associated with the misuse or misinterpretation of the generated text. ​It helps ensure ethical, safe, and responsible use of the model.

![[Pasted image 20260913140742.png]]

