# Generating and visualizing marketing insights from Amazon reviews using AWS ecosystem

“This project repository is created in partial fulfillment of the requirements for the Big Data Analytics course offered by the Master of Science in Business Analytics program at the Carlson School of Management, University of Minnesota.”

** place holder for introduction about the marketing insights and what is currently happening**.

In this project, we are automating the generation and visualization of customer insights using AWS tools. 


<img width="461" alt="flowchart" src="https://media.github.umn.edu/user/24686/files/cb6ebcf9-69d5-4ba5-b311-6107ba6908e9">


As shown in the above stack, we upload the any product review data as a CSV/text file to a S3 bucket. We then use AWS comprehend to analyze the text in the reviews and upload the relavent outputs to a DynamoDB table which is then used for depicting insights from the reviews using a QuickSight Dashboard. The entire pipeline is built using AWS Lambda which is used for connecting various AWS tools.



**Flyer Image here:**


**Bibiliography and Credits:**
1. https://docs.aws.amazon.com/comprehend/latest/dg/tutorial-reviews-add-docs.html
2. https://www.youtube.com/watch?v=vXiZO1c5Sk0&ab_channel=BeABetterDev
3. https://aws.amazon.com/getting-started/hands-on/analyze-sentiment-comprehend/
4. https://dev.to/aws-builders/finally-dynamodb-support-in-aws-quicksight-sort-of-2lbl

