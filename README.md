# Crypto Youtube CHat
This Project leverages langchaing tools and framework to accomplish the following. 

1. Retrieve the transcript from a youtube link: The youtube video is mainly going to be composed of Cryptocurrency information. 

2. Clean the transcript: Clean the transcript, remove not relevant information that might be in the transcript like introductions and sporships, anything that's not relevant and that doesn't provide information about a cryptocurrency or the market context. 

3. Analyse the transcript: Understand which are the coins or tokens mentioned in the video, and which information is being provided for each specific code. The objective is to separate the information of each token so that it is not mixed between each other. Within this AI, if there's any Macro context provided it should be also separated from the information provided about the tokens. 

4. Further analyse each coin: For the information extracted about each of the tokens, extract Critical Prices Mentioned, the sentiment for the coin, and the main reasons behind the sentiment of the coin. This for each of the coins extracted on the previous steps. 

5. Process the information into a table: Create a table with the information extracted around the market context, and each of the coins.

LangChain Tools Needed:

Transcript Retrieval:
YoutubeLoader from LangChain document loaders
pytube or youtube-transcript-api for transcript extraction

Transcript Cleaning:
RecursiveCharacterTextSplitter for text segmentation
LangChain's text processing utilities
Prompt-based cleaning with Language Models

Cryptocurrency Token Identification:
ChatOpenAI or similar chat models
Prompt engineering to extract tokens
Structured output parsing with PydanticOutputParser

Token Analysis:
ChatOpenAI for sentiment and context analysis
PromptTemplate for structured information extraction
OutputParser to convert LLM outputs to structured data

Information Processing:
pandas for table creation
LangChain's output parsing capabilities

Additional Recommended Tools:
LangSmith for debugging and tracing
LangGraph for complex workflow management if needed

Potential Challenges:
Accuracy of AI-based extraction
Handling varied video formats
Potential hallucinations in token analysis

