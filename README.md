# functionCallingAzureOpenAI

### Getting structured output from raw LLM generations is hard.

For example, suppose you need the model output formatted with a specific schema for:

Extracting a structured row to insert into a database
Extracting API parameters
Extracting different parts of a user query (e.g., for semantic vs keyword search)

#### Overview
There are two primary approaches for this:

Functions: Some LLMs can call functions to extract arbitrary entities from LLM responses.

Parsing: Output parsers are classes that structure LLM responses.

Only some LLMs support functions (e.g., OpenAI), and they are more general than parsers.

Parsers extract precisely what is enumerated in a provided schema (e.g., specific attributes of a person).

Functions can infer things beyond of a provided schema (e.g., attributes about a person that you did not ask for).
