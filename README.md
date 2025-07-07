# AI_calculator

 

##  Features

- Uses an LLM (like OpenAI or Anthropic) to understand natural queries
-  Extracts structured arguments using `JsonOutputParser`
-  Dynamically calls custom Python tools (e.g., multiply, convert)
-  Chaining made easy with LangChain's operator `|` style
-  Handles function arguments cleanly from model output

## How it works?

 1. Prompt: user-friendly instruction like "Multiply 7 and 3"
 2. LLM: generates structured output {"arguments": {"a": 7, "b": 3}}
 3. JsonOutputParser: parses it into a Python dictionary
 4. itemgetter("arguments"): extracts just the "arguments" dict
 5. multiply: passes the extracted args to a function
o/p - 54

---

##  Dependencies

```txt
langchain
langchain-community
openai

