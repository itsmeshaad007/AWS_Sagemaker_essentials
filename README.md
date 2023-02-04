# ML_Workflow_for_Scones_Unlimited_on_Amazon_SageMaker

Project Steps Overview
Step 1: Data staging
Step 2: Model training and deployment
Step 3: Lambdas and step function workflow
Step 4: Testing and evaluation
Step 5: Cleanup cloud resources

Important features:
Created three lambda functions for the following operations:
 1- A function to serialize target data from S3
 2- ImageClassifier : Lambda function to predict image classification
 3- InferenceConfidenceFilter : Lambda function to fiter inference results based on confidence > 0.97
 
Picture of Lambda functions shown as yellow highlighted:
<img width="689" alt="image" src="https://user-images.githubusercontent.com/121497007/216783841-927af44d-d518-4378-a699-5cf22d57dcf6.png">

Created a step function to integrate these three lambda functions in order
Created some invocations, below is the screenshot of one of the successful invocation:
<img width="832" alt="image" src="https://user-images.githubusercontent.com/121497007/216783908-6f51cae7-12c2-4e50-a9be-9ce29c0e6d2c.png">

The JSON code has been provided separately

We have created total 14 invocations, based on the prediction probability screenshot has been shown below:
<img width="511" alt="image" src="https://user-images.githubusercontent.com/121497007/216783988-4bf83293-4737-409a-8a3e-e0dfd64294d2.png">

