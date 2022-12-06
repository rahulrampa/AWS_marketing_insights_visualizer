# Generating and visualizing marketing insights from Amazon reviews using AWS ecosystem

“This project repository is created in partial fulfillment of the requirements for the Big Data Analytics course offered by the Master of Science in Business Analytics program at the Carlson School of Management, University of Minnesota.”

Usually, generating marketing insights is a manual process which is done via sending out surveys and collecting the results. In this project, we are automating the generation and visualization of customer insights using Amazon reviews and tweets. 


<img width="461" alt="flowchart" src="https://media.github.umn.edu/user/24686/files/cb6ebcf9-69d5-4ba5-b311-6107ba6908e9">


As shown in the above stack, we upload the any product review data or tweets as a CSV/text file to a S3 bucket. We then use AWS comprehend to analyze the text in the reviews to extract the sentiments of the reviews and the key phrases present in them. We then upload the outputs of Comprehend to a DynamoDB table. Since, Quicksight requires the data to be in a tabular format, we use AWS Athena to query the DynamoDB table. We then use the Athena results for displaying the dashboard using Quicksight. The entire pipeline is built using AWS Lambda which is used for connecting various AWS tools.



**Flyer:**
![flyer1](https://user-images.githubusercontent.com/40022088/206045627-40741113-1b48-416a-a6ea-9e9a398d2b16.png)
![flyer2](https://user-images.githubusercontent.com/40022088/206045642-9ef544e7-01af-4801-8bbb-432f3a428c20.png)

**Dashboard:
<img width="898" alt="image" src="https://user-images.githubusercontent.com/40022088/206047348-91559a72-42a2-49cc-8097-f020bfbba4f0.png">

**Bibiliography and Credits:**
1. https://docs.aws.amazon.com/comprehend/latest/dg/tutorial-reviews-add-docs.html
2. https://www.youtube.com/watch?v=vXiZO1c5Sk0&ab_channel=BeABetterDev
3. https://aws.amazon.com/getting-started/hands-on/analyze-sentiment-comprehend/
4. https://dev.to/aws-builders/finally-dynamodb-support-in-aws-quicksight-sort-of-2lbl

