# Langchain Agent Project
### Project Overview
This project demonstrates the use of Langchain's agent framework to build a conversational agent that can solve basic mathematical expressions using the OpenAI API ```` LangChain_LLM_Math.ipynb   ````. It utilizes tools from Langchain to set up the agent and memory buffers, allowing the model to persist context across interactions and handle specific queries, such as mathematical evaluations, by delegating the task to a custom tool.


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
3.  **Key Components:** Langchain Components:
  *   ChatOpenAI is used to integrate OpenAI's GPT model (GPT-3.5-turbo).
  *   ConversationBufferWindowMemory maintains a memory buffer of the conversation, storing the last k=5 interactions.
  *   EvaluateMathExpression is a custom tool defined to evaluate mathematical expressions using Python's eval function.
  *  **Agent Initialization:** The agent is initialized with the tool for evaluating mathematical expressions. The agent uses OpenAI's GPT model and interacts 
        with it through a prompt that instructs the model to always rely on available tools for math calculations.
4. **Modify and Extend:**
    * You can modify the tools, the memory buffer, and prompts to handle other tasks such as data fetching, file handling, or more complex math evaluations.
    * The agent can handle more complex conversations by extending the memory buffer or by adding more tools.

## Example Execution
Upon running the provided code, the agent will:
1. Solve the expression ````2 * 2 * 0.13 - 1.001 ```` using the EvaluateMathExpression tool.
2. It will reprocess the same query but using a system prompt that forces it to always use the provided tools for solving math expressions, regardless of the model's internal abilities.

## Code Explanation
* **API Key:** You need to input your OpenAI API key to allow the GPT model to be used.
* **Custom Tool:** The  ```` EvaluateMathExpression ```` class defines a tool that can run simple mathematical expressions using Python's  ```` eval  ```` function.
* **Agent:** The agent is initialized with a list of tools and the LLM model. It uses conversational memory to remember the last few interactions.
* **Prompt Adjustment:** The system prompt is adjusted to ensure the model doesn't attempt to solve math by itself and always refers to the  ```` EvaluateMathExpression  ```` tool.

## How to Customize
* **Adding More Tools:** You can add more tools by extending the ```` BaseTool ```` class and adding them to the ```` tools ```` list when initializing the agent.
* **Custom Memory Management:** You can adjust how much context the agent remembers by changing the ```` k  ```` value in ```` ConversationBufferWindowMemory ````.

## Example Output
Here is an example output:
```` 
System message: Unfortunately, Assistant is terrible at maths. Assistant should always refer to available tools and never try to answer math questions by itself.
Agent: Evaluating expression 2 * 2 * 0.13 - 1.001 using Math Evaluation tool.
Result: -0.481
````

## Conclusion
This project serves as a basic template for building an agent that interacts with an LLM and uses custom tools to handle specific tasks. It also shows how to manage memory and prompts within Langchain's ecosystem.
