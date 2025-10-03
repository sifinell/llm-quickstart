## LLM Notebooks: Prompting, Structured Output, and Function Calling

Short, practical notebooks showing how to:
- Prompt effectively
- Produce strict JSON outputs
- Use function calling (tool invocation) with OpenAI-compatible chat APIs on Databricks

### Notebooks
- 01.prompt_engineering.ipynb: Prompt engineering basics, temperature, few-shot, reasoning.
- 02.structured_output.ipynb: Returning strict JSON objects and common extraction patterns.
- 03.function_calling.ipynb: End-to-end tool calling flow with arguments and second call.

### Running on Databricks
- Import the notebooks and attach to a cluster.
- The examples read a workspace token via `dbutils` and call Databricks Model Serving endpoints (`base_url` set to your workspace).
- Ensure you have an available serving endpoint compatible with the OpenAI Chat Completions API.

### Notes
- The function calling example expects you to parse the tool call arguments, execute your function, and pass results back to the model for a final answer.
- The structured output examples request strict JSON; validate responses as needed in production.
