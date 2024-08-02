# bankingbotw-awslex
BankerBot is a sophisticated chatbot designed to revolutionize customer interactions in the banking sector. Built using Amazon Lex and AWS Lambda, this project demonstrates the creation of a powerful, context-aware virtual assistant capable of handling complex banking tasks such as account balance inquiries and fund transfers.
Building a Multi-Slot Chatbot with Amazon Lex and AWS Lambda
Project Overview
This project demonstrates the creation of a sophisticated chatbot called BankerBot using Amazon Lex and AWS Lambda. The chatbot is designed to assist bank customers with checking account balances and transferring funds between accounts. This project showcases the integration of various AWS services and advanced chatbot features.
Technologies Used

Amazon Lex
AWS Lambda
AWS CloudFormation
AWS CloudWatch

Features

Multiple intents: WelcomeIntent, CheckBalance, FollowupCheckBalance, TransferFunds
Custom slot types for account types
Context carryover between intents
Integration with AWS Lambda for dynamic responses
Confirmation prompts for sensitive operations
CloudFormation template for rapid deployment

Step-by-Step Guide
1. Setting Up the Chatbot

Created a new Amazon Lex bot named "BankerBot".
Configured basic settings including IAM permissions and voice interaction options.
Set up the WelcomeIntent with appropriate utterances and responses.
Customized the FallbackIntent for better user experience.

2. Creating Custom Slot Types

Created a custom slot type "accountType" with values: Checking, Savings, Credit.
Added synonyms for better natural language understanding.

3. Implementing CheckBalance Intent

Created the CheckBalance intent with sample utterances.
Added slots for account type and date of birth.
Connected the intent to an AWS Lambda function for dynamic balance retrieval.

4. Setting Up Context Carryover

Created an output context from CheckBalance intent.
Implemented FollowupCheckBalance intent using the carried-over context.
Configured slots to use default values from the previous context.

5. Creating TransferFunds Intent

Set up TransferFunds intent with multiple slots: sourceAccountType, targetAccountType, transferAmount.
Implemented confirmation prompts for fund transfer operations.
Added appropriate responses for confirmation and declination.

6. Exploring Advanced Features

Utilized the Conversation Flow feature to visualize the chatbot's dialogue structure.
Explored the Visual Builder for a graphical representation of the intent structure.

7. Deployment with CloudFormation

Created a CloudFormation template (nextwork-banker-bot.yaml) to define the chatbot resources.
Deployed the chatbot using the CloudFormation template for rapid setup.
Troubleshooted and resolved Lambda function permission issues.

Challenges and Solutions

Encountered issues with Lambda function permissions when deploying via CloudFormation.
Solution: Created a new Lambda function and set up appropriate resource-based policy statements to grant access to the chatbot.

Conclusion
This project demonstrates the power and flexibility of Amazon Lex in creating sophisticated chatbots. By integrating with AWS Lambda and utilizing features like context carryover and custom slot types, we created a functional banking assistant capable of handling account inquiries and fund transfers. The use of CloudFormation for deployment showcases how infrastructure-as-code can streamline the setup process for complex AWS resources.
