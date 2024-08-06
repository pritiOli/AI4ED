# Prompts

**Baseline Prompt [1-5]:**
> Analyze if the two sentences are similar and provide a score between 1 to 5, with 1 indicating minimal similarity and 5 representing maximal similarity. Provide semantic similarity score for *<user explanation>* and *<expert explanation>* between 1 to 5. Only provide the score without any other text.

**Baseline Prompt [0-1]:**
> Assess the similarity of the two sentences and assign a similarity score on a scale from 0 to 1, with 0 indicating minimal similarity and 1 representing maximal similarity. Provide semantic similarity score for *<user explanation>* and *<expert explanation>* between 0 to 1. Only provide the score without any other text.

**Few Shot Prompt [0-1]:**
> Assess the similarity of the two sentences and assign a similarity score on a scale from 0 to 1, with 0 indicating minimal similarity and 1 representing maximal similarity. Provide a semantic similarity score for `Declares the array we want to use for our assignment' and `We initialize the array of type int to hold the specified numbers.' between 0 and 1. Only provide the score without any other text. Similarity Score: 0.87

> Assess the similarity of the two sentences and assign a similarity score on a scale from 0 to 1, with 0 indicating minimal similarity and 1 representing maximal similarity. Provide semantic similarity score for `run a while-loop as long as the remainder of num/divisor is not equal to 0' and `We could check whether the divisor is not a factor of the number by computing the remainder of the division of the number by the divisor.' between 0 and 1. Only provide the score without any other text. Similarity Score: 0.75

> ...

> Assess the similarity of the two sentences and assign a similarity score on a scale from 0 to 1, with 0 indicating minimal similarity and 1 representing maximal similarity. Provide semantic similarity score for *<user explanation>* and *<expert explanation>* between 0 to 1. Only provide the score without any other text. Similarity Score: 

**Chain-of-Thought (CoT) Prompt [0-1]:**
> Discuss how these two texts are similar and different, then assign a semantic similarity score between [0.0-1.0] which describes their semantic similarity:
> `Declares the array we want to use for our assignment' and `We initialize the array of type int to hold the specified numbers.'
> Similarity: Let's think step by step. Both the texts are about declaration or initialization of array. The slight difference between the two texts is the second text provides additional information about the type of the declared array. Thus, these sentences have a [semantic similarity = 0.87]

> Discuss how these two texts are similar and different, then assign a semantic similarity score between [0.0-1.0] which describes their semantic similarity:
> `We could check whether the divisor is not a factor of the number by computing the remainder of the division of the number by the divisor.' and 
> `run a while-loop as long as the remainder of num/divisor is not equal to 0'
> Similarity: Let's think step by step. Both the texts are about computing the checking whether divisor is a factor of number or not. However, the first text is more specific about using a while-loop and the condition for the loop to continue, while the second text is more focused on the purpose of the operation, which is to check if the divisor is a factor of the number. Thus, these sentences have a [semantic similarity = 0.75]

> ...

> Discuss how these two texts are similar and different, then assign a semantic similarity score between [0.0-1.0] which describes their semantic similarity:
> `Loop start' and `We need to increment the divisor repeatedly as long as the divisor is not a factor of the number.
> Similarity: Let's think step by step. Both texts are discussing loop. The first text is simply stating the start of a loop, while the second text is explaining a specific condition within a loop. Thus, these sentences have a [semantic similarity = 0.2]

> Discuss how these two texts are similar and different, then assign a semantic similarity score between [0.0-1.0] which describes their semantic similarity: *<user explanation>* and *<expert explanation>*
> Similarity: Let's think step by step
