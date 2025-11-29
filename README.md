# Shop Assist 2.0 – Intelligent Laptop Recommendation Chatbot
## Objective:
The goal of this project is to enhance Shop Assist AI by leveraging the newly introduced 'function calling' feature. This will enable us to enhance the customer experience by creating a more streamlined and efficient chatbot, gaining valuable experience in conversational AI while contributing to the development of innovative AI solutions. The key tasks include:
1. Integrate Function Calling API: Update the existing architecture to incorporate the Function Calling API, improving performance. Identify which layers can be removed or updated to align with the new approach.
2. Refine Conversation Flow: Improve the chatbot's conversation flow using function calling to make interactions with users more natural and dynamic.
## Project Background:
The increasing popularity of e-commerce has introduced challenges like information overload and lack of personalized assistance. Consumers often struggle to navigate vast catalogs of products to find items matching their preferences. ShopAssist 2.0 addresses this issue by combining large language models and rule-based functions to deliver tailored and dynamic shopping assistance.
## Problem Statement:
Given a dataset containing detailed information about laptops (product names, specifications, descriptions, etc.), the objective is to:
* Build a chatbot capable of processing this dataset.
* Provide accurate and personalized laptop recommendations based on user inputs.
* Leverage advanced AI capabilities for seamless, dynamic, and user-centric conversations.
## Approach:
The implementation follows a structured three-step process:
1. Conversation and Information Gathering: The chatbot interacts with the user to gather preferences, using natural language processing to extract requirements.
2. Dataset Processing and Information Extraction: Rule-based functions parse the dataset to identify laptops that best match the criteria.
3. Personalized Recommendations: The system refines and delivers suggestions, maintaining a conversational flow to address further questions.
## System Design
Dataset: We have a dataset laptop.csv where each row describes the features of a single laptop and also has a small description at the end. The chatbot that we build will leverage LLMs to parse this Description column and provide recommendations.

Here's the overall flow of conversation for the ShopAssist Chatbot:
The chatbot should ask a series of questions to determine the user's requirements. For simplicity, we have used 6 features to encapsulate the user's needs. The 6 features are as follows:
1. GPU intensity
2. Display quality
3. Portability
4. Multitasking
5. Processing speed
6. Budget
   
Confirm if the user's requirements have been correctly captured at the end.

After that the chatbot lists down the top 3 products that are the most relevant and engages in further conversation to help the user find the best one.
## Building the Chatbot
There are three stages of the chatbot, which are as follows:

Stage 1: Intent Clarity Layer - Captures user requirements using LLMs and Guided by Thought-1/Thought-2 logic with dynamic questioning and contextual understanding

Stage 2: Product Mapping Layer - Parses laptop descriptions and classifies features into high/medium/low Using LLMs to auto-interpret product descriptions .

Stage 3: Product Recommendation Layer - Matches user requirements with laptop features and recommends the top 3 options.
## Enhancements in ShopAssist 2.0:
Utilizes OpenAI’s Function Calling feature.

Eliminates redundant layers from ShopAssist 1.0: intent_confirmation_layer(), dictionary_present(), initialize_conv_reco().
