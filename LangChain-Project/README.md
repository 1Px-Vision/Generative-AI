#Langchain Agent Project


## Project Overview
This project demonstrates the use of Langchain's agent framework to build a conversational agent that can solve basic mathematical expressions using the OpenAI API. It utilizes tools from Langchain to set up the agent and memory buffers, allowing the model to persist context across interactions and handle specific queries, such as mathematical evaluations, by delegating the task to a custom tool.


## Prerequisites
Before running the project, you must have the following installed:

1. Python 3.8 or above
2. OpenAI API Key
3. Required libraries, which can be installed using: 
````
pip install openai langchain
````

## Usage
### Step-by-step guide
1. **Set up OpenAI API key:** Replace the placeholder 'your OpenAI API key here' with your actual OpenAI API key in the following line:
   ````
   OPENAI_API_KEY = 'your OpenAI API key here'
   ````
2.  **Run the Agent:** The agent is initialized with a simple mathematical evaluation tool to evaluate basic math expressions. To run this, execute the code in any Python environment.

   ### Key Components
   Langchain Components:

  *   ChatOpenAI is used to integrate OpenAI's GPT model (GPT-3.5-turbo).
  *   ConversationBufferWindowMemory maintains a memory buffer of the conversation, storing the last k=5 interactions.
  *   EvaluateMathExpression is a custom tool defined to evaluate mathematical expressions using Python's eval function.
  *  **Agent Initialization:** The agent is initialized with the tool for evaluating mathematical expressions. The agent uses OpenAI's GPT model and interacts 
        with it through a prompt that instructs the model to always rely on available tools for math calculations.
3. Modify and Extend:

