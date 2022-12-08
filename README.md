# Generating and visualizing marketing insights from Amazon reviews using AWS ecosystem

“This project repository is created in partial fulfillment of the requirements for the Big Data Analytics course offered by the Master of Science in Business Analytics program at the Carlson School of Management, University of Minnesota.”

Usually, generating marketing insights is a manual process which is done via sending out surveys and collecting the results. In this project, we are crowdsourcing market insights using publicly available data such as Amazon reviews and tweets. The advantages of using AWS over other services is that it is cost-effective and it is very easy to integrate various components of the pipeline.

<img width="461" alt="flowchart" src="https://media.github.umn.edu/user/24686/files/cb6ebcf9-69d5-4ba5-b311-6107ba6908e9">

As shown in the above stack, we upload the any product review data or tweets as a CSV/text file to a S3 bucket. We then use AWS comprehend to analyze the text in the reviews to extract the sentiments of the reviews and the key phrases present in them. We then upload the outputs of Comprehend to a DynamoDB table. Since, Quicksight requires the data to be in a tabular format, we use AWS Athena to query the DynamoDB table. We then use the Athena results for displaying the dashboard using Quicksight. The entire pipeline is built using AWS Lambda function.

**Lambda function:**\
Before running the Lambda function, we have a create a role with the following permissions and assign it to the Lambda function.

<img width="630" alt="image" src="https://user-images.githubusercontent.com/40022088/206337079-d989b6c9-86d2-4602-89f3-d51ac3d69e97.png">


**Flyer:**\
![flyer1_new](https://user-images.githubusercontent.com/40022088/206339985-6574d9ce-b50e-455c-83ad-3455ca34a33b.png)
![flyer2new](https://user-images.githubusercontent.com/40022088/206340087-0c3a2d75-075c-4730-bb70-826e6ef93134.png)


**Video Link:**\
The dashboard isn't fully visible in the video. Please refer to the screenshot below for the final dashboard structure.
https://drive.google.com/file/d/1hslRXD58ruDWRPImhlfgIlaFD7vcLn-f/view

**Dashboard:**

<img width="898" alt="image" src="https://user-images.githubusercontent.com/40022088/206047348-91559a72-42a2-49cc-8097-f020bfbba4f0.png">

For the demo, we used sample reviews and tweets forthe latest Apple Watch to build the dashboard. We are displaying the overall sentiment with the major key phrases in each of the reviews.

**Bibiliography and Credits:**
1. https://docs.aws.amazon.com/comprehend/latest/dg/tutorial-reviews-add-docs.html
2. https://www.youtube.com/watch?v=vXiZO1c5Sk0&ab_channel=BeABetterDev
3. https://aws.amazon.com/getting-started/hands-on/analyze-sentiment-comprehend/
4. https://dev.to/aws-builders/finally-dynamodb-support-in-aws-quicksight-sort-of-2lbl

