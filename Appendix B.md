# Chain-of-Thought-Prompting Example

## LLM response with semantic similarity and reasoning for CoT Prompting

**Code statement:** 
> `System.out.println("The integer is positive.");`

**Expert explanation:** 
> Print that the integer is positive if it is greater than 0.

**Student explanation:** 
> This statement prints that the integer is positive.

**Benchmark Similarity:** 
> 1

**LLM:** 
> GPT-4

> Both texts are discussing the same action of printing a statement that an integer is positive. The first text, however, provides a condition for this action (if the integer is greater than 0), while the second text does not specify any condition. Thus, these sentences have a [semantic similarity = 0.8]

---

**Code statement:** 
> `int divisor = 2;`

**Expert explanation:** 
> We define a variable divisor to store the smallest divisor of the number.

**Student explanation:** 
> We initialize another variable named divisor with the value 2.

**Benchmark Similarity:** 
> 0.33

**LLM:** 
> GPT-4

> Both texts discuss initializing a variable named 'divisor', but they differ in the context and purpose of this variable. The first text simply states that the variable is initialized with the value 2, while the second text explains that the variable is used to store the smallest divisor of a number. Thus, these sentences have a [semantic similarity = 0.6]

## Fail case: LLM fails in numerical reasoning

**Code statement:** 
> `int num = 15;`

**Expert explanation:** 
> In this program, we initialize variable num to 15.

**Student explanation:** 
> Creates variable integer entitled "num" with initial value 5.

**Benchmark Similarity:** 
> 0.466666667

**LLM:** 
> GPT-4

**LLM response to Chain-of-thought Prompting:** 
> Both texts are discussing the initialization of a variable named "num", but the initial values they assign to "num" are different. The first text assigns a value of 5, while the second assigns a value of 15. Thus, these sentences have a [semantic similarity = 0.8]

**Comment:** 
> LLM assigns high semantic equivalence score to the two texts, which although linguistically similar involve different numerical values. In such situations where there is a numerical disparity between a student's explanation and an expert's explanation, current Language Models (LLMs) do not account for this difference when automatically evaluating the similarity between the two texts.
